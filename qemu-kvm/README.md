# qemu-kvm

## Installation

It is possible to install only QEMU and KVM for a very minimal setup, but most users will also want `libvirt` for convenient configuration and management of the virtual machines (`libvirt-daemon-system` - libvirt, `virt-manager` - a GUI for libvirt). Typically a user should install: 
```shell
$ sudo apt install qemu-system libvirt-daemon-system
```
When installing on a server, you can add the --no-install-recommends apt option, to prevent the installation of extraneous graphical packages:
```shell
$ sudo apt install --no-install-recommends qemu-system libvirt-clients libvirt-daemon-system
```
The libvirtd daemon (in `libvirt-daemon` on most architectures, and in `libvirt-bin` on others) will start automatically at boot time and load the appropriate KVM modules, kvm-amd or kvm-intel, which are shipped with the Linux kernel Debian package. If you intend to create Virtual Machines (VMs) from the command-line, install `virtinst`.

In order to manage virtual machines as a regular user, that user needs to be added to the libvirt group: 
```shell
$ adduser <youruser> libvirt
```
You should then be able to list your domains, that is virtual machines managed by libvirt:
```shell
$ virsh list --all
```

## Dynamic screen sizing

1. Start `virt-manager` and go to `View -> Edit -> Preferences -> Console`. Activate `Resize guest with window: On`;
2. In the VM machine go to `View -> Scale Display -> Auto resize VM with window`;
3. Install the following packages on the guest virtual machine `qemu-guest-agent`, `xserver-xorg-video-qxl`, `spice-vdagent`;
4. Enable `spice-vdagent` service in systemctl with command `systemctl enable spice-vdagent`;
5. Run `spice-vdagent` service in systemctl with command `systemctl start spice-vdagent`.

## Shared clipboard

1. Install `spice-vdagent` package on the guest virtual machine;
4. Enable `spice-vdagent` service in systemctl with command `systemctl enable spice-vdagent`;
5. Run `spice-vdagent` service in systemctl with command `systemctl start spice-vdagent`.


