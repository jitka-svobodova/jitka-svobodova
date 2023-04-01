# SSH access
[original](https://carnifis.medium.com/how-to-configure-ssh-key-on-windows-for-github-3d5ef6f244a6)

0. Open a new PowerShell window.
1. Create a new ssh key pair locally running the following command:
```
ssh-keygen -t rsa -b 4096 -C "example@email.com"
```
2. We need to add the private key to the local agent, so you must run:
```
ssh-add .\.ssh\id_rsa
```
3. Copy your public key into the clipboard with the following command:
```
cat ~/.ssh/id_rsa.pub | clip
```
4. Go into github and create a new SSH entry copiying the content you have on the clipboard.
```
Settings > SSH and GPG keys > New SSH key
```
