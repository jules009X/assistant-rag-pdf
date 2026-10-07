# Origine et préparation du dépôt

## Origine

Notebook fourni : `Copie_de_Objectif_IA_Atelier_Code_03_09_2026.ipynb`.

Le document se présente comme un atelier « Objectif IA » préparé par Machine Learnia. Il propose des cellules à compléter et une correction. Le code de base et les six PDF de la franchise fictive Club Odyssée sont attribués à cet atelier.

Les sorties d’origine attestent de l’extraction des PDF, de l’encodage, de l’inférence et d’un lancement Gradio. Elles ne permettent pas de déterminer seules la part de code rédigée personnellement par le participant.

## Modifications pour la présentation GitHub

- Réorganisation en étapes techniques avec explication de leur rôle.
- Suppression des sorties, identifiants de cellules Colab et métadonnées de session ; génération de nouveaux identifiants de cellules.
- Conservation du pipeline et du corpus de secours de l’atelier.
- Liste explicite des dépendances ; retrait des messages destinés au chat de l’atelier et des indications de trous à compléter.
- Remplacement d’un message affirmant la réussite de la recherche par une invitation à contrôler les résultats.
- Adaptation du titre de l’interface ; passage de `share=True` à `share=False` pour le lancement explicite.
- Documentation des observations, limites et instructions d’exécution.

Cette préparation a été réalisée avec une assistance IA. Elle n’est pas présentée comme une nouvelle réalisation algorithmique de Jules APEDOH.

## Validation

La structure du notebook, la syntaxe Python des cellules, les liens relatifs et l’intégrité de l’archive sont contrôlés lors de la préparation. Le téléchargement des modèles et l’exécution complète sur GPU ne sont pas répétés. Le dépôt ne contient donc pas de nouvelle preuve d’exécution de la version nettoyée.

## Présentation publique

Une page statique de portfolio a été ajoutée dans `site/` avec trois observations interactives, le parcours de Jules et une explication de l’architecture. Les cartes sont des résumés du fichier `resultats-et-limites.md`, pas des transcriptions complètes ni de nouvelles inférences. Aucune réponse supplémentaire ni métrique de performance n’a été inventée. Le notebook n’a pas été modifié pour cette publication.

Le workflow `.github/workflows/pages.yml` publie uniquement `site/` sur GitHub Pages, après contrôle de la syntaxe JavaScript. La page ne charge aucun modèle et ne demande aucune clé API. Pour changer le contenu, modifier les fichiers du site et publier sur `main`.
