Check flag.Here is your token : g1qKMiRpXf53AWhDaU7FEkczr

Nous avons commence par analyse le script perl, nous avons remarque qu'il pouvait
etre appelle par curl ou par le navigateur.

Nous avons remarque que au debut du script les argument passes en parametres sont 
traite notamment mit en uppercase.

Nous avons donc creer un fichier /tmp/script qui contient:

`getflag > /tmp/flag`

Nous lui avons accorde les droits +x a l'aide de chmod pour qu'il puisse etre
execute.

Ensuite nous avons passer l'url suivant le navigateur:

http://<ip>:4646/?x=`/*/SCRIPT`

pour que le script perl s'execute
