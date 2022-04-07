# Charte de programmation SQL-Server 
## Introduction
La convention de nommage utilisée pour SQL-Server se base sur la base de données AdventureWorks fournie par Microsoft®.

## Langue
La langue choisie pour nommer l'ensemble des éléments de la base de données est le Français. Ce choix a été effectué dans le but de simplifier la lecture entre les développeurs. Les accents ne seront pas spécifiés lors de l'écriture des champs.

## Nommage
### Base de données
La base de données est nommée en Pascal Case.
> SaisieDesTemps

### Table
Les tables sont nommées en Pascal Case, au singulier.
> Utilisateur 

### Colonne
Les colonnes sont nommées en Pascal Case au singulier.
> Prenom 

### Clés
1. Les clés primaires  
   La clé primaire se nomme : NomTableID
   > UtilisateurID  

   La contrainte s'écrit : PK_NomTable_NomColonne  
   > PK_Utilisateur_UtilisateurID

2. Les clés étrangères  
   La clé étrangère se nomme : NomTableID
   > RoleID 
   
   La contrainte s'écrit : FK_NomTable_NomTableOrigine_NomColonne
   > FK_Utilisateur_Role_RoleID
3. Les clés alternatives (clé unique)  
   La clé unique se nomme : NomColonne 
   > Email 

   La contrainte s'écrit : AK_NomTable_NomColonne
   > AK_Utilisateur_Email

### Procédure Stockée
Les procédures stockées sont nommées avec le préfixe : usp (User-defined Stored Procedures) en Pascal Case.  
> uspCalculerAbsences 

### Fonction 
Les fonctions sont nommées avec le préfixe : ufn (User-defined Functions) en Pascal Case.  
> ufnRecupereStock 

### Vue 
Les vues sont nommées avec le préfixe : v en minuscule puis avec un nom en Pascal Case.  
> vProduitEtDescription
