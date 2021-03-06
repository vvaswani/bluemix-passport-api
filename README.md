# User Authentication and Management Example

This repository accompanies the [IBM developerWorks article](https://www.ibm.com/developerworks/cloud/library/cl-bluemix-manage-authenticate-users-php-passport-1/index.html). It's built with PHP, Slim 3.x and Bootstrap. It delivers an example application that uses a hosted Passport service instance on Bluemix for user authentication and user account management. 

The steps below assume that a Passport service instance has been instantiated via the the Bluemix console. For details, refer to the [accompanying article on IBM developerWorks](https://www.ibm.com/developerworks/cloud/library/cl-bluemix-manage-authenticate-users-php-passport-1/index.html).

To deploy this application to your local development environment:

 * Clone the repository to your local system.
 * Run `composer update` to install all dependencies.
 * Create `config.php` with credentials for the Passport service. Use `config.php.sample` as an example.
 * (optional) Define a virtual host pointing to the `public` directory, as described in the article.
 
To deploy this application to your Bluemix space:

 * Clone the repository to your local system.
 * Create `manifest.yml` with your custom hostname. Use `manifest.yml.sample` as an example.
 * Push the application to Bluemix and bind the Passport service to it, as described in the article.
 * Define the application ID as an environment variable for your Bluemix application, as described in the article.
 
## Application routes

 * `/home` - Public page, accessible to all
 * `/account` - Private page, accessible to logged-in users only
 * `/login` - Login page
 * `/logout` - Logout page
 * `/password-request` - Password recovery page
 * `/password-reset` - Password reset page
 * `/admin/users/index` - User list
 * `/admin/users/save` - User creation/modification form
 * `/admin/users/delete` - User deletion page
 * `/admin/users/activate/UID` - User activation page
 * `/admin/users/deactivate/UID` - User deactivation page
 * `/members/gold` - Private page, restricted to users with role "member-gold" 
 * `/members/silver` - Private page, restricted to users with role "member-silver" 
