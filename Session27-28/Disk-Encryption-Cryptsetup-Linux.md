# Full Disk Encryption using Cryptsetup

1. Shut down the VM. Attach an additional hard disk of 20GB to the Virtual machine. Power on the virtual machine. 

1. Install **cryptsetup** if it is not installed.

    For Ubuntu
    ```
    apt install cryptsetup
    ```

    For CentOS/Rocky 

    ```
    dnf install cryptsetup
    ```

1. Verify installation with 

    ```
    cryptsetup -h 
    OR
    cryptsetup --help
    ```

1. Now find out the hard disk device name using

    ```
    lsblk
    ```

1. Create a partition on the hard disk using 
    ```
    fdisk <hard-disk-device-name>
    fdisk /dev/nvme0n2
    ```

1. Check the partition name using 
    ```
    lsblk
    ```

1. Format the partition using cryptsetup

    ```
    cryptsetup luksFormat <hard-disk-partition>
    cryptsetup luksFormat /dev/nvme0n2p1
    ```

    > - it will prompt for the passphrase(password)
    >-  **Remember this password** as each time you want to mount this device the tool will prompt you for this password.


1. create a mapper device for this partition.

    ```
    cryptsetup luksOpen <hard-disk-partition> <mapper-name>
    cryptsetup luksOpen /dev/nvme0n2p1 my_mapper
    ```

1. One the command finishes, check that mapper was created successfully using  

    ```sh
    lsblk
    ```
    also with
    
    ```sh
    ls /dev/mapper 
    ```
    
    This should display an entry by the name that you specified in the above command.


1. Now you have to format the mapper device with the Linux file system. 

    ```sh
    mkfs.ext4 /dev/mapper/<mapper-name> # (given above)
    mkfs.ext4 /dev/mapper/my_mapper 
    ```

1. To mount this device create a mount point (directory).

    ```sh
    mkdir /mnt/<mount-directory-name>
    mkdir /mnt/cipher-data
    ```

1. Now mount the device
    
    ```sh
    mount /dev/mapper/<mapper-name> /mnt/<mount-directory-name>
    mount /dev/mapper/my_mapper /mnt/cipher-data
    ```

1. Now go to the directory 
    
    ```sh
    cd /mnt/<mount-directory-name>
    cd /mnt/cipher-data
    ```
    
> 🟢 Now you can create directories and files inside this.

## Unmounting  

Once you are done with accessing or creating the data then for safety reasons you can close the device.


1. Come of the directory then unmount the mapper device.

    ```sh
    umount /dev/mapper/<mapper-name>
    umount /dev/mapper/my_mapper
    ```
1. Now close the device.
    
    ```sh
    cryptsetup luksClose /dev/mapper/<mapper-name>
    cryptsetup luksClose /dev/mapper/my_mapper
    ```

1. You can check the properties of the device using 
    ```sh
    cryptsetup luksDump <hard-disk-device-name>
    cryptsetup luksDump /dev/nvme0n2
    ```

## Mounting

1. To mount the device again using following steps

    ```sh
    cryptsetup luksOpen <hard-disk-partition> <mapper-name>
    cryptsetup luksOpen /dev/nvme0n2p1 my_mapper
    ```

1. Then Mount it.
