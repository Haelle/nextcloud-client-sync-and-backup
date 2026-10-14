# README

## Dépendances

Installation de `nextcloud-status` pour obtenir le status de sync Nextcloud en ligne de commande :

```sh
cd /xxx/
git clone https://github.com/fabianostermann/nextcloud-status.git
mkdir -p ~/.local/bin
cd ~/.local/bin
ln -s /path/to/nextcloud-status/nextcloud-status.py
```

## Crontab

```crontab -e
# Check Nextcloud sync status at 9:00
0 9 * * * /home/me/Projets/nextcloud-client-sync-and-backup/check-nextcloud-sync-status >/home/me/Projets/nextcloud-client-sync-and-backup/logs/cron-sync.log 2>&1

# Backup Nextcloud dir every month at 9:00
0 3 1 * * /home/me/Projets/nextcloud-client-sync-and-backup/simple-backup >/home/me/Projets/nextcloud-client-sync-and-backup/logs/cron-backup.log 2>&1
```
