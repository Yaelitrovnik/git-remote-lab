# GitHub SSH Authentication

1. Generate SSH Key:
   ssh-keygen -t ed25519 -C "your_email@example.com"

2. Add SSH key to SSH agent:
   eval "SSH_AUTH_SOCK=/tmp/ssh-JH5eeR4ZltIK/agent.2800; export SSH_AUTH_SOCK;
SSH_AGENT_PID=2801; export SSH_AGENT_PID;
echo Agent pid 2801;"
   ssh-add ~/.ssh/id_ed25519

3. Copy public key to GitHub:
   cat ~/.ssh/id_ed25519.pub
   # Paste it into GitHub > Settings > SSH and GPG keys

4. Change remote URL to SSH:
   git remote set-url origin git@github.com:Yaelitrovnik/git-remote-lab.git

