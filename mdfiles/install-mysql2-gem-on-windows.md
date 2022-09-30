---
title: Install mysql2 gem on Windows
description: Instructions for installing Ruby gem mysql2 on Windows 11 machines
published: true
---

# Install mysql2 gem on Windows

If you have a Rails project that connects to a MySQL database, and your development machine is powered by Windows 10...

Then probably you run into some low-level errors when trying to install the mysql2 gem.

If that's the case, then this post if for you!

### Step 1 -- Install the C++ connector

That's easy, it's either a side-effect of installing MySQL + dev kit on your machine... or you can download the `msi` / `zip` from MySQL website.

### Step 2 -- Install the gem

Simply open a Terminal window, and execute the following command:

`gem install mysql2 -platform=ruby -- '--with-mysql-dir="C:\Program Files (x86)\MySQL\Connector C++ 8.0"'`

If you need to install a specific version of the gem, for example 0.5.4... then adjust the command like so:

`gem install mysql2 -v 0.5.4 -platform=ruby -- '--with-mysql-dir="C:\Program Files (x86)\MySQL\Connector C++ 8.0"'`

