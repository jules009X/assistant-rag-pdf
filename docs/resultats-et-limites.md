# Résultats observés et limites

## Source des observations

Les éléments ci-dessous proviennent des sorties enregistrées dans `Copie_de_Objectif_IA_Atelier_Code_03_09_2026.ipynb`, fourni par Jules APEDOH. Ils ne sont pas issus d’une nouvelle exécution. Les sorties ont été retirées du notebook nettoyé pour éviter les anciens liens publics, les journaux de téléchargement et les métadonnées de session.

## Comparaison avec et sans contexte

Question : « Combien coûte l’abonnement Premium au club de Marseille ? »

| Mode | Comportement enregistré |
|---|---|
| Sans documents | Le modèle indique ne pas disposer des informations tarifaires spécifiques. |
| Avec les passages retrouvés | Le modèle donne le montant de 42,90 euros par mois et l’application affiche les références des passages retrouvés. |

Cette comparaison illustre l’apport du contexte documentaire. Elle ne démontre pas une amélioration statistique ni un taux de fiabilité. Le montant doit être vérifié dans le document source pour être compté comme une réponse correcte dans un benchmark.

## Observations à prendre en compte

1. **Mélange des villes dans la recherche.** Pour une question sur les vélos à Paris, le premier résultat enregistré est un passage de Lyon, avec un score de 0,55, devant deux passages de Paris à 0,53 et 0,52. Le message de succès imprimé dans l’original ne suffit donc pas à conclure que la recherche est correcte.
2. **Contexte potentiellement incomplet.** Les trois premiers résultats ne couvrent pas nécessairement toutes les informations nécessaires, notamment pour les questions portant sur plusieurs clubs.
3. **Consigne de refus imparfaitement suivie.** Sur la question du cours du Bitcoin, le modèle ne donne pas de cours, mais il n’utilise pas la phrase de refus demandée et fait référence à un « club de boxe ». Cela montre que le prompt ne garantit pas la fidélité au contexte.
4. **Pas de validation automatique des citations.** L’application affiche les titres de tous les passages retrouvés, sans vérifier lesquels étayent effectivement chaque affirmation.
5. **Tests qualitatifs seulement.** Six questions exploratoires et une comparaison avec/sans contexte apparaissent dans les sorties. Il n’existe pas de jeu d’évaluation annoté, de mesure de latence ou de métrique de qualité.
6. **Partage temporaire.** Le notebook original contient un lancement Gradio public réussi. Ce lien est lié à une session et ne constitue pas un service permanent ; il n’est pas réutilisé dans ce dépôt.

## Protocole d’évaluation proposé

À réaliser avant toute affirmation de performance :

- Constituer un jeu de questions couvrant tarifs, horaires, équipements, résiliation, comparaison entre villes et questions hors corpus.
- Associer à chaque question une réponse attendue et les passages justificatifs.
- Mesurer séparément la récupération du passage attendu parmi les trois résultats et la justesse de la réponse générée.
- Examiner les erreurs de ville, les informations inventées et les refus injustifiés.
- Enregistrer les versions logicielles, les modèles, le matériel et les paramètres pour reproduire les essais.

Ce protocole est une proposition d’amélioration et n’a pas été exécuté dans le cadre de la préparation du dépôt.
