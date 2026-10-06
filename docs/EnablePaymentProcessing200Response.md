# EnablePaymentProcessing200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**message** | **str** |  | [optional] 
**data** | [**EnablePaymentProcessing200ResponseData**](EnablePaymentProcessing200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.enable_payment_processing200_response import EnablePaymentProcessing200Response

# TODO update the JSON string below
json = "{}"
# create an instance of EnablePaymentProcessing200Response from a JSON string
enable_payment_processing200_response_instance = EnablePaymentProcessing200Response.from_json(json)
# print the JSON string representation of the object
print(EnablePaymentProcessing200Response.to_json())

# convert the object into a dict
enable_payment_processing200_response_dict = enable_payment_processing200_response_instance.to_dict()
# create an instance of EnablePaymentProcessing200Response from a dict
enable_payment_processing200_response_from_dict = EnablePaymentProcessing200Response.from_dict(enable_payment_processing200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


