## 公共接口-基础说明

	测试地址：http://test.fleetsoft.com.cn
	正式地址：http://www.fleetsoft.com.cn

---
### 1、接口返回码

	每次调用接口时，可能获得正确或错误的返回码，开发者可以根据返回码信息调试接口，排查错误。

**接口返回码说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">返回码</th>
			<th width="80%">说明</th>
		</tr>
		<tr>
            <td>200</td>
			<td>成功</td>
        </tr>
		<tr>
            <td>400</td>
			<td>错误</td>
        </tr>
    </tbody>
<table>

----

### 2、分页查询

**分页查询示例**

	分页查询接口?pageIndex=1&pageRows=20

**分页查询参数说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">是否必须</th>
			<th width="10%">字段类型</th>
			<th width="60%">参数说明</th>
		</tr>
		<tr>
            <td>pageIndex</td>
			<td>否</td>
			<td>int</td>
			<td>请求的页数（从1开始），不设则默认为1</td>
        </tr>
		<tr>
            <td>pageRows</td>
			<td>否</td>
			<td>int</td>
			<td>请求的每页行数，不设则默认为20</td>
        </tr>
    </tbody>
<table>

**分页查询结果 JSON 格式**

    "page": {
        "pageIndex": 1,
        "pageRows": 20,
        "fromIndex": 0,
        "toIndex": 20,
        "totalRows": 0,
        "totalPages": 1,
        "hasPrevPage": false,
        "hasNextPage": false
    }

**分页查询结果参数说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">字段类型</th>
			<th width="70%">参数说明</th>
		</tr>
		<tr>
            <td>pageIndex</td>
			<td>int</td>
			<td>请求的页数（从1开始），不设则默认为1</td>
        </tr>
		<tr>
            <td>pageRows</td>
			<td>int</td>
			<td>请求的每页行数，不设则默认为20</td>
        </tr>
		<tr>
            <td>fromIndex</td>
			<td>int</td>
			<td>请求的页数的开始偏移量（包含），不设则默认为0</td>
        </tr>
		<tr>
            <td>toIndex</td>
			<td>int</td>
			<td>请求的页数的结束偏移量（不包含），不设则默认为20</td>
        </tr>
		<tr>
            <td>totalRows</td>
			<td>int</td>
			<td>总行数</td>
        </tr>
		<tr>
            <td>totalPages</td>
			<td>int</td>
			<td>总页数</td>
        </tr>
		<tr>
            <td>hasPrevPage</td>
			<td>boolean</td>
			<td>是否有上一页</td>
        </tr>
		<tr>
            <td>hasNextPage</td>
			<td>boolean</td>
			<td>是否有下一页</td>
        </tr>
    </tbody>
<table>

----

**如有问题，请与(April Han)联系**
