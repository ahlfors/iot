# EnableThing {#reference_xkt_drz_wdb .reference}

You can call this operation to enable a device that has been disabled.

## Request parameters {#section_u1b_qwm_xdb .section}

|Name|Type|Required|Description|
|:---|:---|:-------|:----------|
|Action|String|Yes|The operation you want to perform. Set the value to EnableThing.|
|IotId|String|No| Disabled device ID.

 **Note:** If this parameter is provided, the ProductKey and DeviceName parameters are not required. IotId is the GUID. Each IotId corresponds to a combination of ProductKey and DeviceName. If you provide both IotId and the combination of ProductKey and DeviceName, IotId is used.

 |
|ProductKey|String|No| Key of the product to which a disabled device belongs.

 **Note:** You must specify this parameter together with the DeviceName parameter.

 |
|DeviceName|String|No| Name of a disabled device.

 **Note:** You must specify this parameter together with the ProductKey parameter.

 |

## Response parameters {#section_u5c_nxm_xdb .section}

|Name|Type|Description|
|:---|:---|:----------|
|RequestId|String|The GUID generated by Alibaba Cloud for the request.|
|Success|Boolean|Indicates whether this call is successful. A value of true indicates that the call is successful. A value of false indicates that the call has failed.|
|ErrorMessage|String|The error message returned when the call fails.|

## Examples {#section_ezy_5xm_xdb .section}

**Request example**

```
https://iot.cn-shanghai.aliyuncs.com/?Action=EnableThing
          &IotId=SR8FiTu1R9tlUR2V1bmi0010a5****
          &Common Request Parameters
```

**Response example**

-   JSON format

    ```
    {
      "RequestId":"57b144cf-09fc-4916-a272-a62902d5b207",
      "Success": true
    }
    ```

-   XML format

    ```
    <? xml version='1.0' encoding='utf-8'? >
    <EnableThingResponse>
        <RequestId>57b144cf-09fc-4916-a272-a62902d5b207</RequestId>
        <Success>true</Success>
    </EnableThingResponse>
    ```

