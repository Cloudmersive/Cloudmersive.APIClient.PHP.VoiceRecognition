# cloudmersive_voicerecognition_api_client
Speech APIs enable you to recognize speech and convert it to text using advanced machine learning, and also to convert text to speech.

[Cloudmersive Speech API](https://www.cloudmersive.com/voice-recognition-and-speech-api) provides advanced voice recognition and text to speech capabilities

- API version: v1
- Package version: 1.5.0


## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/cloudmersive/cloudmersive_voicerecognition_api_client.git"
    }
  ],
  "require": {
    "cloudmersive/cloudmersive_voicerecognition_api_client": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/cloudmersive_voicerecognition_api_client/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\RecognizeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$language_code = ""; // string | ISO 639-3 three-letter language code (e.g. eng, spa, fra). Empty for auto-detect.
$recognition_mode = "Normal"; // string | Recognition mode: Fast, Normal (default), or Advanced. Advanced is only available on Private Cloud and Managed Instance deployments.
$speech_file = "/path/to/file.txt"; // \SplFileObject | 

try {
    $result = $apiInstance->speechRecognizeFilePost($language_code, $recognition_mode, $speech_file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecognizeApi->speechRecognizeFilePost: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://testapi.cloudmersive.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*RecognizeApi* | [**speechRecognizeFilePost**](docs/Api/RecognizeApi.md#speechrecognizefilepost) | **POST** /speech/recognize/file | Recognize audio input as text using Advanced AI
*SpeakApi* | [**speechSpeakTextVoiceBasicAudioPost**](docs/Api/SpeakApi.md#speechspeaktextvoicebasicaudiopost) | **POST** /speech/speak/text/voice/basic/audio | Generate audio from text using Advanced AI


## Documentation For Models

 - [SpeechRecognitionResult](docs/Model/SpeechRecognitionResult.md)
 - [TextToSpeechRequest](docs/Model/TextToSpeechRequest.md)
 - [TokenTimestamp](docs/Model/TokenTimestamp.md)


## Documentation For Authorization


## Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header


## Author




