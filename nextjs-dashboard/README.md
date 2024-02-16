## cours

Next. Js : 
    · est un Framework pour React
fait par vercel

Js => coté client 

Server side rendering ( SSR ) ( la création => rendering) : 
    · Permet le rendu coté serveur des pages web , améliore la performance et le SEO 

React est la création coté web 

Static site generation (SSG) :   
    · Pour une vitesse de chargement rapide 
    
Type script c'est un surcouche de javascript 
Typer les paramètre les variables  
Plus rebuter au moment du dev


Tailwind : ensemble de classe qui évite d'écrire de css / ca genere du css


Tous les component react sont présenter coté 

Fichier layout.tsx :   Il y a 

Children c'est la props 

Layout structure identique à tous les page 

Layout c'est un component 
Affichier les pages de site global 

import '@/app/ui/global.css';
Le @ est la racine de notre projet 


Cascade :  fait référence à une séquence de requêtes réseau qui dépendent de la réalisation des requêtes précédentes. Dans le cas de la récupération de données, chaque requête ne peut commencer qu'une fois que la requête précédente a renvoyé des données.

le rendu statique :  la récupération et le rendu des données se produisent sur le serveur au moment de la construction (lors du déploiement)

Le rendu statique présente quelques avantages :

Sites Web plus rapides :  Cela garantit que les utilisateurs du monde entier peuvent accéder au contenu de votre site Web de manière plus rapide et plus fiable.
Charge de serveur réduite : le contenu étant mis en cache, votre serveur n'a pas besoin de générer dynamiquement du contenu pour chaque demande utilisateur.
SEO – Le contenu pré-rendu est plus facile à indexer pour les robots des moteurs de recherche, car le contenu est déjà disponible lors du chargement de la page. Cela peut conduire à un meilleur classement dans les moteurs de recherche.


le rendu dynamique : le contenu est rendu sur le serveur pour chaque utilisateur au moment de la demande (lorsque l'utilisateur visite la page)


Partial Prerendering : une fonctionnalité expérimentale qui vous permet de restituer un itinéraire avec un shell de chargement statiqu


    - Les rôles des dossier :  de définir les route de l'application 
        ○ Les dossier pour définir les route 
        ○ Tous les dossier dans app c'est pour définir le route

Image

        
    - Une route est un enchainement de dossier imbriqués 
    - Les rôles des fichier : c'est de définir le contenu de la page 
    - Next fournit toute une liste de dossier et de fichier pour définir les routes de l'application 
    
Image 1 


    - Pour créer une router imbriquée :  il suffit d'imbriquer les dossier 
        ○ Par exemple : créer une route/about, il suffit de créer un dossier about dans le dossier app et de créer le component 'route.tsx' dans ce dossier 
    - Routing : page et layout 
        ○ Une page c'est l'UI associé à une route. Dans le code on le présente par un composent React par un fichier appelé 'route.tsx'
    
    
Image 2



    - Par défaut toutes les page =s des composent serveur , il faut utiliser 'use client' pour les rendre des composents client 
    - Layout : 
        ○ Est une partie d'UI partagés entre plusieurs pages, 
        ○ Exemple : un header, un footer, une sidebar 
        ○ Son but est de préservé chaque chargement de page 
    - Comme les pages on peut imbriquer des layouts 
        ○ Exemple : un layout peut contenir un autre layout 
        
        
Image 3 


    - Pour créer un layout, il sufit de créer un composent react exporté par un fichier appelé 'layout.tsx'
    - Le root layout est obligatoire , doit contenir les tags : 'html' 'body' 
    - Possible de créer un layout pour un groupe de pages 


Imbriquer des layout:


Image 4


Grouper des routes : 'Route Groups'

    - A l'intérieur du répertoire on peut mapper l'imbrication des dossier sur les routes de l'application. Il est possible de créer des dossier spéciaux qui seront ignorés par le routing next 

    - Tous les dossier dans des (  )    => Ignorer dans la construction de l'URL  


Image 5

Image 6 

Ou encore plusiuers root layout

Image 7



Routes dynamique :

    - Pour créer une route dynamique , il suffit de créer un dossier dont le nom est enre crochets
    - Exemple [id] cette info sera passée a la props 'params'  des fonction : page , route , layout et generateMetadata

Image 9 

Code

Le segment de route dynamique ' catch-all'

    - On peut rendre dynamique le nombre de paramètre au sein d'une route dynamique, pour cela il faut précéder le nom de la route dynamique par '…'


Image 10

Routing : Navigation 

Il existe 4 méthode pour naviguer entre les pages :
    - Link : composent 
    - useRouter : hook
    - Redirect : fonction 
    - L'API  History 


Link :
    - Est un composent fournit par Next qui est en réalité un wrapper autour de la balise html 
    - Il permet de naviger entre les pages sans recharger la pages 


Code 


Le hook usePathname

    - Permet de récupérer le pathname de la page courante. Il permet par exemple de mettre en surbrillance de la page courante 
    - Pour utiliser un hook au sein d'un composent Next i faut utiliser la directive use client 
    - Pour connaitre la route courante 


Le  hook useRouter 

    - Permet de changer par le code la route courante de l'application. Il permet aussi de récupérer les paramètre de la route courante 

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

    - Les actions React Server vous permettent d'exécuter du code asynchrone directement sur le serveur. 







 







