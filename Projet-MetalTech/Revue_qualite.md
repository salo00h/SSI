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
- Commit 2 : rapport révisé V2, PDF compilé, README, ce journal, inventaire des supports mis à jour.
- Commit 3 : révision V3 (section 9 ci-dessous).
- Aucun secret, aucun fichier temporaire de compilation dans Git.

## 9. Révision V3 (25 novembre 2026)

Point de départ : commit `5386a4b` de la branche, à jour avec `origin` (aucune modification du groupe entre-temps). Le texte des dix réponses, de l'introduction, de la conclusion et de l'annexe a été réécrit en français plus simple. Les 12 figures ont été conservées et retouchées quand le fond l'exigeait.

### 9.1 Auteurs

- Cinquième membre ajouté sur la couverture et dans les métadonnées du PDF : **Adel ELDARAWY**. Orthographe confirmée par Abdulrahman BA GUBAIR le 25/11/2026, ainsi que celle des quatre autres noms.

### 9.2 Corrections de fond par question

| Question | Correction V3 |
|---|---|
| 9.1.1 | « 4 à 12 jours ouvrés de travail effectif » remplacé par un total indicatif de **4,31 à 11,75 jours** de durées cumulées (étapes successives, 8 h/j, une seule opération 2+). Comparaison avec les 8 semaines présentée comme un indice à vérifier sur des commandes comparables. Boucle NC : « retouche validée : reprise » et « sinon : rebut enregistré, OF relancé si besoin ». Figure 1 placée juste avant le tableau des points critiques, sur la page qui suit son appel. |
| 9.1.2 | SMED défini en une phrase. Calcul détaillé : 8 × 90 min = 12 h/semaine, 20 % = 2,4 h, 46 semaines = 110,4 h, à 80 €/h = 8 832 € de capacité théorique. Ce n'est ni une économie de trésorerie ni un bénéfice. Coût du pilote « à estimer » (plus de « coût faible »). |
| 9.1.3 | Devis p. 8 : ambiguïté et risque d'erreur à clarifier, pas une preuve d'erreur de facturation (texte, figure 3 et annexe A). 35 % = taux du pipeline CRM. Scénario 420 → 480 k€ explicitement illustratif. Licences et paramétrage des outils à vérifier. |
| 9.1.4 | « Dans le tableau des fournisseurs du cas » précisé. 6 630 k€ = total du tableau, différent des 7 200 k€ d'achats du compte de résultat. Hypothèses de la formule du stock de sécurité (délai fixe, demande indépendante, loi à peu près normale). Exemple du titane présenté comme ordre de grandeur, pas comme commande. |
| 9.2.1 | Tableau des flux refait : colonne « connexion (client → serveur) » distincte des « données échangées ». OPC-UA : le connecteur MES (client) ouvre la connexion vers le serveur de la machine ; PubSub signalé comme exception. MQTT : publication, broker, abonnement. Flux ajoutés : administration et prestataires vers le bastion, bastion vers OT, mises à jour. Flux restant à inventorier listés (NTP, DNS, journaux, sauvegarde de la DMZ). Numéros de la figure 7 mis à jour. Continuité en mode local nuancée. Sécurité des personnes rappelée. |
| 9.2.2 | Seuils de risque définis et couleurs vérifiées. Résiduel « estimé, pas constaté ». Windows 10 22H2 : fin du support standard le 14/10/2025 ; éditions LTSC différentes (LTSC 2021 Entreprise : 12/01/2027). Paragraphe « Faisabilité avec trois personnes ». Le CA de 84 k€ par jour n'est plus présenté comme une perte certaine. |
| 9.2.3 | Notions simples : AES, TLS, empreinte, DLP, RBAC. Une empreinte seule ne prouve pas l'origine : signature numérique ou empreinte transmise par un canal de confiance. Limites de BitLocker. Ligne « Conservation des journaux » ajoutée. DLP : fonctions des licences existantes d'abord. |
| 9.2.4 | Plus aucune phrase liant un arrêt d'urgence à l'accord du chef d'atelier : ligne « Sécurité des personnes » (la mise en sécurité prime). Isolement IT/OT avec le FortiGate et les VLAN existants (pare-feu OT = cible). Identité : assainir ou reconstruire l'annuaire, révoquer sessions et jetons, renouveler secrets et comptes à privilèges. Azure jamais reconnecté automatiquement. Ordre de reprise complété (PLM et traçabilité avant toute nouvelle série) et conditions du mode dégradé. Écart entre restauration en jours et RTO de 4 h expliqué. RACI : R/A/C/I expliqués, colonne « Dir. com. » ajoutée, chaque ligne a un seul A et au moins un R. |
| 9.2.5 | Quatre sources distinguées (directive, loi française, RGPD, recommandations ANSSI). État au 25/11/2026 : adoption en première lecture par l'Assemblée le 17/11/2026, non promulgué. Pré-enregistrement ANSSI présenté comme démarche préparatoire. Art. 34.5 NIS2 : plafond minimal à prévoir par chaque État, pas une amende automatique. RGPD art. 83 : deux niveaux (10 M€/2 % pour la sécurité et la notification, 20 M€/4 % pour d'autres manquements). ISO 27001 : scénarios A et B, tableau avec preuves et échéances (scénario B : certification conditionnelle au T4 2027, horizon 2028 au plus tard). |
| 9.2.6 | IAM, VPN, MFA, PAM et ZTNA définis. Le VPN n'ouvre pas forcément tout le réseau : cela dépend du filtrage. Azure AD = Microsoft Entra ID. Prérequis à vérifier (licences d'accès conditionnel, MDM, intégration Fortinet). Tests par profil (salarié, administrateur, prestataire, invité). |
| Conclusion | Comparaison « un jour d'arrêt = plus de cinq ans de SOC » supprimée. Nouveau tableau « Budget par priorité » : coûts connus, estimations, devis à obtenir. |

