# Guide Télégestion — commerciaux

Outil d'aide à l'entretien pour proposer la télégestion de l'éclairage public : découverte du parc, télégestion existante ou non, objections, recommandation finale et synthèse du rendez-vous.

## Les fichiers

| Fichier | Rôle | À modifier ? |
| --- | --- | --- |
| `arbre-telegestion.json` | Tout le contenu : questions, réponses, conseils, objections, recommandations | Oui, c'est le seul fichier à faire évoluer |
| `index.html` | La page qui affiche le guide | Non, sauf pour changer l'apparence |
| `README.md` | Cette notice | Si besoin |

## Modifier le contenu

1. Ouvrir `arbre-telegestion.json` sur GitHub, puis cliquer sur le crayon (Edit this file).
2. Faire la modification (voir les exemples ci-dessous).
3. Cliquer sur **Commit changes**, écrire en une ligne ce qui a changé, valider.
4. Le site se met à jour en une à deux minutes.

Si le guide affiche « Le guide ne peut pas se charger », c'est qu'une virgule ou un guillemet manque dans la dernière modification. Ouvrir **History** sur le fichier pour revoir ou annuler le changement.

### Changer le texte d'une question

Chercher la question (Ctrl+F dans l'éditeur) et modifier le texte entre guillemets :

```json
"question": "Combien de points lumineux compte votre commune ?",
```

### Ajouter une réponse à une question

Ajouter une ligne dans `"reponses"`, avec une virgule entre chaque réponse :

```json
"reponses": [
  { "label": "Moins de 500", "set": { "taille": "petite" }, "next": "p1_armoires" },
  { "label": "500 à 3 000", "set": { "taille": "moyenne" }, "next": "p1_armoires" },
  { "label": "Plus de 10 000", "set": { "taille": "tres_grande" }, "next": "p1_armoires" }
]
```

- `label` : le texte affiché sur le bouton.
- `next` : l'identifiant de la question suivante.
- `set` : l'information retenue pour choisir la recommandation finale (facultatif).
- `objections` : les objections à afficher si le client donne cette réponse (facultatif), par exemple `"objections": ["o_abonnement"]`.
- `signal` : un signal d'opportunité affiché au commercial (facultatif).

### Ajouter une question

Copier un bloc de question existant, lui donner un nouvel identifiant (par exemple `p2_astreinte`), puis faire pointer le `next` d'une réponse de la question précédente vers ce nouvel identifiant.

### Ajouter ou modifier une objection

Les objections sont en fin de fichier, dans `"objections"`. Chacune a un thème, le texte de l'objection, la réponse et une question de rebond.

## Règles à respecter

- Les textes sont toujours entre guillemets droits `"…"`.
- Une virgule entre deux éléments, jamais après le dernier.
- Un identifiant (`next`, `objections`) doit exister dans le fichier.
