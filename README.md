# OT-Slim-Restore

A modified restore script that allows OriginTrail Node restores from any backup method with minimal disk space.

OriginTrails restore script unneccesarily makes a copy of the entire backup you get when you download from wherever you store it. This is what takes up so much space and prevents restores without having 3x the space of the backup size available as free space.

This script simply removes that copy and restores from the original backup you downloaded!

Follow Milians guide here:  

https://otnode.com/node-backup/

With these changes:

Step 5:

1. mv otnode*/*/ backup
3. rm -rf otnode*

Step 8:

Skip this step entirely.

Done!
