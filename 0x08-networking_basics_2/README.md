# Networking basics #1

## Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

## General
* What is localhost/127.0.0.1
* What is 0.0.0.0
* What is /etc/hosts
* How to display your machine’s active network interfaces

## Requirements
### General
* Allowed editors: vi, vim, emacs
* All your files will be interpreted on Ubuntu 20.04 LTS
* All your files should end with a new line
* A README.md file, at the root of the folder of the project, is mandatory
* All your Bash script files must be executable
* Your Bash script must pass Shellcheck (version 0.7.0 via apt-get) without any errors
* The first line of all your Bash scripts should be exactly ***#!/usr/bin/env bash***
* The second line of all your Bash scripts should be a comment explaining what is the script doing

#### LIST OF FILES
#### 0-change_your_home_IP
Bash script that configures an Ubuntu server with the below requirements.<br>
Requirements: <br>
	      - localhost resolves to `127.0.0.2`
	      - facebook.com resolves to `8.8.8.8.`

#### 1-show_attached_IPs
Bash script that displays all active IPv4 IPs on the machine s executed on.it

#### 100-port_listening_on_localhost
Bash script that listens on port 98 on localhost.</br>
