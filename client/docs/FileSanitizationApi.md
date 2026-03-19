# CloudmersiveCdrApiClient::FileSanitizationApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**file**](FileSanitizationApi.md#file) | **POST** /cdr/sanitization/file | Content Disarm and Reconstruction on a File
[**file_advanced**](FileSanitizationApi.md#file_advanced) | **POST** /cdr/sanitization/file/advanced | Advanced Content Disarm and Reconstruction on a File
[**file_to_pdf**](FileSanitizationApi.md#file_to_pdf) | **POST** /cdr/sanitization/file/to/pdf | Content Disarm and Reconstruction on a File with PDFA Output
[**file_to_pdf_advanced**](FileSanitizationApi.md#file_to_pdf_advanced) | **POST** /cdr/sanitization/file/to/pdf/advanced | Advanced Content Disarm and Reconstruction on a File with PDFA Output


# **file**
> String file(opts)

Content Disarm and Reconstruction on a File

Processes the input file via CDR to produce a secured output file.  Input content is parsed, disarmed, and then reconstructed into a new output file with the same file format as the input.

### Example
```ruby
# load the gem
require 'cloudmersive-cdr-api-client'
# setup authorization
CloudmersiveCdrApiClient.configure do |config|
  # Configure API key authorization: Apikey
  config.api_key['Apikey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Apikey'] = 'Bearer'
end

api_instance = CloudmersiveCdrApiClient::FileSanitizationApi.new

opts = { 
  input_file: File.new('/path/to/file.txt') # File | Input document, or photos of a document, to extract data from
}

begin
  #Content Disarm and Reconstruction on a File
  result = api_instance.file(opts)
  p result
rescue CloudmersiveCdrApiClient::ApiError => e
  puts "Exception when calling FileSanitizationApi->file: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

**String**

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream



# **file_advanced**
> String file_advanced(opts)

Advanced Content Disarm and Reconstruction on a File

Processes the input file via CDR to produce a secured output file with advanced scan options and response headers containing scan metadata.

### Example
```ruby
# load the gem
require 'cloudmersive-cdr-api-client'
# setup authorization
CloudmersiveCdrApiClient.configure do |config|
  # Configure API key authorization: Apikey
  config.api_key['Apikey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Apikey'] = 'Bearer'
end

api_instance = CloudmersiveCdrApiClient::FileSanitizationApi.new

opts = { 
  allow_executables: true, # BOOLEAN | Set to false to block executable files (EXE, DLL, etc.)
  allow_invalid_files: true, # BOOLEAN | Set to false to block files that are not valid for their detected type
  allow_scripts: true, # BOOLEAN | Set to false to block script files. PDF and Office macro sanitization still runs regardless.
  allow_password_protected_files: true, # BOOLEAN | Set to false to block password-protected files
  allow_macros: true, # BOOLEAN | Set to false to block files containing macros. Office macro removal still runs regardless.
  allow_xml_external_entities: true, # BOOLEAN | Set to false to block XML files with external entity references (XXE)
  allow_insecure_deserialization: true, # BOOLEAN | Set to false to block files with insecure deserialization patterns
  allow_html: true, # BOOLEAN | Set to false to block HTML files
  allow_unsafe_archives: true, # BOOLEAN | Set to false to block archive files flagged as unsafe (e.g., zip bombs)
  allow_ole_embedded_object: true, # BOOLEAN | Set to false to block files with embedded OLE objects
  allow_unwanted_action: true, # BOOLEAN | Set to false to block files with unwanted actions
  restrict_file_types: 'restrict_file_types_example', # String | Comma-separated list of allowed file extensions (e.g., \".pdf,.docx,.xlsx\"). Files not matching will be blocked.
  input_file: File.new('/path/to/file.txt') # File | Input document to CDR process
}

begin
  #Advanced Content Disarm and Reconstruction on a File
  result = api_instance.file_advanced(opts)
  p result
rescue CloudmersiveCdrApiClient::ApiError => e
  puts "Exception when calling FileSanitizationApi->file_advanced: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **allow_executables** | **BOOLEAN**| Set to false to block executable files (EXE, DLL, etc.) | [optional] 
 **allow_invalid_files** | **BOOLEAN**| Set to false to block files that are not valid for their detected type | [optional] 
 **allow_scripts** | **BOOLEAN**| Set to false to block script files. PDF and Office macro sanitization still runs regardless. | [optional] 
 **allow_password_protected_files** | **BOOLEAN**| Set to false to block password-protected files | [optional] 
 **allow_macros** | **BOOLEAN**| Set to false to block files containing macros. Office macro removal still runs regardless. | [optional] 
 **allow_xml_external_entities** | **BOOLEAN**| Set to false to block XML files with external entity references (XXE) | [optional] 
 **allow_insecure_deserialization** | **BOOLEAN**| Set to false to block files with insecure deserialization patterns | [optional] 
 **allow_html** | **BOOLEAN**| Set to false to block HTML files | [optional] 
 **allow_unsafe_archives** | **BOOLEAN**| Set to false to block archive files flagged as unsafe (e.g., zip bombs) | [optional] 
 **allow_ole_embedded_object** | **BOOLEAN**| Set to false to block files with embedded OLE objects | [optional] 
 **allow_unwanted_action** | **BOOLEAN**| Set to false to block files with unwanted actions | [optional] 
 **restrict_file_types** | **String**| Comma-separated list of allowed file extensions (e.g., \&quot;.pdf,.docx,.xlsx\&quot;). Files not matching will be blocked. | [optional] 
 **input_file** | **File**| Input document to CDR process | [optional] 

### Return type

**String**

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream



# **file_to_pdf**
> String file_to_pdf(opts)

Content Disarm and Reconstruction on a File with PDFA Output

Processes the input file via CDR to produce a secured PDF/A output file.  Input content is parsed, disarmed, and then reconstructed into a new PDF/A output file.

### Example
```ruby
# load the gem
require 'cloudmersive-cdr-api-client'
# setup authorization
CloudmersiveCdrApiClient.configure do |config|
  # Configure API key authorization: Apikey
  config.api_key['Apikey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Apikey'] = 'Bearer'
end

api_instance = CloudmersiveCdrApiClient::FileSanitizationApi.new

opts = { 
  input_file: File.new('/path/to/file.txt') # File | Input document, or photos of a document, to extract data from
}

begin
  #Content Disarm and Reconstruction on a File with PDFA Output
  result = api_instance.file_to_pdf(opts)
  p result
rescue CloudmersiveCdrApiClient::ApiError => e
  puts "Exception when calling FileSanitizationApi->file_to_pdf: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

**String**

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream



# **file_to_pdf_advanced**
> String file_to_pdf_advanced(opts)

Advanced Content Disarm and Reconstruction on a File with PDFA Output

Processes the input file via CDR to produce a secured PDF/A output file with advanced scan options and response headers containing scan metadata.

### Example
```ruby
# load the gem
require 'cloudmersive-cdr-api-client'
# setup authorization
CloudmersiveCdrApiClient.configure do |config|
  # Configure API key authorization: Apikey
  config.api_key['Apikey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  #config.api_key_prefix['Apikey'] = 'Bearer'
end

api_instance = CloudmersiveCdrApiClient::FileSanitizationApi.new

opts = { 
  allow_executables: true, # BOOLEAN | Set to false to block executable files (EXE, DLL, etc.)
  allow_invalid_files: true, # BOOLEAN | Set to false to block files that are not valid for their detected type
  allow_scripts: true, # BOOLEAN | Set to false to block script files. PDF and Office macro sanitization still runs regardless.
  allow_password_protected_files: true, # BOOLEAN | Set to false to block password-protected files
  allow_macros: true, # BOOLEAN | Set to false to block files containing macros. Office macro removal still runs regardless.
  allow_xml_external_entities: true, # BOOLEAN | Set to false to block XML files with external entity references (XXE)
  allow_insecure_deserialization: true, # BOOLEAN | Set to false to block files with insecure deserialization patterns
  allow_html: true, # BOOLEAN | Set to false to block HTML files
  allow_unsafe_archives: true, # BOOLEAN | Set to false to block archive files flagged as unsafe (e.g., zip bombs)
  allow_ole_embedded_object: true, # BOOLEAN | Set to false to block files with embedded OLE objects
  allow_unwanted_action: true, # BOOLEAN | Set to false to block files with unwanted actions
  restrict_file_types: 'restrict_file_types_example', # String | Comma-separated list of allowed file extensions (e.g., \".pdf,.docx,.xlsx\"). Files not matching will be blocked.
  input_file: File.new('/path/to/file.txt') # File | Input document to CDR process
}

begin
  #Advanced Content Disarm and Reconstruction on a File with PDFA Output
  result = api_instance.file_to_pdf_advanced(opts)
  p result
rescue CloudmersiveCdrApiClient::ApiError => e
  puts "Exception when calling FileSanitizationApi->file_to_pdf_advanced: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **allow_executables** | **BOOLEAN**| Set to false to block executable files (EXE, DLL, etc.) | [optional] 
 **allow_invalid_files** | **BOOLEAN**| Set to false to block files that are not valid for their detected type | [optional] 
 **allow_scripts** | **BOOLEAN**| Set to false to block script files. PDF and Office macro sanitization still runs regardless. | [optional] 
 **allow_password_protected_files** | **BOOLEAN**| Set to false to block password-protected files | [optional] 
 **allow_macros** | **BOOLEAN**| Set to false to block files containing macros. Office macro removal still runs regardless. | [optional] 
 **allow_xml_external_entities** | **BOOLEAN**| Set to false to block XML files with external entity references (XXE) | [optional] 
 **allow_insecure_deserialization** | **BOOLEAN**| Set to false to block files with insecure deserialization patterns | [optional] 
 **allow_html** | **BOOLEAN**| Set to false to block HTML files | [optional] 
 **allow_unsafe_archives** | **BOOLEAN**| Set to false to block archive files flagged as unsafe (e.g., zip bombs) | [optional] 
 **allow_ole_embedded_object** | **BOOLEAN**| Set to false to block files with embedded OLE objects | [optional] 
 **allow_unwanted_action** | **BOOLEAN**| Set to false to block files with unwanted actions | [optional] 
 **restrict_file_types** | **String**| Comma-separated list of allowed file extensions (e.g., \&quot;.pdf,.docx,.xlsx\&quot;). Files not matching will be blocked. | [optional] 
 **input_file** | **File**| Input document to CDR process | [optional] 

### Return type

**String**

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/octet-stream



