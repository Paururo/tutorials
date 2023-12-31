# Configure GitHub in a server

**Install Git:** First, ensure that Git is installed on your Ubuntu server. You can do this by running the following commands in the terminal:

```bash
sudo apt-get update
sudo apt-get install git
```

**Configure Git**: Once Git is installed, you'll need to configure it. Set up your Git username and email address with these commands:

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

*This information will be used in your commits.*

**Generate an SSH Key**: GitHub uses SSH to securely communicate with your server. Generate a new SSH key by running:

```bash
ssh-keygen -t rsa -b 4096 -C "youremail@example.com"
```

*Follow the prompts to create the key. By default, it will be saved in `~/.ssh/id_rsa`.*

**Add the SSH Key to Your GitHub Account**: You need to add your SSH public key to your GitHub account. You can get your SSH public key with the command:

```bash
cat ~/.ssh/id_rsa.pub
```

*Then, go to GitHub, navigate to "Settings" > "SSH and GPG keys" > "New SSH key", and add your public key.*


**Test the SSH Connection**: To make sure everything is set up correctly, test your SSH connection to GitHub with:

```bash
ssh -T git@github.com
```

*If you see a message saying you've successfully authenticated, everything is set up!*

**Clone a Repository**: You can now clone repositories from GitHub to your Ubuntu server. Use:

```bash
git clone git@github.com:username/repository.git
```

*Where `username/repository` is the path to the repository you want to clone.*

**Working with Git**: You can now start working with Git on your server. You can make commits, push, pull, etc., using the standard Git commands.
