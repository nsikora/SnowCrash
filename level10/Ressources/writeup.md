token to flag10 = woupa2yuojeeaaed06riuj63c

Check flag.Here is your token : feulo4b72j7edeahuete3no7c

Nous avons commence par regarder le binaire fourni avec strings:

strings level10

puis nous avons trouve la fonction access, a la lecture du man nous nous sommes
rendu compte qu'elle avait une fail de securite. Nous avons trouve "race condition"

lien sur le race condition:

https://samsclass.info/127/proj/E10.htm
http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.210.1202&rep=rep1&type=pdf
https://en.wikipedia.org/wiki/Time-of-check_to_time-of-use

Nous avons donc exploite cette fail.
Nous avons d'abord ouvert une socket grace a open_socket.sh
puis tricks_access.sh qui permet d'intervertir un lien symbolique entre deux fichier
un qui a des droits de lecture et le token qui ne les a pas, en boucle.
Puis nous avons excute exec_command.sh qui permet de lancer le binaire en boucle
afin que la fail reussi.

Resume de la fail:
