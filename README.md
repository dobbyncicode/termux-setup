# About this repo
I hate long setups. Will update this on later date (or maybe not)

Nothing fancy for now. This is just for me to get Termux rolling. 

# Dependencies
- nala
- eza
- git
- wget
- zip
- unzip
- neovim
- fd
- tealdeer
- fastfetch 
- termux-api (the APK, and the apt package)

# Installation / Setup 

### 1.) Update packages
```bash
apt update -y && apt upgrade -y
```

### 2.) Install dependencies
```bash 
apt install nala eza git wget zip unzip neovim fd tealdeer fastfetch termux-api
```
### 3.) Give storage permission to termux 
```bash 
termux-setup-storage
```
### 4.1) Generate SSH key (optional)
```bash 
rm -rf ~/.ssh 

ssh-keygen -t ed25519 -C "email@email.email"

cat ~/.ssh/id_ed25519.pub
```

### 4.2.) Add SSH key to GitHub
- Copy the `cat ~/.ssh/id_ed25519.pub` command output from step 4.1 if applicable
- Open your web browser
- Click Profile icon > Settings > SSH and GPG Keys
- Click "New SSH"
- Title: Anything
- Paste the public SSH key 

### 4.3.) Test
- Back to Termux, type `ssh -T git@github.com`
- Type `yes` then hit 'Enter'

### 5.) Clone the repo, and run the script
```bash 
git clone git@github.com:dobbyncicode/termux-setup.git

chmod +x ~/termux-setup/scripts/setup

~/termux-setup/scripts/setup
```

