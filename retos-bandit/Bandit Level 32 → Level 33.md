Bandit Level 32→ Level 33

## Objetivo

After all this `git` stuff its time for another escape. Good luck!
## Datos de acceso al nivel

```
Usuario: bandit32
Contraseña: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
```
## Solución
```
Bash
WELCOME TO THE UPPERCASE SHELL

>> ls

sh: 1: LS: Permission denied

>> LS

sh: 1: LS: Permission denied

>> man

sh: 1: MAN: Permission denied

>> 0 $

sh: 1: 0: Permission denied

>> $0

$ pwd

/home/bandit32

$ ls -la

total 36

drwxr-xr-x  2 root     root      4096 Apr 23 18:04 .

drwxr-xr-x 70 root     root      4096 Apr 23 18:05 ..

-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout

-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc

-rw-r--r--  1 root     root       807 Jan  6  2022 .profile

-rwsr-x---  1 bandit33 bandit32 15128 Apr 23 18:04 uppershell

$ cat uppershell

ELF?4?64 

         (444``???00 ??

                       /

                        ?

                        0</?????DDP?td, ,,,,Q?tdR?td

                                                    /

                                                     ?

                                                     ??/lib/ld-linux.so.2GNU?dG?Vm@?U20X?y3|

                                                                                            GNU

                                                                                               ?( 

                                                                                                  ?K??gUa4HOU/A? ];@_IO_stdin_usedexittoupper__libc_start_mainputsprintfstdinsystemfflushfgetsgeteuidsetreuidlibc.so.6GLIBC_p???z@?C_2.34__gmon_start__fii

 $(?    ,?

0?

 ??S??#???/????????t?Ѓ[??5??%

                             h??????%??????%h??????%h?????%h ?????% h(?????%$h0?????%(h8?p????%,h@?`????%0hH?P?????1?^????PTR???

                  /jjQV???P?4????$?f?f?f?f?f?f?f?????f?f?f?f?f???$?f?f?f?f?f?f??<=<t$???t???h<?Ѓ??Í?&f?Í?&??&??<-<?????????t ???tU???Ph<?҃??Ít&Í?&???=Du???h????D?Í?&Í?&??늍L$????q?U??SQ?? ?ȋ@??????e??E?1??Z??????S????SP????????

      ?I???????

               h'?????????

                          j????????@??Ph???????P?????????u

