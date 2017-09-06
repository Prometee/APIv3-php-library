# Swagger\Client\TransactionalSMSApi

All URIs are relative to *https://api.sendinblue.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getSmsEvents**](TransactionalSMSApi.md#getSmsEvents) | **GET** /transactionalSMS/statistics/events | Get all the SMS activity (unaggregated events)
[**getTransacAggregatedSmsReport**](TransactionalSMSApi.md#getTransacAggregatedSmsReport) | **GET** /transactionalSMS/statistics/aggregatedReport | Get your SMS activity aggregated over a period of time
[**getTransacSmsReport**](TransactionalSMSApi.md#getTransacSmsReport) | **GET** /transactionalSMS/statistics/reports | Get your SMS activity aggregated per day
[**sendTransacSms**](TransactionalSMSApi.md#sendTransacSms) | **POST** /transactionalSMS/sms | Send the SMS campaign to the specified mobile number


# **getSmsEvents**
> \Swagger\Client\Model\GetSmsEventReport getSmsEvents($limit, $startDate, $endDate, $offset, $days, $phoneNumber, $event, $tags)

Get all the SMS activity (unaggregated events)

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');

$api_instance = new Swagger\Client\Api\TransactionalSMSApi();
$limit = 50; // int | Number of documents per page
$startDate = new \DateTime("2013-10-20"); // \DateTime | Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report
$endDate = new \DateTime("2013-10-20"); // \DateTime | Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report
$offset = 0; // int | Index of the first document of the page
$days = 56; // int | Number of days in the past including today (positive integer). Not compatible with 'startDate' and 'endDate'
$phoneNumber = "phoneNumber_example"; // string | Filter the report for a specific phone number
$event = "event_example"; // string | Filter the report for specific events
$tags = "tags_example"; // string | Filter the report for specific tags passed as a serialized urlencoded array

try {
    $result = $api_instance->getSmsEvents($limit, $startDate, $endDate, $offset, $days, $phoneNumber, $event, $tags);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionalSMSApi->getSmsEvents: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Number of documents per page | [optional] [default to 50]
 **startDate** | **\DateTime**| Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report | [optional]
 **endDate** | **\DateTime**| Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report | [optional]
 **offset** | **int**| Index of the first document of the page | [optional] [default to 0]
 **days** | **int**| Number of days in the past including today (positive integer). Not compatible with &#39;startDate&#39; and &#39;endDate&#39; | [optional]
 **phoneNumber** | **string**| Filter the report for a specific phone number | [optional]
 **event** | **string**| Filter the report for specific events | [optional]
 **tags** | **string**| Filter the report for specific tags passed as a serialized urlencoded array | [optional]

### Return type

[**\Swagger\Client\Model\GetSmsEventReport**](../Model/GetSmsEventReport.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTransacAggregatedSmsReport**
> \Swagger\Client\Model\GetTransacAggregatedSmsReport getTransacAggregatedSmsReport($startDate, $endDate, $days, $tag)

Get your SMS activity aggregated over a period of time

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');

$api_instance = new Swagger\Client\Api\TransactionalSMSApi();
$startDate = new \DateTime("2013-10-20"); // \DateTime | Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report
$endDate = new \DateTime("2013-10-20"); // \DateTime | Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report
$days = 56; // int | Number of days in the past including today (positive integer). Not compatible with startDate and endDate
$tag = "tag_example"; // string | Filter on a tag

try {
    $result = $api_instance->getTransacAggregatedSmsReport($startDate, $endDate, $days, $tag);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionalSMSApi->getTransacAggregatedSmsReport: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **startDate** | **\DateTime**| Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report | [optional]
 **endDate** | **\DateTime**| Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report | [optional]
 **days** | **int**| Number of days in the past including today (positive integer). Not compatible with startDate and endDate | [optional]
 **tag** | **string**| Filter on a tag | [optional]

### Return type

[**\Swagger\Client\Model\GetTransacAggregatedSmsReport**](../Model/GetTransacAggregatedSmsReport.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTransacSmsReport**
> \Swagger\Client\Model\GetTransacSmsReport getTransacSmsReport($startDate, $endDate, $days, $tag)

Get your SMS activity aggregated per day

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');

$api_instance = new Swagger\Client\Api\TransactionalSMSApi();
$startDate = new \DateTime("2013-10-20"); // \DateTime | Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report
$endDate = new \DateTime("2013-10-20"); // \DateTime | Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report
$days = 56; // int | Number of days in the past including today (positive integer). Not compatible with 'startDate' and 'endDate'
$tag = "tag_example"; // string | Filter on a tag

try {
    $result = $api_instance->getTransacSmsReport($startDate, $endDate, $days, $tag);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionalSMSApi->getTransacSmsReport: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **startDate** | **\DateTime**| Mandatory if endDate is used. Starting date (YYYY-MM-DD) of the report | [optional]
 **endDate** | **\DateTime**| Mandatory if startDate is used. Ending date (YYYY-MM-DD) of the report | [optional]
 **days** | **int**| Number of days in the past including today (positive integer). Not compatible with &#39;startDate&#39; and &#39;endDate&#39; | [optional]
 **tag** | **string**| Filter on a tag | [optional]

### Return type

[**\Swagger\Client\Model\GetTransacSmsReport**](../Model/GetTransacSmsReport.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **sendTransacSms**
> \Swagger\Client\Model\SendSms sendTransacSms($sendTransacSms)

Send the SMS campaign to the specified mobile number

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');

$api_instance = new Swagger\Client\Api\TransactionalSMSApi();
$sendTransacSms = new \Swagger\Client\Model\SendTransacSms(); // \Swagger\Client\Model\SendTransacSms | Values to send a transactional SMS

try {
    $result = $api_instance->sendTransacSms($sendTransacSms);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TransactionalSMSApi->sendTransacSms: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sendTransacSms** | [**\Swagger\Client\Model\SendTransacSms**](../Model/SendTransacSms.md)| Values to send a transactional SMS |

### Return type

[**\Swagger\Client\Model\SendSms**](../Model/SendSms.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)
