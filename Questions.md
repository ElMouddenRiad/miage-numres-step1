# Q1 : Quels sont  les avantages de Gitpod ?
Réponse:
-Le projet est préparé automatiquement au démarrage
-Toutes les dépendances sont installées dans un environnement cloud
-Les workspaces sont séparés ce qui permet de travailler en équipe
# Q2 : Quels sont les défauts de Gitpod ?
Réponse:
-Besoin d'unne connexion internet
-Moins de controle sur les dépendances qu'en local
-Offre est plus tard payante et les ressources peuvent etre limitées

# Q3 : Quelle est la taille du fichier jar `api-springboot-0.0.1-SNAPSHOT.jar` ?
Réponse:
 La commande pour caculer la taille du fichier : ls -lh api-springboot/target/api-springboot-0.0.1-SNAPSHOT.jar
 -rw-rw-rw- 1 vscode vscode 20M Feb 16 13:21 api-springboot/target/api-springboot-0.0.1-SNAPSHOT.jar 

 On déduit que la taille du fichier est de 20M
# Q4 : Qu'est ce que  la RSS ?
Réponse:
Le RSS (Resident Set Size) est la mémoire occupée en RAM, il inclut aussi la mémoire partagée entre les Libraries
# Q5 : Quelle est la valeur de la RSS utilisée par l'api SpringBoot (Préciser l'unité)?
Réponse:
La commande : ps -e -o pid,rss,args | grep api-springboot
Retourne : 17596 181000 java -jar api-springboot/target/api-springboot-0.0.1-SNAPSHOT.jar
  18100  2304 grep api-springboot

  La taille est donc 181000KB environ 176MB

# Q6 : Quel est le temps de démarrage l'api SpringBoot ?
Réponse:
Sur le terminal après avoir lancé l'api, je remarque :
2026-02-16T13:21:57.403Z  INFO 17596 --- [api-springboot] [           main] org.aepsilon.ApiSpringbootApplication    : Started ApiSpringbootApplication in 3.248 seconds (process running for 3.915)

Donc le temps de démarrage est de 3.248 seconds
# Q7 : Quelle est la taille du fichier jar `quarkus-run.jar` ?
Réponse:

# Q8 : Quelle est la valeur de la RSS utilisée par l'api quarkus en mode JVM (Préciser l'unité)?
Réponse:

# Q9 : Quel est le temps de démarrage l'api Quarkus en mode JVM ?
Réponse:

# Q10 : Quelle est la valeur de la RSS utilisée par l'api quarkus en mode natif (Préciser l'unité)?
Réponse:

# Q11 : Quel est le temps de démarrage l'api Quarkus en mode natif ?
Réponse: