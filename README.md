# Ansible Users git Role

[![Build Status](https://travis-ci.org/weareinteractive/ansible-users-git.png?branch=master)](https://travis-ci.org/weareinteractive/ansible-users-git)
[![Stories in Ready](https://badge.waffle.io/weareinteractive/ansible-users-git.svg?label=ready&title=Ready)](http://waffle.io/weareinteractive/ansible-users-git)

> `users-git` is an [ansible](http://www.ansible.com) role which: 
> 
> * configures git for users

## Installation

Using `ansible-galaxy`:

```
$ ansible-galaxy install franklinkim.users-git
```

Using `arm` ([Ansible Role Manager](https://github.com/mirskytech/ansible-role-manager/)):

```
$ arm install franklinkim.users-git
```

Using `git`:

```
$ git clone https://github.com/weareinteractive/ansible-users-git.git
```

## Dependencies

* [franklinkim.users](https://github.com/weareinteractive/ansible-users)

## Variables

Here is a list of all the default variables for this role, which are also available in `defaults/main.yml`.

```
# Extends the franklinkim.users variable with git
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

## Example playbook

```
- host: all
  roles: 
    - franklinkim.users-git
  vars:
    users:
      - name: Foo Bar
        username: foobar
        authorized_keys: []
        git:
          user:
            name: Foo Bar
            email: foo@bar
          github:
            user: foobar
```

## Testing

```
$ git clone https://github.com/weareinteractive/ansible-users-git.git
$ cd ansible-users-git
$ vagrant up
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests and examples for any new or changed functionality.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License
Copyright (c) We Are Interactive under the MIT license.
