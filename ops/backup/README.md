# Backups

- slwin11ops backup based on [netstack backup-powershell-wdadmin](https://netstack.org/docs/ops/backup/backup-powershell-wbadmin)

```powershell
wbadmin start backup -backupTarget:E: -include:C: -quiet -allCritical
```
