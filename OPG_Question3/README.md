# Pre-interview test answer to Question 3
Submitted by Nick Romney 2 January 2018

## Question
Write a script in python or bash that can configure ephemeral storage on an AWS instance to create a logical volume that can be mounted on /opt. The script would be run as part of the bootstrap process and make use of all ephemeral storage devices.

### Approach
From https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html#instance-store-volumes we will pick an EC2 instance type which will support adding an Instance store
m1.medium (from an older generation, but still available)

If we run the command
```
sudo fdisk -l
```
we see that the instance store is available as /dev/xvdb
It already contains an ext3 file system

In the context of the userdata step on instance launch, this command will mount it to /opt
```
sudo mount -t ext3 /dev/xvdb /opt
```