## 用户接口

### 1、获取用户详情

**请求**

    请求方式： get
    请求url： /user/get/{id}

**请求参数说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">是否必须</th>
			<th width="10%">字段类型</th>
			<th width="60%">参数说明</th>
		</tr>
		<tr>
            <td>id</td>
			<td>是</td>
			<td>long</td>
			<td>用户id</td>
        </tr>	
    </tbody>
<table>

**返回结果**

	{
	    "code": 200,
	    "data": {
			"id": 1,
			"name": "fleet"
		}
	}

**返回结果参数说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">字段类型</th>
			<th width="70%">参数说明</th>
		</tr>
		<tr>
            <td>id</td>
			<td>long</td>
			<td>用户id</td>
        </tr>
		<tr>
            <td>name</td>
			<td>string</td>
			<td>用户名</td>
        </tr>
    </tbody>
<table>

----

### 2、获取用户列表(不含分页)

**请求**

    请求方式： get
    请求url： /user/list

**请求参数说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">是否必须</th>
			<th width="10%">字段类型</th>
			<th width="60%">参数说明</th>
		</tr>
		<tr>
            <td>id</td>
			<td>否</td>
			<td>long</td>
			<td>用户id</td>
        </tr>	
		<tr>
            <td>name</td>
			<td>否</td>
			<td>string</td>
			<td>用户名(可模糊查询)</td>
        </tr>
    </tbody>
<table>

**返回结果**

	{
	    "code": 200,
	    "data": [
			{
				"id": 1,
				"name": "fleet-1"
			},
			{
				"id": 2,
				"name": "fleet-2"
			}
		]
	}

**返回结果参数说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">字段类型</th>
			<th width="70%">参数说明</th>
		</tr>
		<tr>
            <td>id</td>
			<td>long</td>
			<td>用户id</td>
        </tr>
		<tr>
            <td>name</td>
			<td>string</td>
			<td>用户名</td>
        </tr>
    </tbody>
<table>

----

### 3、获取用户列表(含分页)

**请求**

    请求方式： get
    请求url： /user/listPage

**请求参数说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">是否必须</th>
			<th width="10%">字段类型</th>
			<th width="60%">参数说明</th>
		</tr>
		<tr>
            <td>id</td>
			<td>否</td>
			<td>long</td>
			<td>用户id</td>
        </tr>	
		<tr>
            <td>name</td>
			<td>否</td>
			<td>string</td>
			<td>用户名(可模糊查询)</td>
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

**返回结果**

	{
	    "code": 200,
	    "data": {
			"list": [
				{
					"id": 1,
					"name": "fleet-1"
				},
				{
					"id": 2,
					"name": "fleet-2"
				}
			],
			"page": {
				省略
		    }
		}
	}

**返回结果参数说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">字段类型</th>
			<th width="70%">参数说明</th>
		</tr>
		<tr>
            <td>id</td>
			<td>long</td>
			<td>用户id</td>
        </tr>
		<tr>
            <td>name</td>
			<td>string</td>
			<td>用户名</td>
        </tr>
    </tbody>
<table>

----

**如有问题，请与(April Han)联系**
