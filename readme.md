# Raspberry Pi - Shutdown Button and Status-LED

## Installation
Move python programm to bin directory and make it executable
```shell
sudo mv listen-for-shutdown.py /usr/local/bin/
sudo chmod +x /usr/local/bin/listen-for-shutdown.py
```

Place shell script in /etc/init.d/ and make it executable
```shell
sudo mv listen-for-shutdown.sh /etc/init.d/
sudo chmod +x /etc/init.d/listen-for-shutdown.sh
```

Register the script to run on boot
```shell
sudo update-rc.d listen-for-shutdown.sh defaults
```

Since the script won't be running, you can start it manually
```shell
sudo /etc/init.d/listen-for-shutdown.sh start
```