# Benhamida Oumaima , Master 1 Biochimie Appliquée , 10/12/2025
#Liste des membres de l'équipe :
#Benhamida Oumaima
#Benmeddah Wissam 
#Benslimane Hind Ahlam 
#Benyahia Chahinez
#Cherf Yousra 
import pandas as pd

# Données : Séquences ADN , longueur , Pourcentages de GC
data = { 
     "Séquence" : ["ATGCGTACGTA" , "GCTAGCTAGGCC" , "ATGCGCGTAAGT" , "TACGATCGTA" , "ATGAAAGGCTT" , "CGTACGTAGC" , "TTAACCGGAT"] ,
     "longueur" : [11, 12, 12, 10, 11, 10, 10] ,
     "Pourcentages GC" : [50, 66.67, 58.33, 40, 45.45, 60, 50]
}

# 1)Créer et afficher le tableau en utilisant la bibliothèque pandas 
#Création d'un DataFrame (tableau pandas)
df = pd.DataFrame(data)
print("**************** Création et affichage ****************")

#Affichage du tableau
print(Tableau des séquence ADN:")
print(df,"\n\n") 

# Opérations sur le tableau :
# 2)Sélectionner et Afficher uniquement la colonne "longueur"
print("**************** Colonne longueur ****************")
#Sélectionner et afficher uniquement la colonne "longueur" 
print(df["longueur"])
print("\n\n")

# 3)Filtrer les séquences dont la longueur est supérieure à 10
print("**************** Filtrage avec longueur "****************")
#Filtrer les séquences dont la lonugeur est supérieur à 10
filtre = df[df["longueur"] > 10]
print(filtre,"\n\n")


# 4) Calculer le Pourcentage moyen de GC
print("**************** Calcul de Pourcentage moyen de GC ****************")
#Calculer le Pourcentage moyen de GC avec 3 chiffres après la virgule 
average_GC = df["Pourcentages GC"] .mean()
print (f"Pourcentages moyen de GC : {average_GC:.3f}%")

# 5) Ajouter une nouvelle colonne avec des calculs 
print("**************** Ajout d'une nouvelle colonne ****************")
#Ajouter une nouvelle colonne"Catégorie GC"
df["Catégorie GC"] = df["Pourcentages GC"].apply(lambda x:"Riche" if x >55 else "Moyen" if 45 <= x <= 55 else "faible")
print(df,"\n\n")

# 6) Ajouter une colonne comptant les 'G'
print (**************** Ajout d'une colonne comptant les 'G' ****************) 
#Ajouer une colonne donnant le nombre de 'G' dans chaque séquance 
df["nombre de G"] = df ["séquence"].str.count("G")

print("=================== Nombre de G ajoutés ===================")
print(df,"\n")

# 7) calculer l'écart-type du %GC et la longueurdes séquence
print(*************** écart-type des donnés ***************)
#calculer l'écart-type pour la colonne "porcentages GC" et la colonne "longueur"
std_GC = df["porcentages GC"].std()
std_longueur = df["longueur"].std()

print(f"écart-type de GC: {std_GC: .3f}")
print(f"écart-type de la longueur: {std_longueur: .3f}")
print("\n\n")

# 8)Sauvegarder le DataFrame dans un fichier CSV
print("****************Sauvgarde et chargement des données avec pandas****************")
#Sauvgarder le DataFrame dans un fichier csv
nom_fichier="BenhamidaOumaima_M1_BA"df.to_csv(BenhamidaOumaima_M1_B1.csv",index=False)

print(f"le tableau final a été sauvegardé dans le fichier:{nom de fichier}")
print("\n\n")

