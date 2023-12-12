# Purple-Dragon-Defense

## GVM
### Useful Commands
- Get new hashes!
  > gvm-feed-update
- 

### Troubleshooting

1. While attempting to start GVM I received the following error:
  > Job for ospd-openvas.service failed because the control process exited with error code.
See "systemctl status ospd-openvas.service" and "journalctl -xeu ospd-openvas.service" for details.
Job for gvmd.service failed because a timeout was exceeded.
See "systemctl status gvmd.service" and "journalctl -xeu gvmd.service" for details.

In order to see the status here run this command:
  > journalctl -xeu ospd-openvas.service -o cat

So likely this is a permission issue and is the result of pulling down the new hashes as root
