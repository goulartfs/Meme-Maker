PHP-Projekt
===========

Slutprojekt i Webbutveckling i PHP. En meme-generator - ett system där användaren kan välja en bild, eller ladda upp en, för att sedan skriva en text över den.
Den ska sedan gå att dela den genererade bilden på sociala medier. Även ett internt topplistesystem skall finnas.

Användarfallen finns beskrivna i dokumentet "Use Cases.md".


# Meme Maker!
An awesome meme generator built on PHP. Includes member system, meme generation, image upload to IMGUR, and more.

Meme Maker! is tested on `PHP 5.5.14` and requires `cURL`. Released under the [MIT license](LICENSE).

## Installation
You need to generate a API-key from [IMGUR](https://api.imgur.com) (Example key that you can use: 497c18f153a4d3e) and
edit `Settings.php`:

```php
<?php
  class Settings {
  	public static $DB_USERNAME = "YOUR DB USERNAME";
  	public static $DB_PASSWORD = "YOUR DB PASSWORD";
  	public static $DB_CONNECTION = "mysql:host=localhost;dbname=YOUR DB NAME";
  	public static $IMGUR_CLIENTID = "IMGUR CLIENT ID";
    public static $ROOT_PATH = "/";
  }
?>
```

Don't forget to also upload the DB-backup that is contained in the `/DB-Backup/` folder.

The application is bundled with a [Vagrant-file](https://www.vagrantup.com). Just run `vagrant up` and it should work.