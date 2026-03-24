# PE-QEMU-KVM-Install

# Converting Our System Into A Hypevisor 

- Turning our system into a hypervior will allow me to create an entire production env without purchasing hardware

# Command Issued

```
dnf group install "Virtualization Host"

dnf install virt_viewer virt-install cockpit-machines
```
```
usermod -aG kvm,libvirt cortizaldana
```
```
for i in qemu network nodedev nwfilter secret storage interface; do systemctl start virt${i}d{,-ro,-admin}.socket; done
```
```
virsh uri

vim .bashrc

export LIBVIRT_DEFAULT_URI="qemu:///system"

:wq

source .bashrc
```
```
virt-host-validate
```

# Video
