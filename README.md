### Truenas zfs scripts
These are handy truenas and ZFS scripts to do things such as:
1. `system_config_save`: make truenas config backups automatically
2. `zfs_diff`: (using the API) to compare current with any past snapshot
3. `zfs mv`: rename zfs dataset or zvol (similar to mv)
4. `tcp_params_set`: triple the bandwidth on a single stream
5. `zfs_backup`: Uses `zfs send` to create a backup file of certain datasets
6. `zvol_backup`: Uses `zfs send` to create a backup file of just my zVols
7. `seatbelts`: Fasten before big change. Release when done. Don't keep them on long because you can't do certain operations with seatbelts on. Allows you to roll back a pool, NOT truenas config chanes.