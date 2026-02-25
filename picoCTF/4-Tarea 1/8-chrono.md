## ASCII Numbers

### Descripción
How to automate tasks to run at intervals on linux servers?
Additional details will be available after launching your challenge instance.
### Solución

#### Solución 1

```

picoplayer@challenge:~$ cd ..
picoplayer@challenge:/home$ cd ..
picoplayer@challenge:/$ ls
bin   challenge  etc   lib    lib64   media  opt   root  sbin  sys  usr
boot  dev        home  lib32  libx32  mnt    proc  run   srv   tmp  var
picoplayer@challenge:/$ cd challenge/
-bash: cd: challenge/: Permission denied
picoplayer@challenge:/$ cd etc/
picoplayer@challenge:/etc$ ls
adduser.conf            e2scrub.conf  legal                passwd       ssh
alternatives            environment   libaudit.conf        passwd-      ssl
apt                     fstab         localtime            profile      subgid
bash.bashrc             gai.conf      login.defs           profile.d    subgid-
bindresvport.blacklist  group         logrotate.d          python3      subuid
binfmt.d                group-        lsb-release          python3.8    subuid-
ca-certificates         gshadow       machine-id           rc0.d        sudoers
ca-certificates.conf    gshadow-      magic                rc1.d        sudoers.d
cloud                   gss           magic.mime           rc2.d        sysctl.conf
cron.d                  host.conf     mailcap              rc3.d        sysctl.d
cron.daily              hostname      mailcap.order        rc4.d        systemd
cron.hourly             hosts         mime.types           rc5.d        terminfo
cron.monthly            hosts.allow   mke2fs.conf          rc6.d        timezone
cron.weekly             hosts.deny    modules-load.d       rcS.d        tmpfiles.d
crontab                 init.d        mtab                 resolv.conf  ucf.conf
dbus-1                  inputrc       networkd-dispatcher  rmt          ufw
debconf.conf            issue         networks             security     update-motd.d
debian_version          issue.net     nsswitch.conf        selinux      wgetrc
default                 kernel        opt                  shadow       xattr.conf
deluser.conf            ld.so.cache   os-release           shadow-      xdg
dhcp                    ld.so.conf    pam.conf             shells
dpkg                    ld.so.conf.d  pam.d                skel
picoplayer@challenge:/etc$ cat crontab 
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_5b7059d0}
```
picoCTF{Sch3DUL7NG_T45K3_L1NUX_5b7059d0}
### Notas adicionales

### Referencias

-