### 9.3 Sources recontrôlées le 25/11/2026

| Source | Résultat |
|---|---|
| Assemblée nationale, actualité du 17/11/2026 | Adoption en première lecture du projet de loi « résilience » confirmée. Ajoutée en [14]. |
| Légifrance, loi n° 2025-379 | Lien direct vérifié : `https://www.legifrance.gouv.fr/loda/id/JORFTEXT000051528207` (sûreté dans les transports). |
| EUR-Lex, RGPD art. 83.4 et 83.5 | Deux niveaux d'amendes vérifiés. Les art. 25 à 39 (dont 32 à 34) relèvent du niveau 10 M€/2 %. |
| EUR-Lex, NIS2 (lien « ALL » des consignes) | Page fonctionnelle. Articles déjà lus le 24/11. |
| Microsoft Learn, informations sur les versions de Windows 10 (mise à jour 19/11/2026) | 22H2 : fin des mises à jour standard. LTSC 2021 : fin du support standard le 12/01/2027. LTSC 2019 : support étendu jusqu'au 09/01/2029. Ajoutée en [18]. |
| MesServicesCyber | Transposition en cours. Service de pré-enregistrement en ligne disponible. |

### 9.4 Contrôles réalisés (V3)

- `latexmk -pdf` (MiKTeX) : 0 erreur, 0 référence indéfinie, 0 `Overfull`.
- 38 pages rendues en image et inspectées une par une. Figures 7, 10 et 12 vérifiées en gros plan. Chevauchements corrigés (étiquette du rebut dans la figure 1, cercle « 9 » en pointillés dans la figure 7, étiquette « interdit » dans la figure 12).
- Texte extrait du PDF : 10 questions dans l'ordre (p. 4, 7, 9, 11, 14, 18, 21, 23, 28, 31), 5 auteurs, métadonnées avec les 5 auteurs, année, enseignant, date de remise, aucune marque provisoire, aucun point-virgule dans le texte, 10 liens externes et 18 liens internes.
- Guillemets français rendus insécables (`\og` / `\fg`) pour éviter « en fin de ligne.

### 9.5 Points encore ouverts

