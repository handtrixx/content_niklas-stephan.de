+++
title = 'Distrobox oder: "Ich baue mir die Welt, so wie sie mir gefällt"'
image = '01_mac_time_machine_logo-56a5d49b5f9b58b7d0de9f0b-1.jpg'
date = 2025-03-19
lastmod = 2025-03-19
draft = false
tags = ['deutsch', 'linux']
+++

## Installation

```bash
sudo dnf install distrobox
```

## Create a OS container

```bash
distrobox create --name ubuntu_container --image ubuntu:latest
```

## Enter container

```bash
distrobox enter ubuntu_container
```

## Other commands

```bash
distrobox list
distrobox stop ubuntu_container
distrobox rm ubuntu_container
```
