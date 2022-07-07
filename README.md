Create Directory for save configuration and running ansible-playbook
# group_vars
Create Directory group_vars, add file :
-  managed1-host-(username).yml
-  managed2-host-(username).yml
# inventory
Creat inventory file for declare managed host
# ansible-vault
- Create secret file for store password user (secret.yml)
- Encrypt files "ansible-vault encrypt secret.yml"
# run playbook
- Ask vault pass "ansible-playbook --syntax-check --ask-vault-pass quiz2-tasks.yml"
- Store encrypted pass in vault-pass file "echo '(password)' > vault-pass
- Give vault-pass permission 600
- Run playbook with vault-pass "ansible-playbook --vault-password-file=vault-pass quiz2-tasks.yml"

<br>
<br>
  
  ref : Adinusa course "Automation with Ansible" : lab 5.2 & quiz2
