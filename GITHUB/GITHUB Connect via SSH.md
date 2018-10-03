# GITHUB CONNECT VIA SSH

[Docs](https://help.github.com/articles/connecting-to-github-with-ssh/)


**Checking for existing SSH keys**

```
ls -al ~/.ssh
```

By default, the filenames of the public keys are one of the following:

  - id_dsa.pub
  - id_ecdsa.pub
  - id_ed25519.pub
  - id_rsa.pub

If you don't have an existing public and private key pair, or don't wish to use any that are available to connect to GitHub, then [generate a new SSH key](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

If you see an existing public and private key pair listed (for example id_rsa.pub and id_rsa) that you would like to use to connect to GitHub, you can [add your SSH key to the ssh-agent](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#adding-your-ssh-key-to-the-ssh-agent).



**Generate a new SSH key**

Paste the text below, substituting in your GitHub email address.
```
ssh-keygen -t rsa -b 4096 -C "propalparolnapervom@gmail.com"
```


**Adding your SSH key to the ssh-agent**


1. Start the ssh-agent in the background.
```
eval "$(ssh-agent -s)"
```


2. If you're using `macOS Sierra 10.12.2` or later, you will need to modify your `~/.ssh/config` file to automatically load keys into the ssh-agent and store passphrases in your keychain.
```
Host *
 AddKeysToAgent yes
 UseKeychain yes
 IdentityFile ~/.ssh/id_rsa
```
 
 
3. Add your SSH private key to the ssh-agent and store your passphrase in the keychain. If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_rsa in the command with the name of your private key file.
```
ssh-add -K ~/.ssh/id_rsa
```

> Note: The `-K` option is Apple's standard version of ssh-add, which stores the passphrase in your keychain for you when you add an ssh key to the ssh-agent.


4. [Add the SSH key to your GitHub account](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)

4.1. Copy the SSH key to your clipboard.

If your SSH key file has a different name than the example code, modify the filename to match your current setup. When copying your key, don't add any newlines or whitespace.
```
  # Copies the contents of the id_rsa.pub file to your clipboard
  
pbcopy < ~/.ssh/id_rsa.pub
```

> Tip: If `pbcopy` isn't working, you can locate the hidden `.ssh` folder, open the file in your favorite text editor, and copy it to your clipboard.


4.2. In the upper-right corner of any page, click your profile photo, then click Settings.












