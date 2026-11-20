# Fusion passation-conversation -> memoire-relais (2026-11-20, premier cas réel)
Terminé = 1 skill au lieu de 2 pour la passation, contenu repris 100 %, déclenchement de l'hôte >= celui de l'original, 0 défaut analyser.py sur l'hôte, original archivé et inscrit au registre, ZIP OK.

## Étape 1-2 : lire, mesurer, déjà fait ?
`analyser.py --parent` sur les 24 skills du dossier source : 2 doublons seulement (>= 50 %) : memoire-relais + passation-conversation 95 %, chiffrage-projet + decision-business 54 %. Les 4 skills Roblox : 2 % entre eux (usages distincts, pas de fusion). Contenu de passation-conversation déjà copié dans memoire-relais (references/passation-chat.md (historique, non fourni)) le même jour, mais fusion pas finie : original toujours en place, routage « à archiver », 1 déclencheur manquant, 1 lien Notion privé dans l'hôte.
Effets de bord trouvés par le même scan (hors de ce cas, signalés) : 0 vraie référence manquante après correction du script (renvois vers un autre skill = faux positifs, corrigés) ; 1 exemple de chemin générique dans un autre skill (non modifié).

## Avant
- Texte commun : 95 % ; défauts sur l'hôte : 1 (lien Notion, SKILL.md l.64).
- Contenu de l'original présent dans l'hôte : 18/19 lignes ; manque la description « conversation longue ».
- Déclenchement (« passation » · « nouveau chat » · « context transfer » · « la conversation est trop longue » · « fais-moi un bloc à coller dans un autre chat ») : hôte 4/5 (manque « trop longue »), original 5/5.
- Skills qui répondent à « passation » dans le dossier source : 2.
- Liens vivants vers l'original : routage, état des skills (2 lignes), 2 notes du second cerveau.

## Après
- Contenu repris : 19/19 (la 19e ligne devient un déclencheur de la description).
- Déclenchement de l'hôte : 5/5 (= original, aucune baisse).
- Skills qui répondent à « passation » : 1.
- analyser.py sur l'hôte : 0 référence manquante, 0 chemin privé.
- Original déplacé vers l'archive datée, ligne au registre des archives ; liens vivants mis à jour (routage, état, notes) ; 2 fichiers de règles d'un autre propriétaire citent encore l'ancien nom : signalés au propriétaire, pas réécrits.
- ZIP hôte et ZIP skill-booster : `--zip` OK.

## Verdict
GARDER : la fusion ne perd rien et gagne un déclencheur ; mesure de déclenchement statique (le routeur réel n'est pas mesuré, HYPOTHÈSE).

