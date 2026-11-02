# What is Azure VM or Virtual Machine

Imagine I need a computer, but I don't want to buy one. So I rent a computer that sits in Microsoft’s giant building, and I control it from my own laptop over the internet. That rented computer is an Azure VM. It behaves like a real computer: it has a processor (CPU), memory (RAM), storage (disk), and an operating system (Windows or Linux). I can install software on it, run a website on it, and switch it off when I am done. The only difference is that I never touch it physically.

## Where does the VM actually stays?

This connects to the azure architecture that we have learned.

```bash
Region → Datacenter → Rack → Physical server → Your VM
```

- **Region**: a city or area where Microsoft has datacenters, like Central India or South India. We choose this when we create the VM.
- **Datacenter**: a huge, secure building full of servers, with its own power, cooling, and internet.
- **Physical Server**: a powerful real machine. Software called a hypervisor splits it into many small virtual computers.
- **Your VM**: one of those slices, completely separated from the other people’s VMs on the same machine.
