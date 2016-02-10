# umount-nexus:<br>unmount a Nexus device from a Unix filesystem

Syntax:

    umount-nexus [path]

Example:

    umount-nexus

Example using a specific device:

    umount-nexus /media/nexus6

The path defaults to the most recent directory that matches:

    /media/nexus*

This script tries these steps to unmount:

   * use `umount` to unmount the directory
   * test if the directory still exists
   * if so, then try `lsof`, then try `fuser`