1. État de la loi de transposition NIS2 : à recontrôler juste avant l'envoi du 29/11.
2. Hébergement réel du MES (SaaS ou sur site) et existence de serveurs OPC-UA sur chaque machine : hypothèses à confirmer.
3. Cycle de vie du FortiGate 200E : non vérifiable sur une source publique officielle.
4. Validation du fond par les cinq membres avant l'envoi à l'enseignant.


## 10. Corrections factuelles V4 — 25/11/2026

- Clarification des prix unitaires du devis et des quantités absentes, des indicateurs CRM non documentés et du CA potentiel.
- Correction de la formulation de l'écart de chiffre d'affaires et des données de marge brute.
- Tarifs annuels ESU (61, 122, 244 USD par poste) et caractère cumulatif du programme.
- Distinction entre chiffrement simple et authentifié (AES-GCM), référence NIST SP 800-38D ajoutée.
- Précision des articles 21 et 23 de NIS2, du principe Zero Trust, du calendrier de crise et de la date de sortie de SAP Business One 10.0.

**État du dépôt :** le fichier LaTeX contient les corrections V4. Le PDF du dépôt reste celui de la V3 tant qu'il n'a pas été recompilé à partir du nouveau LaTeX. Une copie PDF corrigée directement a été produite séparément pour le groupe. Recompiler (`latexmk -pdf Projet_MetalTech.tex`), contrôler les pages et remplacer le PDF du dépôt avant la fusion. Aucun envoi à l'enseignant.


## 11. Relecture V5 — 25/11/2026

40 modifications du source LaTeX : phrases simplifiées, définitions CAO, RFID, DSO, TRS, HTTPS, SFTP, MQTT, SAML et firmware ; clarification du BFR, du risque résiduel et du RPO. Vérification du cas, notamment p. 5, 7–9, 11–12, 18–20, 22, 24, 26–28, 30, 33 et 38–42. Le taux de conversion des devis n'est pas fourni, la marge par affaire est déjà suivie, les fonctions EDR restent à confirmer selon la licence, et la date de mise à niveau SAP Business One 10.0 est inconnue. Contrôle statique : dix questions dans l'ordre, douze blocs TikZ, cinq auteurs conservés. Les consignes imposent un groupe de 4–5 et un PDF pour le 29/11, sans nombre de pages prescrit. Pas de nouvelle compilation ni de contrôle visuel V5 réalisés à ce stade. Le PDF versionné reste V3 et doit être régénéré depuis le LaTeX V5. Aucun envoi à l'enseignant ni fusion.


## 12. Finalisation V5 : contrôles ciblés, compilation et PDF final — 25/11/2026

Point de départ : commit `4ee6935` de la branche `revision-metaltech-v2`, récupéré par `git fetch` puis `git pull --ff-only` (avance rapide depuis `65485de`, aucune modification locale, aucun conflit). Les corrections V4 et V5 de Saleh sont conservées. Seuls les écarts réellement constatés ont été corrigés.

### 12.1 Corrections apportées au source

