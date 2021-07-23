# projet_2
## Description du projet :
Le projet consiste a développer une version bêta d’un système pour suivre les prix des livres chez Books to Scrape, un revendeur de livres en ligne.Dans cette version bêta, le programme n'effectuera pas une véritable surveillance en temps réel des prix sur la durée. Il s'agira simplement d'une application exécutable à la demande visant à récupérer les prix au moment de son exécution. 

### 1-Création et activation de l’environnement virtuel:
- ouvrir un terminal de commande (ex:powershell).
- A l’aide de la commande pwd trouver votre emplacement sur l’ordinateur.
- A l’aide de la commande cd placez vous dans le répertoire qui contient le projet.
- Taper la commande python -m venv nom (nom= choisissez un nom a donner à votre environnement. 
- Taper la commande .python\nom\Scripts\Activate.ps1 pour activer votre environnement virtuel.

### 2-Exécution du code de l’application :
- Le fichier requirements.txt nous indique les packages nécéssaire a voir avant l’exécution du code.
- Le programme se décompose en 6 modules :

- main.py :c’est le module principale sans lequel le programme ne fonctionne pas ,le main regroupe toute les commande nécéssaire a la bonne éxécution du programme.
- category_module.py:consiste a récuperer la liste de  en parsant le site https://books.toscrape.com/ grace a méthode get et requests et html parser.
- one_category_module.py:ce module récupere la liste des des urls de toutes les categories et exploite chaqu’une d’elle pour récupérer la liste de tous les urls de tous  livres et en prenant en compte la pagination.
- book_module.py:récupere le lien de chaque livre et extrait les données (product_page_url,universal_ product_code (upc),title,price_including_tax,price_excluding_tax,number_available,product_description,category,review_rating,image_url) 
- class_module.py :contien le scripte pour creer la class category en lui associant une url.
- io_module.py ;contien le scripte pour créer les fichiers csv ainsi que les dossiers ou sont sotockés les données 
Toutes les données extraite sont stocké dans un fichier csv pour chque categorie ainsi que les images de tous les livres de cette derniere.le tous est stocké dans un dossier qui porte le meme nom que la catégorie scrapé.


