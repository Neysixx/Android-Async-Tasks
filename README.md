Un thread est un chemin d'exécution indépendant dans un programme en cours d'exécution. Lorsqu'un
programme Android est lancé, le système crée un thread principal, également appelé thread UI. Ce thread
UI est utilisé par votre application pour interagir avec les composants de la boîte à outils de l'interface
utilisateur Android (Android UI toolkit).
Parfois, une application doit effectuer des tâches gourmandes en ressources telles que le
téléchargement de fichiers, l'exécution de requêtes sur une base de données, la lecture de médias ou le
calcul d'analyses complexes. Ce type de travail intensif peut bloquer le thread UI (interface utilisateur) ce
qui empêche l'application de répondre aux entrées de l'utilisateur ou de dessiner à l'écran. Les utilisateurs
peuvent alors être frustrés et désinstaller votre application.
Pour assurer le bon fonctionnement de l'expérience utilisateur (UX), le Framework Android fournit une
classe d'assistance appelée AsyncTask, qui permet d'exécuter des tâches en dehors du thread UI. En
utilisant AsyncTask pour déplacer le traitement intensif sur un thread séparé, le thread UI reste réactif.
Étant donné que le thread séparé n'est pas synchronisé avec le thread appelant, il est appelé thread
asynchrone. Un AsyncTask contient également un rappel (callback) qui vous permet d'afficher les résultats
du calcul dans le thread UI (interface utilisateur).
Dans cet exercice pratique, vous apprendrez comment ajouter une tâche en arrière-plan à votre
application Android en utilisant un AsyncTask.
