# Metricbeat

Metricbeat est un expéditeur léger que vous pouvez installer sur vos serveurs pour collecter périodiquement des métriques du
système d'exploitation et à partir des services exécutés sur le serveur. Metricbeat prend les métriques et les statistiques qu'il collecte
et les expédie vers la sortie que vous spécifiez, comme Elasticsearch ou Logstash.

## Utilisation

Pour inclure Metricbeat dans la pile, exécutez Docker Compose à partir de la racine du référentiel avec une ligne de commande supplémentaire
argument référençant le fichier `metricbeat-compose.yml`:

`` `console
$ docker-compose -f extensions docker-compose.yml -f / metricbeat / metricbeat-compose.yml up
''

## Configuration de Metricbeat

La configuration de Metricbeat est stockée dans [`config / metricbeat.yml`] (./ config / metricbeat.yml). Vous pouvez modifier ce fichier
à l'aide de la [Référence de configuration] [metricbeat-config].

Toute modification de la configuration de Metricbeat nécessite un redémarrage du conteneur Metricbeat:

`` `console
$ docker-compose -f extensions docker-compose.yml -f / metricbeat / metricbeat-compose.yml redémarrer metricbeat
''

Veuillez consulter la page de documentation suivante pour plus de détails sur la configuration de Metricbeat dans un
Conteneur Docker: [Exécutez Metricbeat sur Docker] [metricbeat-docker].

## Voir également

[Documentation Metricbeat] [metricbeat-doc]

[metricbeat-config]: https://www.elastic.co/guide/en/beats/metricbeat/current/metricbeat-reference-yml.html
[metricbeat-docker]: https://www.elastic.co/guide/en/beats/metricbeat/current/running-on-docker.html
[metricbeat-doc]: https://www.elastic.co/guide/en/beats/metricbeat/current/index.html
