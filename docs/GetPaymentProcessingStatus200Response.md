# GetPaymentProcessingStatus200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**GetPaymentProcessingStatus200ResponseData**](GetPaymentProcessingStatus200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.get_payment_processing_status200_response import GetPaymentProcessingStatus200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetPaymentProcessingStatus200Response from a JSON string
get_payment_processing_status200_response_instance = GetPaymentProcessingStatus200Response.from_json(json)
# print the JSON string representation of the object
print(GetPaymentProcessingStatus200Response.to_json())

# convert the object into a dict
get_payment_processing_status200_response_dict = get_payment_processing_status200_response_instance.to_dict()
# create an instance of GetPaymentProcessingStatus200Response from a dict
get_payment_processing_status200_response_from_dict = GetPaymentProcessingStatus200Response.from_dict(get_payment_processing_status200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


