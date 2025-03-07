# Geraldine_profil
Mon profil d'autodidacte en python et assimilé
- 👋 Hi, I’m Géraldine
- 👀 I'm a quality technician
- 📫 How to reach me: https://www.linkedin.com/in/geraldinecalletti/

  -------------------------------------------------

  ## Projet en cours
  Ce projet est actuellement en cours de développement. Vous pouvez le suivre sur le dépôt GitHub :  
  [https://github.com/superoroborus/blog_personnel](https://github.com/superoroborus/blog_personnel)

---

  ## Ressources en Français pour apprendre à coder en Python :

### cours de bases python openclassrooms:
 * https://openclassrooms.com/fr/courses/4366701-decouvrez-le-fonctionnement-des-algorithmes
 * https://openclassrooms.com/fr/courses/7168871-apprenez-les-bases-du-langage-python
 * https://openclassrooms.com/fr/courses/6951236-mettez-en-place-votre-environnement-python
 * https://openclassrooms.com/fr/courses/6204541-initiez-vous-a-python-pour-lanalyse-de-donnees
 * https://openclassrooms.com/fr/courses/7771531-decouvrez-les-librairies-python-pour-la-data-science
 * https://openclassrooms.com/fr/courses/7150616-apprenez-la-programmation-orientee-objet-avec-python

### Exercices : Projet Euler
 * https://www.lucaswillems.com/fr/articles/19/project-euler-traduction-des-problemes-1-a-50

### cours sur GIT openclassrooms:
 * https://openclassrooms.com/fr/courses/7162856-gerez-du-code-avec-git-et-github

### cours de la formation openclasrooms data-science :
 * https://github.com/loedata/FORMATION-DATA_SCIENTIST-OPENCLASSROOM/tree/main

### Très bon bootcamp
 * https://github.com/kevindegila/data-analyst
### en particulier les exercicies :
 * https://github.com/superoroborus/Geraldine_profil/blob/main/01_07_Exercices_sur_les_bases_de_python%20-%20reponse_geraldine.ipynb

 ## Ressources en Anglais pour apprendre à coder en Python :

### Principalement de l'apprentissage par le jeu :
* Learn to Code — For Free — Coding Courses for Busy People : https://www.freecodecamp.org/
* https://www.codewars.com/kata
* https://www.hackerrank.com/dashboard
* https://www.codingame.com/start/fr/

### Git permattant d'obtenir des certificats Gratuits sur plein de sujets différents :
* https://github.com/cloudcommunity/Free-Certifications

 -------------------------------------------------

 ## Exemple de petit projet pour extraire certains mails outlook :

### Instructions : 


https://nanonets.com/blog/export-outlook-emails-to-excel/
Directly exporting emails from Outlook to Excel is pretty easy, but this method will only retain plain text and basic links – all other formatting will be lost.

1. Open Outlook >> click on "File" >> and select "Open and Export"
2. Click on "Import/Export" >> select "Export to a file" >> and select Excel or csv as the file type
3. Select a destination folder to save the file in
4. Click "Finish"

Exit Outlook, open the folder and verify the Excel/csv file you just exported from Outlook.
vérifier que l'export se situe bien : C:/Users/callettige/Desktop/Projet-python/export-outlook/export_pv_diffuses.CSV"

Executer "search export pv diffuses" :
Appuyer sur le bouton : exécuter
Le fichier excel "fichier_search" doit apparaître.

Faire un filtre sur la première colonne avec le mot "final".
Le filtre permet d'enlever le décompte un peu génant.

Pour modifier le mot clés pour la recherche :
Faire un clic droit sur C:\Users\callettige\Desktop\Projet-python\export-outlook\search_export_pv_diffuses\search export pv diffuses
Vérifier que le code a bien les 2 ligne avec 'diffusion et passage T2', modifier si besoin.



------------------------------------------------------------------
 ## code source :

```# Importer le module tkinter pour créer une interface graphique
import tkinter as tk

# Créer une fonction qui exécute le code donné
def run_code():
    # Ouvrir le fichier CSV en mode lecture
    with open("ENTRER/LIEN/", 'r') as text_file:
        # Ouvrir le fichier de sortie en mode écriture
        sourceFile = open('fichier_search.csv', 'w')
        # Lire toutes les lignes du fichier CSV
        lines = text_file.readlines()
        # Initialiser un compteur
        count = 0
        # Parcourir chaque ligne du fichier CSV
        for line in lines:
            # Vérifier si la ligne contient la chaîne "diffusion et passage T2"
            if "diffusion et passage T2" in line:
                # Incrémenter le compteur
                count += 1
                # Afficher la ligne et le compteur dans le fichier de sortie
                print(line, f"diffusion et passage T2' {count} times.", file=sourceFile)
    # Fermer les fichiers
    text_file.close()
    sourceFile.close()

# Créer une fenêtre principale
window = tk.Tk()
# Donner un titre à la fenêtre
window.title("Interface python")
# Créer un bouton qui appelle la fonction run_code quand on clique dessus
button = tk.Button(window, text="Exécuter le code", command=run_code)
# Placer le bouton dans la fenêtre
button.pack()
# Lancer la boucle principale de la fenêtre
window.mainloop()
