# Requirements

Take a look at the official documentation about the requirements [HERE](https://docs.k3s.io/installation/requirements)

## What you should know already

You should have a basic understanding of working with Linux, containers, Kubernetes etc. You don't need to be a master of Kubernetes
or k3s, but you should know what a container is, what a pod is etc. It is not a hard requirement, but I am writing these without
explaining all the fundamentals, but I will be sure to leave references throughout, so you can read more about it as you go.

## Hardware

You can install k3s on practically any hardware. 

Minimum 1 cpu core and 512MB ram. So, you should be able to run k3s even on a several generation old raspberry pi

### Should I use baremetal or virtual machine?

This is a personal choice. Assuming that you have a dedicated machine that you want to use for k3s, you can choose
to install k3s directly on the host machine or install it via a hypervisor like Proxmox. 

Initially, I used k3s on the baremetal and it worked great. But I found that I was wasting resources on that host
because it would be annoying to run other things on the same host.

### My recommendation

If you have a dedicated hardware that you want to use for this purpose, I suggest you install [Proxmox](https://www.proxmox.com/en/) on it
and create virtual machines on it that will be used to install k3s. This is what I do personally. I have a 3 node Proxmox cluster (three old mini PCs with Proxmox, and running 3 Virtual Machines for 3 k3s nodes.) This lets me make use of the rest of the hardware to run other virtual machines, docker etc.

If you don't have dedicated hardware, you can install VirtualBox or VMWare or Parallels to create a VM on your computer. This is totally fine for learning.

### I want to buy new hardware for this

Great. Don't buy Raspberry Pis for it. Buy a used 1L mini PC from eBay or any used hardware marketplace. ServeTheHome has a great artcile and video about what sort of hardware. Check it out [HERE](https://www.servethehome.com/introducing-project-tinyminimicro-home-lab-revolution/)

I personally like the "Lenovo ThinkCentre M720q". You can get one for around $100 or cheaper from ebay.

## Networking

If you have a firewall in your network, you should read [THIS](https://docs.k3s.io/installation/requirements#networking) and make sure
that the firewall rules work with k3s


## Conclusion

- Before you proceed, you should have at least one virtual machine or physical machine with at least 1 CPU core and 1GB of RAM.
- You should install Debian 12 on it (my recommendation). You can install whatever you are comfortable with, if you choose to. But I will be using Debian 12
- These machines will be referred to as "k3s Nodes" going forward



