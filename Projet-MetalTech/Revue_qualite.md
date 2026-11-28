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


## 13. V6 courte — 25/11/2026

Point de départ : V5 de 39 pages, commit `5ebef82` (`git fetch` puis contrôle : branche à jour, aucune modification du groupe depuis). La V5 reste récupérable à ce commit. Les supports originaux ne sont pas modifiés. Résultat : **31 pages A4** au lieu de 39.

### 13.1 Mise en page

- Corps du texte inchangé (11 pt). Tableaux en 10 pt (`\small`), légendes et sources inchangées.
- Marges de 20 mm (au lieu de 22 à 24 mm), interligne des tableaux 1,18 (au lieu de 1,22), liste des références en 10 pt.
- Règles des titres assouplies (une question demande 13 lignes libres au lieu de 14, une sous-section 6 au lieu de 9, une partie 28 % de page au lieu de 45 %), pour réduire les grands blancs.
- Figures 1, 2, 4, 5, 6 et 7 placées dans le texte (`[H]`), pour éviter qu'elles soient reportées loin de leur sous-section ou qu'elles croisent un tableau long. Figure 1 placée après le tableau des points critiques. Figure 1 un peu moins haute (écart entre étapes 1,26 au lieu de 1,36), sans changer la taille du texte.

### 13.2 Correspondance V5 → V6

