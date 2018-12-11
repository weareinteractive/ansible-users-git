# Ansible weareinteractive.users-git role

[![Build Status](https://img.shields.io/travis/weareinteractive/ansible-users-git.svg)](https://travis-ci.org/weareinteractive/ansible-users-git)
[![Galaxy](http://img.shields.io/badge/galaxy-weareinteractive.users-git-blue.svg)](https://galaxy.ansible.com/weareinteractive/users-git)
[![GitHub tag](https://img.shields.io/github/tag/weareinteractive/ansible-users-git.svg)](https://github.com/weareinteractive/ansible-users-git/releases)
[![GitHub stars](https://img.shields.io/github/stars/weareinteractive/ansible-users-git.svg?style=social&label=Star)](https://github.com/weareinteractive/ansible-users-git)

> `weareinteractive.users-git` is an [Ansible](http://www.ansible.com) role which:
>
> * configures git for users

**Note:**

> Since Ansible Galaxy switched all role names to the organization name, this role has moved from `franklinkim.users-git` to `weareinteractive.users-git`!

## Installation

Using `ansible-galaxy`:

```shell
$ ansible-galaxy install weareinteractive.users-git
```

Using `requirements.yml`:

```yaml
- src: weareinteractive.users-git
```

Using `git`:

```shell
$ git clone https://github.com/weareinteractive/ansible-users-git.git weareinteractive.users-git
```

## Dependencies

* Ansible >= 2.4
* weareinteractive.users

## Variables

Here is a list of all the default variables for this role, which are also available in `defaults/main.yml`.

```yaml
---
# For more information about default variables see:
# http://www.ansibleworks.com/docs/playbooks_variables.html#id26
#
# Extends the weareinteractive.users variable with git
#
# users:
#   - name: Foo Bar
#     username: foobar
#     authorized_keys: []
#     git:
#       user:
#         name: Foo Bar
#         email: foo@bar
#       github:
#         user: foobar
#

```


## Usage

This is an example playbook:

```yaml
---

- hosts: all
  become: yes
  roles:
    - weareinteractive.users-git
  vars:
    users:
      - name: Foo Bar
        username: foobar
        git:
          user:
            name: Foo Bar
            email: foo@bar
          github:
            user: foobar
```


## Testing

```shell
$ git clone https://github.com/weareinteractive/ansible-users-git.git
$ cd ansible-users-git
$ make test
```

## Contributing
In lieu of a formal style guide, take care to maintain the existing coding style. Add unit tests and examples for any new or changed functionality.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

*Note: To update the `README.md` file please install and run `ansible-role`:*

```shell
$ gem install ansible-role
$ ansible-role docgen
```

## License
Copyright (c) We Are Interactive under the MIT license.
