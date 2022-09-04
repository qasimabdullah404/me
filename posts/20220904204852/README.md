# Vagrant init

![It works on my machine ](Images/say_it.jpeg)

Minimal steps to get vagrant box setup and ready:

- Verify vagrant is installed i.e. `vagrant --version`
- Verify VirtualBox is installed i.e. `vboxmanage --version`
- `cd` into a directory e.g. `cd ~/Documents/lab` assuming **_lab_** directory exists
- Lets make a directory for the Ubuntu Jammy i.e. `mkdir -p vm/ubuntu/jammy`

These directories are obviously not required, a single **_lab_** directory was enough in the first place but little housekeeping doesn't hurt, eh? Now, onto the actual task at hand:

> Vagrant box initialization with ubuntu jammy as base image

Running following commands would make a basic jammy box up and running:

```bash
vagrant init ubuntu/jammy64
vagrant up
vagrant ssh
```

1. `vagrant init ubuntu/jammy64`: This creates a **Vagrantfile** with the config required. This is the main file which can be altered to setup RAM, networks etc
2. `vagrant up`: This creates the VM as per the configurations in **Vagrantfile**
3. `vagrant ssh`: SSH'ing into the created VM. You will be inside the vagrant box you had just setup isolated from your machine / laptop / PC.
