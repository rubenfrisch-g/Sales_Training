# Sales Call Trainer

Page web d'entraînement aux appels commerciaux : le sale s'identifie, puis simule un appel vocal avec un prospect IA directement dans le navigateur (pas de vrai appel téléphonique), via [Vapi](https://vapi.ai).

## Scénarios

Les 6 personas (basés sur de vrais appels Aircall de Developers Institute) sont documentés dans [vapi_scenarios.md](vapi_scenarios.md) — First Message + System Prompt prêts à coller dans un assistant Vapi. Les 6 assistants sont créés et branchés dans `index.html`.

[product_knowledge.md](product_knowledge.md) contient les infos produit vérifiées (prix, financements, planning, banque d'objections) tirées des brochures officielles et de la FAQ interne — sert de référence pour garder les personas réalistes et à jour.

`VAPI_PUBLIC_KEY` (clé publique, Dashboard > API Keys) est déjà renseignée dans `index.html`.

Vérifier aussi la méthode `vapi.start(assistantId, options)` dans la doc actuelle du SDK web Vapi (l'API peut évoluer).

## Déploiement (GitHub Pages)

1. Créer un dépôt GitHub (public ou privé — Pages fonctionne sur les deux avec un compte GitHub Pro pour le privé).
2. Pousser ce dossier.
3. Dans les Settings du dépôt > Pages, choisir la branche `main` et le dossier `/ (root)`.
4. La page sera disponible à `https://<ton-user>.github.io/<nom-du-repo>/`.

## Feedback

Pas de scoring automatique côté site : à la fin de l'appel, un bouton "Download transcript" permet de télécharger le transcript complet en PDF pour l'analyser ailleurs (manuellement, ou avec un autre outil).
