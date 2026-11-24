# Revue qualité — rapport MétalTech (journal interne)

Journal de travail de la révision V2 (24 novembre 2026, branche `revision-metaltech-v2`). Il n'est pas destiné à l'enseignant. Il sert au groupe pour valider le fond : ce qui a changé, pourquoi, avec quelles preuves, et ce qui reste ouvert.

## 1. Sources lues

Les neuf supports originaux ont été copiés à l'identique depuis `Cours-SSI.zip` dans `Cours-SSI/originaux/`. Lecture : texte extrait page par page **et** rendu de chaque page en image pour vérifier tableaux et schémas (le texte brut mélange les colonnes). PowerPoint : texte des 61 diapositives, notes et images (dont le schéma DMZ de la diapositive 45).

| Fichier original | Volume | SHA-256 (début) |
|---|---|---|
| Cas MetalTech SIA version 1(2).pdf | 42 pages | aeeb704e61dd… |
| PCA MetalTech v1.0 SIA(2).pdf | 9 pages | 9e6e3c2e0f6d… |
| PRA MetalTech  v1.0 SIA(2).pdf (PAR) | 11 pages | c8977b8ebf05… |
| 1 - Cyber.pdf | 17 pages, 33 diapositives | 45d1d036efa2… |
| 2 - Chiffrement.pdf | 27 pages, 54 diapositives | 53cf082a98b3… |
| Fdtx Réseaux et Cyber Réseaux SIA 2026(2).pptx | 61 diapositives | fce0765ee42d… |
| Fdtx IAM SIA 2026(2).pdf | 20 pages, 39 diapositives | bb82227b6295… |
| Fdtx Audit et Gouvernance SIA 2026.pdf | 18 pages, 36 diapositives | 0222bb046442… |
| Fdtx Gestion de crise SIA 2026.pdf | 20 pages, 39 diapositives | f094141d4912… |

Dans le rapport, les supports de cours sont cités par numéro de diapositive (numéro imprimé sur la diapositive), le cas par page, le PCA et le PAR par paragraphe.

## 2. Tableau de vérification des données

