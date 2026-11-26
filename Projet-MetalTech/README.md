# Rapport MétalTech — M2 SIA, iaelyon

Rapport collectif du cours **Audit et gestion de la sécurité des systèmes d'information** (Eric Disson), étude de cas *MétalTech Solutions SAS*. Remise prévue le 29 novembre 2026, en PDF, à l'enseignant (envoi fait par le groupe après validation).

Auteurs : Saleh BA-ZIGHIFAN, Abdulrahman BA GUBAIR, Abdulaziz AL-KHULAQI, Mouhamadou Moustapha DIOP, Adel ELDARAWY.

## Contenu du dossier

| Fichier | Rôle |
|---|---|
| `Projet_MetalTech.tex` | Source LaTeX complète (un seul fichier, figures en TikZ, aucune image externe) |
| `Projet_MetalTech.pdf` | PDF V7 compilé à partir du source final (A4, 22 pages) |
| `Revue_qualite.md` | Journal de travail interne : corrections, preuves, hypothèses ouvertes, contrôles réalisés |

Il n'y a pas de dossier `figures/` : les 7 figures de la V7 sont dessinées en TikZ dans le `.tex`.

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

## Version V5 — validation finale du source

Le LaTeX V5 intègre les corrections factuelles V4 et une relecture de la langue (40 modifications), notamment les définitions des sigles, les hypothèses et les limites des outils existants. Les dix questions, les douze figures TikZ et les cinq auteurs sont conservés.

**Finalisation V5 (25/11/2026).** Le PDF du dépôt a été recompilé depuis zéro à partir du source V5 final, avec `latexmk -pdf -interaction=nonstopmode -halt-on-error -file-line-error Projet_MetalTech.tex`. Résultat lu dans le journal de compilation : 0 erreur, 0 référence indéfinie, 0 dépassement (`Overfull`), 39 pages A4. Les 39 pages ont été inspectées une par une. Les messages « ignored error: Infinite glue shrinkage » du journal viennent du noyau LaTeX, qui ignore volontairement cette erreur autour des tableaux longs, et n'ont pas d'effet sur le PDF. Détails, corrections et points ouverts dans `Revue_qualite.md`, section 12.

## Version V6 — rapport raccourci (25/11/2026)

La V6 part de la V5 (commit `5ebef82`) et ramène le PDF de 39 à **31 pages**, sans retirer de réponse, de figure ni de référence : dix réponses complètes, 12 figures, 19 références, annexe des hypothèses. Le corps du texte reste en 11 pt. Les répétitions entre texte, tableaux et conclusion sont supprimées (un seul budget, en conclusion). Marges de 20 mm et tableaux en 10 pt. Compilation depuis un dossier vide : 0 erreur, 0 référence indéfinie, 0 `Overfull`, 0 `Underfull`. Les 31 pages ont été inspectées une par une. Tableau de correspondance V5 → V6 et contrôles dans `Revue_qualite.md`, section 13.

La V5 de 39 pages reste disponible au commit `5ebef82` : https://github.com/salo00h/SSI/blob/5ebef82b0d79e3c6999a7d48d5bd443b3b6c24c4/Projet-MetalTech/Projet_MetalTech.pdf

## Version V7 — corrections et simplification ciblées (26/11/2026)

La V7 applique les consignes ciblées du groupe à partir de la V6 (commit `d4cf674`) : textes de remplacement, 5 figures en double supprimées (7 figures gardées), tableaux simplifiés, Gantt corrigé (pilote ERP à M5). Résultat : **22 pages**, corps en 11 pt et marges de la V6 inchangés, dix réponses dans l'ordre, 19 références toutes citées. Compilation depuis un dossier vide : 0 erreur, 0 référence indéfinie, 0 `Overfull`, 0 `Underfull`. Les 22 pages ont été inspectées une par une. Détail des coupes, contrôles et points à faire valider par le groupe dans `Revue_qualite.md`, section 14. Les choix et hypothèses restent à valider ensemble.

La V6 de 31 pages reste disponible au commit `d4cf674` : https://github.com/salo00h/SSI/blob/d4cf6745a717086953a19896cd53b179917467b6/Projet-MetalTech/Projet_MetalTech.pdf

Avant l'envoi : revérifier l'état de la transposition NIS2 à la date effective de remise. La validation collective reste nécessaire.
