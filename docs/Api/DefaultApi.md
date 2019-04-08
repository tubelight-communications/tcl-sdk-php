# OpenAPI\Client\DefaultApi

All URIs are relative to *http://https://eecd2b1a.ap.ngrok.io/api/internal*

Method | HTTP request | Description
------------- | ------------- | -------------
[**leadsGet**](DefaultApi.md#leadsGet) | **GET** /leads | Fetch lead info
[**leadsPost**](DefaultApi.md#leadsPost) | **POST** /leads | collect lead data


# **leadsGet**
> \OpenAPI\Client\Model\InlineResponse200[] leadsGet($format, $lead_id)

Fetch lead info

gets lead info from DB

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$format = 'json'; // string | format query
$lead_id = 3.4; // float | lead id of the lead to be found

try {
    $result = $apiInstance->leadsGet($format, $lead_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->leadsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **format** | **string**| format query | [optional] [default to &#39;json&#39;]
 **lead_id** | **float**| lead id of the lead to be found | [optional]

### Return type

[**\OpenAPI\Client\Model\InlineResponse200[]**](../Model/InlineResponse200.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json; charset=utf-8, application/xml; charset=utf-8, text/html; charset=utf-8, application/csv; charset=utf-8, text/html; charset=UTF-8, text/plain; charset=utf-8, application/vnd.php.serialized; charset=utf-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **leadsPost**
> leadsPost($inline_object)

collect lead data

this api collects lead data

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$inline_object = new \OpenAPI\Client\Model\InlineObject(); // \OpenAPI\Client\Model\InlineObject | 

try {
    $apiInstance->leadsPost($inline_object);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->leadsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inline_object** | [**\OpenAPI\Client\Model\InlineObject**](../Model/InlineObject.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json; charset=utf-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

