# DescribeAvailableResource {#doc_api_Slb_DescribeAvailableResource .reference}

调用DescribeAvailableResource查询某个Region的可用区支持的资源售卖情况，支持白名单用户越过限制资源。

**说明：** 只返回支持售卖的可用区及资源类型。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Slb&api=DescribeAvailableResource)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAvailableResource|要执行的操作。

 取值：**DescribeAvailableResource**

 |
|RegionId|String|是|cn-hangzhou|地域ID。

 |
|AddressIPVersion|String|否|ipv4|IP地址类型。

 取值：**ipv4|ipv6**

 |
|AddressType|String|否|vpc|网络类型。

 取值：**vpc|classic-internet|classic-intranet**

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|AvailableResources| | |可用区及支持的资源列表。

 |
|└MasterZoneId|String|cn-shanghai-a|主可用区。

 |
|└SlaveZoneId|String|cn-shanghai-b|备可用区。

 |
|└SupportResources| | |支持的资源。

 |
|└AddressIPVersion|String|ipv4|IP地址类型。

 取值：**ipv4|ipv6**

 |
|└AddressType|String|classic\_internet|网络类型。

 取值：**vpc|classic-internet|classic-intranet**

 |
|RequestId|String|173B0EEA-22ED-4EE2-91F9-3A1CDDFFBBBA|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeAvailableResource
&RegionId=cn-hangzhou
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeAvailableResource>
  <RequestId>173B0EEA-22ED-4EE2-91F9-3A1CDDFFBBBA</RequestId>
  <AvailableResources>
    <AvailableResource>
      <SupportResources>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_internet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_intranet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>vpc</AddressType>
        </SupportResource>
      </SupportResources>
      <SlaveZoneId>cn-shanghai-b</SlaveZoneId>
      <MasterZoneId>cn-shanghai-a</MasterZoneId>
    </AvailableResource>
    <AvailableResource>
      <SupportResources>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_internet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_intranet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>vpc</AddressType>
        </SupportResource>
      </SupportResources>
      <SlaveZoneId>cn-shanghai-a</SlaveZoneId>
      <MasterZoneId>cn-shanghai-b</MasterZoneId>
    </AvailableResource>
    <AvailableResource>
      <SupportResources>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_internet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_intranet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>vpc</AddressType>
        </SupportResource>
      </SupportResources>
      <SlaveZoneId>cn-shanghai-c</SlaveZoneId>
      <MasterZoneId>cn-shanghai-b</MasterZoneId>
    </AvailableResource>
    <AvailableResource>
      <SupportResources>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_internet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_intranet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>vpc</AddressType>
        </SupportResource>
      </SupportResources>
      <SlaveZoneId>cn-shanghai-b</SlaveZoneId>
      <MasterZoneId>cn-shanghai-c</MasterZoneId>
    </AvailableResource>
    <AvailableResource>
      <SupportResources>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_internet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_intranet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>vpc</AddressType>
        </SupportResource>
      </SupportResources>
      <SlaveZoneId>cn-shanghai-e</SlaveZoneId>
      <MasterZoneId>cn-shanghai-d</MasterZoneId>
    </AvailableResource>
    <AvailableResource>
      <SupportResources>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_internet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_intranet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>vpc</AddressType>
        </SupportResource>
      </SupportResources>
      <SlaveZoneId>cn-shanghai-f</SlaveZoneId>
      <MasterZoneId>cn-shanghai-e</MasterZoneId>
    </AvailableResource>
    <AvailableResource>
      <SupportResources>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_internet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_intranet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>vpc</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv6</AddressIPVersion>
          <AddressType>classic_internet</AddressType>
        </SupportResource>
      </SupportResources>
      <SlaveZoneId>cn-shanghai-d</SlaveZoneId>
      <MasterZoneId>cn-shanghai-e</MasterZoneId>
    </AvailableResource>
    <AvailableResource>
      <SupportResources>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_internet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_intranet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>vpc</AddressType>
        </SupportResource>
      </SupportResources>
      <SlaveZoneId>cn-shanghai-e</SlaveZoneId>
      <MasterZoneId>cn-shanghai-f</MasterZoneId>
    </AvailableResource>
    <AvailableResource>
      <SupportResources>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_internet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_intranet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>vpc</AddressType>
        </SupportResource>
      </SupportResources>
      <SlaveZoneId>cn-shanghai-g</SlaveZoneId>
      <MasterZoneId>cn-shanghai-f</MasterZoneId>
    </AvailableResource>
    <AvailableResource>
      <SupportResources>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_internet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>classic_intranet</AddressType>
        </SupportResource>
        <SupportResource>
          <AddressIPVersion>ipv4</AddressIPVersion>
          <AddressType>vpc</AddressType>
        </SupportResource>
      </SupportResources>
      <SlaveZoneId>cn-shanghai-f</SlaveZoneId>
      <MasterZoneId>cn-shanghai-g</MasterZoneId>
    </AvailableResource>
  </AvailableResources>
