# workbookRange: columnsBefore

Gets a certain number of columns to the left of the given range.

### Prerequisites
The following **scopes** are required to execute this API: _Files.Read,
Files.ReadWrite_
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/<id>/range/columnsBefore(count=n)

```
### Request headers
| Name       | Description|
|:---------------|:----------|
| Authorization  | Bearer {code}|
| Workbook-Session-Id  | Workbook session Id that determines if changes are persisted or not. Optional.|

### Parameters

| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|
|count|Int32|The number of columns to include in the resulting range. In general, use a positive number to create a range outside the current range. You can also use a negative number to create a range within the current range. The default value is 1|

### Request body

### Response
If successful, this method returns `200, OK` response code and [workbookRange](../resources/range.md) object in the response body.

### Example
Here is an example of how to call this API.
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "workbookrange_columnsBefore"
}-->
```http
POST https://graph.microsoft.com/{ver}/drive/root/workbook/worksheets/<id>/range/columnsBefore(count=2)
```

##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 157

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnHidden": true,
  "columnIndex": 99
}
```
