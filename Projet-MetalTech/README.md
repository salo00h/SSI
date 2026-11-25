# Rapport MétalTech — M2 SIA, iaelyon

Rapport collectif du cours **Audit et gestion de la sécurité des systèmes d'information** (Eric Disson), étude de cas *MétalTech Solutions SAS*. Remise prévue le 29 novembre 2026, en PDF, à l'enseignant (envoi fait par le groupe après validation).

Auteurs : Saleh BA-ZIGHIFAN, Abdulrahman BA GUBAIR, Abdulaziz AL-KHULAQI, Mouhamadou Moustapha DIOP, Adel ELDARAWY.

## Contenu du dossier

| Fichier | Rôle |
|---|---|
| `Projet_MetalTech.tex` | Source LaTeX complète (un seul fichier, figures en TikZ, aucune image externe) |
| `Projet_MetalTech.pdf` | PDF compilé à partir de ce source (A4, 38 pages) |
| `Revue_qualite.md` | Journal de travail interne : corrections, preuves, hypothèses ouvertes, contrôles réalisés |

Il n'y a pas de dossier `figures/` : les 12 figures sont dessinées en TikZ dans le `.tex`.

## Compilation

Prérequis : une distribution LaTeX récente (TeX Live 2024+ ou MiKTeX 25+) avec `latexmk`. Paquets utilisés : `babel` (french), `lmodern`, `microtype`, `amsmath`, `geometry`, `xcolor`, `graphicx`, `tabularx`, `xltabular`, `booktabs`, `multirow`, `enumitem`, `fancyhdr`, `ragged2e`, `needspace`, `float`, `flafter`, `placeins`, `caption`, `titlesec`, `tikz`, `xurl`, `hyperref`, `bookmark`. MiKTeX les installe automatiquement à la première compilation si l'installation automatique des paquets est activée.

```bash
cd Projet-MetalTech
latexmk -pdf Projet_MetalTech.tex
```

Sans `latexmk`, lancer deux fois `pdflatex Projet_MetalTech.tex` (la deuxième passe met à jour le sommaire et les renvois aux figures).

Nettoyer les fichiers temporaires :

```bash
latexmk -c
```

Les fichiers `.aux`, `.log`, `.toc`, `.out`, `.fls`, `.fdb_latexmk` ne doivent pas être ajoutés au dépôt.

## Version

- Version de départ : rapport transmis par le groupe (commit « Ajouter les neuf supports originaux et le rapport MetalTech de depart »).
- Version V2 (commit `5386a4b`) : réponses complétées selon les consignes V2, 12 figures vectorielles, annexe des écarts du cas, vérifications externes datées du 24 novembre 2026 (33 pages).
- Version V3 (branche `revision-metaltech-v2`) : corrections de fond des consignes V3, français simplifié (plus de points-virgules, sigles définis à leur première apparition), cinquième auteur, sources recontrôlées le 25 novembre 2026. Compilation contrôlée : 0 erreur, 0 dépassement de ligne (`Overfull`), 38 pages inspectées une par une. Détails dans `Revue_qualite.md`, section 9.

Le fond reste à valider par le groupe avant l'envoi à l'enseignant.
