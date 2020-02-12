pyFTPclient
===========

FTP client is written in Python with monitoring and reconnection; it utilises the ftplib & threading.
This client can be usefull if it needs to download big files ( >1 Gb)


**Features**
- it shows a download progress
- socket settings are optimised for download 
- it monitors status of the FTP connection
- it reconnects in case of a disconnect and continues file download from the point of disconnect
- amount of attemps are configurable

**How to use**
```python
    logging.basicConfig(format='%(asctime)s %(levelname)s: %(message)s', level=cfg.logging.level)
    obj = PyFTPclient('192.168.0.59', port = 2121, login = 'test', passwd = 'testftp')
    obj.DownloadFile('my-huge-file.mp4')
```    