??

  j????ǅ?????9??????????????????

                                P??????????????????Ȉ??????????????????????u???

                                                                               ??????P???????G?????S????????,?[?WELCOME TO THE UPPERCASE SHELL>> (???l????D????X?????zR|

                                                         h???10???? D????F

                                                                          J

D                                                                          tx?;*2$"$h2???

 IuBuxu|?f

?         ?

???o??

?

?DT{?o????o???o?FVfv????GCC: (Ubuntu 11.3.0-1ubuntu1~22.04) 11.3.0 ??@?

 ??????????,??

1C<O?CS<Z`r4?? ??8???@?H ?

    crt1.o__abi_tagcrtstuff.cderegister_tm_clones__do_global_dtors_auxcompleted.0__do_global_dtors_aux_fini_array_entryframe_dummy__frame_dummy_init_array_entryupper.c__FRAME_END___DYNAMIC__GNU_EH_FRAME_HDR_GLOBAL_OFFSET_TABLE___libc_start_main@GLIBC_2.34__x86.get_pc_thunk.bxprintf@GLIBC_2.0fflush@GLIBC_2.0fgets@GLIBC_2.0_edata_finigeteuid@GLIBC_2.0__data_startputs@GLIBC_2.0system@GLIBC_2.0__gmon_start__exit@GLIBC_2.0__dso_handle_IO_stdin_usedsetreuid@GLIBC_2.0stdin@GLIBC_2.0_end_dl_relocate_static_pie_fp_hw__bss_startmaintoupper@GLIBC_2.0__TMC_END___init.symtab.strtab.shstrtab.interp.note.gnu.build-id.note.ABI-tag.gnu.hash.dynsym.dynstr.gnu.version.gnu.version_r.rel.dyn.rel.plt.init.text.fini.rodata.eh_frame_hdr.eh_frame.init_array.fini_array.dynamic.got.got.plt.data.bss.comment?#??$? D???o?$N

                                   ?V???^???o??k???o??0z ? B???$?00????#?? +?,, ,?XX ??

                                                                                                    ?

                                                                                                    /?/?/???/?04?44@< ?0<0+h0? 83U?5$ ^[[A^[[B^C

$ ls      

uppershell

$ cat .profile

# ~/.profile: executed by the command interpreter for login shells.

# This file is not read by bash(1), if ~/.bash_profile or ~/.bash_login

# exists.

# see /usr/share/doc/bash/examples/startup-files for examples.

# the files are located in the bash-doc package.

  

# the default umask is set in /etc/profile; for setting the umask

# for ssh logins, install and configure the libpam-umask package.

#umask 022

  

# if running bash

if [ -n "$BASH_VERSION" ]; then

    # include .bashrc if it exists

    if [ -f "$HOME/.bashrc" ]; then

. "$HOME/.bashrc"

    fi

fi

  

# set PATH so it includes user's private bin if it exists

if [ -d "$HOME/bin" ] ; then

    PATH="$HOME/bin:$PATH"

fi

  

# set PATH so it includes user's private bin if it exists

if [ -d "$HOME/.local/bin" ] ; then

    PATH="$HOME/.local/bin:$PATH"

fi

$ cd /etc

$ ls

NetworkManager       group   logrotate.d   rcS.d

PackageKit       group-   lsb-release   resolv.conf

X11       grub.d   ltrace.conf   rmt

acpi       gshadow   lvm   rpc

adduser.conf       gshadow-   machine-id   rsyslog.conf

alternatives       gss   magic   rsyslog.d

apache2       hdparm.conf   magic.mime   screenrc

apparmor       hibagent-config.cfg   manpath.config   security

apparmor.d       hibinit-config.cfg   mdadm   selinux

apport       host.conf   mime.types   sensors.d

apt       hostname   mke2fs.conf   sensors3.conf

bandit_pass       hosts   modprobe.d   services

bash.bashrc       hosts.allow   modules   shadow

bash_completion       hosts.deny   modules-load.d   shadow-

bash_completion.d       inetd.conf   motd   shells

bindresvport.blacklist       inetd.d   mtab   skel

binfmt.d       init.d   multipath   sos

byobu       initramfs-tools   multipath.conf   ssh

ca-certificates       inputrc   nanorc   ssl

ca-certificates.conf       iproute2   needrestart   subgid

ca-certificates.conf.dpkg-old  iscsi   netconfig   subgid-

chrony       issue   netplan   subuid

cloud       issue.bandit   network   subuid-

console-setup       issue.bandit.fail   networkd-dispatcher   sudo.conf

cron.d       issue.bandit.localhost   networks   sudo_logsrvd.conf

cron.daily       issue.drifter   newt   sudoers

cron.hourly       issue.drifter.fail   nftables.conf   sudoers.d

cron.monthly       issue.drifter.localhost   nsswitch.conf   supervisor

cron.weekly       issue.formulaone   opt   sysctl.conf

crontab       issue.formulaone.fail   os-release   sysctl.d

cryptsetup-initramfs       issue.formulaone.localhost  overlayroot.conf   sysstat

crypttab       issue.krypton   overlayroot.local.conf  systemd

dbus-1       issue.krypton.fail   pam.conf   terminfo

debconf.conf       issue.krypton.localhost   pam.d   timezone

debian_version       issue.net   passwd   tmpfiles.d

default       kernel   passwd-   ubuntu-advantage

deluser.conf       kernel-img.conf   perl   ucf.conf

depmod.d       krypton_pass   pm   udev

dhcp       landscape   polkit-1   ufw

dpkg       ld.so.cache   pollinate   update-manager

drifter_pass       ld.so.conf   ppp   update-motd.d

e2scrub.conf       ld.so.conf.d   profile   update-notifier

ec2_version       ldap   profile.d   usb_modeswitch.conf

emacs       legal   protocols   usb_modeswitch.d

environment       libaudit.conf   python2.7   vim

ethertypes       libblockdev   python3   vmware-tools

fonts       libnl-3   python3.10   vtrgb

formulaone_pass       lighttpd   rc0.d   watchdog.conf

fstab       locale.alias   rc1.d   wgetrc

fuse.conf       locale.gen   rc2.d   xattr.conf

gai.conf       localtime   rc3.d   xdg

gdb       logcheck   rc4.d   zsh_command_not_found

gitconfig       login.defs   rc5.d

groff       logrotate.conf   rc6.d

$ cd bandit_pass

$ ls

bandit0   bandit12  bandit16  bandit2 bandit23  bandit27  bandit30  bandit4  bandit8

bandit1   bandit13  bandit17  bandit20 bandit24  bandit28  bandit31  bandit5  bandit9

bandit10  bandit14  bandit18  bandit21 bandit25  bandit29  bandit32  bandit6

bandit11  bandit15  bandit19  bandit22 bandit26  bandit3   bandit33  bandit7

$ cat bandit33

odHo63fHiFqcWWJG9rLiLDtPm45KzUKy
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| cd | cambiar a un directorio o subdirectorio|
|- cd / | cambiar a un directorio o subdirectorio concreto|
| ls | lista los archivos|
| - ls -a | muestra todos los archivos|
| - ls -l | muestra los archivos de forma mas detallada|
| cat| me muestra el contenido de un archivo|
## Referencias

sh, man