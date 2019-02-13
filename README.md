## One-liner command to rTorrent

That's the composefile I use to quickly deploy and manage my own seedbox. Since I store my downloads within a NAS via an smb share, this composefile maps the download-volume to a network share using creds provided by `.env` file. If you don't want to use any SMB shares, please edit the download volume configuration in [`docker-compose.yml`](docker-compose.yml).

### Quick deploy
1. `git clone https://github.com/StayPirate/rtorrent-flood.git`  
2. `cd rtorrent-flood`
3. `cp .env.example .env`  
4. Change information in `.env` with your smb share's data.
5. `docker-compose up`
6. Open `http://localhost` in your browser.
7. Create a new Flood account. Connect Flood to rTorrent using `rtorrent` as host and port `16891` (as for the screenshot below).
 ![alt text](https://s5.nofilecdn.io/g/tZiZkxmJAfscqJiYGpwmihH34rGZeWW924QmJ7i7yLabNKz7RIkQ02d2UfXgywm9/p/flood.png "Flood Account Creation")  
8. Enjoy your torrents while **keep seeding!**
