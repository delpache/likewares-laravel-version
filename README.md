# Package pour la gestion de version pour Laravel

Il s'agit d'un logiciel de gestion de versions compatible avec [SemVer] (http://semver.org) pour tout logiciel construit sur Laravel.

## Démarrer

### 1. Installation

Exécutez la commande suivante :

```bash
composer require likewares/laravel-version
```

### 2. Enregistrer (for Laravel < 5.5)

Enregistrer le fournisseur de services dans `config/app.php`.

```php
Likewares\Version\Provider::class,
```

Ajoutez un alias si vous souhaitez utiliser la facade.

```php
'Version' => Likewares\Version\Facade::class,
```

### 3. Publication

Publication du fichier de configuration.

```bash
php artisan vendor:publish --tag=version
```


### 4. Configuration

Vous pouvez changer les informations de version de votre application à partir du fichier `config/version.php`.

## Utilisation

### version($method = null)

Vous pouvez soit saisir la méthode comme `version('short')` soit la laisser vide afin de pouvoir d'abord obtenir l'instance puis appeler les méthodes comme `version()->short()`

## License

La licence MIT (MIT). Veuillez consulter [LICENSE](LICENSE.md) pour plus d'informations.
