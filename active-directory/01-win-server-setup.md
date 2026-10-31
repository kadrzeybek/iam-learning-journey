# Windows Server 2016 Setup

In this lab, a Windows Server 2016 virtual machine was created on macOS using
UTM for the Active Directory environment.

## Step 1: Create a new virtual machine

UTM was opened and **Create a New Virtual Machine** was selected.

![Create a new virtual machine in UTM](../images/win-server-setup/setup-1.png)

## Step 2: Select emulation

 **Emulate** was selected because Windows Server runs on the x86_64 architecture.

![Select Emulate](../images/win-server-setup/setup-2.png)

## Step 3: Select the operating system type

**Other** was selected from the operating system list. A custom installation was used instead of the predefined Windows profile.

![Select Other as the operating system](../images/win-server-setup/setup-3.png)

## Step 4: Configure hardware resources

 The virtual machine was assigned 4096 MiB of memory and 4 CPU cores. You can choose higher if your system is available.

![Virtual machine hardware settings](../images/win-server-setup/setup-4.png)

## Step 5: Configure boot settings

The boot device was initially left as **None**, and **UEFI Boot** was not enabled.

![Boot settings](../images/win-server-setup/setup-5.png)

## Step 6: Set the virtual disk size

The virtual disk size was set to **40 GiB** for the Windows Server installation. You Can choose higher if your system is available.

![Virtual disk size](../images/win-server-setup/setup-6.png)

## Step 7: Skip shared directory configuration

No folder was shared with the host operating system. The shared directory path was left empty and the setup continued.

![Shared directory settings](../images/win-server-setup/setup-7.png)

## Step 8: Review the virtual machine summary

The machine name was set to `SRVDC1` on the summary screen. You can give different name.  **Open VM Settings** was left selected before completing the creation process.

![Review the virtual machine summary](../images/win-server-setup/setup-8.png)

## Step 9: Add a new drive

In the UTM virtual machine settings, **New...** was selected to add a new IDE device.

![Add a new IDE device](../images/win-server-setup/setup-9.png)

## Step 10: Configure the drive for the ISO

The new device interface was left as **IDE**, its size was set to **40 GiB** and **Import...** was selected to attach the ISO.

![IDE device and ISO import](../images/win-server-setup/setup-10.png)

## Step 11: Select the Windows Server ISO

The `Windows_Server_2016 ISO` file was selected.

![Windows Server 2016 ISO file](../images/win-server-setup/setup-11.png)

## Step 12: Move the new drive up

The newly created drive was selected in the UTM settings and **Move Up** was chosen so that the drive order was correct.

![Move the new drive up](../images/win-server-setup/setup-12.png)

## Step 13: Set the ISO as a CD/DVD image

The attached device's **Image Type** was changed to **CD/DVD (ISO) Image**.

![Select the ISO image type](../images/win-server-setup/setup-13.png)

## Step 14: Start the virtual machine

The settings were saved, and `SRVDC1` was started by clicking the play button on the UTM home screen.

![Start the virtual machine](../images/win-server-setup/setup-14.png)


## Step 15: Configure language and keyboard settings

The installation language was left as English. The time and currency format was set to **Turkish (Turkey)**, and the keyboard layout was set to **Turkish Q**.

![Language, region, and keyboard settings](../images/win-server-setup/setup-15.png)

## Step 16: Start the installation

**Install now** was selected in the Windows Server 2016 setup wizard.

![Start the installation](../images/win-server-setup/setup-16.png)

## Step 17: Select the installation edition

**Windows Server 2016 Standard Evaluation (Desktop Experience)** was selected because a graphical user interface was required. **Next** was then selected.

![Select the installation edition](../images/win-server-setup/setup-17.png)

## Step 18: Accept the license terms

The **I accept the license terms** checkbox was selected, and **Next** was clicked.

![Accept the license terms](../images/win-server-setup/setup-18.png)

## Step 19: Select the installation type

Because this was a clean installation on a new virtual machine, **Custom: Install Windows only (advanced)** was selected.

![Select the installation type](../images/win-server-setup/setup-19.png)

## Step 20: Select the installation disk

The 40 GB unallocated space was selected, allowing Windows to create the
required partitions, and **Next** was clicked.

![Select the installation disk](../images/win-server-setup/setup-20.png)

## Step 21: Install Windows Server

The setup was allowed to prepare files and install the required features and updates until the installation was complete.