</DescribeAvailableResource>

```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"173B0EEA-22ED-4EE2-91F9-3A1CDDFFBBBA",
	"AvailableResources":{
		"AvailableResource":[
			{
				"SlaveZoneId":"cn-shanghai-b",
				"SupportResources":{
					"SupportResource":[
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_internet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_intranet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"vpc"
						}
					]
				},
				"MasterZoneId":"cn-shanghai-a"
			},
			{
				"SlaveZoneId":"cn-shanghai-a",
				"SupportResources":{
					"SupportResource":[
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_internet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_intranet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"vpc"
						}
					]
				},
				"MasterZoneId":"cn-shanghai-b"
			},
			{
				"SlaveZoneId":"cn-shanghai-c",
				"SupportResources":{
					"SupportResource":[
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_internet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_intranet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"vpc"
						}
					]
				},
				"MasterZoneId":"cn-shanghai-b"
			},
			{
				"SlaveZoneId":"cn-shanghai-b",
				"SupportResources":{
					"SupportResource":[
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_internet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_intranet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"vpc"
						}
					]
				},
				"MasterZoneId":"cn-shanghai-c"
			},
			{
				"SlaveZoneId":"cn-shanghai-e",
				"SupportResources":{
					"SupportResource":[
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_internet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_intranet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"vpc"
						}
					]
				},
				"MasterZoneId":"cn-shanghai-d"
			},
			{
				"SlaveZoneId":"cn-shanghai-f",
				"SupportResources":{
					"SupportResource":[
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_internet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_intranet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"vpc"
						}
					]
				},
				"MasterZoneId":"cn-shanghai-e"
			},
			{
				"SlaveZoneId":"cn-shanghai-d",
				"SupportResources":{
					"SupportResource":[
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_internet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_intranet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"vpc"
						},
						{
							"AddressIPVersion":"ipv6",
							"AddressType":"classic_internet"
						}
					]
				},
				"MasterZoneId":"cn-shanghai-e"
			},
			{
				"SlaveZoneId":"cn-shanghai-e",
				"SupportResources":{
					"SupportResource":[
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_internet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_intranet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"vpc"
						}
					]
				},
				"MasterZoneId":"cn-shanghai-f"
			},
			{
				"SlaveZoneId":"cn-shanghai-g",
				"SupportResources":{
					"SupportResource":[
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_internet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_intranet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"vpc"
						}
					]
				},
				"MasterZoneId":"cn-shanghai-f"
			},
			{
				"SlaveZoneId":"cn-shanghai-f",
				"SupportResources":{
					"SupportResource":[
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_internet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"classic_intranet"
						},
						{
							"AddressIPVersion":"ipv4",
							"AddressType":"vpc"
						}
					]
				},
				"MasterZoneId":"cn-shanghai-g"
			}
		]
	}
}
```

## 错误码 { .section}

[查看本产品错误码](https://error-center.aliyun.com/status/product/Slb)

