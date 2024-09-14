# Generate SSH Keys for GitHub

Here you can learn how to generate an SSH key and how to add it to your account

### 1. Generate a New SSH Key Pair

Open your terminal and run:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

Replace `your_email@example.com` with the email address associated with your GitHub account.

When prompted to "Enter file in which to save the key," you can press Enter to use the default path.

You'll then be asked to enter a passphrase. It's recommended to use a secure passphrase for added security.

### 2. Add the SSH Key to the SSH Agent

First, start the SSH agent (if it's not already running):

```bash
eval "$(ssh-agent -s)"
```

Then, add your SSH key to the agent:

```bash
ssh-add ~/.ssh/id_ed25519
```

### 3. Add the SSH Key to GitHub

Display your public key by running:

```bash
cat ~/.ssh/id_ed25519.pub
```

Copy the entire output.

Now, add this key to your GitHub account:

1. Go to your GitHub account settings.
2. Navigate to "SSH and GPG keys."
3. Click "New SSH key."
4. Paste the copied key into the "Key" field.
5. Give it a descriptive title (e.g., "Personal Git SSH").
6. When adding your SSH key to GitHub, select "Authentication Key."
7. Click "Add SSH key" to save.


