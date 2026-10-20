[entretien-telegestion.json](https://github.com/user-attachments/files/33710041/entretien-telegestion.json)
[entretien.html](https://github.com/user-attachments/files/33710065/entretien.html)[LISEZMOI-entretien.md](https://github.com/user-attachments/files/33710074/LISEZMOI-entretien.md)# Entretien Télégestion — à ajouter au dépôt du guide

Déposez `entretien.html` et `entretien-telegestion.json` dans le même dépôt GitHub que le guide.
L'entretien sera alors en ligne à l'adresse : `https://votre-pseudo.github.io/guide-telegestion/entretien.html`

## Modifier le contenu
Tout est dans `entretien-telegestion.json` (crayon > modifier > Commit changes).

- Une question : `"question"`, ses réponses dans `"options"` (`"label"` = texte du bouton).
- `"argument"` sur une réponse : l'argument qui s'affiche quand le client donne cette réponse.
- `"objections"` sur une question : les objections proposées sous la question (identifiants de la liste `"objections"` en fin de fichier).
- `"objections"` sur une réponse : l'objection s'ouvre automatiquement quand le client choisit cette réponse.
- `"multi": true` : plusieurs réponses possibles.
- `"si"` : la question (ou la partie) ne s'affiche que si une réponse précédente l'a déclenchée, via `"set"`.
- Une objection : `"theme"`, `"objection"` (ce que dit le client), `"reponse"` (ce que répond le commercial), `"rebond"` (la question qui relance).

Si la page affiche « L'entretien ne peut pas se charger », une virgule ou un guillemet manque : ouvrez History sur le fichier pour annuler la dernière modification.
