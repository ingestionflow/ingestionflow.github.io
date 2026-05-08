# Ingestionflow.com web

```bash
# Generate your ssh keys specific to your login account
ssh-keygen -t ed25519 -C "admin@ingestionflow.com"
## choose ~/.ssh/id_ed25519_admin_ingestionflow

# Copy the ssh public key and add to your github.com profile ssh keys https://github.com/settings/keys
cat ~/.ssh/id_ed25519_admin_ingestionflow.pub


# Clone the repo

git -c core.sshCommand="ssh -i ~/.ssh/id_ed25519_admin_ingestionflow" clone git@github.com:ingestionflow/ingestionflow.github.io.git
cd ingestionflow.github.io

# set default ssh private key to use for the cloned repo
git config core.sshCommand "ssh -i ~/.ssh/id_ed25519_admin_ingestionflow"
git config user.name "admin@ingestionflow.com"
git config user.email "admin@ingestionflow.com"

# validate the git config
git config --list --local
```
