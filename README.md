# PHP JWT Class

This PHP class provides functionality for generating, validating, and decoding JSON Web Tokens (JWT).

## Usage

### Installation

Simply include the `myjwt.php` file in your PHP project.

### Instantiation

```php
// Include the class file
include 'myjwt.php';

// Instantiate the class with your secret key
$jwt = new MyJWT('your_secret_key_here');
```

### Examples

```PHP
// Define the payload data
$data = [
    'user_id' => 123,
    'username' => 'john_doe',
    // Add more claims as needed
];

// Generate the JWT
$token = $jwt->generate('HS256', $data);

echo "Generated JWT: $token\n";
```
