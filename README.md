# OJS3_roadWarrior
Bash script for installing OJS3 on Debian 10. Great for quickly testing out OJS3 on a virtual machine.

## Instructions

Run `bash roadWarrior.sh` as root from a fresh Debian 10 installation and enter the desired MySQL root password. The script will automatically:

1. Install prerequisite packages for OJS3
2. Configure MySQL with an `ojs` user
3. Download and install OJS3 `/var/www/html/`
4. The installation is available on `http://your.ip/`

## Notes

- MySQL user: `ojs` with a password `ojsPass1234`
- Username for OJS is `ojs`
- Password for OJS is `ojsPass1234`
- The script sets the `base_url` parameter in `config.inc.php` by the result of `hostname -I` command. If you have a domain, it's safer to change the first line of `roadWarrior.sh` to `ip="your.doman.name"`
