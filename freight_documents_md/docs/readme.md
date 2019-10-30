# IO.Swagger.Api.DocumentApi

All URIs are relative to *http://142.93.207.215:3000*

Method | HTTP request | Description
------------- | ------------- | -------------
[**DocumentCreate**](DocumentApi.md#documentcreate) | **POST** /document | Create document
[**DocumentGet**](DocumentApi.md#documentget) | **GET** /document/{REFERENCE_ID} | Get document
[**DocumentGetByReferenceId**](DocumentApi.md#documentgetbyreferenceid) | **GET** /document/getByReferenceId/{REFERENCE_ID} | Search document by referenceId
[**DocumentGetbyHash**](DocumentApi.md#documentgetbyhash) | **GET** /document/getbyHash/{HASH} | Search document by hash
[**DocumentUpdate**](DocumentApi.md#documentupdate) | **PUT** /document/{REFERENCE_ID} | Update Document


<a name="documentcreate"></a>
# **DocumentCreate**
> CreateDocumentResponse DocumentCreate (Document body)

Create document

Creates a new document

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class DocumentCreateExample
    {
        public void main()
        {
            var apiInstance = new DocumentApi();
            var body = new Document(); // Document | 

            try
            {
                // Create document
                CreateDocumentResponse result = apiInstance.DocumentCreate(body);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DocumentApi.DocumentCreate: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Document**](Document.md)|  | 

### Return type

[**CreateDocumentResponse**](CreateDocumentResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="documentget"></a>
# **DocumentGet**
> Document DocumentGet (string REFERENCE_ID)

Get document

Get document by referenceId

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class DocumentGetExample
    {
        public void main()
        {
            var apiInstance = new DocumentApi();
            var REFERENCE_ID = REFERENCE_ID_example;  // string | 

            try
            {
                // Get document
                Document result = apiInstance.DocumentGet(REFERENCE_ID);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DocumentApi.DocumentGet: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **REFERENCE_ID** | **string**|  | 

### Return type

[**Document**](Document.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="documentgetbyreferenceid"></a>
# **DocumentGetByReferenceId**
> ReferenceIdArray DocumentGetByReferenceId (string REFERENCE_ID)

Search document by referenceId

Search document by referenceId

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class DocumentGetByReferenceIdExample
    {
        public void main()
        {
            var apiInstance = new DocumentApi();
            var REFERENCE_ID = REFERENCE_ID_example;  // string | 

            try
            {
                // Search document by referenceId
                ReferenceIdArray result = apiInstance.DocumentGetByReferenceId(REFERENCE_ID);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DocumentApi.DocumentGetByReferenceId: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **REFERENCE_ID** | **string**|  | 

### Return type

[**ReferenceIdArray**](ReferenceIdArray.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="documentgetbyhash"></a>
# **DocumentGetbyHash**
> ReferenceIdArray DocumentGetbyHash (string HASH)

Search document by hash

Search document by hash

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class DocumentGetbyHashExample
    {
        public void main()
        {
            var apiInstance = new DocumentApi();
            var HASH = HASH_example;  // string | 

            try
            {
                // Search document by hash
                ReferenceIdArray result = apiInstance.DocumentGetbyHash(HASH);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DocumentApi.DocumentGetbyHash: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **HASH** | **string**|  | 

### Return type

[**ReferenceIdArray**](ReferenceIdArray.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="documentupdate"></a>
# **DocumentUpdate**
> CreateDocumentResponse DocumentUpdate (Document body, string REFERENCE_ID)

Update Document

Adds a new version of an existing document by providing previous referenceId

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class DocumentUpdateExample
    {
        public void main()
        {
            var apiInstance = new DocumentApi();
            var body = new Document(); // Document | 
            var REFERENCE_ID = REFERENCE_ID_example;  // string | 

            try
            {
                // Update Document
                CreateDocumentResponse result = apiInstance.DocumentUpdate(body, REFERENCE_ID);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling DocumentApi.DocumentUpdate: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Document**](Document.md)|  | 
 **REFERENCE_ID** | **string**|  | 

### Return type

[**CreateDocumentResponse**](CreateDocumentResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