Statut : **OK** (vérifié, conforme), **Corrigé** (erreur de la version de départ ou du cas, traitée), **Hypothèse** (contradiction du cas, choix signalé), **Ouvert** (à confirmer par le groupe ou l'entreprise).

| Donnée | Page(s) exacte(s) | Constat | Traitement dans le rapport | Statut |
|---|---|---|---|---|
| CA 2025 | p. 4, 11, 36 / p. 32 | 18,4 M€ vs 13,2 M€ | 18,4 M€ retenu ; 462 k€ / 18,4 M€ = 2,51 % (et non 3,5 %) | Corrigé |
| Budget sécurité | p. 27, 32 | 28 k€ inclus dans les 462 k€ (6 %) | Présenté comme déjà engagé, pas comme enveloppe libre | OK |
| ERP | p. 17–19, 30, 33 / p. 6, 7, 12, 40 / p. 4 | SAP B1 10.0 (2019) vs S/4HANA vs « nouvel ERP 2020 » | SAP B1 10.0 ; S/4HANA = cible (p. 33) | Hypothèse |
| CRM | p. 17, 22 / p. 7, 35, 40 | Dynamics 365 vs Salesforce | Dynamics 365 | Hypothèse |
| PLM / CAO | p. 17, 21 / p. 6, 40 | Windchill + Creo vs Siemens NX | Windchill | Hypothèse |
| WMS | p. 10 / p. 17 / PAR §2.1 | SAP WM + Easy WMS vs « WMS (sage) » vs Sage X3 | Non tranché (sans effet) | Hypothèse |
| MES | p. 20, 30, PAR §2.1 / p. 28 | SaaS vs sur site | Hébergement à confirmer ; connecteurs locaux dans l'architecture cible | Ouvert |
| Bilan 2025 | p. 11 | Actif 13 300 k€ ; somme du passif 11 300 k€ | Signalé ; aucun calcul financier fin | Hypothèse |
| Marge brute | p. 11, 36 | 7,36 M€ (40 %) incompatible avec achats 7,2 M€ (→ 11,2 M€) ; budget 2026 à 57,5 % | 40 % cité « avec réserve » | Hypothèse |
| Compte de résultat | p. 11–12 | Charges 18 050 k€ vs produits 18 605 k€ | Écart de 555 k€ signalé | Hypothèse |
| Équipe SI | p. 13 / p. 30 / p. 31 | DSI + 3 admins + RSSI ½ temps vs 2 personnes + poste vacant ; « 3 personnes » | Scénario du sujet (3 personnes, sans SOC) | Hypothèse |
| SOC | p. 33 | Projet 2026, ~15 k€/an | Présenté comme projet, pas comme capacité | OK |
| Postes | p. 28, 30 / p. 33, énoncé 9.2.2 | 45 Windows 11 Pro + 15 portables vs Windows 10 | Inventaire préalable ; pas « tous sous Windows 10 » | Hypothèse |
| Postes anciens | p. 33 | 12 sur 60 ont plus de 5 ans | Repris ; âge ≠ vulnérabilité | OK |
| CMM | p. 6 / p. 20, 28 | 1 Zeiss listée vs 3 CMM connectées | 3 CMM | Hypothèse |
| Durées des 8 étapes | p. 5 | 2–4 h ; 1–3 j ; 4–8 h ; 2–8 h ; 2–8 h ; 30 min–2 h ; 1–3 j ; 1–2 j | Reprises dans la figure 1 ; somme ≈ 4 à 12 j ouvrés (hyp. 8 h/j) | OK |
| Devis DEV-2026-0847 | p. 8 | Lot de 500 pièces, pas de quantités ; total HT 281,70 € = somme des prix unitaires | Utilisé comme preuve d'erreur de devis (9.1.3) | OK (constat nouveau) |
| Conversion ~35 % | p. 22 | Taux du pipeline d'opportunités CRM, pas des devis | Distinction nombre / valeur ; exemple illustratif seulement | OK |
| Fournisseurs | p. 9 | Total 6 630 k€ ; parts conformes ; seul l'acier a deux sources dans le tableau | Matrice de criticité ; titane = priorité | OK |
| TRS, rebuts, rupture, délai fournisseur, service client, DSO | p. 20, 23–24 | Objectifs ou indicateurs donnés | Étiquetés [Objectif] ; aucune valeur avant/après inventée | OK |
| BFR | p. 37 | 78 jours de CA, « un peu élevé » | Repris pour limiter le stock de sécurité | OK |
| RTO/RPO | PCA §4.1, PAR §4 | Production 4 h/1 h ; ERP-HANA 4 h/1 h ; MES 4 h/4 h ; PLM 8 h/8 h ; Qualité 8 h/4 h | Tableau 9.2.4 vérifié dans les originaux, écarts commentés | OK |
| Sauvegardes | p. 27 ; PAR §6.1, annexe B | Veeam toutes les 4 h, rétention 30 j ; journaux HANA « à confirmer » ; réplication Azure asynchrone ~15 min | RPO 1 h non prouvé ; pas de bascule aveugle vers Azure ; 3-2-1 + copie immuable | OK |
| Test PRA | p. 27 | Mars 2026 : RTO 4 h, RPO 1 h | Pas une garantie après rançongiciel | OK |
| ISO 27001 | p. 27, 34 / p. 35 | T4 2026 vs 2028 | T4 2026 = objectif ; pré-audit proposé si SMSI pas encore opérationnel | Hypothèse |
| NIS2 | p. 27, 34 / énoncé 9.2.5 | Évaluation en cours / probable / entité importante | Hypothèse du sujet ; classification NACE à confirmer | Hypothèse |
| ISO 9001 | p. 4 / p. 4, 16 | 2010 vs 2012 | Sans effet | Hypothèse |
| NADCAP | p. 16 / p. 25 | Audit déc. 2026 vs renouvellement en cours | Signalé | Hypothèse |
| Effectif | p. 4 / p. 13–14 | 127 vs 128 (somme de l'organigramme) | 127 | Hypothèse |

## 3. Modifications par question (par rapport à la version de départ)

| Question | Ce qui a été fait |
|---|---|
| Introduction | Tableau des données clés sourcé ; méthode et étiquettes [Fait] / [Objectif] / [Hypothèse] / [Proposition] ; renvoi vers l'annexe A. |
| 9.1.1 | Figure 1 : huit étapes (dont op. 1 et op. 2+ séparées), acteurs, durées, entrées, sorties, décision qualité et boucle NC proposée ; goulots **potentiels** (G) et mesures de charge/capacité ; calcul du temps de travail vs délai de 8 semaines (VSM) ; tableau des informations par processus (8 processus) ; figure 2 des flux applicatifs ; preuves d'audit (cours Audit, diap. 28–29). |
| 9.1.2 | SMED expliqué (interne/externe), préparation des outils, 5S, planning MES, maintenance, première pièce ; pilote avec mesure avant/après ; exemple chiffré explicitement illustratif ; contrôles qualité jamais réduits. |
| 9.1.3 | Figure 3 : huit étapes p. 7 avec points faibles ; analyse de l'incohérence du devis p. 8 ; définition du taux de conversion en nombre et en valeur ; actions avec responsable et indicateur ; exemple 420 → 480 k€ présenté comme illustratif. |
| 9.1.4 | Figure 4 (flux physiques et d'information) ; tableau fournisseurs avec total ; figure 5 (matrice de criticité) ; plan d'actions daté ; formules point de commande et stock de sécurité ; ordre de grandeur titane (≈ 45 k€ pour 10 jours) et effet sur le BFR. |
| 9.2.1 | Figure 6 : existant limité aux éléments documentés (règles inter-VLAN et hébergement MES signalés comme inconnus) ; tableau des risques de convergence ; figure 7 : cible avec **exactement** les trois mesures (VLAN, DMZ industrielle, pare-feu OT) ; liste fermée des flux (source, destination, protocole, port usuel, initiateur, rôle) ; mise en œuvre sans arrêter l'atelier, sécurité des opérateurs. |
| 9.2.2 | Démarche ISO 27005 du cours ; échelle 4×4 définie pour MétalTech ; 6 risques avec actif, menace, vulnérabilité, initial et résiduel ; figure 8 (matrices avant/après) ; figure 9 (Gantt 18 mois, M0 = déc. 2026, dépendances, jalons) ; coûts connus ou à chiffrer ; vérifications Microsoft et SAP. |
| 9.2.3 | Classification à 4 niveaux ; tableau de 10 mesures techniques et organisationnelles avec preuve ; nuance BitLocker ; EN 9100/NADCAP sans exigence cyber inventée ; priorités M0–M6. |
| 9.2.4 | Hypothèses et moyens ; niveaux de déclenchement (cours diap. 12, 16) ; figure 10 (chronologie indicative) ; plan opérationnel en 7 phases ; RACI avec **un seul A par ligne** ; tableau RTO/RPO avec écarts ; ordre de reprise ; canal hors SI (Teams jugé insuffisant) ; préparation à faible coût. |
| 9.2.5 | Distinction directive / transposition / RGPD ; état de la transposition vérifié ; tableau NIS2 art. 20, 21, 23, 34 / RGPD art. 32–34 ; figure 11 (deux procédures de notification) ; correspondance art. 21 ↔ réponses du rapport ; plan ISO 27001 en 8 étapes et avis réaliste sur le T4 2026. |
| 9.2.6 | Tableau des risques ; figure 12 (identité + MFA → état du poste → VPN/ZTNA → filtrage par rôle → applications ou bastion) ; VPN vs Zero Trust ; profils d'accès ; mesures avec vérification ; tests d'accès autorisés **et refusés**. |
| Conclusion | Priorités P1/P2 ; investissement, financement et rentabilité (cohérence demandée p. 42) sans ROI inventé. |
| Annexe A | Nouvelle : 20 écarts du cas avec pages et hypothèse retenue. |
| Sources | 9 supports + 8 sources officielles datées. |

## 4. Corrections factuelles et preuves

1. **Transposition NIS2.** Le support Cyber (diap. 28 et 30) présente la « loi n° 2025-379 du 29 avril 2025 » comme loi de transposition. Recherche Légifrance (24/11/2026) : la loi n° 2025-379 du 28 avril 2025 est « relative au renforcement de la sûreté dans les transports ». Le dossier Vie publique/Légifrance du projet de loi « résilience des infrastructures critiques et renforcement de la cybersécurité » (dernière modification 18/11/2026) indique : texte adopté par le Sénat le 12/03/2025, texte modifié en 1re lecture par l'Assemblée nationale le 17/11/2026, procédure accélérée ; pas de promulgation. MesServicesCyber : « transposition en cours », ReCyF publié. → Le rapport retient « transposition en cours » et signale l'erreur du support avec tact. **À vérifier par le groupe avant la remise si une étape parlementaire intervient d'ici le 29/11.**
2. **Support SAP Business One 10.0.** Le cas dit « fin 2027 ». La page officielle SAP « Maintenance & Release Family » indique une maintenance principale jusqu'au **31 décembre 2028**, « dates subject to change ». → Le rapport garde l'échéance du sujet et mentionne la date officielle.
3. **Windows 10.** Microsoft Learn (mise à jour 12/11/2026) : fin de support le 14/10/2025 ; ESU payantes pour les organisations, 61 USD par poste la 1re année, trois ans au maximum. Cohérent avec le sujet.
4. **NIS2, articles.** Textes lus sur EUR-Lex (version HTML française) : art. 20 (approbation, supervision, responsabilité, formation de la direction) ; art. 21.2 a) à j) ; art. 23.4 (24 h, 72 h, rapport intermédiaire sur demande, rapport final un mois après la notification, cas de l'incident en cours) ; art. 34.5 (entité importante : au moins 7 M€ ou 1,4 %) ; annexe II, secteur 5 « Fabrication » (NACE 26 à 30).
5. **RGPD.** EUR-Lex, art. 32.1, 33.1-5, 34.1-3 ; page CNIL (publiée le 19/06/2018) : 72 h si risque, retard motivé, notification échelonnée, registre de toutes les violations, information des personnes si risque élevé, trois exceptions.
6. **Ratio budget SI / CA** : 2,51 % (et non 3,5 %).
7. **Devis d'exemple** : total HT égal à la somme des prix unitaires pour un lot de 500 pièces (constat nouveau, utilisé en 9.1.3).
8. **Formulations non genrées** : rôles décrits par la fonction (par exemple « direction de production comme suppléance »).

## 5. Vérifications externes non abouties

- **FortiGate 200E** : cycle de vie et version de firmware non vérifiables sur une source officielle publique (portail Fortinet sous authentification). Des sites de revendeurs donnent des dates, mais ils ne sont pas cités. Le rapport dit explicitement « à contrôler sur le portail Fortinet ». Aucune CVE citée.
- **Guides ANSSI systèmes industriels** : le PDF n'a pas pu être ouvert dans le navigateur (téléchargement direct) ; il n'est donc pas cité. Le guide ANSSI/CDSE de gestion de crise a été vérifié (publié le 6/12/2021) mais n'a pas été ajouté aux sources pour ne pas citer un document non lu en entier.
- **ISO 27001/27002/27005** : normes payantes non lues ; le rapport s'appuie sur ce qu'en dit le cours (Audit, diap. 20–21) et ne cite aucune clause précise.

## 6. Hypothèses ouvertes à valider par le groupe

1. Orthographe des quatre noms (reprise de la version validée).
2. Échéance ERP : garder la date du sujet (fin 2027) en mentionnant la date SAP réelle (fin 2028) — choix fait, à confirmer.
3. Architecture cible 9.2.1 : un pare-feu OT à trois interfaces (IT, DMZ, OT). Si le groupe préfère deux pare-feu en cascade, la figure 7 est facile à adapter.
4. ISO 27001 : position « T4 2026 = pré-audit si le SMSI n'a pas encore fonctionné ». À confirmer par le groupe.
5. Exemples illustratifs (SMED 8,8 k€/an ; devis +60 k€ ; titane ≈ 45 k€ ; 84 k€ de CA par jour ouvré) : tous marqués comme hypothèses.
6. État de la loi de transposition NIS2 : à recontrôler juste avant la remise.

## 7. Contrôles réalisés

| Contrôle | Résultat |
|---|---|
| Compilation (`latexmk -pdf`, MiKTeX 25.12, pdfTeX) | 0 erreur, 0 référence manquante |
| Dépassements | 0 `Overfull` (1 `Underfull` mineur dans un tableau) |
| Compilation depuis un clone propre du dépôt | Faite après commit (voir section 8) |
| Rendu image de chaque page et inspection visuelle | 33 pages inspectées, plusieurs passes ; chevauchements corrigés dans les figures 1, 2, 3, 7, 9, 10, 11 et 12 ; pages à moitié vides supprimées (pénalités de coupure, tableaux sécables, flottants placés après leur appel) |
| Texte extrait du PDF | Les 10 titres de questions présents, dans l'ordre (p. 4, 7, 8, 10, 13, 16, 19, 21, 25, 28) ; 4 auteurs ; « 29 novembre 2026 », « Eric Disson », « 2026-2027 », intitulé du cours présents ; aucune marque provisoire (« À compléter », « TODO », « ?? »…) |
| Liens | 18 liens internes (sommaire), 16 signets PDF, 8 liens externes, tous ouverts le 24/11/2026 (EUR-Lex en version HTML, Légifrance par recherche) |
| Palette des graphiques | Validée par le script `validate_palette.js` du skill *dataviz* (contraste, daltonisme) ; niveaux de risque toujours accompagnés d'un libellé |
| Accents et typographie | `AutoSpacePunctuation=false` pour éviter « 27001 :2022 » ; espaces fines françaises conservées devant « ; : ! ? » saisies |

## 8. Dépôt

- Branche : `revision-metaltech-v2` (créée depuis `main` ; `main` non modifiée).
- Commit 1 : supports originaux + rapport de départ (traçabilité des changements).
- Commit 2 : rapport révisé, PDF compilé, README, ce journal, inventaire des supports mis à jour.
- Aucun secret, aucun fichier temporaire de compilation dans Git.
