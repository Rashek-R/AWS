## Attach and Mount an EBS volume to EC2 Linux Instance
### AWS allows you to create new EBS volumes, and you can attach them to instances for extra storage,to make EBS volume usable as storage inside the instance, you need to mount it to a specific folder.
### Step1:
### create a new volume of your preferred size and type.

1-Selete volume option from left side dashboared on EC2

![1](https://github.com/Rashek-R/AWS/assets/134732001/9728ee9e-4066-459e-8047-986dffc87768)

2-Click create volume

![image](https://github.com/Rashek-R/AWS/assets/134732001/258c2db4-46ed-4147-91aa-4a22f77ca24b)

3- create a new volume as required type and size.

![image](https://github.com/Rashek-R/AWS/assets/134732001/5615ef58-568c-4c79-9d55-fe89a7050cfa)

4-Now select the created voulme and attach to the insatnce 

![image](https://github.com/Rashek-R/AWS/assets/134732001/a7123f45-9b97-4ce4-93da-0010c634e35c)

5-Select the instance and Attach the volume 

![image](https://github.com/Rashek-R/AWS/assets/134732001/91948070-bc3c-4420-adf7-eb916c926da5)

### Now, login to your ec2 instance .

1-list the available disks using the following command- "lsbk"

![image](https://github.com/Rashek-R/AWS/assets/134732001/709b503c-a343-4228-a008-4d7e80fdbd5b)

2-Format the volume to the ext4 filesystem using the following command-"sudo file -s /dev/xvdf"

![image](https://github.com/Rashek-R/AWS/assets/134732001/93bf4e33-1b21-41cd-862a-0580aeddf4a8)







