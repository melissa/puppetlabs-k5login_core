
# k5login_core

#### Table of Contents

1. [Description](#description)
2. [Setup - The basics of getting started with k5login_core](#setup)
    * [Beginning with k5login_core](#beginning-with-k5login_core)
3. [Usage - Configuration options and additional functionality](#usage)
4. [Reference - User documentation](#reference)
5. [Limitations - OS compatibility, etc.](#limitations)
6. [Development - Guide for contributing to the module](#development)

## Description

Manage k5login context of files.

## Setup

### Beginning with k5login_core

To set the `.k5login` file for a user:
```
file { "/home/name/.k5login":
  ensure => present,
  mode => '644',
  principals => ['foo@site.com', 'bar@site.com'],
  selrange => 's0',
  selrole => 'role_r',
  seltype => 'tmp_t',
  seluser => 'user_u',
}
```

## Usage

For details on usage, please see the puppet docs on [k5login](https://puppet.com/docs/puppet/latest/types/k5login.html).

## Reference

Please see REFERENCE.md for the reference documentation.

This module is documented using Puppet Strings.

For a quick primer on how Strings works, please see [this blog post](https://puppet.com/blog/using-puppet-strings-generate-great-documentation-puppet-modules) or the [README.md](https://github.com/puppetlabs/puppet-strings/blob/master/README.md) for Puppet Strings.

To generate documentation locally, run
```
bundle install
bundle exec puppet strings generate ./lib/**/*.rb
```
This command will create a browsable `\_index.html` file in the `doc` directory. The references available here are all generated from YARD-style comments embedded in the code base. When any development happens on this module, the impacted documentation should also be updated.ß

## Development

Puppet Labs modules on the Puppet Forge are open projects, and community contributions are essential for keeping them great. We can't access the huge number of platforms and myriad of hardware, software, and deployment configurations that Puppet is intended to serve.

We want to keep it as easy as possible to contribute changes so that our modules work in your environment. There are a few guidelines that we need contributors to follow so that we can have a chance of keeping on top of things.

For more information, see our [module contribution guide.](https://docs.puppetlabs.com/forge/contributing.html)
