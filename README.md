<div align="center">

# DPO News

**Veille juridique automatisée pour les DPO : un dashboard et des notifications Telegram**

![Python](https://img.shields.io/badge/Python-3.11+-1D4ED8?style=flat-square&logo=python&logoColor=white)
![Telegram](https://img.shields.io/badge/Telegram-Bot-26A5E4?style=flat-square&logo=telegram&logoColor=white)
![RSS](https://img.shields.io/badge/RSS-feedparser-F26522?style=flat-square&logo=rss&logoColor=white)
![IA](https://img.shields.io/badge/IA-locale%20(Ollama)-1E3A5F?style=flat-square)
![Dashboard](https://img.shields.io/badge/Dashboard-web-1E3A5F?style=flat-square)
![Statut](https://img.shields.io/badge/Statut-En%20d%C3%A9veloppement-4A6FA5?style=flat-square)

[Présentation](#présentation) ·
[Fonctionnement](#fonctionnement) ·
[Dashboard](#dashboard) ·
[Notifications Telegram](#notifications-telegram) ·
[Feuille de route](#feuille-de-route)

</div>

---

## Présentation

**DPO News** rassemble en un seul endroit l'actualité utile aux délégués à la protection des données : RGPD, décisions de la CNIL et du CEPD, cybersécurité, régulation de l'IA (AI Act).

L'outil :

- **collecte** les articles depuis des flux RSS de sources juridiques ;
- **filtre** les actualités importantes ;
- **résume** chaque article en une brève de 2 à 4 phrases (*TL;DR*), grâce à une IA locale ;
- **diffuse** les brèves sur un **dashboard** et par **notification Telegram**.

---

## Fonctionnement

```mermaid
flowchart LR
    A[Flux RSS juridiques] --> B[Collecte]
    B --> C[Filtrage]
    C --> D["Résumé TL;DR<br>IA locale"]
    D --> E[(Base d'articles)]
    E --> F[Dashboard]
    E --> G[Bot Telegram]
```

| Étape | Rôle |
|---|---|
| Collecte | Lecture des flux RSS par rubrique (titre, lien, chapô, date) |
| Filtrage | Suppression des doublons, sélection des sujets pertinents |
| Résumé | Brève en style *flash news*, rédigée **uniquement** à partir du texte de l'article : aucune décision, date ou référence inventée |
| Diffusion | Publication sur le dashboard et envoi d'une notification Telegram |

Les résumés sont générés par un **modèle de langage local** (Ollama) : aucun article n'est envoyé à une API externe.

---

## Dashboard

Une interface web pour consulter la veille :

- fil des dernières brèves, avec la source et le lien vers l'article complet ;
- filtres par thème (RGPD, sanctions, cybersécurité, IA) et par date ;
- recherche par mot-clé.

---

## Notifications Telegram

Le bot envoie chaque nouvelle brève sur un canal Telegram :

> **📰 Titre de l'article**
> Résumé en 2 à 4 phrases.
> 🔗 Lien vers la source

---

## Feuille de route

- [x] Collecte des articles depuis les flux RSS
- [x] Résumé des articles par une IA locale
- [ ] Filtrage des actualités importantes et suppression des doublons
- [ ] Stockage des articles et des résumés
- [ ] Envoi des brèves sur Telegram
- [ ] Dashboard : fil d'actualité, filtres et recherche
- [ ] Exécution planifiée (collecte automatique à intervalle régulier)

---

## Avertissement

Les résumés sont générés automatiquement et peuvent contenir des imprécisions. Ils ne constituent **pas un conseil juridique** : reportez-vous toujours à l'article source.
