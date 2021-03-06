---
title: Catalog
layout: rancher-default
---

## Catalog
---

Rancher provides a catalog of application templates that make it easy to deploy these complex stacks. By accessing the **Applications** -> **Catalog** tab, you can view all the templates that are available in the [enabled catalogs]({{site.baseurl}}/rancher/configuration/settings/#catalog). By default, the catalog is enabled with our [official catalog](https://github.com/rancher/rancher-catalog) and [community-catalog](https://github.com/rancher/community-catalog).

> **Note:** Though Rancher is defaulted with templates from both the official catalog and community catalog, Rancher will only be maintaining support for templates in our official catalog. 

### Launching Templates 

Search for your desired template or use the filters for category or catalog. Once you have found your template, click on **Launch**. Fill in the required information for the template.

1. By default, latest **version** of a template is selected, but if desired, you could select an older version. 
2. Select a **stack** name and if desired, **description** of the stack. 
3. Fill in the **Configuration Options**, which are questions specific to the selected template. 
4. Click on **Create** to create the stack based on the template. You can review the `docker-compose.yml` and `rancher-compose.yml` files that are being used to generate the stacks by expanding **Preview** before creating the stack. 

After you click on **Create**, the stack is immediately created, but none of the services have started. Click on **Start Services** from the the stack dropdown menu to start all the services of the stack. 

### Upgrading Templates

The great thing about Rancher is that if a newer version of a template has been uploaded to the catalog, we'll inform you that a newer version is available to upgrade to. When you click on **Upgrade Available**, you can select which version you want to upgrade to. After selecting the version, the **Configuration Options** will need to be reviewed before clicking on **Save**. 

After all the services have been upgraded, the stack and services will be in an **Upgraded** state. If you are satisfied with your upgrade, the last step is to confirm the upgrade by clicking on the **Finish Upgrade** in the stack dropdown menu. **Note: Once you have finished your upgrade, you will not be able to revert to the older version.**

#### Rolling back 

If something went wrong during your upgrade and you need to revert to the previous version, you would want to select **Rollback** in the stack dropdown menu. 


### Catalogs in Rancher

By default, the catalog is populated with templates from the [official catalog](https://github.com/rancher/rancher-catalog) and [community-catalog](https://github.com/rancher/community-catalog).


An [admin]({{site.baseurl}}/rancher/configuration/accounts/#admin) has the ability to add or remove catalogs to Rancher in the **Admin** -> **[Settings]({{site.baseurl}}/rancher/configuration/settings/#catalog)**. Whenever a new catalog is added, the templates in the new catalog is added to the list of all other enabled catalogs.

Private catalogs can be created by [following the expected format]({{site.baseurl}}/rancher/catalog/#creating-private-catalogs). 



