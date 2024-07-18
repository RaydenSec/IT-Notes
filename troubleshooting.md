# Troubleshooting

- [Windows Memory](##windows-memory)
- [Windows Installation](##windows-installation)
- [slow Internet](##slow-internet)
- [Dns](##dns)
- [Flushing DNS](##flushing-dns)
- [Python CLI Error](##python-cli-error)

## slow Internet
If a lot of customers are complaining about slow internet, you might need to increase bandwidth (Dos attack can also cause this)

## Dns
If can ping localhost, own IP, Router on network and IP of website on the internet, but user can’t access webpages on the internet, means they have incorrect Dns address assigned -> if you type in youtube.com, w/out DNs, it does not know what youtube.com is

## Flush DNS
ipconfig /flushdns

## Python CLI Error
Windows: Installed Python3 from official website, but when running `Python3` in CLI, redirected to Microsoft Store page to download Python. 
Reason: Need to run Python3 where the software is located, not just anywhere in other directories. 
Solution: Find where Python3 is located, copy the path. Then goto properties for `This PC`, in `Advanced system settings`, click on `Environment Variables`. Find `path` variable and `edit`, and create `New` path. Paste in path to directory where Python is. Can check if it's installed and accessible anywhere in CLI w/ `python3 --version`
