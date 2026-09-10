# VerifyPayment200ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subscription** | [**VerifyPayment200ResponseDataSubscription**](VerifyPayment200ResponseDataSubscription.md) |  | [optional] 

## Example

```python
from mudbase.models.verify_payment200_response_data import VerifyPayment200ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of VerifyPayment200ResponseData from a JSON string
verify_payment200_response_data_instance = VerifyPayment200ResponseData.from_json(json)
# print the JSON string representation of the object
print(VerifyPayment200ResponseData.to_json())

# convert the object into a dict
verify_payment200_response_data_dict = verify_payment200_response_data_instance.to_dict()
# create an instance of VerifyPayment200ResponseData from a dict
verify_payment200_response_data_from_dict = VerifyPayment200ResponseData.from_dict(verify_payment200_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