| Question | Écart constaté | Correction |
|---|---|---|
| Introduction | Le cas conseille les outils d'analyse stratégique (p. 42), aucun n'était utilisé | Synthèse SWOT courte (quatre cases), uniquement avec des éléments du cas (p. 4, 7, 9, 16, 18–22, 25, 27, 29, 30, 33–35). Pas de donnée financière, car les tableaux du cas sont incohérents |
| 9.1.3 | La figure 3 présentait comme des faits deux points que le cas ne permet pas d'établir (critères de qualification « non formalisés », motif de perte « non enregistré ») | Ils sont présentés comme des risques à vérifier dans la figure, la légende et le tableau des axes (colonne « Problème ou risque »). Le texte disait déjà que le cas ne précise pas ce suivi |
| 9.1.4 | Origine des 48 % et 46 % non dite. Faute « dépend du probabilité ». 95 % pouvait être lu comme un taux de service | Précision « en additionnant les parts arrondies ». Faute corrigée. Ajout : ce n'est pas forcément le taux de service en volume |
| 9.2.2 | « Les trois risques critiques ou élevés (R1, R2, R3) » alors que 16 et 12 sont critiques selon les seuils | « Selon les seuils de la matrice, R1 (16), R2 et R3 (12) sont des risques critiques » |
| 9.2.2 et conclusion | ESU : 122 et 244 USD présentés comme publiés. La page Microsoft donne 61 USD la 1re année et le doublement annuel | « 61 USD la 1re année, prix doublé chaque année (122 puis 244 USD) ». Achat par année, 3 ans au plus, programme cumulatif (phrase de la page Microsoft) |
| 9.2.3 | Confidentialité, intégrité et authenticité pas clairement distinguées. Rôle de la signature pour l'origine absent | Nouveau point : chiffrement = confidentialité, hachage = intégrité, AES-GCM = chiffrement authentifié [19], signature vérifiée avec une clé de confiance = authenticité. [19] ajouté aux sources de la question |
| 9.2.4 | Figure 10 : restauration jusqu'à J+10 et validation « jusqu'à J+10 », alors que le tableau donne restauration J+1–J+5 et validation J+5–J+30. Rapport final NIS2 placé à J+30 | Barres et légende alignées sur le tableau. Rapport final placé après J+30 (« 1 mois après la notification », vers J+33 si notification à H+72). H0 défini comme la prise de connaissance |
| 9.2.4 | Vérification de l'intégrité des plans avant une série non explicite | Ordre de reprise, étape 6 : versions validées, signatures ou empreintes vérifiées avant toute série qui dépend de ces plans |
| 9.2.5 | Rôle du DPO ambigu (registre « tenu par le DPO ») | Le DPO conseille et contrôle, l'entreprise reste responsable. Registre tenu par l'entreprise avec l'aide du DPO. État de la loi précisé (texte modifié par l'Assemblée, procédure accélérée, aucune étape après le 17/11) |
| 9.2.6 | FIDO2 recommandé sans condition de compatibilité | « si le VPN et les applications sont compatibles » |
| Sources | Titre NIST approximatif | Titre exact de SP 800-38D, date (novembre 2007) et révision annoncée en 2024 |
| Mise en page | Bloc SWOT coupé entre deux pages. Figure 5 débordant sur le pied de la page 13 (figure 4 reportée en haut de page, mal prise en compte par les tableaux longs) | Bloc SWOT gardé d'un seul tenant. Figure 4 placée dans le texte et figure 5 sans placement « ici ». Renvoi à la figure 2 ajouté dans le texte |