| Question | Éléments conservés | Changements | Sources et contrôles |
|---|---|---|---|
| Introduction | Données clés, SWOT (quatre cases), choix d'hypothèses (logiciels, CA 18,4 M€ et 2,51 %, priorité aux énoncés), étiquettes Fait/Objectif/Hypothèse/Proposition | Phrases raccourcies. Ligne « Qualité » des données clés retirée : les certifications restent dans la SWOT | [1] p. 4, 7, 9, 11, 16–36, 42. 462 / 18 400 = 2,51 % recalculé |
| 9.1.1 | Figure 1 (8 étapes, acteurs, durées, entrées/sorties, boucle NC), tableau des points critiques, tableau des informations par processus, figure 2, preuves d'audit, 4,31–11,75 jours avec hypothèses, VSM | Textes condensés. Sigles regroupés en une phrase. Preuves d'audit en trois points. Figure 1 après le tableau | [1] p. 5–8, 13–25, 40, [5] diap. 28–29 |
| 9.1.2 | SMED, 5S, préparation, planification, maintenance, contrôle de la première pièce, TRS, pilote, indicateurs, 110,4 h et 8 832 € de capacité théorique, pas une économie | Tableau du pilote remplacé par une liste de trois lignes. Exemple chiffré en un paragraphe | 8 × 90 min = 12 h ; 20 % = 2,4 h × 46 = 110,4 h ; × 80 € = 8 832 € recalculés |
| 9.1.3 | Figure 3, devis p. 8 (prix unitaires, quantités absentes, 281,70 € = 125,00 + 89,50 + 67,20), pipeline 35 % et 1,2 M€ distincts du taux des devis, taux en nombre et en valeur, tableau des actions, test de trois mois, CA potentiel 60 k€ | Analyse et définitions condensées. Scénario en un paragraphe | [1] p. 7–8, 13, 19, 22, 24. 35 % et 40 % de 1,2 M€ = 420 et 480 k€ recalculés |
| 9.1.4 | Figures 4 et 5, tableau des fournisseurs, 6 630 k€ distincts des 7 200 k€ d'achats, 48 % et 46 % (parts arrondies), priorité titane, deuxième source qualifiée, plan d'actions, formule du stock de sécurité et hypothèses, 95 % ≠ taux de service, ordre de grandeur, BFR 78 jours, indicateurs | Textes condensés | [1] p. 9–11, 24–25, 37, [8] §7.2, §9.3. 980 / 220 ≈ 4,5 k€ ; 45 / 2 120 ≈ 2 % recalculés |
| 9.2.1 | Figures 6 et 7 (existant et cible), tableau des risques, sécurité des personnes, trois mesures, tableau des 10 flux avec sens de connexion, PubSub, NTP/DNS/journaux/sauvegardes, hébergement MES à confirmer, mise en œuvre et tests | Colonnes « Données échangées » et « Rôle » fusionnées. Mesures et mise en œuvre condensées | [1] p. 5, 18, 20, 26–31, [2] diap. 7, [4] diap. 26, 43–46, [9] §2.1, §5.1 |
| 9.2.2 | Méthode ISO 27005, échelles V et G, seuils, six risques initiaux et résiduels, matrice (figure 8), impact, Gantt sur 18 mois (figure 9), faisabilité à trois, vérifications Windows/LTSC/SAP/FortiGate, indicateurs | Tableau des échelles remplacé par un paragraphe (mêmes définitions). Tableau des coûts supprimé : ses lignes sont reportées dans le budget de la conclusion (ESU détaillées, remplacement du pare-feu ajouté) | [5] diap. 9–12, 21, [9] §4, [16]–[18]. R1 = 16, R2 = R3 = 12 : critiques |
| 9.2.3 | Windchill 120 Go et A320, classification, AES, TLS, hachage, signature, AES-GCM, DLP, RBAC, MFA, BitLocker et ses limites, journaux et conservation, sauvegardes, facteur humain, agilité cryptographique, EN 9100/NADCAP sans clause inventée, priorités | Notions regroupées en quatre points. Cellules du tableau des mesures raccourcies. Priorités en un paragraphe | [1] p. 16, 21, 25–27, 33, [3] diap. 15, 21, 25, 33, 36, 39, 42, [6], [19] |
| 9.2.4 | Hypothèses et moyens, trois niveaux de crise, figure 10, plan en huit phases avec délais (J+1–J+5, J+5–J+30), refus de payer, RACI (un A et au moins un R par ligne), RTO/RPO exacts, trois écarts de sauvegarde, règle 3-2-1, ordre de reprise, intégrité des plans, communication, préparation | Tableau des niveaux remplacé par une liste. Paragraphe « Délais et RTO » fondu dans le texte. « Se préparer » fusionné avec la communication | [7] diap. 10, 12–13, 16, 19–20, 22, 25, 27, [8] §4.1, §6.1, §7.1–7.3, §8.1, [9] §4, §5.3, §6, §7.3, §8.1 |
| 9.2.5 | Hypothèse entité importante, NACE, quatre sources, état de la loi daté, art. 20, 21, 23, 34.5, RGPD 32–34 et 83, rôle du DPO, figure 11, deux scénarios ISO 27001, tableau des étapes | Liste des sources en une phrase. Tableau « Ce que cela demande » remplacé par un paragraphe de renvois (mêmes exigences) | [10]–[15], Vie publique relue le 25/11/2026 (dossier modifié le 18/11/2026, aucune étape après le 17/11) |
| 9.2.6 | Situation, sept risques, phrase du cours sur le VPN, figure 12, VPN et Zero Trust distingués du ZTNA, prérequis (licences, MDM, SAML), filtrage par rôle, mesures (FIDO2 si compatible, PAM, prestataires temporaires), plan, tests positifs et négatifs | Cellules raccourcies. Plan en un paragraphe. Tests en trois points | [4] diap. 50, 54–57, [6] diap. 2–7, 30–37 |
| Conclusion | Priorités, budget (statut et source de chaque ligne), financement, rentabilité sans ROI fictif | Phrase ajoutée : montants annuels et pluriannuels non additionnés. Lignes ESU et pare-feu reprises de 9.2.2 | [1] p. 11, 27, 32–35, 42, [16] |
| Annexe A | 18 sujets d'écart avec version A, version B et hypothèse | WMS, ISO 9001 et effectif regroupés en une ligne « Écarts sans effet sur nos réponses » | Pages du cas inchangées |

### 13.3 Compilation et contrôles

Commandes exécutées dans un dossier de compilation vide :

```sh
latexmk -pdf -interaction=nonstopmode -halt-on-error -file-line-error Projet_MetalTech.tex
pdfinfo Projet_MetalTech.pdf
pdftotext -enc UTF-8 -layout Projet_MetalTech.pdf metaltech-v6.txt
```

- Journal lu : code 0, deux passes de pdfLaTeX, 0 erreur, 0 référence indéfinie, 0 `Overfull`, 0 `Underfull`. 8 messages « ignored error: Infinite glue shrinkage », émis volontairement par le noyau LaTeX autour des tableaux longs (voir section 12.3), sans effet sur le PDF.
- `pdfinfo` : 31 pages A4, titre et cinq auteurs dans les métadonnées.
- Texte extrait : 10 énoncés dans l'ordre, 12 figures numérotées de 1 à 12, 19 références, 11 liens externes, 16 signets, aucun texte provisoire.
- Contrôle de contenu automatique : pour chaque question, présence des éléments indispensables de la consigne V6 (chiffres, distinctions, termes clés). Tous sont présents.
- Contrôle visuel : 31 pages rendues en image et inspectées une par une, après chaque changement de mise en page. Corrections faites pendant ce contrôle : titre « Principaux risques » isolé en bas de page, titre et énoncé de 9.1.4 séparés de la réponse, figures 6 et 7 reportées sur une page à part.

