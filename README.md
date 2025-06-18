# datagram-node-run
datagran node setup in vps
```
wget -O datagram-installer.sh https://gist.githubusercontent.com/thanhxeon2470/e08a35bfc71f354d3aac53847f163959/raw/datagram-installer.sh && chmod +x datagram-installer.sh && sudo bash datagram-installer.sh
```
```
sudo mkdir -p /root/.datagram/tmp
sudo chown root:root /root/.datagram/tmp
```
```
sudo apt install nano
```
```
sudo systemctl edit datagram.service
```
now paste the following inside datagram.service
```
[Service]
Environment=TMPDIR=/root/.datagram/tmp
```
```
sudo systemctl daemon-reexec
sudo systemctl daemon-reload
sudo systemctl restart datagram.service
```
