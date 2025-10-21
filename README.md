# Creation-de-mot-de-passe-Verificateur-de-conformite-
vérifier qu'un mot de passe respecte les règles suivantes : 10 caractères minimum, au moins une majuscule, une minuscule, un chiffre et un caractère spécial. Affiche si le mot de passe est conforme ou non et liste les conditions manquantes.
Petit script Python pour vérifier qu'un mot de passe respecte des règles minimales de sécurité.

Conditions vérifiées :
- Minimum 10 caractères
- Au moins une majuscule
- Au moins une minuscule
- Au moins un chiffre
- Au moins un caractère spécial (ponctuation ASCII)

Usage :
```bash
python password_checker.py
# ou
python3 password_checker.py
```
Le script demande le mot de passe. Si le mot de passe est conforme il affiche :
- "mot de passe conforme"

Sinon il affiche :
- "mot de passe non conforme"
- la liste des règles et celles qui manquent

Pourquoi on ne voit pas ce que l'on tape ?
- Le script utilise getpass.getpass() : cela désactive l'écho dans le terminal pour éviter qu'un mot de passe soit affiché à l'écran (bonne pratique de sécurité).
- Si getpass ne fonctionne pas dans ton environnement (ex : certaines consoles web), le script passe en fallback sur input() et là la saisie sera visible.

Suggestions d'amélioration :
- Ajouter des tests unitaires pour validate_password.
- Proposer un retour plus détaillé (niveau de force).
- Ne jamais stocker ni afficher le mot de passe en clair.
