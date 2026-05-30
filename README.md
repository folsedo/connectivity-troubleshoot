# Dev-Machine2 Web Server Connectivity Troubleshooting

## Objective
Troubleshoot connectivity issues reported by end users on the Dev-Machine2 web server.

## Troubleshooting Summary

I investigated the connectivity issue on the Dev-Machine2 server by validating the network configuration, testing connectivity, reviewing firewall settings, checking listening ports, and verifying the web service status.

### Verify Network Interface Status
```bash
nmcli dev status
```
Verified that the network interface was connected and operational.

### Verify IPv4 Configuration
```bash
nmcli con show <connection-name> | grep IP4
```
Reviewed the server's IPv4 address, gateway, and DNS settings to ensure the network configuration was correct.

### Test Connectivity
```bash
ping <target-ip>
```
Tested communication between the server and network resources to verify connectivity.

### Review Firewall Configuration
```bash
sudo firewall-cmd --list-all
```
Checked active firewall rules, allowed services, and open ports to ensure traffic was not being blocked.

### Check Listening Ports and Services
```bash
sudo ss -tulnp
```
Reviewed listening ports and identified active processes accepting network connections.

### Verify Web Service Status
```bash
systemctl status httpd
```
Checked the Apache web server service to determine whether it was running, stopped, or experiencing failures.

## Results

During troubleshooting, I confirmed that the network interface was active, verified the server's IP configuration, tested network communication, reviewed firewall accessibility, validated listening ports, and checked the Apache service status. These steps helped isolate potential causes of the reported connectivity issue and provided a structured approach to diagnosing web server availability problems.

## Commands Used

```bash
nmcli dev status
nmcli con show <connection-name> | grep IP4
ping <target-ip>
sudo firewall-cmd --list-all
sudo ss -tulnp
systemctl status httpd
```

## Skills Demonstrated

- Linux Network Troubleshooting
- Network Connectivity Validation
- Firewall Analysis
- Service Management
- Port and Socket Inspection
- Web Server Troubleshooting
- Root Cause Investigation
- Technical Documentation
