# Benhamida Oumaima , Master 1 Biochimie Appliquée , 10/12/2025
#Liste des membres de l'équipe :
#Benhamida Oumaima
#Benmeddah Wissam 
#Benslimane Hind Ahlam 
#Benyahia Chahinez
#Cherf Yousra 
import pandas as pd

#Données : Séquences ADN , longueur , Pourcentages de GC
data = { 
     "Séquence" : ["ATGCGTACGTA" , "GCTAGCTAGGCC" , "ATGCGCGTAAGT" , "TACGATCGTA" , "ATGAAAGGCTT" , "CGTACGTAGC" , "TTAACCGGAT"] ,
     "longueur" : [11, 12, 12, 10, 11, 10, 10] ,
     "Pourcentages GC" : [50, 66.67, 58.33, 40, 45.45, 60, 50]
}

#Création d'un DataFrame (tableau pandas)
#1)Créer et afficher le tableau en utilisant la bibliothèque pandas
df = pd.DataFrame(data)
print("**************** Création et affichage ****************")

# Affichage du tableau
print(Tableau des séquence ADN:")
print(df,"\n\n")





