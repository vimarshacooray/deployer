<!-- DO NOT EDIT THIS FILE! -->
<!-- Instead edit recipe/zend_framework.php -->
<!-- Then run bin/docgen -->

# How to Deploy Zend Framework

[Source](/recipe/zend_framework.php)

## How to deploy a Zend Framework project with zero downtime?

- First, [install](/docs/installation.md) the Deployer. 
- Second, require `recipe/zend_framework.php` recipe into your _deploy.php_ or _deploy.yaml_ file.
- Third, now you can have a zero downtime deployment!

Did you know that you can deploy **Zend Framework** project with a single command? Just execute `dep deploy`.
Something went wrong? Just run `dep rollback` to rollback your changes.
Also, you can take an advantages of the [Deployer's CLI](/docs/cli.md) to deploy your project.

Another feature of the Deployer is [provisioning](/docs/recipe/provision.md). Take any server, and run `dep provision` command.
This command will configure webserver, databases, php, ssl certificates, and more. 
You will get everything you need to run your **Zend Framework** project.

Deployer does next steps to [deploy](#deploy) **Zend Framework**:
* Displays info about deployment
* Prepares host for deploy
* Locks deploy
* Prepares release
* Updates code
* Creates symlinks for shared files and dirs
* Makes writable dirs
* Installs vendors
* Creates symlink to release
* Unlocks deploy
* Cleanup old releases


The zend_framework recipe is based on the [common](/docs/recipe/common.md) recipe.


## Tasks

### deploy
[Source](https://github.com/deployphp/deployer/blob/master/recipe/zend_framework.php#L12)

Deploys your project.

Main task


This task is group task which contains next tasks:
* [deploy:prepare](/docs/recipe/common.md#deployprepare)
* [deploy:vendors](/docs/recipe/deploy/vendors.md#deployvendors)
* [deploy:publish](/docs/recipe/common.md#deploypublish)


