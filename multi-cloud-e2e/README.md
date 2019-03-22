# End-to-End Multi-Cloud & Stack Lab Scenario For Azure

This is the End-to-End blueprint, which automates the installation of the [Multi-Cloud scenario (Part 2)](https://wp.cloudify.co/knowledge-base/multi-cloud-governance-solution-azure/#intermediate).

![multi-cloud-scenario](https://wp.cloudify.co/wp-content/uploads/2018/06/openstack-cloudify-drupal-azure-mariadb-768x313.png)

## Blueprints included

  * [Azure Example Network](https://github.com/cloudify-examples/azure-example-network),
  * [OpenStack Example Network*](https://github.com/cloudify-examples/openstack-example-network),
  * [MariaDB Blueprint](https://github.com/cloudify-examples/mariadb-blueprint),
  * [HAProxy Blueprint](https://github.com/cloudify-examples/haproxy-blueprint),
  * [Drupal Blueprint](https://github.com/cloudify-examples/drupal-blueprint).

  \* _openstack-example-network_ is supposed to be already installed in Cloudify Manager before running this scenario

## Compatibility

Tested with:
  * Cloudify 4.5

## Pre-installation steps

Upload the required plugins:

  * [Azure Plugin](https://github.com/cloudify-incubator/cloudify-azure-plugin/releases),
  * [OpenStack Plugin](https://github.com/cloudify-cosmo/cloudify-openstack-plugin/releases),
  * [Utilities Plugin](https://github.com/cloudify-incubator/cloudify-utilities-plugin/releases).

_Check the blueprint for the exact version of the plugin._

You must have these secrets on your Cloudify Manager `tenant`:

  * `azure_subscription_id`
  * `azure_tenant_id`
  * `azure_client_id`
  * `azure_client_secret`
  * `azure_location`, such as `eastus`.

## Installation

Upload the blueprint, create the deployment and execute install workflow in one command using the CLI:

```bash
cfy install e2e.yaml -b  multi-cloud-e2e
```

## Uninstallation

Navigate to the deployment and select `Uninstall`. When the uninstall workflow is finished, select `Delete deployment`. Or use the CLI:

```bash
cfy uninstall multi-cloud-e2e
```
