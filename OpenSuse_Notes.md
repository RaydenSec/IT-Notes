Knowledge Base for OpenSuse Tumbleweed Rolling Update Distribution

Update OpenSuse Tumbleweed
`sudo zypper refresh`
`sudo zypper update`

Change Screensize in VirtualBox
- Install `Guest additions`, open the directory in `Konsole`. Run the `autorun.sh` script w/ `./autorun.sh`, then try Full-screen. If i
- If it doesn't work, try  `auto-resize guest display` in the top bar, or exit and go to `settings -> display -> change resolution to resolution of your computer screen`

Increase speed for slow OpenSuse   
- In `etc/zypp/zypp.conf`, change `download.max_concurrent_connections` to `10` (while `zypp` does not support parallel downloads, it allows connection to several mirrors at one time to chooses the fastest one, rather than going through the options one at a time. Change `download.min_download_speed` to `20000` -> prevent connecting to mirrors slower than this. 

`YaST` for software management

`Codecs` for video compatability (community)

`sudo zypper install [software]` -> install 
`sudo zypper search [software]` -> list packages of search software