### 13.4 Pourquoi 31 pages et pas 30

La matière restante remplit 31 pages. Les blancs résiduels (14 à 23 % des pages 9, 12, 17, 19 et 21) viennent des règles qui gardent un titre avec son début et des figures placées dans le texte. Descendre à 30 pages demanderait de retirer une figure ou un tableau, de réduire la police du texte ou de serrer davantage les marges, ce que la consigne exclut. Nous gardons donc 31 pages.

### 13.5 Points encore ouverts

1. Revérifier l'état de la loi NIS2 le jour de la remise.
2. Hébergement réel du MES et présence de serveurs OPC-UA sur les machines : hypothèses.
3. Licences Sophos (EDR), Entra ID et MDM, compatibilité FIDO2 du VPN : à confirmer.
4. Cycle de vie du FortiGate 200E : non vérifiable sur une source officielle publique.
5. Validation du fond par les cinq membres. Aucun envoi à l'enseignant, PR non fusionnée.


## 14. V7 — corrections et simplification ciblées — 26/11/2026

Base : V6, commit `d4cf674` (blob du source `20674044e53f634a6383a467c7e9b86ea7087b0e`, contrôlé après `git fetch` : aucun changement ultérieur du groupe). La V6 de 31 pages reste disponible à ce commit. Consigne appliquée : `MetalTech_V7_Execution_Ciblee.md` (textes de remplacement fournis par le groupe). Aucune nouvelle analyse, aucun chiffre ni source ajoutés. Résultat : **22 pages A4** (objectif 22–25), corps en 11 pt et marges V6 inchangés.

### 14.1 Ce qui a été supprimé ou remplacé

