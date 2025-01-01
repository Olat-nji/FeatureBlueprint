# Laravel Feature Blueprint  

**FeatureBlueprint** is a Laravel package designed to automate the creation of all necessary files and components required for a new feature. It streamlines the development process, enabling developers to quickly scaffold controllers, models, migrations, tests, and more with a single command.  

## Features  
- Automatically generates all essential files for a Laravel feature:
  - Controllers
  - Models
  - Migrations
  - Views
  - Routes
  - Tests
- Customizable templates to suit your coding standards.
- Seamless integration with Laravel's Artisan commands.
- Configurable options for fine-grained control over generated files.

---

## Installation  

Install the package via Composer:  

```bash
composer require your-vendor/feature-blueprint
```

If you want to install it globally for easier use across projects:  

```bash
composer global require your-vendor/feature-blueprint
```

---

## Configuration  

Publish the configuration file to customize templates:  

```bash
php artisan vendor:publish --tag=feature-blueprint-config
```

This will create a `feature-blueprint.php` file in the `config` directory where you can define defaults for file structures, naming conventions, and more.

---

## Usage  

Generate a new feature by running the following Artisan command:  

```bash
php artisan make:feature FeatureName
```

### Command Options:  
- `--with-tests`: Include test files.  
- `--no-migration`: Skip generating migration files.  
- `--api`: Scaffold feature files for an API structure.  

Example:  
```bash
php artisan make:feature BlogPost --with-tests --api
```

---

## Customizing Templates  

FeatureBlueprint allows you to customize the scaffolding templates. Publish the default templates with:  

```bash
php artisan vendor:publish --tag=feature-blueprint-templates
```

Modify the templates in the `resources/vendor/feature-blueprint` directory to match your project's coding standards.  

---

## Contributing  

Contributions are welcome! If you’d like to contribute, please fork the repository and submit a pull request. For major changes, please open an issue first to discuss what you’d like to change.  

---

## License  

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Support  

If you encounter any issues or have feature requests, please [open an issue](https://github.com/your-vendor/feature-blueprint/issues).  

---

### Example Workflow  

1. Run `php artisan make:feature UserManagement`.  
2. Review the generated files:
   - `app/Http/Controllers/UserManagementController.php`
   - `app/Models/UserManagement.php`
   - `database/migrations/xxxx_xx_xx_create_user_management_table.php`
   - `routes/user-management.php`
   - `tests/Feature/UserManagementTest.php`  
3. Customize the files as needed and start building your feature!  

--- 
