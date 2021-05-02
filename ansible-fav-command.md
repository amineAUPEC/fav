%title: Kubernetes 
%author: AA
%sources:




# HIGH TITLE
- SUBTITLE
- SUBTITLE2

<br>

* 1. intro
		* 
		* 
		* 

* 2. run
		* 
		* 

* 3. test


----------------------------------------------------------------------------------------------
# 1. Intro :

Pour cela, vous pourriez vous connecter en SSH sur chaque serveur, l'un après l'autre, 
et exécuter ladite commande … mais cette méthode est un peu rébarbative et source 
d'erreurs (imaginez devoir réaliser cette opération sur 100 serveurs identiques) !


<br>

Si vous devez administrer un grand nombre de serveurs et d'équipements réseau, 
l'utilisation d'un gestionnaire de configuration vous simplifiera la tâche. Dans cette
partie, vous allez découvrir le gestionnaire Ansible.
Ansible se base sur SSH pour configurer les équipements2. Il requiert simplement :
• L'activation de SSH avec une authentification par clé publique
• L'installation de Python sur les serveurs à administrer (S'il ya usage de template || de fichiers jinja j2)
… et c'est précisément ce que vous venez de configurer !
Sur le PC d'administration, installez simplement le paquetage ansible.
Ansible permet de définir un playbook, : il s'agit d'un fichier qui décrit précisément 
l'état dans lequel vos serveurs doivent se trouver. Le rôle du gestionnaire est de 
réaliser toutes les tâches nécessaires pour amener les serveurs dans cet état, et les y 
maintenir.


Soit le fichier nginx.conf.j2 (l’extension j2 indique qu’il s’agit d’un fichier  jinja2, le format utilisé pour les templates ansible) :

```

```

```

```

<br>

* bold

-------------------------------------------------------------------
# 2. Variables internes

- The *inventory_hostname* variable is equivalent to hostname
"{{ inventory_hostname }}"


- The *ansible_user_id* var is related to **whoami** command so here is equivalent too root || ansible || clientuser
{{ansible_user_id}}



slide.md | less
slide.md | more

%sources :
https://devhints.io/ansible-modules#:~:text=%20Ansible%20modules%20cheatsheet%20%201%20%20Format.,%204%20%20Local%20actions.%20%20More%20