| Partie | Supprimé | Remplacé ou conservé |
|---|---|---|
| Introduction | Deux paragraphes d'introduction, quatre puces d'hypothèses | Texte court fourni. Paragraphe d'hypothèses fourni, renvois [1, p. 4, 11, 17–22, 32, 36] conservés. Données clés, SWOT et étiquettes conservés |
| 9.1.1 | Figure des flux entre applications (doublon du tableau), paragraphe VSM, procédure PC-QNC-004, sous-section « Preuves d'audit » | Textes fournis. Tableau des goulots, figure 1 et tableau des informations conservés. Flux Power BI (API, 5 min) gardé dans une note sous le tableau. PC-QTR-005 et [5, diap. 28–29] conservés |
| 9.1.2 | Paragraphes de définition, liste du pilote, encadré « À retenir » | Textes fournis. Tableau des six actions conservé |
| 9.1.3 | Phrase sur les logiciels, sous-sections « Analyse » et « Définir le taux » | Texte fourni. Figure du parcours conservée (DSO défini en légende). Trois lignes du tableau renommées en risques. Exemple fourni |
| 9.1.4 | Figure des flux de la supply chain, matrice des fournisseurs (seuils J+5 et 12 % arbitraires), formule statistique du stock de sécurité, encadré « À retenir » | Textes fournis. Tableau des fournisseurs (avec la réserve « d'autres fournisseurs peuvent exister »), plan d'actions et indicateurs conservés |
| 9.2.1 | Tableau des 10 flux (ports, sens de session, PubSub), numéros sur la figure cible, six risques | Texte fourni, tableau de 4 risques, 3 mesures en liste, tableau de 4 familles de flux, note (SaaS, DNS/NTP/sauvegardes, retour arrière, test). Figures existant et cible conservées |
| 9.2.2 | Explication ISO 27005, long paragraphe de vérifications, tableau des coûts déjà retiré en V6 | Textes fournis. Échelles, six risques R1–R6, matrice et Gantt conservés. Justification de R3 et R5 ajoutée. R2 : « choisir entre migration et maintien temporaire avec support confirmé ». « Dette technique » définie |
| 9.2.3 | Tableau de classification, notions détaillées, « stocker maintenant, déchiffrer plus tard », agilité cryptographique | Textes fournis. Tableau de six mesures avec un contrôle par famille. Lien EN 9100/NADCAP et priorités fournis |
| 9.2.4 | Figure de chronologie, matrice RACI, niveaux de crise, sous-section communication séparée | Texte fourni, tableau de six phases avec responsables et délais indicatifs, rôles explicites. Tableau RTO/RPO conservé (colonne « Mode dégradé ou moyen de reprise »). Commentaire, ordre de reprise et préparation fournis |
| 9.2.5 | Figure des notifications, sous-section « Ce que cela demande », code NACE, dates parlementaires du corps | Texte fourni, tableau NIS2/RGPD fourni, texte ISO fourni, plan ISO en 5 lignes (pilotes repris de la V6) |
| 9.2.6 | Tableaux séparés risques et mesures, paragraphes VPN/Zero Trust et prérequis, détail SAML | Texte fourni, tableau « risque → solution », figure conservée (état du poste : « si l'outil existe »), tableau des rôles, note PAM, texte de fin fourni |
| Conclusion | Tableau des priorités | Paragraphe fourni, budget condensé, calcul SOC 15 / 28 = 53,6 %, réserve sur CAF et trésorerie |
| Annexe A | WMS, effectif, CMM, ISO 9001, NADCAP dans le tableau | Note courte sous le tableau. Bilan, marge brute et compte de résultat reformulés selon la consigne |

Figures : 12 → 7 (fabrication, parcours commercial, architecture existante, architecture cible, matrice des risques, Gantt, accès distants). Aucune référence ne renvoie à une figure supprimée.

### 14.2 Vérifications de fond faites pendant l'application

- **Chiffres recalculés** : 980 / 220 × 10 ≈ 45 k€ et 45 / 2 120 ≈ 2 % ; 48 % et 46 % (parts arrondies) ; 15 / 28 = 53,6 % ; 35 % et 40 % de 1,2 M€ = 420 et 480 k€ ; 110,4 h × 80 € = 8 832 €.
- **Annexe financière contrôlée dans le cas (p. 11–12)** : passif affiché 13 300 k€, somme des lignes 11 300 k€ ; total des charges 18 050 k€ résultat net de 1 120 k€ compris ; produits 18 605 k€ ; écart 555 k€.
- **Gantt** : pilote ERP décalé de M4 à M5 (après la fin de la migration Windows à M5), décision à M3, bascule M9–M12, stabilisation M12–M18. Flèche de dépendance adaptée.
- **Loi NIS2** : Vie publique relue le 26/11/2026, dossier toujours daté du 18/11/2026, aucune nouvelle étape. Le statut daté du 25/11 n'est donc pas modifié.

### 14.3 Points signalés au groupe (décision à prendre ensemble)

1. **9.2.5, statut NIS2** : le texte fourni disait « Le cas indique que son statut reste à confirmer selon l'activité et la taille ». Le cas dit seulement « en cours d'évaluation » (p. 27) et « probable » (p. 34) ; le critère activité/taille vient de la directive. Formulation appliquée : « Le cas indique que ce statut reste à confirmer (p. 27, 34) ; il dépend de l'activité et de la taille de l'entreprise. » À valider.
2. **Gantt** : en décalant le début du pilote ERP à M5 sans déplacer sa fin (M9), le pilote passe de 5 à 4 mois. À confirmer par le groupe.
3. **Budget** : la ligne « Autres coûts » précise que le pare-feu peut déjà relever du budget matériel de 25 k€ par an, pour éviter de le compter deux fois (consigne). À confirmer avec le cas p. 33.
4. **Ajouts de forme** (sigles et renvois, sans nouveau contenu) : phrase d'appel de la figure 2 en 9.1.3, définitions de PCA et PAR en 9.2.4, définition de la dette technique en 9.2.2, renvois [16]–[18] dans le paragraphe de vérifications, [5, diap. 28–29] dans la phrase de vérification de 9.1.1.

Points que chaque membre doit pouvoir expliquer (consigne, §13) : priorité au titane, rôle de VLAN, DMZ et pare-feu OT, notes V × G et mesures R1–R6, RPO de 1 h face à des instantanés toutes les 4 h, délais de notification NIS2 et RGPD, choix du MFA.

### 14.4 Compilation et contrôles

```sh
latexmk -pdf -interaction=nonstopmode -halt-on-error -file-line-error Projet_MetalTech.tex
pdfinfo Projet_MetalTech.pdf
pdftotext -enc UTF-8 -layout Projet_MetalTech.pdf metaltech-v7.txt
```

- Journal lu : code 0, deux passes, 0 erreur, 0 référence indéfinie, 0 `Overfull` (un dépassement de 5 pt sur « Responsabilité » corrigé en élargissant la colonne), 0 `Underfull`. 6 messages « ignored error » du noyau LaTeX autour des tableaux longs, sans effet (section 12.3).
- `pdfinfo` : 22 pages A4, cinq auteurs dans les métadonnées. `pdftotext` : 10 énoncés dans l'ordre, 7 figures numérotées de 1 à 7, 11 liens externes, 16 signets, aucun texte provisoire.
- Contrôle automatique : éléments indispensables de chaque question présents (chiffres, distinctions, termes clés). Les 19 références sont toutes citées dans le corps.
- Contrôle visuel : 22 pages rendues en image et inspectées une par une. Correction faite : espace manquante après l'étiquette [Hypothèse] (page 8).
- Limites : les contrôles vérifient la présence et la cohérence des éléments ; ils ne remplacent pas la relecture et la validation du fond par les cinq membres.

### 14.5 Points encore ouverts

1. Revérifier l'état de la loi NIS2 le jour de la remise.
2. Hébergement du MES, OPC-UA sur les machines, mode d'accès des prestataires : hypothèses.
3. Licences EDR, Entra ID et MDM, compatibilité FIDO2 du VPN, version et support du FortiGate : à vérifier.
4. Validation collective des choix et des hypothèses, puis décision des cinq membres sur l'envoi. Aucun envoi à l'enseignant, PR non fusionnée.


## 15. Version finale à valider (V7 retouchée) — 28/11/2026

**Base.** Le travail part du commit `427f5cc`, qui contient les dernières corrections ciblées du 26/11 : Power BI, Wi-Fi et capteurs, dette technique, Veeam et Azure, communication, RPO, RGPD, « MFA si nécessaire ». Avant toute modification, la branche a été contrôlée : elle n'avait pas changé. Consigne appliquée : le message du groupe du 28/11 (propositions d'Adel, vérifiées par Saleh). Aucune nouvelle analyse n'a été ajoutée.

**Références.**
- Les lignes de synthèse « Sources » sont supprimées dans l'introduction, les dix réponses et la conclusion.
- La réponse 9.1.2 se termine par la phrase fournie, avec le renvoi [1, p. 5–6, 20].
- Les 19 références, les URL et les renvois précis du texte, des tableaux et des légendes sont conservés.

**Contrôle documentaire des renvois retirés.** Pour chaque ligne supprimée, chaque page, diapositive ou section citée a été recherchée dans le texte de la même section. Un seul renvoi n'était justifié que par une ligne supprimée : la p. 7 du cas (devis sous Excel), en 9.1.1. Le renvoi « (p. 7) » est donc placé à côté d'« Excel », dans la ligne « Commercial » du tableau.

**Textes fournis, appliqués tels quels.** Les faits cités ont été retrouvés dans le cas (p. 22, 27, 34 et 35) et dans le PCA (§7.1–7.2).
- 9.1.3 : exemple de conversion, étiquette de la figure 2 et sa légende.
- 9.2.4 : RTO présenté comme un objectif, mode dégradé dès l'activation du PCA.
- 9.2.5 : paragraphe ISO 27001, première colonne renommée « Période (si report) ».

**Mise en page seulement.**
- « Excel » n'est plus coupé en fin de ligne.
- Le paragraphe « Méthode » de 9.2.2 est resserré d'une ligne (`\looseness`) pour que la note du tableau R1–R6 reste sur la même page que le tableau.

**Contrôles.**
- `latexmk` dans un dossier vide : code 0, 0 erreur, 0 référence indéfinie, 0 `Overfull`, 0 `Underfull`.
- PDF : 22 pages A4, cinq auteurs, 10 énoncés, 7 figures, 19 références citées dans le corps, 17 liens externes, 19 liens internes. Sommaire et 16 signets inchangés.
- Comparaison mot à mot avec `427f5cc` : seules les modifications demandées apparaissent.
- Contrôle visuel : les 15 pages modifiées ont été inspectées en image, les 7 autres sont identiques au pixel près.

**Loi NIS2, revérifiée le 28/11/2026.** L'ANSSI indique toujours « transposition en cours ». Le dossier Vie publique est toujours daté du 18/11/2026 : la dernière étape est le texte modifié par l'Assemblée nationale le 17/11/2026, sans promulgation. Le texte du rapport n'est pas modifié.

**Points ouverts.** Ceux de la section 14.5 restent valables.
