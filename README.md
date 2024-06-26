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

### Generate

```PHP
$data = [
    'user_id' => 123,
    'username' => 'john_doe',
];

// $jwt->validate(Algotithm , token)
$token = $jwt->generate('sha256', $data);

echo "Generated JWT: $token\n";
```

### decoding

```PHP
// Provide the algorithm and the JWT token to decode
[$header, $payload, $signature] = $jwt->decode('sha256', $token);

echo "Decoded Header: $header\n";
echo "Decoded Payload: $payload\n";
echo "Decoded Signature: $signature\n";
```

### Validate

```PHP

$validation_result = $jwt->validate('sha256', $token);

echo "Validation Result: $validation_result\n";
```