![Install Windows Server](../images/win-server-setup/setup-21.png)

## Step 22: Set the administrator password

A strong password was entered and confirmed for the built-in `Administrator` account. **Finish** was then selected.

![Set the Administrator password](../images/win-server-setup/setup-22.png)

## Step 23: Send Ctrl+Alt+Delete

To open the sign-in screen, **Virtual Machine > Send Key > Ctrl+Alt+Delete** was selected from the UTM menu.

![Send Ctrl+Alt+Delete](../images/win-server-setup/setup-23.png)

## Step 24: Sign in as Administrator

The `Administrator` account password was entered to sign in to Windows Server.

![Sign in as Administrator](../images/win-server-setup/setup-24.png)

## Step 25: Verify the Windows Server desktop

The Windows Server 2016 desktop opened, confirming that the installation was completed successfully.

![Verify the Windows Server desktop](../images/win-server-setup/setup-25.png)

## Step 26: Open computer properties

In File Explorer, **This PC** was right-clicked and **Properties** was selected.

![Open computer properties](../images/win-server-setup/setup-26.png)

## Step 27: Open computer name settings

In the System window, **Change settings** was selected to open the computer name settings.

![Open computer name settings](../images/win-server-setup/setup-27.png)

## Step 28: Open the computer name dialog

The **Change...** button was selected to open the computer name change dialog.

![Open the computer name dialog](../images/win-server-setup/setup-28.png)

## Step 29: Set the server name to `SRVDC1`

The computer name was changed to `SRVDC1`, and the workgroup was left as`WORKGROUP`. A standard naming rule is useful for future administration.

![Set the server name to SRVDC1](../images/win-server-setup/setup-29.png)

## Step 30: Open network connection settings

After,restarting, The network icon was right-clicked, and **Open Network and Sharing Center** was selected.

![Open network connection settings](../images/win-server-setup/setup-30.png)

## Step 31: Open adapter settings

In Network and Sharing Center, **Change adapter settings** was selected.

![Open adapter settings](../images/win-server-setup/setup-31.png)

## Step 32: Open Ethernet properties

The Ethernet connection was right-clicked, and **Properties** was selected.

![Open Ethernet properties](../images/win-server-setup/setup-32.png)

## Step 33: Open IPv4 properties

**Internet Protocol Version 4 (TCP/IPv4)** was selected from the list, and the **Properties** button was clicked.

![Open IPv4 properties](../images/win-server-setup/setup-33.png)

## Step 34: Configure the static IP and DNS

The following static values were entered instead of obtaining an address
automatically:

- IP address: `10.0.100.10`
- Subnet mask: `255.255.255.255`
- Default gateway: empty
- Preferred DNS server: `10.0.100.10`


![Configure the static IP and DNS](../images/win-server-setup/setup-34.png)

## Step 35: Verify the network connection

The connection was shown as an unidentified network with no internet access. This is consistent with the isolated network scenario used for the lab. It is normal, don't worry.

![Verify the network connection](../images/win-server-setup/setup-35.png)

## Step 36: Open Windows Firewall settings

The **Windows Firewall** link was opened from Network and Sharing Center. **Turn Windows Firewall on or off** was selected.

![Open Windows Firewall settings](../images/win-server-setup/setup-36.png)


## Step 37: Open Turn Windows Firewall on or off

**Turn Windows Firewall on or off** was clicked.

![Open Turn Windows Firewall on or off](../images/win-server-setup/setup-37.png)

## Step 38: Turn off the firewall

To simplify connectivity testing in the lab environment, **Turn off Windows Firewall** was selected for both private and public network profiles.

> This setting is not recommended in production. In real environments, the firewall should remain enabled and only required ports should be allowed.

![Turn off Windows Firewall](../images/win-server-setup/setup-38.png)

## Step 39: Verify the firewall status

The Windows Firewall screen confirmed that the status was **Off** for both private and public network profiles.

![Verify firewall status](../images/win-server-setup/setup-39.png)

## Installation Result

The `SRVDC1` Windows Server 2016 Standard Evaluation virtual machine was
successfully prepared. The server was assigned 4 GB of RAM, 4 CPU cores, and a
40 GB disk. The static IPv4 address `10.0.100.10` was configured, and the same
address was set as the DNS server. This machine will be used for the subsequent
installation of Active Directory Domain Services.
