# Swagger\Client\RecognizeApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**recognizeFile**](RecognizeApi.md#recognizeFile) | **POST** /speech/recognize/file | Recognize audio input as text using machine learning


# **recognizeFile**
> \Swagger\Client\Model\SpeechRecognitionResult recognizeFile($speech_file)

Recognize audio input as text using machine learning

Uses advanced machine learning to convert input audio, which can be mp3 or wav, into text.

### Example
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
$speech_file = "/path/to/file.txt"; // \SplFileObject | Speech file to perform the operation on.  Common file formats such as WAV, MP3 are supported.

try {
    $result = $apiInstance->recognizeFile($speech_file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecognizeApi->recognizeFile: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **speech_file** | **\SplFileObject**| Speech file to perform the operation on.  Common file formats such as WAV, MP3 are supported. |

### Return type

[**\Swagger\Client\Model\SpeechRecognitionResult**](../Model/SpeechRecognitionResult.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

