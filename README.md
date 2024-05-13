# Dépot des configurations ansible sur le serveur distant 

## Tester la connection avec un ping
`ansible-playbook -i inventory.ini main.yaml -v`
`ansible-vault encrypt_string --name 'ansible_password' '!!Art94721805&'` : Pour chiffrer le mot de passe et copier dans l'inventory le passphrase est toto
ansible-playbook -i Win_Config/config_win/hosts Win_Playbook/win_playbooks/ping.yaml --ask-vault-pass -vvv

    ansible_winrm_scheme: http
    ansible_winrm_transport: ntlm : pour les comptes locaux et du domaine
NTLM est le protocole d'authentification le plus simple à utiliser et est plus sécurisé que Basicl'authentification. S'il est exécuté dans un environnement de domaine, Kerberos doit être utilisé à la place de NTLM.

Kerberos présente plusieurs avantages par rapport à l'utilisation de NTLM :

NTLM est un protocole plus ancien et ne prend pas en charge les protocoles de chiffrement plus récents.

NTLM est plus lent à s'authentifier car il nécessite davantage d'allers-retours vers l'hôte lors de la phase d'authentification.

Contrairement à Kerberos, NTLM n'autorise pas la délégation d'informations d'identification.

Cet exemple montre les variables hôte configurées pour utiliser l'authentification NTLM :

