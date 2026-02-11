# Authentication Log Analysis (Lab)

## Overview
This project demonstrates basic SSH authentication log analysis using a Kali Linux VM.

## Objective
- Start OpenSSH service
- Generate controlled failed login attempts
- Analyze authentication logs using journalctl
- Identify repeated "Failed password" events
- Verify event counts

## Commands Used

```bash
sudo service ssh start
sudo journalctl -b | grep "Failed password"
sudo journalctl -b | grep "Failed password" | wc -l
