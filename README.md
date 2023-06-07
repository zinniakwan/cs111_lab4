## UID: 205777626

(IMPORTANT: Only replace the above numbers with your true UID, do not modify spacing and newlines, otherwise your tarfile might not be created correctly)

# Hey! I'm Filing Here

Creation of a mountable file system with a directory, file, and symbolic link to the file.

## Building

Build with `make`.

## Running

Show how to compile, mount, and example output of `ls -ain` your mounted
filesystem.
Compile with `./ext2-create`, and that will build the cs111-base.img file.

Mount directory by first creating mnt directory (`mkdir mnt`) and then running `sudo mount -o loop cs111-base.img mnt`.

If we run `cd mnt` and then `ls -ain`, the output should be:
```
total 7
2 drwxr -xr -x  3 0     0       1024 .
                                    ..
13 lrw -r--r--  1 1000  1000    11  hello->hello-world
12 -rw -r--r--  1 1000  1000    12  hello-world
11 drwxr -xr -x 2 0     0       1024 lost+found
```


## Cleaning up

We unmount the filesystem by calling `sudo umount mnt` and remove directory with `rmdir mnt`. 

Clean up all files with `make clean`.
