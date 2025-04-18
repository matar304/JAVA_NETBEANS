# MDMSchool

## Description

MDMSchool est un système de gestion scolaire basé sur Java, conçu pour gérer les informations des étudiants, les paiements et les états financiers. L'application utilise une base de données MySQL pour le stockage des données et fournit une interface graphique construite avec Java Swing.

## Technologies utilisées

- Java 21
- MySQL (avec MySQL Connector/J)
- Java Swing pour l'interface graphique
- Maven pour la gestion de la construction et des dépendances

## Fonctionnalités

- Gestion des étudiants : Ajouter, modifier, supprimer et rechercher des dossiers d'étudiants.
- Gestion des paiements : Gérer les dossiers de paiement, y compris l'ajout, la modification, la suppression et la recherche des paiements.
- Gestion des états financiers (impliquée par les noms des packages).
- Support d'impression pour les listes d'étudiants et de paiements via JTable.

## Structure du projet

- `src/main/java/com/mycompany/mdmschool/MDMSchool.java` : Point d'entrée principal (actuellement un placeholder).
- `src/main/java/dao/Connecte.java` : Gestion de la connexion à la base de données.
- `src/main/java/Controleur/` : Contient les classes contrôleurs pour la logique métier (ex. `controlEtudiant`, `controlPaiement`).
- `src/main/java/Model/` : Classes de modèle de données (ex. `TraitementEtudiant`, `TraitementPaiement`).
- `src/main/java/vue/` : Formulaires et classes GUI construits avec Java Swing.

## Prérequis

- Java Development Kit (JDK) 21
- Maven 3.x
- Serveur MySQL en fonctionnement local avec une base de données nommée `mdm`
- Utilisateur MySQL `root` sans mot de passe (ou modifier les paramètres de connexion dans `Connecte.java` en conséquence)

## Installation et compilation

1. Cloner le dépôt.
2. Assurer que le serveur MySQL est en fonctionnement et que la base de données `mdm` est créée.
3. Compiler le projet avec Maven :
   ```bash
   mvn clean package
   ```
4. Lancer l'application :
   ```bash
   mvn exec:java -Dexec.mainClass="com.mycompany.mdmschool.MDMSchool"
   ```

## Connexion à la base de données

L'application se connecte à la base de données MySQL avec les paramètres suivants (dans `Connecte.java`) :

- URL : `jdbc:mysql://localhost/mdm`
- Utilisateur : `root`
- Mot de passe : (vide)

Modifiez ces paramètres dans `src/main/java/dao/Connecte.java` si votre configuration de base de données est différente.

## Auteur

Matar Ndoye KEITA

## Licence

Ce projet est sous licence MIT (ou spécifiez si différente).
