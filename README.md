# Generate SSH Keys for GitHub

A Step-by-step tutorial to generate SSH keys and add them to your GitHub account for secure authentication.

## Table of Contents
- [Generate a New SSH Key Pair](#generate-a-new-ssh-key-pair)
- [Add the SSH Key to the SSH Agent](#add-the-ssh-key-to-the-ssh-agent)
- [Add the SSH Key to GitHub](#add-the-ssh-key-to-github)


### Generate a New SSH Key Pair

1. Open your terminal and run:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

Replace `your_email@example.com` with the email address associated with your GitHub account.

2. When prompted to "Enter file in which to save the key," you can press Enter to use the default path.

3. You'll then be asked to enter a passphrase. It's recommended to use a secure passphrase for added security.

### Add the SSH Key to the SSH Agent

1. start the SSH agent (if not already running):

```bash
eval "$(ssh-agent -s)"
```

2. Add your SSH key to the agent:

```bash
ssh-add ~/.ssh/id_ed25519
```

### Add the SSH Key to GitHub

1. Display your public key by running:

```bash
cat ~/.ssh/id_ed25519.pub
```

2. Copy the entire output.

3. Go to your GitHub account:
   - Navigate to Settings → SSH and GPG keys → New SSH key.
   - Paste the copied key into the "Key" field.
   - Give it a descriptive title (e.g., "Personal Git SSH").
   - Select "Authentication Key" when adding your SSH key to GitHub.
   - Click "Add SSH key" to save.


