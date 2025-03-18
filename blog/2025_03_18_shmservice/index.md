+++
title = 'SHM Service'
date = 2025-03-18
lastmod = 2025-03-18
draft = true
tags = ['english']
+++

To execute your shm.sh script on every boot before the Docker service starts, you can 
create a systemd service unit that runs your script and configures it to run before the Docker service. 
Here are the steps to achieve this:


1. Create a systemd service unit file for your script:
Create a new file /etc/systemd/system/shm.service with the following content:
```shell
[Unit]
Description=Run shm.sh script
Before=docker.service
Wants=docker.service

[Service]
Type=oneshot
ExecStart=/bin/bash /path/to/your/shm.sh
RemainAfterExit=true

[Install]
WantedBy=multi-user.target
```

Replace shm.sh with the actual path to your shm.sh script.

2. Reload systemd to recognize the new service:
```bash
sudo systemctl daemon-reload
```

3. Reload systemd to recognize the new service:
```bash
sudo systemctl enable shm.service
```

4. Reload systemd to recognize the new service:
```bash
sudo systemctl start shm.service
```