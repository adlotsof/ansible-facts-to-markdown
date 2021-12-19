# tim-virtualbox

- 192.168.122.1
- 192.168.0.173
- 172.17.0.1

### Docker 

#### Containers running

| NAME | MOUNTS | COMMAND | PORTS | STATE |
| ---- | -----  | ------- | ----- | ----- |
| ['/nostalgic_euler'] |  03da7f9c1955423f170acc8b7c29991191043302695bcbe7ef67f3db41e7db58,   | /docker-entrypoint.sh nginx -g 'daemon off;' | [{'PrivatePort': 80, 'Type': 'tcp'}] | running |

#### Volumes
| NAME | MOUNT | DRIVER | OPTIONS | 
| ---- | -----  | ------- | ----- | 
| 7812c8f6d8c9a1db4a644e3e75a757cfec75cb0da166aefcc103eaf054f1c9d5 | /var/lib/docker/volumes/7812c8f6d8c9a1db4a644e3e75a757cfec75cb0da166aefcc103eaf054f1c9d5/_data local |  | 
| 03da7f9c1955423f170acc8b7c29991191043302695bcbe7ef67f3db41e7db58 | /var/lib/docker/volumes/03da7f9c1955423f170acc8b7c29991191043302695bcbe7ef67f3db41e7db58/_data local |  | 


#### Images
| LABELS | SIZE | 
| ---- | -----  |
| {'maintainer': 'NGINX Docker Maintainers <docker-maint@nginx.com>'} | 141490839 1638442769 |




### Open Ports

#### TCP

| name | user | port | adress |
| --- | --- | --- | --- |
| dnsmasq | libvirt-dnsmasq | 53 | 192.168.122.1 |
| systemd-resolve | systemd-resolve | 53 | 127.0.0.53%lo |
| cupsd | root | 631 | 127.0.0.1 |
| anydesk | root | 7070 | 0.0.0.0 |
| cupsd | root | 1 | : |


#### UDP

| name | user | port | adress |
| --- | --- | --- | --- |
| dnsmasq | libvirt-dnsmasq | 53 | 192.168.122.1 |
| systemd-resolve | systemd-resolve | 53 | 127.0.0.53%lo |
| dnsmasq | libvirt-dnsmasq | 67 | 0.0.0.0%virbr0 |
| cups-browsed | root | 631 | 0.0.0.0 |
| chrome | tim | 5353 | 224.0.0.251 |
| chrome | tim | 5353 | 224.0.0.251 |
| avahi-daemon | avahi | 5353 | 0.0.0.0 |
| anydesk | root | 50001 | 0.0.0.0 |
| avahi-daemon | avahi | 50443 | 0.0.0.0 |
| skypeforlinux | tim | 33397 | * |
| avahi-daemon | avahi | 5353 | :: |
| avahi-daemon | avahi | 45909 | :: |
| --- | --- | --- | --- | --- |

## Hardware

### Memory

| - | total | free | used |
| ----- | --- | --- | --- | 
| Memory| 39203 | 27930 | 11273 |
| Swap | 979  | 979 | 0 |
| total | 39203 |  |  | 
### CPUs


| Type| Count | Cores | Vcpus |
| --- | --- | --- | --- |
| Intel(R) Core(TM) i7-8565U CPU @ 1.80GHz | 1 | 4 | 8 |


### Mounts


| device | type | mount | total | available |
| --- | --- | --- | --- | --- |
| /dev/mapper/vgubuntu-root | ext4 | / | 500680400896| 288436973568 |
| /dev/loop0 | squashfs | /snap/android-studio/114 | 1011613696| 0 |
| /dev/loop2 | squashfs | /snap/core/11798 | 104333312| 0 |
| /dev/loop1 | squashfs | /snap/android-studio/115 | 1011351552| 0 |
| /dev/loop3 | squashfs | /snap/core18/2246 | 58195968| 0 |
| /dev/loop4 | squashfs | /snap/code/83 | 224264192| 0 |
| /dev/loop6 | squashfs | /snap/core/11993 | 104333312| 0 |
| /dev/loop5 | squashfs | /snap/core18/2253 | 58195968| 0 |
| /dev/loop7 | squashfs | /snap/core20/1242 | 64880640| 0 |
| /dev/loop8 | squashfs | /snap/gnome-3-28-1804/161 | 172883968| 0 |
| /dev/loop9 | squashfs | /snap/bare/5 | 131072| 0 |
| /dev/loop10 | squashfs | /snap/gnome-3-34-1804/77 | 229638144| 0 |
| /dev/loop11 | squashfs | /snap/keepassxc/1522 | 163708928| 0 |
| /dev/loop12 | squashfs | /snap/gtk-common-themes/1514 | 68026368| 0 |
| /dev/loop13 | squashfs | /snap/snap-store/558 | 56885248| 0 |
| /dev/loop14 | squashfs | /snap/gnome-3-34-1804/72 | 229638144| 0 |
| /dev/loop15 | squashfs | /snap/snapd/14066 | 44302336| 0 |
| /dev/loop16 | squashfs | /snap/spotify/53 | 170000384| 0 |
| /dev/loop17 | squashfs | /snap/gnome-3-38-2004/87 | 260046848| 0 |
| /dev/loop19 | squashfs | /snap/gtk-common-themes/1519 | 68419584| 0 |
| /dev/loop20 | squashfs | /snap/signal-desktop/378 | 178388992| 0 |
| /dev/loop21 | squashfs | /snap/skype/194 | 141033472| 0 |
| /dev/loop22 | squashfs | /snap/snap-store/547 | 53477376| 0 |
| /dev/loop23 | squashfs | /snap/skype/197 | 141033472| 0 |
| /dev/loop24 | squashfs | /snap/snapd/14295 | 45481984| 0 |
| /dev/nvme0n1p5 | ext4 | /boot | 737656832| 320061440 |
| /dev/nvme0n1p1 | vfat | /boot/efi | 535805952| 535801856 |
| /dev/loop25 | squashfs | /snap/core20/1270 | 65011712| 0 |
| /dev/loop26 | squashfs | /snap/spotify/56 | 175505408| 0 |
| /dev/fuse | fuse | /run/user/1000/doc | 0| 0 |
| /dev/loop27 | squashfs | /snap/code/85 | 228065280| 0 |


### Interfaces

- virbr0-nic
- veth5867623
- virbr0
- wlp0s20f3
- docker0
- enp0s31f6
- lo



## Software

### OS
|  -  |  -  |
| --- | --- |
| id | Ubuntu |
| description | Ubuntu 20.04.3 LTS focal |
| release | 20.04 |
| kernel | 5.11.0-41-generic |
### Upgradable apt

--------
changed
stdout
stderr
rc
cmd
start
end
delta
msg
stdout_lines
stderr_lines
failed
--------

ansible localhost -b -K -a "apt list --upgradable"

### Git Status

#### /home/tim/Desktop/terrafree-base/
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	core-workflow/
	github/
	oracle/

nothing added to commit but untracked files present (use "git add" to track)



