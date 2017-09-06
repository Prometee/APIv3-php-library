# Swagger\Client\ListsApi

All URIs are relative to *https://api.sendinblue.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**addContactToList**](ListsApi.md#addContactToList) | **POST** /contacts/lists/{listId}/contacts/add | Add existing contacts to a list
[**createList**](ListsApi.md#createList) | **POST** /contacts/lists | Create a list
[**deleteList**](ListsApi.md#deleteList) | **DELETE** /contacts/lists/{listId} | Delete a list
[**getContactsFromList**](ListsApi.md#getContactsFromList) | **GET** /contacts/lists/{listId}/contacts | Get the contacts in a list
[**getFolderLists**](ListsApi.md#getFolderLists) | **GET** /contacts/folders/{folderId}/lists | Get the lists in a folder
[**getList**](ListsApi.md#getList) | **GET** /contacts/lists/{listId} | Get the details of a list
[**getLists**](ListsApi.md#getLists) | **GET** /contacts/lists | Get all the lists
[**removeContactToList**](ListsApi.md#removeContactToList) | **POST** /contacts/lists/{listId}/contacts/remove | Remove existing contacts from a list
[**updateList**](ListsApi.md#updateList) | **PUT** /contacts/lists/{listId} | Update a list


# **addContactToList**
> \Swagger\Client\Model\PostContactInfo addContactToList($listId, $contactEmails)

Add existing contacts to a list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');

$api_instance = new Swagger\Client\Api\ListsApi();
$listId = "listId_example"; // string | Id of the list
$contactEmails = new \Swagger\Client\Model\AddRemoveContactToList(); // \Swagger\Client\Model\AddRemoveContactToList | Emails addresses of the contacts

try {
    $result = $api_instance->addContactToList($listId, $contactEmails);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->addContactToList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **listId** | **string**| Id of the list |
 **contactEmails** | [**\Swagger\Client\Model\AddRemoveContactToList**](../Model/AddRemoveContactToList.md)| Emails addresses of the contacts |

### Return type

[**\Swagger\Client\Model\PostContactInfo**](../Model/PostContactInfo.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **createList**
> \Swagger\Client\Model\CreateModel createList($createList)

Create a list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');

$api_instance = new Swagger\Client\Api\ListsApi();
$createList = new \Swagger\Client\Model\CreateList(); // \Swagger\Client\Model\CreateList | Values to create a list

try {
    $result = $api_instance->createList($createList);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->createList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createList** | [**\Swagger\Client\Model\CreateList**](../Model/CreateList.md)| Values to create a list |

### Return type

[**\Swagger\Client\Model\CreateModel**](../Model/CreateModel.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteList**
> deleteList($listId)

Delete a list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');

$api_instance = new Swagger\Client\Api\ListsApi();
$listId = "listId_example"; // string | Id of the list

try {
    $api_instance->deleteList($listId);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->deleteList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **listId** | **string**| Id of the list |

### Return type

void (empty response body)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getContactsFromList**
> \Swagger\Client\Model\GetContacts getContactsFromList($listId, $modifiedSince, $limit, $offset)

Get the contacts in a list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');

$api_instance = new Swagger\Client\Api\ListsApi();
$listId = "listId_example"; // string | Id of the list
$modifiedSince = "modifiedSince_example"; // string | Filter the contacts modified after a given date (YYYY-MM-DD HH:mm:ss)
$limit = 50; // int | Number of documents per page
$offset = 0; // int | Index of the first document of the page

try {
    $result = $api_instance->getContactsFromList($listId, $modifiedSince, $limit, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->getContactsFromList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **listId** | **string**| Id of the list |
 **modifiedSince** | **string**| Filter the contacts modified after a given date (YYYY-MM-DD HH:mm:ss) | [optional]
 **limit** | **int**| Number of documents per page | [optional] [default to 50]
 **offset** | **int**| Index of the first document of the page | [optional] [default to 0]

### Return type

[**\Swagger\Client\Model\GetContacts**](../Model/GetContacts.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getFolderLists**
> \Swagger\Client\Model\GetFolderLists getFolderLists($folderId, $limit, $offset)

Get the lists in a folder

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');

$api_instance = new Swagger\Client\Api\ListsApi();
$folderId = "folderId_example"; // string | Id of the folder
$limit = 10; // int | Number of documents per page
$offset = 0; // int | Index of the first document of the page

try {
    $result = $api_instance->getFolderLists($folderId, $limit, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->getFolderLists: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **folderId** | **string**| Id of the folder |
 **limit** | **int**| Number of documents per page | [optional] [default to 10]
 **offset** | **int**| Index of the first document of the page | [optional] [default to 0]

### Return type

[**\Swagger\Client\Model\GetFolderLists**](../Model/GetFolderLists.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getList**
> \Swagger\Client\Model\GetExtendedList getList($listId)

Get the details of a list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');

$api_instance = new Swagger\Client\Api\ListsApi();
$listId = "listId_example"; // string | Id of the list

try {
    $result = $api_instance->getList($listId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->getList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **listId** | **string**| Id of the list |

### Return type

[**\Swagger\Client\Model\GetExtendedList**](../Model/GetExtendedList.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getLists**
> \Swagger\Client\Model\GetLists getLists($limit, $offset)

Get all the lists

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');

$api_instance = new Swagger\Client\Api\ListsApi();
$limit = 10; // int | Number of documents per page
$offset = 0; // int | Index of the first document of the page

try {
    $result = $api_instance->getLists($limit, $offset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->getLists: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **int**| Number of documents per page | [optional] [default to 10]
 **offset** | **int**| Index of the first document of the page | [optional] [default to 0]

### Return type

[**\Swagger\Client\Model\GetLists**](../Model/GetLists.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **removeContactToList**
> \Swagger\Client\Model\PostContactInfo removeContactToList($listId, $contactEmails)

Remove existing contacts from a list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');

$api_instance = new Swagger\Client\Api\ListsApi();
$listId = "listId_example"; // string | Id of the list
$contactEmails = new \Swagger\Client\Model\AddRemoveContactToList(); // \Swagger\Client\Model\AddRemoveContactToList | Emails adresses of the contact

try {
    $result = $api_instance->removeContactToList($listId, $contactEmails);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->removeContactToList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **listId** | **string**| Id of the list |
 **contactEmails** | [**\Swagger\Client\Model\AddRemoveContactToList**](../Model/AddRemoveContactToList.md)| Emails adresses of the contact |

### Return type

[**\Swagger\Client\Model\PostContactInfo**](../Model/PostContactInfo.md)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **updateList**
> updateList($listId, $updateList)

Update a list

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api-key
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('api-key', 'YOUR_API_KEY');

$api_instance = new Swagger\Client\Api\ListsApi();
$listId = "listId_example"; // string | Id of the list
$updateList = new \Swagger\Client\Model\UpdateList(); // \Swagger\Client\Model\UpdateList | Values to update a list

try {
    $api_instance->updateList($listId, $updateList);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->updateList: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **listId** | **string**| Id of the list |
 **updateList** | [**\Swagger\Client\Model\UpdateList**](../Model/UpdateList.md)| Values to update a list |

### Return type

void (empty response body)

### Authorization

[api-key](../../README.md#api-key)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)
