### Truenas zfs scripts
These are some truenas and ZFS scripts I wrote for my own use. 

**CAUTION**
Use these scripts at your own risk.

They worked for me, but need to be adapted for general purpose use.

Some of these use hard coded paths.

Read the code before using and modify to fit your taste.

They may save you time if you are trying to do similar things as I did:
1. `system_config_save`: make truenas config backups automatically. be sure to edit the destination for 
where you want to put the backup.
2. `zfs_diff`: to compare current with any past snapshot
3. `zfs mv`: rename zfs dataset or zvol (similar to mv). Last arg is an absolute path, e.g., main/new/dataset/name
4. `tcp_params_set`: triple the bandwidth on a single stream for remote sites with high ping times. You can do this in sysctl settings in TN, but the script form was less work if you have to do it on multiple systems. I added to crontab of my TN as a startup task.
5. `zfs_backup`: Uses `zfs send` to create a backup file of certain datasets. I no longer use this because I now use TN to TN replication in the GUI.
6. `seatbelts`: Fasten before big change. Release when done. Don't keep them on long because you can't do certain operations with seatbelts on. Creates a config backup too. 
