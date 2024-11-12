## PHP Configure Cloudinary

This is a simple PHP project that demonstrates how to configure and use Cloudinary for image management. The program loads Cloudinary credentials from a .env file, generates an image tag with specified transformations, and outputs it to the browser.


### Prerequisites

* PHP (version 7.4 or higher recommended)
* Composer for dependency management
* A Cloudinary account (you can sign up here if you don’t have one)


### Installation

1. Clone the repository:
    ```
    git clone https://github.com/cloudinary-devs/php_credentials.git
    cd php_credentials
    ```

2. Install dependencies: <p>Run the following command to install PHP dependencies using Composer:</p>
    ```
    composer install
    ```

3. Set up environment variables:
    * Create a .env file in the root of your project.
    * Add your Cloudinary URL (from the [API Keys](https://console.cloudinary.com/settings/api-keys) page in the Console Settings) in the `.env` file like this:
        ```
        CLOUDINARY_URL=cloudinary://API_KEY:API_SECRET@CLOUD_NAME
        ```

4. This project uses `vlucas/phpdotenv` to load environment variables, so make sure your `.env` file is in the same directory as your PHP file.

### Usage

1. Start a local server: You can use the built-in PHP server to serve the file:
    ```
    php -S localhost:8000
    ```

2. Access the program: Open your browser and go to `http://localhost:8000` to see the output, which will display a Cloudinary image with specified transformations.

### Code Explanation

* **Dotenv**: This project uses `vlucas/phpdotenv` to load environment variables from a `.env` file.
* **Cloudinary PHP SDK**: The code configures Cloudinary using credentials from `.env` and generates an image tag with a transformation (resizing to 400px width).
* **Image transformation**: The example includes a resize transformation for the sample image using Resize::scale().

### Example Output

The program will display the following HTML image tag:

```
<img src="https://res.cloudinary.com/my-shop/image/upload/c_scale,w_400/cld-sample">
```

### Dependencies

* `vlucas/phpdotenv` for environment variable management
* Cloudinary PHP SDK for managing Cloudinary assets

### License

This project is licensed under the MIT License.
