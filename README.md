# Hey! I'm Filing Here

This lab helps us build a file system and understand ext2. 
## Building

To build this program, run 'make'. 

## Running

Show how to compile, mount, and example output of `ls -ain` your mounted
filesystem.

Once the code is complete, run 'make'. Then, './ext2-create' to create the cs111-base.img. Then, run 'dumpe2fs cs111-base.img' to dump the filesystem. 
Then, 'fsck.ext2 cs111-base.img' to check the filesystem. Then, to mount your filesystem to the directory create a mount with  'mkdir mnt'. 
Then, run 'sudo mount -o loop cs111-base.img mnt' to mount the filesystem and loop allows for a file. Then, do 'cd mnt' and then run 'ls -ain' to see the filesystem, permissions,
inode numbers, bytes, and more. An example output of 'ls-ain' is:

total 7
     2 drwxr-xr-x 3    0    0 1024 Jun  4 10:22 .
942269 drwxr-xr-x 5 1000 1000 4096 Jun  4 10:24 ..
    13 lrw-r--r-- 1 1000 1000   11 Jun  4 10:22 hello -> hello-world
    12 -rw-r--r-- 1 1000 1000   12 Jun  4 10:22 hello-world
    11 drwxr-xr-x 2    0    0 1024 Jun  4 10:22 lost+found

## Cleaning up

To unmount the filesystem, 'sudo umount mnt'. Then, to remove the mount directory is 'rmdir mnt'. Then to clean up all binary files run 'make clean'. 
