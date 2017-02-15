michaeldfallen.scm_repos
========================

Ansible role that checks out scm repos.

Role Defaults Variables
-----------------------

See [defaults/main.yml](defaults/main.yml) for more information.


    # Controls whether repos are shallow cloned (depth = 1)
    default_git_repos_shallow_clone: yes

    # Controls whether repos get updated by default
    default_git_repos_update: yes

Example Playbook
----------------

    - hosts: localhost
      vars:
        git_repos:
          - repo: git@github.com:foo/bar.git
            path: ~/.repos/bar
          - repo: git@github.com:foo/baz.git
            path: ~/.repos/baz
            latest: no
            shallow: no
      roles:
        - { role: michaeldfallen.scm_repos }

License
-------

Licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
