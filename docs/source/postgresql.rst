sudo systemctl stop postgresql-14.service
sudo dnf remove postgresql14 postgresql14-server postgresql14-contrib
sudo rm -rf /var/lib/pgsql/14/data
sudo rm -rf /etc/postgresql/14
sudo systemctl daemon-reload
systemctl status postgresql-14.service
sudo rm -f /etc/systemd/system/postgresql-14.service
systemctl status postgresql-14.service
sudo reboot

sudo dnf remove pgdg-fedora-repo
sudo dnf list installed | grep pgdg-fedora-repo


sudo dnf remove postgresql postgresql-server postgresql-contrib
sudo rm -rf /var/lib/pgsql/data
sudo rm -rf /etc/postgresql
sudo userdel postgres
sudo groupdel postgres
sudo dnf autoremove
