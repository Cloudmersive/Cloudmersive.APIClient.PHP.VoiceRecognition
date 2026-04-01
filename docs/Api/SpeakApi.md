# Swagger\Client\SpeakApi

All URIs are relative to *https://testapi.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**speechSpeakTextVoiceBasicAudioPost**](SpeakApi.md#speechSpeakTextVoiceBasicAudioPost) | **POST** /speech/speak/text/voice/basic/audio | Generate audio from text using Advanced AI


# **speechSpeakTextVoiceBasicAudioPost**
> string speechSpeakTextVoiceBasicAudioPost($body)

Generate audio from text using Advanced AI

Converts text to speech using advanced AI. Supports English, Spanish, French, Hindi, Italian, Japanese, Portuguese, and Chinese. Specify language with LanguageCode (ISO 639-3, default: eng) and gender with Gender (Male or Female, default: Female). Output format is controlled by the Format field (mp3 or wav, default: mp3). Consumes 1 API call per second of generated audio.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\SpeakApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\TextToSpeechRequest(); // \Swagger\Client\Model\TextToSpeechRequest | String input request

try {
    $result = $apiInstance->speechSpeakTextVoiceBasicAudioPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SpeakApi->speechSpeakTextVoiceBasicAudioPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\TextToSpeechRequest**](../Model/TextToSpeechRequest.md)| String input request | [optional]

### Return type

**string**

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: application/octet-stream

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

