# centos-jekyll-sites

Community effort to make CentOS websites over with
[https://jekyllrb.com/](jekyll) 4 and [https://getbootstrap.com/](bootstrap) 4.

## Installation

This section describes the steps you need to follow in order to render the
final site using jekyll in Fedora 31.

1. Clone this repository:

    ]$ git clone git@github.com:areguera/centos-jekyll-sites.git

1. Download jekyll container:

    ]$ podman pull jekyll/jekyll

2. Create an alias to run jekyll container by adding the following line to
`~/.bashrc`:

    ]$ alias jekyll='podman run --volume="$PWD:/srv/jekyll:z" --volume="$PWD/vendor/bundle:/usr/local/bundle:z" -p 4000:4000/tcp --rm -it jekyll/jekyll jekyll'

3. Reload the `./bashrc` file:

    ]$ source ~/.bashrc

4. Update directory permissions using the container user namespace uid (1000)
and gid (1000). This is necessary for jekyll inside the container to be able of
writing in the host filesystem through the specified volumes:

    ]$ podman unstage chown 1000:1000 centos-jekyll-sites

  The permissions must be applied to all the files and directories jekyll reads
  and writes to (e.g., `_site` for the final site, `vendor/bundle` for bundle
  cache, `.jekyll-cache`, etc.). Once the files permission have been changed
  this way you will see them using a high number (e.g., 100999). This number is
  the subordinate uid and gid the host uses to related to container user
  namespace uid and gid (e.g., 1000).

5. Create the `vendor/bundle` directory inside the `centos-jekyll-site`
directory:

    ]$ podman unstage mkdir -p vendor/bundle

At this point you should be able to run the following:

    ]$ jekyll -v
    ruby 2.6.5p114 (2019-10-01 revision 67812) [x86_64-linux-musl]
    jekyll 4.0.0

  The first time you run jekyll, it will take some time downloading all the
  gems it needs. After this first download, it behaves like a regular command.

# Accessing the final site

To access the final site you need to be inside the repository directory
structure, where the `Gemfile` is, and run the following:

    ]$ jekyll serve

Then visit the site accessing to http://127.0.0.1:4000 in your host.

# Making changes

Operations like editing, copying, creating, moving and removing files owned by
by jekyll container user namespace uid and gid must be executed using `podman
unshare <command> [arg]`. Otherwise, you may have permission issues. For
example, to edit jekyll main configuration, run the following command:

    ]$ podman unshare nvim _config.yml

## Additional resources

* https://github.com/envygeeks/jekyll-docker/blob/master/README.md
* https://www.redhat.com/sysadmin/rootless-podman-makes-sense
