# Stack site web institution
Déploie une stack :
- 2x LoadBalancer qui écoute sur une VIP
- (Scalable) Web workers : apache2+PHP Mod+SMB Mount
> Le serveur SMB est managé en externe car basé sur Win 2019 (WSFC role sur VIP) 

## Setup 
1- Copier le `vars_example.yml` dans `vars.yml`
````bash
cp vars_example.yml vars.yml
````
2 - Remplir le fichier vars.yml avec les valeurs souhaité
3 - Executer le playbook !
````bash
ansible-playbook --inventory host.ini --ask-become-pass infrastructure.yml
````
:)
