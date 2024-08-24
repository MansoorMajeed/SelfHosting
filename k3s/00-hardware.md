# Hardware

You can install k3s on any hardware. Take a look at the official documentation about the requirements [HERE](https://docs.k3s.io/installation/requirements)

Minimum 1 cpu core and 512MB ram. So, you should be able to run k3s even on a several generation old raspberry pi

## Should I use baremetal or virtual machine?

This is a personal choice. Assuming that you have a dedicated machine that you want to use for k3s, you can choose
to install k3s directly on the host machine or install it via a hypervisor like Proxmox. 

Initially, I used k3s on the baremetal and it worked great. But I found that I was wasting resources on that host
because it would be annoying to run other things on the same host.

## My recommendation

If you have a dedicated hardware that you want to use for this purpose, I suggest you install [Proxmox](https://www.proxmox.com/en/) on it
and create virtual machines on it that will be used to install k3s. This is what I do personally. I have a 3 node Proxmox cluster (three old mini PCs with Proxmox, and running 3 Virtual Machines for 3 k3s nodes.) This lets me make use of the rest of the hardware to run other virtual machines, docker etc.

## So what is the requirement for this tutorial?

- At least one VM of 1 CPU core and 1GB of memory to install k3s.
- If you don't have dedicated hardware, you can install VirtualBox or VMWare or Parallels to create a VM on your computer