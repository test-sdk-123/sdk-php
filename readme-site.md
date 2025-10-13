---
order: 0
title: Example.com PHP SDK
languages:
 - php
install: 'composer require test123test234/sdk-php'
version: 1.0.4
github: 'https://'
packageManagerUrl: ''
---
# Example.com PHP SDK

## Overview

This is an **example** API to demonstrate features of the OpenAPI specification. # Introduction This API definition is intended to to be a good starting point for describing your API in [OpenAPI/Swagger format](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.2.md). It also demonstrates features of the [create-openapi-repo](https://github.com/Redocly/create-openapi-repo) tool and the [Redoc](https://github.com/Redocly/Redoc) documentation engine. Beyond the standard OpenAPI syntax, we use a few  [vendor extensions](https://github.com/Redocly/Redoc/blob/master/docs/redoc-vendor-extensions.md). # OpenAPI Specification The goal of The OpenAPI Specification is to define a standard, language-agnostic interface to REST APIs which allows both humans and computers to discover and understand the capabilities of the service without access to source code, documentation, or through network traffic inspection. When properly defined via OpenAPI, a consumer can  understand and interact with the remote service with a minimal amount of implementation logic. Similar to what interfaces have done for lower-level programming, OpenAPI removes the guesswork in calling the service.

## Installation

```bash
composer require test123test234/sdk-php
```

## Configuration

```php
<?php
require_once('vendor/autoload.php');

use OpenAPI\Client\Configuration;
use OpenAPI\Client\Api\BrandsApi;

// Create configuration with API key
$config = Configuration::getDefaultConfiguration()
    ->setApiKey('api-key', 'your_api_key_here');

// Create API client
$apiInstance = new BrandsApi(
    new GuzzleHttp\Client(),
    $config
);
```

## Example Request

```php
// Get brand data by domain
try {
    $domainRequest = new OpenAPI\Client\Model\DomainRequest([
        'domain' => 'example.com'
    ]);
    
    $response = $apiInstance->byDomain($domainRequest);
    
    // Access brand data
    echo "Brand: " . $response->getBrand()->getName() . "\n";
    echo "Logo: " . $response->getImages()->getLogos()[0]->getUrl() . "\n";
    echo "Primary Color: " . $response->getColors()->getPrimary()[0]->getHex() . "\n";
} catch (Exception $e) {
    echo 'Exception: ', $e->getMessage(), PHP_EOL;
}
```

## API Endpoints

Class | Method | Description
------------ | ------------- | -------------
*EchoApi* | **callEcho** | Echo test


## Models

List of available API Models

[Example.com Models](http://localhost:4321/docs/api-docs/models)

## Authentication

Authentication schemes defined for the API:

[Example.com Authentication Documentation](http://localhost:4321/docs/authentication)


### api_key

- **Type**: API key
- **API key parameter name**: api_key
- **Location**: HTTP header

