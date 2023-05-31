## Attach and Mount an EBS volume to EC2 Linux Instance
### AWS allows you to create new EBS volumes, and you can attach them to instances for extra storage,to make EBS volume usable as storage inside the instance, you need to mount it to a specific folder.

### create a new volume of your preferred size and type.

1-Selete volume option from left side dashboared on EC2

![1](https://github.com/Rashek-R/AWS/assets/134732001/9728ee9e-4066-459e-8047-986dffc87768)

2-Click create volume

![image](https://github.com/Rashek-R/AWS/assets/134732001/258c2db4-46ed-4147-91aa-4a22f77ca24b)

3- create a new volume as required type and size.

![image](https://github.com/Rashek-R/AWS/assets/134732001/1e019754-ee21-49d2-b579-cc19f168e24f)


4-Now select the created voulme and attach to the insatnce 

![image](https://github.com/Rashek-R/AWS/assets/134732001/a7123f45-9b97-4ce4-93da-0010c634e35c)

5-Select the instance and Attach the volume 

![image](https://github.com/Rashek-R/AWS/assets/134732001/91948070-bc3c-4420-adf7-eb916c926da5)

### Now, login to your ec2 instance .

1-list the available disks using the following command- "lsbk"

![image](https://github.com/Rashek-R/AWS/assets/134732001/709b503c-a343-4228-a008-4d7e80fdbd5b)

2-Partion the Ebs volume following command- "fdisk /loacation/diskname eg: fdisk /dev/xvdf

![Capture1](https://github.com/Rashek-R/AWS/assets/134732001/c39b7e02-a9b5-4c4f-ae0e-66b28d5ab261)

3-Format the volume the filesystem using the following command. "sudo mkfs -t filesystem type /dev/xvdf eg: sudo mkfs -t ext4 /dev/xvdf "

![Capture2](https://github.com/Rashek-R/AWS/assets/134732001/d3ca7ac1-331c-41ef-b9d6-1782564fbd30)

4-To make the changes permentent Open /etc/fstab file and make an entry in the following format.
  device_name mount_point file_system_type fs_mntops fs_freq fs_passno eg:"/dev/xvdf1 /var/www/html/  ext4  defaults 0   2"
  
  ![Capture3](https://github.com/Rashek-R/AWS/assets/134732001/fa255ca6-3018-411f-9632-d829c920a157)

5-For mount the volume using following command. "sudo mount -a"

![Capture4](https://github.com/Rashek-R/AWS/assets/134732001/5adc4fe9-062d-4170-8a2f-33c613066193)

### Final Result:

The EBS volume successfull attached to the linux instance

![image](https://github.com/Rashek-R/AWS/assets/134732001/560374a8-31c6-41e9-a656-2397afefc4c2)










