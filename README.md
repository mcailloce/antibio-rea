# Antibio Réa

Application web installable (PWA, fonctionne hors ligne) : posologies des antibiotiques fréquents en réanimation et adaptation à la fonction rénale.

- Source des posologies : **Vidal GPR** (groupe SiteGPR-SPILF). Les données sont chiffrées (`data.enc.js`, AES-256-GCM, clé dérivée du mot de passe par PBKDF2) ; la date de consultation figure en bas de l'application ; chaque fiche indique sa date de mise à jour GPR.
- Fonction rénale : DFG saisi, DFG CKD-EPI 2009 (créatininémie, âge, sexe) ou clairance mesurée U×V/P (créatininurie, volume, durée de recueil, créatininémie).
- Accès protégé par mot de passe.
- Profils : non dialysé (paliers de DFG), hémodialyse, DPCA, EER continue (HVVC/HDVVC/HDFVVC).

Aide à la prescription : vérifier sur la fiche GPR en cas de doute.

Mise à jour : incrémenter `VERSION` dans `sw.js` à chaque modification des fichiers.
