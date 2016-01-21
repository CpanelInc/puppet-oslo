oslo
=======

#### Table of Contents

1. [Overview - What is the oslo module?](#overview)
2. [Module Description - What does the module do?](#module-description)
3. [Setup - The basics of getting started with oslo](#setup)
4. [Implementation - An under-the-hood peek at what the module is doing](#implementation)
5. [Limitations - OS compatibility, etc.](#limitations)
6. [Development - Guide for contributing to the module](#development)
7. [Contributors - Those with commits](#contributors)

Overview
--------

The oslo module is a part of [OpenStack](https://www.openstack.org), an effort by the OpenStack infrastructure team to provide continuous integration testing and code review for OpenStack and OpenStack community projects not part of the core software.  The module its self is used to flexibly configure and manage the FIXME service for OpenStack.

Module Description
------------------

The oslo module is a thorough attempt to make Puppet capable of managing the entirety of oslo libraries.  This includes manifests to provision region specific endpoint and database connections.  Types are shipped as part of the oslo module to assist in manipulation of configuration files.

Following versions of oslo libraries are get from requirements.txt in each project.

| Name | oslo.config | oslo.concurrency | oslo.context | oslo.db | oslo.log | oslo.messaging | oslo.middleware | oslo.policy | oslo.reports | oslo.rootwrap | oslo.serialization | oslo.utils | oslo.versionedobjects | oslo.service | oslo.i18n | oslo.vmware |
| ---- |:-------:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:| -----:|
| Cinder | >=3.2.0 | >=2.3.0 | >=0.2.0 | >=4.1.0| >=1.14.0 | !=2.8.0,!=3.1.0,>2.6.1 | >=3.0.0 | >=0.5.0 | >=0.6.0 | >=2.0.0 | >=1.10.0 | >=3.2.0 | >=0.13.0 | >=1.0.0 | >=1.5.0 | >=1.16.0 |
| Ceilometer | >=3.2.0 | >=2.3.0 | >=0.2.0 | >=4.1.0| >=1.14.0 | !=2.8.0,!=3.1.0,>2.6.1 | >=3.0.0 | >=0.5.0 | >=0.6.0 | >=2.0.0 | >=1.10.0 | >=3.4.0 | n/a | >=1.0.0 | >=1.5.0 | n/a |
| Designate | >=3.2.0 | >=2.3.0 | >=0.2.0 | >=4.1.0| >=1.14.0 | !=2.8.0,!=3.1.0,>2.6.1 | >=3.0.0 | >=0.5.0 | >=0.6.0 | >=2.0.0 | >=1.10.0 | >=3.4.0 | n/a | >=1.0.0 | >=1.5.0 | n/a |
| Glance | >=3.2.0 | >=2.3.0 | >=0.2.0 | >=4.1.0| >=1.14.0 | !=2.8.0,!=3.1.0,>2.6.1 | >=3.0.0 | >=0.5.0 | >=0.6.0 | >=2.0.0 | >=1.10.0 | >=3.2.0 | n/a | >=1.0.0 | >=1.5.0 | n/a |

Setup
-----

**What the oslo module affects**

* [Oslo](https://wiki.openstack.org/wiki/Oslo), the FIXME service for OpenStack.

### Installing oslo

    oslo is not currently in Puppet Forge, but is anticipated to be added soon.  Once that happens, you'll be able to install oslo with:
    puppet module install openstack/oslo

### Beginning with oslo

To utilize the oslo module's functionality you will need to declare multiple resources.

Implementation
--------------

### oslo

oslo is a combination of Puppet manifest and ruby code to delivery configuration and extra functionality through types and providers.

Limitations
------------

* All the oslo types use the CLI tools and so need to be ran on the oslo node.

Beaker-Rspec
------------

This module has beaker-rspec tests

To run the tests on the default vagrant node:

```shell
bundle install
bundle exec rake acceptance
```

For more information on writing and running beaker-rspec tests visit the documentation:

* https://github.com/puppetlabs/beaker/wiki/How-to-Write-a-Beaker-Test-for-a-Module

Development
-----------

Developer documentation for the entire puppet-openstack project.

* https://wiki.openstack.org/wiki/Puppet

Contributors
------------

* https://github.com/openstack/puppet-oslo/graphs/contributors
