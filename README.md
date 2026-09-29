# Rendu de JOUIN Pierre

Une capture par étape, dans l'ordre. Terminal entier non rogné, invite visible.
Afficher l'historique en graphe quand c'est pertinent.

## Niveau 1

1. Configuration Git

   ![Configuration Git](captures/01-config.png)

2. Branche de travail

   ![Branche de travail](captures/02-branche.png)

3. Historique des commits

   ![Historique des commits](captures/03-historique.png)

4. Pull Request

   ![Pull Request](captures/04-pr.png)

5. Revue croisée

   ![Revue croisée](captures/05-revue.png)

## Niveau 2

6. Secret retiré du suivi

   ![Secret retiré du suivi](captures/06-secret.png)

7. Conflit résolu (marqueurs avant, graphe après)

   ![Marqueurs de conflit](captures/07a-marqueurs.png)

   ![Graphe après résolution](captures/07b-graphe.png)

8. Revert du bandeau promo

   ![Revert du bandeau promo](captures/08-revert.png)

9. Issue fermée par une Pull Request

   ![Issue fermée](captures/09-issue.png)

10. Protection de main et CI au vert

    ![Ruleset sur main](captures/10a-protection-haut.png)

    ![Checks requis](captures/10a-protection-bas.png)

    ![CI au vert](captures/10b-ci.png)

## Cible mobile

11. Commit distant récupéré et conflit résolu

    ![Commit mobile récupéré et fusionné](captures/11-mobile.png)

## Trois commits annotés

1. `788ed32` : retire `config/secrets.env` du suivi avec `git rm --cached` et l'ajoute au `.gitignore` pour qu'il ne revienne pas. Le mot de passe reste lisible dans l'historique (commit `ff28a3f`) : en situation réelle, il faudrait le changer et réécrire l'historique.
2. `bccbb81` : fusionne `feature/couleurs` dans ma branche. Les deux branches modifiaient le même `<h1>`. J'ai gardé les deux intentions : la classe `hero` et le nouveau texte du titre.
3. `d0391cd` : annule le bandeau promo avec `git revert`, qui crée un commit inverse sans réécrire l'historique. C'est la bonne méthode sur une branche partagée, contrairement à `reset`.