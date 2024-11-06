# Protocole Interop Malfaçon

## Table des matières

1. [Introduction](#introduction-api-malfaçon)

2. Malfaçon signalée par l'OI vers l'OC

   1. Malfaçon "Imputable" signalée par l'OI vers l'OC

      1. [Cycle de vie et règles de transition entre états](#cycle-de-vie-dune-malfaçon-imputable-oi-vers-oc-non-critique)

      2. [Gestion des compteurs](#liste-des-différents-compteurs-utilisés-dans-le-process-malfaçons-lors-dune-signalisation-oi-vers-oc)

   2. Malfaçon "Non Imputable" ou "Critique" signalée par l'OI vers l'OC

      1. [Cycle de vie et règles de transition entre états](#cycle-de-vie-dune-malfaçon-non-imputable-ou-critique-de-loi-vers-oc)

   3. Diagrammes de séquence de cas d'utilisation de Malfaçons signalée par l'OI vers l'OC

      1. [Diagramme de séquence des 11 Cas d'utilisation](#cas-dutilisation-signalisation-oi)

3. Malfaçon signalée par l'OC vers l'OI

   1. [Cycle de vie](#cycle-de-vie-dune-malfaçon-oc-vers-oi)

   2. [Diagramme de séquence du cas d'utilisation](#cas-dutilisation-signalisation-oc)

## Introduction API Malfaçon

Cette API permet la déclaration et le traitement d'une malfaçon grâce à des flux normalisés:

Une malfaçon est une non-conformité par rapport aux STAS (Spécification Technique d'Accès aux Services) ou règles de l'art, issue de travaux menés dans le cadre d'une prestation de production ou de SAV sur un accès (PM/PBO/PTO). Les malfaçons que l'on constate le plus souvent sont : un non-respect du cheminement de la jarretière, une non-conformité de la jarretière (couleur, diamètre, longueur…) mais aussi des déchets laissés sur place (sachet plastique, chute de jarretière…) ou des dégradations (serrure cassée…). La Malfaçon se distingue de la notion de dysfonctionnement dont est ici rappelée la définition Interop'Fibre : un dysfonctionnement est une problématique qui rend impossible l'adduction du réseau d'un OC au PM mis à disposition par un OI.

Les signalisations peuvent être:

1. De l'OI vers l'OC :

Cas 1 : Malfaçon imputable de l'OI vers l'OC : reprise attendue de la part de l'OC

Il s'agit alors de Malfaçon non critique imputable à un seul OC : c'est alors une notification appelant action corrective de la part de l'OC destinataire. Si l'OC ne corrige pas dans les délais attendus, alors l'OI peut effectuer la correction lui-même.

Cas 2 : "Malfaçon Critique" ou "Malfaçon non imputable" à un seul OC : la reprise est effectuée par l'OI

Dans ces deux sous-cas ci-dessous, l'OI corrige la malfaçon lui-même :

Sous-Cas 2.1 : Malfaçon critique : il peut s'agir d'une signalisation imputable ou non imputable à un seul OC. C'est alors une notification à l'OC (ou aux OC) n'appelant pas action de sa/leur part car la reprise sera effectuée par l'OI compte-tenu de son aspect critique (c'est-à-dire pouvant présenter un danger grave et imminent pour les personnes et entrainer la responsabilité de l'OI à ce titre). L'aspect "Critique" de la malfaçon doit alors être conforme aux travaux Interop.

Sous-Cas 2.2 : Malfaçon non imputable à un seul OC et non critique : c'est alors une notification à l'ensemble des OC concernés n'appelant pas d'action de leur part car la reprise sera effectuée par l'OI

2. De l'OC vers l'OI :

L'OC informe l'OI d’une malfaçon/ dégradation constatée sur le terrain responsable. L'OC a l'origine de la remontée initiale ne suit pas le cycle de vie de la malfaçon et ne sera pas informé de la reprise de la malfaçon qu'il a signalée. La signalisation de la malfaçon par un OC vers un OI est une remontée d'information qui n'implique pas d'engagement de l'OC sur son niveau de précision : cette signalisation constitue une information complémentaire pour l'OI dans le cadre de l'exploitation de son réseau.

Documentation du protocole disponible ici : [Protocoles-SAV](https://www.interop-fibre.fr/les-protocoles-sav)
