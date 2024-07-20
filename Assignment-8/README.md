# Assignment 8: Azure Infrastructure Backup and Monitoring

## Objective:
1. Schedule a daily backup of a Virtual Machine (VM) at 3:00 AM using Azure Backup.
2. Create an alert rule for VM CPU percentage: Criteria - CPU % greater than 80%.

## Prerequisites:
- An active Azure subscription.
- A virtual machine (VM) that you want to back up.
- Basic knowledge of Azure portal and Azure Backup.

## Steps:

### Part A: Schedule a Daily Backup of VM at 3:00 AM Using Vault

#### 1. Create a Recovery Services Vault

1. Navigate to the Azure portal.
2. In the left-hand menu, select **Create a resource**.
3. In the search bar, type "Recovery Services vault" and select **Recovery Services vaults**.
4. Click **Create**.
5. Fill in the necessary details:
   - **Subscription**: Select your subscription.
   - **Resource group**: Select an existing resource group or create a new one.
   - **Name**: Enter a name for your vault.
   - **Region**: Select the region where you want to create the vault.
6. Click **Review + create** and then **Create**.

#### 2. Configure Backup

1. Once the vault is created, go to the newly created Recovery Services vault.
2. In the vault's menu, select **+ Backup**.
3. In the **Where is your workload running?** section, select **Azure**.
4. In the **What do you want to back up?** section, select **Virtual machine**.
5. Click **Backup**.

#### 3. Schedule Backup Policy

1. In the **Backup policy** section, select **Create a new policy**.
2. Fill in the necessary details:
   - **Policy name**: Enter a name for your backup policy.
   - **Frequency**: Select **Daily**.
   - **Time**: Set the time to **3:00 AM**.
   - **Retention**: Configure the retention period according to your requirements.
3. Click **OK** to create the backup policy.

#### 4. Apply Backup Policy to VM

1. In the **Select virtual machines** section, click **Add**.
2. Select the VM you want to back up.
3. Click **OK**.
4. Click **Enable Backup**.

### Part B: Create an Alert Rule for VM CPU Percentage

#### 1. Navigate to the VM

1. In the Azure portal, go to **Virtual machines**.
2. Select the VM for which you want to create the alert rule.

#### 2. Create Alert Rule

1. In the VM's menu, select **Alerts** under **Monitoring**.
2. Click **+ New alert rule**.
3. Under **Scope**, the selected VM should already be listed.
4. Under **Condition**, click **Add condition**.
5. In the **Select a signal** pane, search for and select **Percentage CPU**.
6. Configure the alert logic:
   - **Condition**: Select **Greater than**.
   - **Threshold value**: Enter **80**.
   - **Aggregation granularity**: Select **5 minutes**.
   - **Frequency of evaluation**: Select **5 minutes**.
7. Click **Done**.

#### 3. Define Action Group

1. Under **Actions**, click **+ Add action group**.
2. Fill in the necessary details for the action group:
   - **Action group name**: Enter a name.
   - **Short name**: Enter a short name.
   - **Subscription**: Select your subscription.
   - **Resource group**: Select a resource group.
3. Click **Next: Notifications**.
4. In the **Notification type** drop-down, select **Email/SMS message/Push/Voice**.
5. Fill in the email details and click **OK**.
6. Click **Review + create** and then **Create**.

#### 4. Review and Create Alert Rule

1. Under **Alert rule details**, enter a name and description for the alert rule.
2. Click **Create alert rule**.

## Resources:

- [Microsoft Docs: Azure Administrator](https://learn.microsoft.com/en-us/training/paths/azure-administrator-monitor-backup-resources/)
- [YouTube Tutorial 1](https://www.youtube.com/watch?v=lzVQ3NqMnTE)
- [YouTube Tutorial 2](https://www.youtube.com/watch?v=A0jAeGf2zUQ)
- [YouTube Tutorial 3](https://www.youtube.com/watch?v=DOywwse_j8I)

## Conclusion:
By following these steps, you have successfully configured a daily backup of your VM and created an alert rule for monitoring the VM's CPU percentage. This ensures that your VM is regularly backed up and you are notified when the CPU usage exceeds the defined threshold.

