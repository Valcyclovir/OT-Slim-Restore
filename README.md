# OT-Slim-Restore

A modified restore script that allows OriginTrail Node restores from your S3/B2 bucket with minimal disk space.

** For those that use alternate storage locations than S3/B2: You need the contents of the backup in /root/backup. All the files and folders must be in that folder and not in any additional folders. "ls -la backup" should show the various files and the arango/migrations folders. **

OriginTrails restore script unneccesarily makes a copy of the entire backup you get when you download from your S3/B2 bucket. This is what takes up so much space and prevents restores without having 3x the space of the backup size available as free space.

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
