# Puppet Omnibus Gem Module

Based on original work by Puppet Labs, Inc. at 
https://github.com/puppetlabs/puppetlabs-pe_gem

This module provides management of Ruby gems for Puppet Omnibus. Using the `puppet_omnibus_gem` provider will allow gems to be installed within the monolithic Puppet Omnibus environment so the gem can be used in new types/providers.

    package { 'my_gem':
      ensure   => present,
      provider => puppet_omnibus_gem,
    }

This uses puppet gem as a parent and simply alters the gem binary path to `/opt/puppet-omnibus/embedded/bin/gem`.
