# Étape 5b sur un vrai cas : decision-business 2.2.0 -> 2.2.1 (2026-11-20)

Demande : « améliore decision-business » après la seconde vague d'un banc d'essai (cas 06 noté 3,0/10 par un juge indépendant).
Terminé = au moins 1 gain appliqué, chaque gain prouvé par un chiffre avant -> après, `--test` vert, rien qui baisse.

## Gains trouvés (3 cherchés, 3 trouvés, tous tirés du banc)
| Gain | Source | Appliqué ? | Avant | Après |
|---|---|---|---|---|
| Personne pour répondre au démarrage : pas de réponse simulée, pas de calcul sur des valeurs inventées, verdict « pas décidable » + pistes | cas 06, 5 attendus du juge | oui (SKILL.md, case A) | 1/5 attendus couverts par une ligne écrite | 5/5 (ESTIMÉ : relecture statique) |
| Entrée JSON avec BOM (fichier enregistré par Notepad ou PowerShell) | auto-rapport du cas 06 | oui (chiffrer.py) | JSONDecodeError, 0 sortie | sortie complète |
| Ventes arrondies à l'entier le plus proche (1,44 vente affiché « 1 ») | auto-rapport du cas 06 | oui (chiffrer.py) | « 1 » pour 1,44 ; point mort 185 pour 185,x | arrondi au-dessus : « 2 », 186 |

Contrôle de non-régression : `chiffrer.py --test` 13/13 avant, 14/14 après (un cas ajouté pour l'arrondi) ; SKILL.md 109 -> 110 lignes.
Limite : le gain 1 est un contrôle statique (le texte couvre l'attendu) ; le cas 06 n'a pas été rejoué par un exécutant.

## Verdict
GARDER la 2.2.1 : elle dépasse la 2.2.0 sur 3 chiffres et ne baisse sur aucun.

