---
title: include file
description: include file
services: backup
author: dcurwin
manager: carmonm
ms.service: backup
ms.topic: include
ms.date: 10/18/2018
ms.author: dacurwin
ms.custom: include file
---

## Create a Recovery Services vault

A Recovery Services vault is a storage entity that stores the recovery points created over time. It also contains the backup policies that are associated with protected items.

To create a Recovery Services vault, follow these steps.

1. Sign in to your subscription in the [Azure portal](https://portal.azure.com/).

1. On the left menu, select **All services**.

    ![Select All services](./media/backup-create-rs-vault/click-all-services.png)

1. In the **All services** dialog box, enter *Recovery Services*. The list of resources filters according to your input. In the list of resources, select **Recovery Services vaults**.

    ![Enter and choose Recovery Services vaults](./media/backup-create-rs-vault/all-services.png)

    The list of Recovery Services vaults in the subscription appears.

1. On the **Recovery Services vaults** dashboard, select **Add**.

    ![Add a Recovery Services vault](./media/backup-create-rs-vault/add-button-create-vault.png)

    The **Recovery Services vault** dialog box opens. Provide values for the **Name**, **Subscription**, **Resource group**, and **Location**.

    ![Configure the Recovery Services vault](./media/backup-create-rs-vault/create-new-vault-dialog.png)

   - **Name**: Enter a friendly name to identify the vault. The name must be unique to the Azure subscription. Specify a name that has at least 2 but not more than 50 characters. The name must start with a letter and consist only of letters, numbers, and hyphens.
   - **Subscription**: Choose the subscription to use. If you're a member of only one subscription, you'll see that name. If you're not sure which subscription to use, use the default (suggested) subscription. There are multiple choices only if your work or school account is associated with more than one Azure subscription.
   - **Resource group**: Use an existing resource group or create a new one. To see the list of available resource groups in your subscription, select **Use existing**, and then select a resource from the drop-down list. To create a new resource group, select **Create new** and enter the name. For more information about resource groups, see [Azure Resource Manager overview](../articles/azure-resource-manager/management/overview.md).
   - **Location**: Select the geographic region for the vault. To create a vault to protect any data source, the vault *must* be in the same region as the data source.

      > [!IMPORTANT]
      > If you're not sure of the location of your data source, close the dialog box. Go to the list of your resources in the portal. If you have data sources in multiple regions, create a Recovery Services vault for each region. Create the vault in the first location before you create the vault for another location. There's no need to specify storage accounts to store the backup data. The Recovery Services vault and Azure Backup handle that automatically.
      >
      >

1. When you're ready to create the Recovery Services vault, select **Create**.

    ![Create the Recovery Services vault](./media/backup-create-rs-vault/click-create-button.png)

    It can take a while to create the Recovery Services vault. Monitor the status notifications in the **Notifications** area at the upper-right corner of the portal. After your vault is created, it's visible in the list of Recovery Services vaults. If you don't see your vault, select **Refresh**.

     ![Refresh the list of backup vaults](./media/backup-create-rs-vault/refresh-button.png)
