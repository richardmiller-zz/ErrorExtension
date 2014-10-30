ErrorExtension
==============

Behat extension to provide formatted error messages for fatal errors.

Stops the large stack traces appearing on every fatal error. They will
still appear when behat is run with the verbose flag.

Registering observers to do more with these errors to follow.

Since this does work in the shutdown function there is a good chance things
will go horribly wrong if there are any errors/exceptions in handing the errors.
It's an extension to a dev tool though so this is not that worth worrying about.

Installation
------------

This extension requires:

* Behat 3.0+
* PHP 5.4+

The easiest way to install it is to use Composer

```
$ composer require --dev rmiller/error-extension:dev-master
```

Activate the extension by specifying its class in your ``behat.yml``:

```yaml
# behat.yml
default:
  # ...
  extensions:
    RMiller\ErrorExtension\ErrorExtension: ~
```