# pycopy : a cp/rsync replacement for ACL inheritance when copying

This script works in a similar fashion as cp, except it is recursive by default.

Usage : 
```sh
./pycopy file1 path/to/target/dir
./pycopy file1 file2 dir1 dir2 path/to/target/dir
./pycopy source_file test_file
```

Why not use `rsync` or `cp` ? Because when copying some data in a directory with ACLs that should be inherited, both programs will simply ignore the ACLs, even with `cp --no-preserve` or `rsync --no-A --no-p`