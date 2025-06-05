# Monitoring avec Prometheus et Grafana

Cette configuration permet de suivre l'utilisation CPU et mémoire de votre machine grâce à **Prometheus**, **Grafana** et **Node Exporter**.

## Prérequis
- Avoir Docker et Docker Compose installés sur votre système.

## Démarrage rapide

```bash
docker-compose up -d
```

## Accès aux interfaces
- **Prometheus** : [http://localhost:9090](http://localhost:9090)
- **Grafana** : [http://localhost:3000](http://localhost:3000)
  - utilisateur : `admin`
  - mot de passe : `admin`

## Importer le tableau de bord Grafana
1. Ouvrir Grafana puis aller dans **Dashboards → Import**.
2. Sélectionner le fichier `grafana-dashboard.json` présent dans ce dépôt.
3. Valider pour afficher les graphiques.

Vous devriez voir l'utilisation du CPU et de la mémoire en temps réel.

## Fichiers importants
- `docker-compose.yml` : lance Prometheus, Grafana et Node Exporter.
- `prometheus.yml` : configuration des cibles à surveiller.
- `grafana-dashboard.json` : exemple de tableau de bord.
