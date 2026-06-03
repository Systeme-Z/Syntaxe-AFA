# Syntaxe-AFA


## Pourquoi AFA ?
**AFA = Architecture, Flux, Assembleur**

Les processeurs classiques (ARM, RISC-V, x86) sont conçus pour faire des calculs, exécuter des systèmes d'exploitation, gérer des millions de lignes de code.

Mais si tu veux juste :
- Lire la température d'une pièce
- Comparer avec un seuil
- Allumer un moteur ou une LED

…un processeur généraliste est trop complexe, trop lent (à cause du logiciel), et pas assez sûr.

**AFA fait exactement ça, sans couche logicielle.**

## À quoi ça sert ?

AFA est un **langage matériel** qui contrôle directement des capteurs et des actionneurs.

Avec AFA, tu écris un petit programme (un firmware) qui dit :

> *"Si la température dépasse 50°C, allume le moteur et la LED."*

Ce programme est converti en binaire et chargé dans un FPGA (une puce programmable). Le FPGA exécute ce programme **physiquement**, sans processeur, sans système d'exploitation, sans latence.

## Cas d'usage

- Surveillance de température avec alerte (LED / moteur)
- Contrôle de puissance (`%`)
- Détection de présence ou distance (`?`)
- Réaction à un changement brusque (`!`)
- Temporisation (`TP`)
- Boucle de surveillance (`&`)

## Pourquoi c'est mieux ?

| Problème des CPU classiques | Solution AFA |
|-----------------------------|--------------|
| Latence logicielle | Réaction physique immédiate |
| Bugs possibles dans le code | Rien entre ton firmware et le matériel |
| Vulnérabilités (failes logicielles) | Pas de logiciel = pas de faille |
| Complexité inutile | 15 instructions, pas plus |

## En résumé

> **AFA,  langage pour commander le monde physique. Sans processeur. Sans OS. Sans prise de tête.**



# Commande de base

| Symbole / Action

| 0V Mets à 0 volt

| 5V Mets à 5 volts

| >> Pointeur vers actionneur/capteur

| {} Bascule (stockage 1 bit / état)

| & Boucle infinie


# Comparateur

| Symbole / Action

| G Comparateur (égal)

| GD Comparateur (différent)


# capteur / entrée

| Symbole / Action

| * Température

| % Puissance (courant/tension)

| ? Radar / distance / présence

| ! Front (changement d’état)

| TP Temps (temporisation)


# Horloge / contrôle système

| Symbole / Action

| ~ Cycle d’horloge

| ON Démarrage / reset

| OOF Arrêt complet


# Syntaxe

0V 
5V 
>>
{}
&
G
GD
*
%
?
!
TP
~
ON
OOF

