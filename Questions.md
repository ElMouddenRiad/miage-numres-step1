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
La commande : ls -lh api-quarkus/target/quarkus-app/quarkus-run.jar
retourne :
-rw-rw-rw- 1 vscode vscode 662 Feb 16 13:57 api-quarkus/target/quarkus-app/quarkus-run.jar

donc la taille du fichier quarkus-run.jar est de 662KB soit 0.662MB
# Q8 : Quelle est la valeur de la RSS utilisée par l'api quarkus en mode JVM (Préciser l'unité)?
Réponse:
@ElMouddenRiad ➜ /workspaces/miage-numres-step1 (main) $ ps -e -o pid,rss,args | grep quarkus-run
  43417 102232 java -jar api-quarkus/target/quarkus-app/quarkus-run.jar
  43669  2304 grep quarkus-run

  donc la taille est 102232KB soit 102.232MB

# Q9 : Quel est le temps de démarrage l'api Quarkus en mode JVM ?
Réponse:
sur le terminal du lancement on  a :
2026-02-16 13:58:14,176 INFO  [io.quarkus] (main) api-quarkus 1.0.0-SNAPSHOT on JVM (powered by Quarkus 3.30.8) started in 1.034s. Listening on: http://0.0.0.0:8080

donc le temps de démarrage de l'api Quarkus est de 1.034s
# Q10 : Quelle est la valeur de la RSS utilisée par l'api quarkus en mode natif (Préciser l'unité)?
Réponse:
Résultat : 
  52386 41600 ./api-quarkus/target/api-quarkus-1.0.0-SNAPSHOT-runner
  52752  2304 grep runner

  41600KB est la RSS utilisée par quarkus en mode natif soit 41.6MB
# Q11 : Quel est le temps de démarrage l'api Quarkus en mode natif ?
Réponse:
2026-02-16 14:10:57,406 INFO  [io.quarkus] (main) api-quarkus 1.0.0-SNAPSHOT native (powered by Quarkus 3.30.8) started in 0.041s. Listening on: http://0.0.0.0:8080
2026-02-16 14:10:57,406 INFO  [io.quarkus] (main) Profile prod activated. 
2026-02-16 14:10:57,406 INFO  [io.quarkus] (main) Installed features: [cdi, rest, smallrye-context-propagation, vertx]

le temps de démarrage de quarkus est de 0.041s