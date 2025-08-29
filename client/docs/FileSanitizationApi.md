# CloudmersiveCdrApiClient::FileSanitizationApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**file**](FileSanitizationApi.md#file) | **POST** /cdr/sanitization/file | Complete Content Disarm and Reconstruction on an Input File, and output in same file format
[**file_to_pdf**](FileSanitizationApi.md#file_to_pdf) | **POST** /cdr/sanitization/file/to/pdf | Complete Content Disarm and Reconstruction on an Input File with PDF/A Output


# **file**
> file(opts)

Complete Content Disarm and Reconstruction on an Input File, and output in same file format

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
  #Complete Content Disarm and Reconstruction on an Input File, and output in same file format
  api_instance.file(opts)
rescue CloudmersiveCdrApiClient::ApiError => e
  puts "Exception when calling FileSanitizationApi->file: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

nil (empty response body)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: Not defined



# **file_to_pdf**
> file_to_pdf(opts)

Complete Content Disarm and Reconstruction on an Input File with PDF/A Output

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
  #Complete Content Disarm and Reconstruction on an Input File with PDF/A Output
  api_instance.file_to_pdf(opts)
rescue CloudmersiveCdrApiClient::ApiError => e
  puts "Exception when calling FileSanitizationApi->file_to_pdf: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **File**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

nil (empty response body)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: Not defined



