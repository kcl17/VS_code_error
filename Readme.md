## Having issues in openeing vs code : 

It seems like the package name code is not found in your repository.
This can happen if the Visual Studio Code repository is not added to your system. Let's add the repository and try updating and installing VS Code again.

# 1. Add the Microsoft GPG key:

```
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -o root -g root -m 644 packages.microsoft.gpg /etc/apt/trusted.gpg.d/
rm -f packages.microsoft.gpg

```
# 2. Add the Visual Studio Code repository:

```
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'

```

# 3. Update the package list and install VS Code:

```
sudo apt update
sudo apt install code

```

