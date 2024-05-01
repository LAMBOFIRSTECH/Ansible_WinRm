# Dépot des configurations ansible sur le serveur distant 

## Tester la connection avec un ping
`ansible-playbook -i inventory.ini main.yaml -v`
`ansible-vault encrypt_string --name 'ansible_password' '!!Art94721805&'` : Pour chiffrer le mot de passe et copier dans l'inventory le passphrase est toto
ansible-playbook -i Win_Config/config_win/hosts Win_Playbook/win_playbooks/ping.yaml --ask-vault-pass -vvv

