# linuxadmin
System Administration Commands


Important System Directories
 <details>
## DIRECTORIES ##
cat      /etc/hostname                       # Instance's hostname
cat      /etc/nsswitch.conf                  # List of Databases: 'passwd', 'hosts', and sources for those DBs
cat      /etc/hosts                          # Mapping of hostnames to IP addresses
cat      /etc/hosts.allow                    # Allowed hostnames, processed first
cat      /etc/hosts.deny                     # Denied hostnames, processed second
cat      /etc/nologin                        # If exists, only root can login. Contents of file displayed
cat      /etc/passwd                         # DB of info on users, can include hashed passwords, or x
cat      /etc/shadow                         # DB of users and hashed passwords + password config
cat      /etc/group                          # DB of groups + users in groups, can include group passwords
cat      /etc/gshadow                        # DB of groups and hashed passwords + password config
ls       /etc/skel                           # Its contents will be copied to each new user's /home/ directory
cat      /etc/profile                        # Set system wide environmental variables on users shells
file     /bin/bash                           # Unix shell and command language
cat      /etc/bash.bashrc                    # System wide bash initialization file
cat      /etc/aliases                        # Aliases for sendmail. Not bash aliases
cat      ~/.profile                          # User specific shell initialization script/file.
cat      ~/.bashrc                           # Personal bash initialization file for interactive, non-login shells
cat      ~/.bash_profile                     # Personal bash initialization file login shells (console or ssh)
cat      ~/.bash_aliases                     # Personal bash aliases config, can also go bash_profile, or bashrc
cat      ~/.bash_login                       # Additional config executed right after login
cat      ~/.bash_logout                      # Additional config executed right after logout
cat      ~/.bash_history                     # Bash command history
cat      /etc/issue                          # Message or system identification to be printed before the login prompt
cat      /etc/os-release                     # Contains OS info
cat      /etc/crontab                        # Contains the crontab file jobs and scheduling
ls       /etc/cron.daily                     # Contains the crontab scripts to be run daily
cat      /etc/anacrontab                     # Contains the anacrontab file jobs and scheduling
cat      /etc/at.allow                       # Determines which user can submit commands for later execution via at or batch
cat      /etc/at.deny                        # Determines which user can submit commands for later execution via at or batch
cat      /etc/protocols                      # DB of TCP/IP protocols + protocol number + description
cat      /etc/services                       # DB of services and TCP/UDP ports used + description
cat      /etc/timezone                       # Stores configured timezone
cat      /etc/localtime                      # Stores configured localtime
cat      /etc/sudoers                        # Determines the groups and users sudo priviledges. Edit with visudo
ls       /etc/sudoers.d/                     # Ideal place to add sudoers
cat      /etc/ntp.conf                       # Configuration file for for ntpd
cat      /etc/inetd.conf                     # Configuration file for inetd. Edit requires service restart
cat      /etc/xinetd.conf                    # Configuration file for xinetd. Edit requires service restart
ls       /etc/xinetd.d/                      # Configuration files for each service managed by xinetd . Edit requires service restart
cat      /etc/initramfs-tools/initramfs.conf # Configuration file for initramfs
ls       /etc/udev                           # Device Manager - udev (systemd). Execute changes from kernel in /sys and /dev
cat      /etc/udev/udev.conf                 # udev configuration file.
file     /usr/sbin/logrotate                 # Log rotation utility
cat      /etc/logrotate.conf                 # Configuration file for logrotate
ls       /etc/logrotate.d                    # Configuration files for logrotate - system packages
cat      /etc/logrotate.d/rsyslog            # Configuration files for logrotate - system rsyslog
cat      /etc/rsyslog.conf                   # Configuration file for syslog
ls       /etc/rsyslog.d                      # Configuration files for services
cat      /etc/rsyslog.d/50-default.conf      # Default logging rules
cat      /etc/updatedb.conf                  # Config file read by updatedb before updating the locate database
cat      /etc/environment                    # Stores the PATH env variable
cat      /etc/fstab                          # Where should partitions should be mounted and how
ls       /etc/rc0.d                          # System-v runlevel initiation - halt
ls       /etc/rc6.d                          # System-v runlevel initiation - reboot
cat      /etc/init/dbus.conf                 # dbus config file
file     /sbin/upstart                       # Upstart initialization script
ls       /etc/init                           # Contains configuration files used by Upstart
file     /sbin/init                          # System-V initialization script
ls       /etc/init.d                         # Contains scripts used by the System V init tools
cat      /etc/init.d/networking              # System-v script for service
cat      /etc/init.d/cron                    # System-v script for service
cat      /etc/init.d/halt                    # System-v script for service
cat      /etc/init.d/dbus                    # System-v script for service
cat      /etc/init.d/functions               # Contains functions to be used by most or all shell scripts stored in the /etc/init.d directory
cat      /etc/inittab                        # describes how the INIT process should set up the system in a certain run-level (RedHat - Sys-V)
ls -lrt  /bin/systemd                        # Systemd initialization script symlink
file     /lib/systemd/systemd                # Systemd initialization script
ls -lrt  /etc/systemd/system/                # Contains symlinks to files in lib/systemd/system/
ls       /lib/systemd/system/*.target        # Contains init scripts
cat      /etc/systemd/journald.conf          # Configuration for the systemd journal logging service
cat      /etc/default/grub                   # GRUB config. Run 'update-grub' to update grub.cfg
ls       /etc/grub.d/                        # Additional files to configure the GRUB menu
cat      /boot/grub/menu.lst                 # GRUB menu list config file
cat      /boot/grub/grub.cfg                 # GRUB 2 menu list config file
cat      /etc/dhcp/dhclient.conf             # Configuration file for /sbin/dhclient - DHCP
cat      /etc/network/interfaces             # Network interface configuration information (Debian)
cat      /etc/sysconfig/network              # Network interface configuration information (RedHat)
cat      /etc/sysconfig/network-scripts      # Network interface configuration information (RedHat)
cat      /etc/ssh/sshd_config                # OpenSSH service configuration file
cat      /etc/cups/cupsd.conf                # Configuration file for the CUPS scheduler
ls       /usr/share/X11/xorg.conf.d/         # Xorg configuration file directory
cat      /etc/apt/sources.list               # Lists the 'sources' from which packages can be obtained
cat      /etc/yum.conf                       # Yum configuration file
ls       /etc/yum.repos.d                    # A list of directories where to look for .repo files
cat      /etc/ld.so.conf                     # Contains a list of directories in which to search for libraries for ldconfig
ls       /etc/ld.so.conf.d/                  # Directories in which to search for libraries for ldconfig, add new libs here, run ldconfig
ls       /lib                                # Library directory, also searched by ldconfig
ls       /usr/lib                            # Library directory, also searched by ldconfig
ls       /dev/sd*                            # SCSI drives
cat      /proc/1/status                      # Pseudo filesystem with info on running process
cat      /proc/1/io                          # Pseudo filesystem with info on running process
cat      /proc/1/syscall                     # Pseudo filesystem with info on running process
ls       /var/log                            # Main directory for log files
cat      /var/log/syslog                     # Syslog log files
cat      /var/log/mail.log                   # Mail log files - MTA
cat      ~/.forward                          # Email forwarding configuration
ls       ~/.ssh/                             # Root dir of ssh keys and config
cat      ~/.ssh/id_rsa                       # Example of ssh private key
cat      ~/.ssh/id_rsa.pub                   # Example of ssh public key
cp       ~/.ssh/authorized_keys              # Configures permanent access using SSH keys - copy .pub keys here
cat      /etc/ssh/ssh_known_hosts            # Systemwide list of known host keys.
cat      ~/.ssh/known_hosts                  # list of host keys for user not already in the systemwide list
<summary>
