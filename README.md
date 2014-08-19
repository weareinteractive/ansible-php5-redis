# Ansible Php5-redis Role

[![Build Status](https://travis-ci.org/weareinteractive/ansible-php5-redis.png?branch=master)](https://travis-ci.org/weareinteractive/ansible-php5-redis)
[![Stories in Ready](https://badge.waffle.io/weareinteractive/ansible-php5-redis.svg?label=ready&title=Ready)](http://waffle.io/weareinteractive/ansible-php5-redis)

> `php5-redis` is an [ansible](http://www.ansible.com) role which: 
> 
> * installs php5-redis
> * configures php5-redis

## Installation

Using `ansible-galaxy`:

```
$ ansible-galaxy install franklinkim.php5-redis
```

Using `arm` ([Ansible Role Manager](https://github.com/mirskytech/ansible-role-manager/)):

```
$ arm install franklinkim.php5-redis
```

Using `git`:

```
$ git clone https://github.com/weareinteractive/ansible-php5-redis.git
```

## Dependencies

* PHP 5.4
* [franklinkim.php5](https://github.com/weareinteractive/ansible-php5)
* [franklinkim.redis](https://github.com/weareinteractive/ansible-redis)

## Variables

Here is a list of all the default variables for this role, which are also available in `defaults/main.yml`.

```
# php5_redis_config:
#   - { option: 'foo', value: 'bar' }

# ini settings
php5_redis_config: []
# set state: present | absent
php5_redis_state: present
```

## Example playbook

```
- hosts: all
  roles:
    - franklinkim.apt
    - franklinkim.php5-redis
  vars:
    apt_repositories:
      - 'ppa:ondrej/php5-oldstable'
    php5_redis_state: present
```

## Testing

```
$ git clone https://github.com/weareinteractive/ansible-php5-redis.git
$ cd ansible-php5-redis
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
