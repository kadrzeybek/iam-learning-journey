# Active Directory Setup

In this lab, Active Directory Domain Services (AD DS) was installed on the
`SRVDC1` Windows Server and configured as the first domain controller in a new
forest.

## Step 1: Open Server Manager

The Start menu was opened and **Server Manager** was selected.

![Open Server Manager](../images/active-directory-setup/setup-1.png)

## Step 2: Start the Add Roles and Features wizard

In Server Manager, **Add roles and features** was selected from the dashboard.

![Start the Add Roles and Features wizard](../images/active-directory-setup/setup-2.png)

## Step 3: Review the prerequisites

The **Before You Begin** page was reviewed. The server already had a strong Administrator password and a static network configuration, so **Next** was selected.

![Review the prerequisites](../images/active-directory-setup/setup-3.png)

## Step 4: Select the installation type

**Role-based or feature-based installation** was selected, and **Next** was clicked.

![Select role-based installation](../images/active-directory-setup/setup-4.png)

## Step 5: Select the destination server

The local server `SRVDC1` with IP address `10.0.100.10` was selected from the server pool.

![Select the destination server](../images/active-directory-setup/setup-5.png)

## Step 6: Select Active Directory Domain Services

On the **Server Roles** page, **Active Directory Domain Services** was selected.

![Select Active Directory Domain Services](../images/active-directory-setup/setup-6.png)

## Step 7: Add the required management features

The wizard displayed the required management tools for AD DS. **Add Features** was selected, leaving **Include management tools** enabled.

![Add the required AD DS features](../images/active-directory-setup/setup-7.png)

## Step 8: Confirm the AD DS role selection

The **Active Directory Domain Services** role was shown as selected. **Next** was clicked to continue.

![Confirm the AD DS role selection](../images/active-directory-setup/setup-8.png)

## Step 9: Review the selected features

The automatically selected **Group Policy Management** feature was reviewed, and **Next** was selected.

![Review the selected features](../images/active-directory-setup/setup-9.png)

## Step 10: Review AD DS information

The AD DS information page was reviewed and clicked next.

![Review Active Directory Domain Services](../images/active-directory-setup/setup-10.png)

## Step 11: Confirm the installation

The installation selections were reviewed, and **Install** was selected.

![Confirm the AD DS installation](../images/active-directory-setup/setup-11.png)

## Step 12: Wait for the role installation to complete

The installation is completed. Now, Close button is clicked.

![Wait for the AD DS role installation](../images/active-directory-setup/setup-12.png)

## Step 13: Open the post-deployment configuration

In Server Manager notifications, **Promote this server to a domain controller** was selected.

![Promote the server to a domain controller](../images/active-directory-setup/setup-13.png)

## Step 14: Create a new forest

In the AD DS Configuration Wizard, **Add a new forest** was selected. The root domain name was entered.

![Create a new forest](../images/active-directory-setup/setup-14.png)

## Step 15: Configure domain controller options

The forest functional level  and the domain functional level are selected and a DSRM password was entered and the next button is clicked.

> Now win server 2008 R8 is selected because i will show you how it is updated soon.

![Configure domain controller options](../images/active-directory-setup/setup-15.png)

## Step 16: Review DNS options

DNS delegation is not important for now, click next.

![Review DNS options](../images/active-directory-setup/setup-16.png)

## Step 17: Verify the NetBIOS domain name

The automatically generated NetBIOS domain name was verified.

![Verify the NetBIOS domain name](../images/active-directory-setup/setup-17.png)

## Step 18: Confirm the AD DS paths

The default paths were kept for the AD DS database, log files, and SYSVOL:

- Database: `C:\Windows\NTDS`
- Log files: `C:\Windows\NTDS`
- SYSVOL: `C:\Windows\SYSVOL`

![Confirm the AD DS paths](../images/active-directory-setup/setup-18.png)

## Step 19: Review the domain configuration

Review your selection and click view script.

![Review the domain configuration](../images/active-directory-setup/setup-19.png)

## Step 20: View the generated PowerShell script

The **View script** option was used to review the PowerShell commands generated for the AD DS deployment. Save this script for using in the future.

![View the generated deployment script](../images/active-directory-setup/setup-20.png)

## Step 21: Continue after the server restart

I saved this script on my desktop.

![Verify the server after restart](../images/active-directory-setup/setup-21.png)

## Step 22: Review the deployment configuration

After saving script, click next.

![Review the deployment configuration](../images/active-directory-setup/setup-22.png)

## Step 23: Run the prerequisites check

All prerequisite checks passed successfully. The DNS delegation warning can be ignored in this isolated lab because there is no authoritative parent zone. **Install** was selected to begin the domain controller promotion. After this installation the system will be restarted automatically and everything is completed.

![Run the prerequisites check](../images/active-directory-setup/setup-23.png)