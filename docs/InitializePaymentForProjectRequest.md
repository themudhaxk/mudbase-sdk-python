# InitializePaymentForProjectRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | **float** |  | 
**currency** | **str** |  | [optional] [default to 'USD']
**customer** | [**InitializePaymentRequestCustomer**](InitializePaymentRequestCustomer.md) |  | 
**metadata** | **object** |  | [optional] 

## Example

```python
from mudbase.models.initialize_payment_for_project_request import InitializePaymentForProjectRequest

# TODO update the JSON string below
json = "{}"
# create an instance of InitializePaymentForProjectRequest from a JSON string
initialize_payment_for_project_request_instance = InitializePaymentForProjectRequest.from_json(json)
# print the JSON string representation of the object
print(InitializePaymentForProjectRequest.to_json())

# convert the object into a dict
initialize_payment_for_project_request_dict = initialize_payment_for_project_request_instance.to_dict()
# create an instance of InitializePaymentForProjectRequest from a dict
initialize_payment_for_project_request_from_dict = InitializePaymentForProjectRequest.from_dict(initialize_payment_for_project_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


