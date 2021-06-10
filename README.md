# OT-Slim-Restore 

## A modified restore script that allows OriginTrail Node restores from your S3/B2 bucket with minimal disk space.

*For those that use alternate storage locations than S3/B2: You need the contents of the backup in /root/backup. All the files and folders must be in that folder and not in any additional folders. "ls -la backup" should show the various files and the arango/migrations folders.*

OriginTrails restore script unneccesarily makes a copy of the entire backup you get when you download from your S3/B2 bucket. This is what takes up so much space and prevents restores without having 3x the space of the backup size available as free space.

This script simply removes that copy and restores from the original backup you downloaded!

---

Commands to download and use:

1. Login as root
2. __cd__
3. __wget https://raw.githubusercontent.com/calr0x/OT-Slim-Restore/main/restore.sh__
4. __chmod +x restore.sh__

---

Then follow Milians guide here:  

https://otnode.com/node-backup/

With these changes:

Step 5:

1. __mv otnode*/*/ backup__
2. __rm -rf otnode*__

Step 8:

__Skip this step entirely.__

Done!
