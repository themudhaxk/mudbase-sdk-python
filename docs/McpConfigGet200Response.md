# McpConfigGet200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | [optional] 
**plan** | **str** |  | [optional] 
**allowed_plans** | **List[str]** |  | [optional] 
**free_promo_active** | **bool** | True if this org is on the free plan and MCP is temporarily enabled via the launch promo | [optional] 
**free_promo_ends_at** | **datetime** | When the free-plan MCP promo ends (null if not active) | [optional] 
**endpoint** | **str** |  | [optional] 
**tools** | [**List[McpConfigGet200ResponseToolsInner]**](McpConfigGet200ResponseToolsInner.md) |  | [optional] 

## Example

```python
from mudbase.models.mcp_config_get200_response import McpConfigGet200Response

# TODO update the JSON string below
json = "{}"
# create an instance of McpConfigGet200Response from a JSON string
mcp_config_get200_response_instance = McpConfigGet200Response.from_json(json)
# print the JSON string representation of the object
print(McpConfigGet200Response.to_json())

# convert the object into a dict
mcp_config_get200_response_dict = mcp_config_get200_response_instance.to_dict()
# create an instance of McpConfigGet200Response from a dict
mcp_config_get200_response_from_dict = McpConfigGet200Response.from_dict(mcp_config_get200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


