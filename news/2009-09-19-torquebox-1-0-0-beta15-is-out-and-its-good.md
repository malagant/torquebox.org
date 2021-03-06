---
title: TorqueBox 1.0.0.Beta15 is out, and it's good.
author: Bob McWhirter
version: 1.0.0.Beta15
layout: release
tags: [ releases ]
---
Quick on the heels of 1.0.0.Beta14, I'm happy to announce 1.0.0.Beta15.

[Download it](/download/) and [read the documentation](/documentation/#{page.version}/) now.

First off, this release re-enabled multiple versions of Rails.  Feel free to use anything *2.2.2+*.  This include 2.3.4.

By default the TorqueBox distribution ships with 2.3.4, but you may certainly use others.

Which brings us to some major new functionality: *running apps using Rails gems*. 
You no longer have to freeze rails into your app.  You certainly may still freeze Rails, 
and `vendor/rails/` will take precedence.  Or you can just specify the 
`RAILS_GEM_VERSION` variable in your `config/environment.rb`.

Also, any other gems specified in your environment.rb can be pulled in from the global Gem path.

As usual, `rake gems:install` will attempt to install your app's gems into the global Gem path.

The full list of bugs fixed since 1.0.0.Beta14:

* [TORQUE-5](https://jira.jboss.org/jira/browse/TORQUE-5) - Rails Gem should be loadable from shared JRUBY_HOME-based gempath.
* [TORQUE-24](https://jira.jboss.org/jira/browse/TORQUE-24) - rails.bat missing
* [TORQUE-26](https://jira.jboss.org/jira/browse/TORQUE-26) - reset_session fails with nil


