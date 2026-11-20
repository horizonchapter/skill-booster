# Test avant/après d'une fusion (modèle)

Écrit AVANT de toucher aux skills. Rempli après.

```
# Fusion <original> -> <hôte> (<date>)
Terminé = <condition vérifiable>

## Avant
- analyser.py : texte commun <x> %, défauts <n> (réf. manquantes, chemins privés)
- Déclenchement (5 phrases) : <phrase 1> oui/non ... -> <n>/5 pour l'hôte, <n>/5 pour l'original
- Skills qui répondent à la même demande : <n>
- Références vivantes à l'original (grep) : <n> fichiers
- Cas réel : <entrée> -> <sortie, chiffre>

## Après
- Contenu repris : <n>/<total> lignes (%), lignes écartées et raison
- Déclenchement : <n>/5 (STOP si baisse de plus de 1)
- Skills qui répondent à la même demande : 1
- Références vivantes à l'original : 0 (ou liste des fichiers d'un autre propriétaire, signalés)
- analyser.py : 0 défaut sur l'hôte
- Cas réel : même entrée -> <sortie, chiffre>, meilleur sur au moins un chiffre, pire sur aucun
- ZIP : analyser.py --zip OK

## Amélioration (étape 5b)
| Gain | Source (défaut, retour, piège) | Appliqué ? | Avant | Après |
|---|---|---|---|---|
| <gain 1> | <source> | oui | <chiffre> | <chiffre, meilleur> |
| <gain 2> | <source> | proposé | - | - |
| <gain 3> | <source> | proposé | - | - |

## Verdict
GARDER / STOP / PIVOT, une phrase.
```

Règles de mesure :
- Le déclenchement mesuré ici est statique (l'intention est-elle écrite dans la description ?). Une mesure réelle demande une session neuve ; dis-le.
- Un chiffre sans source est étiqueté HYPOTHÈSE.
- Si l'ancien fait mieux sur un point, garde l'ancien sur ce point ou corrige l'hôte avant d'archiver.
