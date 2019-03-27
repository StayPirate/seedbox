## One-liner command to rTorrent

That's the composefile I use to quickly deploy and manage my own seedbox. Since I store my downloads within a NAS via an NFS, this composefile maps the download-volume to a network file-system. If you don't want to use any network share, please edit the download volume configuration in [`docker-compose.yml`](docker-compose.yml). Or if you want to use CIFS, there is another brach in this repo with the already setuped configuration... switch to that branch.

### Quick deploy
1. `git clone https://github.com/StayPirate/seedbox.git`  
2. `cd seedbox`
3. `cp .env.example .env`  
4. Change information in `.env`.
5. `docker-compose up -d`
6. Use your browser to access the webUI.
7. Create a new Flood account. Connect Flood to rTorrent using `rtorrent` as host and port `16891` (as for the screenshot below).
        ![alt text](https://s5.nofilecdn.io/g/tZiZkxmJAfscqJiYGpwmihH34rGZeWW924QmJ7i7yLabNKz7RIkQ02d2UfXgywm9/p/flood.png "Flood Account Creation")  
8. Enjoy your torrents while **keep seeding!**
