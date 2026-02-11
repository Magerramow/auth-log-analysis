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

## Findings
- Identified multiple failed SSH authentication attempts.
- Observed repeated "Failed password for invalid user" events.
- Confirmed all attempts originated from localhost (::1) as part of controlled lab testing.
- Verified event count using command-line filtering.

## Skills Practiced
- Basic Linux log analysis
- Using journalctl for event investigation
- Filtering security events with grep
