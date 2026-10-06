# GenerateDataProcessingRecordRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**org_id** | **str** |  | 
**record_date** | **datetime** |  | [optional] 

## Example

```python
from mudbase.models.generate_data_processing_record_request import GenerateDataProcessingRecordRequest

# TODO update the JSON string below
json = "{}"
# create an instance of GenerateDataProcessingRecordRequest from a JSON string
generate_data_processing_record_request_instance = GenerateDataProcessingRecordRequest.from_json(json)
# print the JSON string representation of the object
print(GenerateDataProcessingRecordRequest.to_json())

# convert the object into a dict
generate_data_processing_record_request_dict = generate_data_processing_record_request_instance.to_dict()
# create an instance of GenerateDataProcessingRecordRequest from a dict
generate_data_processing_record_request_from_dict = GenerateDataProcessingRecordRequest.from_dict(generate_data_processing_record_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


