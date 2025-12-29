# Troubleshooting

Encountering issues? Here are solutions to common problems.

## Connection Issues

### "Cannot Connect to Router"
- **Check Wi-Fi**: Ensure your phone is connected to the OpenWRT router's Wi-Fi.
- **Verify IP**: Double-check the router IP address (default `192.168.1.1`).
- **HTTPS/HTTP**: WRTune attempts both, but if you have a custom SSL setup, ensure your router accepts the connection.

## Permission Errors

### "Failed to Block Device"
- This usually happens if the router's firewall rules are locked or modified by another custom script.
- **Fix**: Try restarting the router or refreshing the device list. Ensure the user account has `sudo` or root-equivalent permissions for firewall changes via `ubus`.

## Missing Data

### "No Traffic History"
- Historical traffic data relies on the `nlbwmon` package being installed on your OpenWRT router.
- **Install nlbwmon**:
  ```bash
  opkg update
  opkg install nlbwmon
  ```

## Still Need Help?
If your issue isn't listed here, please [open an issue](../../issues) on our GitHub repository.
