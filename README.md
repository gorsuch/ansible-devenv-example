ansible-devenv-example
======================

Example development environment produced by ansible

## What does it include out of the box?

* Ubuntu Trust (14.04)
* chruby
* ruby 2.1.2
* redis
* memcached
* postgres
* tmux
* vim

## How do I run it?

After cloning this repo you need to tell git to resolve submodules.

~~~bash
cd ansible-devenv-example
git submodule update --init --recursive
~~~

### Install VirtualBox

Download an installer from [https://www.virtualbox.org/](https://www.virtualbox.org/).

### Install Vagrant

Download an installer from [http://www.vagrantup.com/](http://www.vagrantup.com/).

### Install ansible locally

```
# for OS X
$ brew install ansible
```

### Vagrant up!

```
$ vagrant up
```

## How do I access it?

After you've run `vagrant up` and the build process completes:

```
$ vagrant ssh
```

Then change to your user:

```
$ sudo su - username
```

## Ruby

By default the system Ruby will be used (1.9.3).  To change to 2.1.2 run this command:

```
$ chruby 2.1.2
```

## How do I iterate?

If you change the ansible config and want to apply it, just:

```
$ vagrant provision
```

## What should I modify?

Pretty much everything you want to.

Start by modifying `site.yml`, replacing your user information.  Then go from there.


