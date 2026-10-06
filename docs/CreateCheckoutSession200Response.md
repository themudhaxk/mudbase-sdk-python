# CreateCheckoutSession200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**data** | [**CreateCheckoutSession200ResponseData**](CreateCheckoutSession200ResponseData.md) |  | [optional] 

## Example

```python
from mudbase.models.create_checkout_session200_response import CreateCheckoutSession200Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateCheckoutSession200Response from a JSON string
create_checkout_session200_response_instance = CreateCheckoutSession200Response.from_json(json)
# print the JSON string representation of the object
print(CreateCheckoutSession200Response.to_json())

# convert the object into a dict
create_checkout_session200_response_dict = create_checkout_session200_response_instance.to_dict()
# create an instance of CreateCheckoutSession200Response from a dict
create_checkout_session200_response_from_dict = CreateCheckoutSession200Response.from_dict(create_checkout_session200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


