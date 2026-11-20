# Changelog skill-booster

## 1.0.0 (2026-11-20)
- Création : méthode de skill-creator + fusion (décision FUSIONNER / APPELER / GARDER SEPARE / REJETER), tests avant/après écrits avant, archivage sans suppression, rebranchement du routage, ZIP, relecture comme un étranger.
- scripts/analyser.py : texte commun par paire, mots communs des descriptions, name = dossier, références manquantes, chemins privés et liens Notion (environnements virtuels ignorés), contrôle de ZIP, --selftest.
- Premier cas réel : fin de la fusion passation-conversation -> memoire-relais (exemples/fusion-passation-conversation.md).


## 1.1.0 (2026-11-20, corrections après le banc : 4 cas notés sur 5 joués, moyenne 7,8)
- analyser.py : texte commun mesuré sur les SKILL.md seuls ET avec references/ (la copie exigée ne fait plus monter le « contenu repris » à 100 %) ; toutes les paires utiles affichées (plus de coupure à 15) ; `--parent` descend dans tous les sous-dossiers ; référence absente bloquante seulement si son dossier existe dans le skill (sinon « à voir » : fichier du projet, renvoi vers un autre skill) ; en-tête YAML invalide détecté ; signaux d'injection (commentaire HTML caché qui donne un ordre, curl | sh, ~/.ssh, ~/.aws, « ignore previous instructions », exécutable lancé) et nombre d'URL ; `--faire-zip` construit le ZIP (noms en /, sans caches). Tests : cas piégé du banc (commentaire caché + YAML invalide) avant « 0 défaut », après 2 défauts ; faux positif `assets/design-tokens.json (historique, non fourni)` avant code 1, après « à voir ». Sur les 16 skills de 02-skills : 1 vrai YAML invalide trouvé dans publication-sure (corrigé) et 1 dans chiffrage-projet (retiré du routage, signalé) ; sur les ~140 skills installés : 12 skills à lire (installateurs curl | sh, pour la plupart), 0 faux positif HTML après réglage.
- SKILL.md : proportion (demande légère = changement léger), périmètre (pas de lecture des copies installées, rien hors du dossier), sorties courtes GARDER SEPARE et REJETER (hôte inchangé), mode DIAGNOSTIC, grille de notation, cas réel principal rejoué sur la version finale, commande ZIP, brief type du contrôleur.

## 1.2.0 (2026-11-20, étape Amélioration demandée par l'utilisateur)
- SKILL.md : étape 5b obligatoire « Amélioration » (au moins 3 gains tirés d'une source réelle, au moins 1 appliqué, preuve chiffrée avant -> après, le nouveau doit dépasser l'ancien sinon on garde l'ancien) ; « améliore » ou « booste » = étapes 1, 4 et 5b ; rapport et Terminé incluent les gains. Modèle de test : tableau Amélioration, « au moins aussi bien » remplacé par « meilleur sur au moins un chiffre, pire sur aucun ».
- Cas réel : decision-business 2.2.0 -> 2.2.1 (exemples/amelioration-decision-business.md) : 3 gains appliqués, attendus du cas 06 1/5 -> 5/5 (ESTIMÉ, relecture statique), JSON avec BOM en erreur -> lu, arrondi 1,44 « 1 » -> « 2 », `--test` 13 -> 14.
- Contrôle statique de la demande (7 critères : étape obligatoire, 3 gains, 1 appliqué, preuve chiffrée, dépasser et non égaler, < 150 lignes, pas de gadget) : 1.1.0 = 1/7 (seul < 150 lignes), 1.2.0 = 7/7 (ESTIMÉ, relecture statique confirmée par un contrôleur). SKILL.md 70 -> 77 lignes.
