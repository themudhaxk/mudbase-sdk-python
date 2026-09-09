# GetPaymentRecords200ResponseDataRecordsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tx_ref** | **str** |  | [optional] 
**amount** | **float** |  | [optional] 
**org_receives** | **float** |  | [optional] 
**status** | **str** |  | [optional] 
**paid_at** | **str** |  | [optional] 

## Example

```python
from mudbase.models.get_payment_records200_response_data_records_inner import GetPaymentRecords200ResponseDataRecordsInner

# TODO update the JSON string below
json = "{}"
# create an instance of GetPaymentRecords200ResponseDataRecordsInner from a JSON string
get_payment_records200_response_data_records_inner_instance = GetPaymentRecords200ResponseDataRecordsInner.from_json(json)
# print the JSON string representation of the object
print(GetPaymentRecords200ResponseDataRecordsInner.to_json())

# convert the object into a dict
get_payment_records200_response_data_records_inner_dict = get_payment_records200_response_data_records_inner_instance.to_dict()
# create an instance of GetPaymentRecords200ResponseDataRecordsInner from a dict
get_payment_records200_response_data_records_inner_from_dict = GetPaymentRecords200ResponseDataRecordsInner.from_dict(get_payment_records200_response_data_records_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


