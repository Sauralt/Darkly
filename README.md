# Darkly — 42 Security Project

## Description

Darkly est un projet pédagogique de l'école 42 axé sur la sécurité web. L'objectif est d'identifier et d'exploiter un ensemble de vulnérabilités présentes sur une application volontairement vulnérable, dans un cadre d'apprentissage contrôlé.

## Objectif

Trouver et documenter l'ensemble des failles de sécurité présentes dans l'application, en respectant une méthodologie claire pour chacune : découverte, preuve de concept, impact, et correction proposée.

## Environnement de test

- **URL cible** : `http://localhost:XXXX`
- **Outils utilisés** : navigateur (DevTools), curl

## Méthodologie

Pour chaque vulnérabilité trouvée :
1. Identifier le point d'entrée (formulaire, endpoint API, upload, etc.)
2. Confirmer la faille avec une preuve de concept minimale
3. Évaluer l'impact (lecture de données, escalade de privilèges, exécution de code, etc.)
4. Documenter le payload exact utilisé
5. Proposer une remédiation

## Liste des brèches trouvées

| Faille | Flag |
| --- | --- |
| 1 - Reset Password | FLAG{r3s3t_t0k3n_w4s_just_md5_lol} |
| 2 - injection php in pfp | FLAG{unr3str1ct3d_upl0ad_g0_brrr} |
| 3 - IDOR private notes | FLAG{1d0r_ur_pr0f1l3_1s_m1n3} |
| 4 - api project access | FLAG{md5_Is_4_n4m3pl4t3_n0t_4_l0ck} |
| 5 - PATCH method http | FLAG{just_p4tch_y0ur_0wn_r0l3_lol} |
| 6 - injection XML | FLAG{d3fus3dxml_n3xt_spr1nt_pr0m1s3} |
| 7 - god permissions on database | FLAG{th3_und3rsc0r3_sl4sh_kn0ws_th3_w4y} |

## Note finale
