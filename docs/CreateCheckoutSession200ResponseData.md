# CreateCheckoutSession200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**checkout_url** | **str** | Hosted payment URL (same as authorizationUrl) | [optional] 
**authorization_url** | **str** | Hosted payment URL | [optional] 
**access_code** | **str** | Gateway access code | [optional] 
**reference** | **str** | Transaction reference (mudbase_...) for verify-payment | [optional] 
**amount** | **float** |  | [optional] 
**currency** | **str** |  | [optional] 

## Example

```python
from mudbase.models.create_checkout_session200_response_data import CreateCheckoutSession200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of CreateCheckoutSession200ResponseData from a JSON string
create_checkout_session200_response_data_instance = CreateCheckoutSession200ResponseData.from_json(json)
# print the JSON string representation of the object
print(CreateCheckoutSession200ResponseData.to_json())

# convert the object into a dict
create_checkout_session200_response_data_dict = create_checkout_session200_response_data_instance.to_dict()
# create an instance of CreateCheckoutSession200ResponseData from a dict
create_checkout_session200_response_data_from_dict = CreateCheckoutSession200ResponseData.from_dict(create_checkout_session200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