Points vérifiés sans correction : 9.1.1 (huit étapes, 4,31–11,75 jours avec journées de 8 h et une seule opération 2+, boucle NC avec retouche validée), 9.1.2 (TRS, 110,4 h et 8 832 € de capacité théorique), devis p. 8 (prix unitaires, quantités absentes, 281,70 € = somme affichée), pipeline p. 22, 6 630 k€ distinct des 7 200 k€ d'achats, 9.2.1 (trois mesures, existant et cible séparés, OPC-UA client/serveur et PubSub, MQTT avec TLS, NTP/DNS/journaux/sauvegardes à inventorier, aucun flux direct IT vers machines, hébergement MES en hypothèse), valeurs RTO/RPO du PCA et du PAR, test de bascule distinct d'une reprise après rançongiciel, snapshots de 4 h et RPO de 1 h, pas de reconnexion Azure automatique, RACI (un seul A et au moins un R sur chacune des 11 lignes), NIS2 art. 20, 21, 23 et 34.5, RGPD art. 32–34 et 83, scénarios ISO 27001, Zero Trust distinct du ZTNA, budget (2,51 %, contradiction 13,2 M€ p. 32, pas d'addition de dépenses de nature différente, pas de ROI).

### 12.2 Références contrôlées

- **Cours** : les 47 citations « [k, diap. n] » du texte ont été rapprochées automatiquement du texte des supports (titre de la diapositive citée). Pour le support Réseaux, les numéros ont été vérifiés dans le PowerPoint original (ordre de présentation et numéro imprimé) : 26 VLAN, 43–45 segmentation et DMZ, 46 pare-feu, 50 VPN, 54–57 authentification et Zero Trust. Aucun numéro faux trouvé. La règle 3-2-1 figure bien sur la diapositive 10 du support Gestion de crise.
- **Sources officielles revues le 25/11/2026** :
  - Vie publique (page lue dans un navigateur, car elle s'affiche en JavaScript) : texte adopté par le Sénat le 12/03/2025, modifié en 1re lecture par l'Assemblée nationale le 17/11/2026, procédure accélérée, dossier modifié le 18/11/2026. Pas de commission mixte paritaire ni de promulgation.
  - Assemblée nationale : adoption en 1re lecture le 17/11/2026.
  - MesServicesCyber : « transposition en cours », pré-enregistrement et ReCyF (version de travail).
  - Microsoft ESU (page mise à jour le 12/11/2026) : 61 USD la 1re année, doublement annuel, programme cumulatif, achat par année.
  - Microsoft, informations de version (19/11/2026) : fin de Windows 10 22H2 le 14/10/2025, LTSC 2021 jusqu'au 12/01/2027.
  - NIST SP 800-38D : GCM est un chiffrement authentifié (« authenticated encryption with associated data »), novembre 2007, révision annoncée.
- **Non revérifié ce jour** : page SAP (maintenance de SAP Business One 10.0), lue le 24/11. Cycle de vie du FortiGate 200E : toujours aucune source officielle publique.

### 12.3 Compilation et contrôles du PDF

Commandes exécutées dans un dossier de compilation vide, avec le `.tex` final (empreinte identique à celle du dépôt) :

```sh
latexmk -pdf -interaction=nonstopmode -halt-on-error -file-line-error Projet_MetalTech.tex
pdfinfo Projet_MetalTech.pdf
pdftotext -enc UTF-8 -layout Projet_MetalTech.pdf metaltech-final.txt
```

- Journal lu : `latexmk` termine avec le code 0, après deux passes de pdfLaTeX. 0 erreur, 0 référence indéfinie, 0 `Overfull`, 1 `Underfull` sans effet visible (cellule « Rapport des connexions refusées », 9.2.6).
- 9 messages « ignored error: Infinite glue shrinkage found in box being split » : ils sont émis par le noyau LaTeX lui-même, qui ignore volontairement cette erreur primitive (`\ignoreprimitiveerror`, `latex.ltx`) pour extraire les marques de page autour des tableaux longs. Ils existaient déjà en V3 (7 messages) et n'ont aucun effet sur le PDF.
- `pdfinfo` : 39 pages A4 (595,276 × 841,89 pt). Titre et cinq auteurs présents dans les métadonnées.
- Texte extrait : 10 énoncés dans l'ordre 9.1.1 à 9.2.6, 12 figures numérotées de 1 à 12, 5 auteurs, date de remise, aucun texte provisoire, 11 liens externes, 16 signets.
- Contrôle visuel : 39 pages rendues en image et inspectées une par une. Gros plans sur les figures 3 et 10 (modifiées). Après chaque correction de mise en page, recompilation complète et nouvelle inspection des pages concernées. Pages en partie vides restantes : fin de l'introduction (p. 4), fin de la partie 1 (p. 14), fin des pages 7 et 18. Elles viennent des règles qui gardent ensemble un titre de partie ou de question avec son début.

### 12.4 Points encore ouverts

1. Revérifier l'état de la loi NIS2 le jour de la remise (une commission mixte paritaire peut intervenir).
2. Hébergement réel du MES et présence de serveurs OPC-UA sur les machines : hypothèses.
3. Licence Sophos (fonctions EDR), licences Entra ID et MDM, compatibilité FIDO2 du VPN : à confirmer.
4. Cycle de vie du FortiGate 200E : non vérifiable sur une source officielle publique.
5. Validation du fond par les cinq membres. Aucun envoi à l'enseignant, PR non fusionnée.
