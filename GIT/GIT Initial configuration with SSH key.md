
[Docs](https://kbroman.org/github_tutorial/pages/first_time.html)

# Set up git with your user name and email.
git config --global user.name "sergiiburtovyi"
git config --global user.email "sergii_burtovyi@goodyear.com"

# (Optional) Enable colored output in the terminal
git config --global color.ui true


# Set up ssh on your computer.

## Look to see if you have files ~/.ssh/id_rsa and ~/.ssh/id_rsa.pub.

## If not, create such public/private keys:
ssh-keygen -t rsa -C "sergii_burtovyi@goodyear.com"

## Copy your public key to clipboard
cat ~/.ssh/id_rsa.pub


# Paste your ssh public key into your github account settings.

# Verify configured SSH access
ssh -T git@github.com
