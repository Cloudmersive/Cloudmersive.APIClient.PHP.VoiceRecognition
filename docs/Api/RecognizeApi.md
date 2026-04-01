# Swagger\Client\RecognizeApi

All URIs are relative to *https://testapi.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**speechRecognizeFilePost**](RecognizeApi.md#speechRecognizeFilePost) | **POST** /speech/recognize/file | Recognize audio input as text using Advanced AI


# **speechRecognizeFilePost**
> \Swagger\Client\Model\SpeechRecognitionResult speechRecognizeFilePost($language_code, $recognition_mode, $speech_file)

Recognize audio input as text using Advanced AI

Uses advanced AI to convert input audio to text. Supports WAV, MP3, M4A, FLAC, OGG, and WMA formats. Consumes 1 API call per second of audio in Fast mode, 5 API calls per second in Normal mode, and 10 API calls per second in Advanced mode.

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

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **language_code** | **string**| ISO 639-3 three-letter language code (e.g. eng, spa, fra). Empty for auto-detect. | [optional] [default to ]
 **recognition_mode** | **string**| Recognition mode: Fast, Normal (default), or Advanced. Advanced is only available on Private Cloud and Managed Instance deployments. | [optional] [default to Normal]
 **speech_file** | **\SplFileObject**|  | [optional]

### Return type

[**\Swagger\Client\Model\SpeechRecognitionResult**](../Model/SpeechRecognitionResult.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

