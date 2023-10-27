# RechercheCharcrede
Bonjour Wilgas ADJOVI,

Pour installer Inertia dans votre projet Laravel, vous pouvez suivre les étapes suivantes:

1. Tout d'abord, vous devez installer Inertia en utilisant Composer. Vous pouvez le faire en exécutant la commande suivante dans votre terminal:

   composer require inertiajs/inertia-laravel

2. Ensuite, vous devez publier les fichiers de configuration d'Inertia en exécutant la commande suivante:

   php artisan vendor:publish --tag=inertia-config

3. Vous devez également publier les fichiers d'Inertia.js en exécutant la commande suivante:

   php artisan vendor:publish --tag=inertia-assets

4. Ensuite, vous devez ajouter le middleware Inertia à votre application Laravel en modifiant le fichier app/Http/Kernel.php. Ajoutez la ligne suivante au tableau de middleware:

   \App\Http\Middleware\HandleInertiaRequests::class

5. Enfin, vous pouvez créer une page d'accueil pour votre application en utilisant Inertia. Pour ce faire, créez un nouveau contrôleur en utilisant la commande suivante:

   php artisan make:controller HomeController

   Dans le fichier HomeController.php, ajoutez la méthode suivante:

   public function index()
   {
       return inertia('Home');
   }

   Cette méthode renvoie la vue 'Home' en utilisant Inertia. Vous pouvez ensuite créer la vue Home.vue dans le dossier resources/js/Pages en utilisant le template fourni par Inertia.

J'espère que cela vous aidera. N'hésitez pas à me poser d'autres questions si vous en avez besoin.

