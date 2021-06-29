## 公共接口-用户

	测试服务器地址（内部访问）：https://10.17.191.55/
	测试服务器地址（外部访问）：http://112.95.226.134/
	外网服务器地址：http://tonghao.byd.com/

### <a id="getDeviceNumber"></a> 1、获取用户信息
**接口调用请求说明**

    请求方式： get
    请求url： https://domain/v1/web/exhibition/user/lock/getDeviceNumber

**参数说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">是否必须</th>
			<th width="10%">字段类型</th>
			<th width="60%">参数说明</th>
		</tr>
		<tr>
            <td>appId</td>
			<td>是</td>
			<td>int</td>
			<td>应用标识</td>
        </tr>
		<tr>
            <td>accessToken</td>
			<td>是</td>
			<td>string</td>
			<td>访问凭证</td>
        </tr>
		<tr>
            <td>timestamp</td>
			<td>是</td>
			<td>int</td>
			<td>时间戳</td>
        </tr>		
    </tbody>
<table>

------

**返回结果**

	{
	    "code": 200,
	    "data": "0JAA-HVGI-64RY-A"
	}

----

### <a id="getLockUserList"></a> 2、获取门锁用户列表（珠海亿胜门锁）
**接口调用请求说明**

    请求方式： get
    请求url： https://domain/v1/web/exhibition/user/lock/getLockUserList

**参数说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">是否必须</th>
			<th width="10%">字段类型</th>
			<th width="60%">参数说明</th>
		</tr>
		<tr>
            <td>appId</td>
			<td>是</td>
			<td>int</td>
			<td>应用标识</td>
        </tr>
		<tr>
            <td>accessToken</td>
			<td>是</td>
			<td>string</td>
			<td>访问凭证</td>
        </tr>
		<tr>
            <td>timestamp</td>
			<td>是</td>
			<td>int</td>
			<td>时间戳</td>
        </tr>
		<tr>
            <td>useName</td>
			<td>否</td>
			<td>string</td>
			<td>用户名</td>
        </tr>
		<tr>
            <td>userCode</td>
			<td>否</td>
			<td>string</td>
			<td>门锁用户编号</td>
        </tr>	
		<tr>
            <td>sex</td>
			<td>否</td>
			<td>int</td>
			<td>性别</td>
        </tr>
		<tr>
            <td>isAdmin</td>
			<td>否</td>
			<td>int</td>
			<td>是否管理员 0-否 1-是</td>
        </tr>	
    </tbody>
<table>

------

**返回结果**

	{
	    "code": 200,
	    "data": [
	        {
				"id": 52,
	            "deviceNumber": "0JAA-HVGI-64RY-A",
	            "userCode": "3",
	            "userName": "马林",
	            "userId": 10333,
	            "isAdmin": 0,
				"lockUserPhotographRecordList": [
               	 {
                    "dataId": 56,
                    "exhibitionUserId": 10505,
                    "lockUserId": 10505,
                    "photographId": 222,
                    "muscleAge": 222,
                    "emotion": "2222"
                }
            ]
	        }
	    ]
	}


**结果说明**
<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">字段类型</th>
			<th width="60%">参数说明</th>
		</tr>
		<tr>
            <td>id</td>
			<td>int</td>
			<td>数据标识</td>
        </tr>		
		<tr>
            <td>deviceNumber</td>
			<td>string</td>
			<td>锁号</td>
        </tr>
		<tr>
            <td>userCode</td>
			<td>string</td>
			<td>用户编码</td>
        </tr>
		<tr>
            <td>userName</td>
			<td>string</td>
			<td>用户名称</td>
        </tr>
		<tr>
            <td>isAdmin</td>
			<td>int</td>
			<td>是否是管理员（1-是 0-否）</td>
        </tr>
		<tr>
            <td>userId</td>
			<td>int</td>
			<td>用户标识</td>
        </tr>
		<tr>
            <td>lockUserPhotographRecordList</td>
			<td>List</td>
			<td>肌肤秘诀照片信息</td>
        </tr>
		<tr>
            <td>&nbsp;&nbsp;&nbsp;&nbsp;photographId</td>
			<td>int</td>
			<td>肌肤秘诀数据标识</td>
        </tr>
		<tr>
            <td>&nbsp;&nbsp;&nbsp;&nbsp;muscleAge</td>
			<td>int</td>
			<td>肌龄</td>
        </tr>
		<tr>
            <td>&nbsp;&nbsp;&nbsp;&nbsp;emotion</td>
			<td>int</td>
			<td>情绪</td>
        </tr>
		<tr>
            <td>&nbsp;&nbsp;&nbsp;&nbsp;lockUserId</td>
			<td>int</td>
			<td>门锁用户标识</td>
        </tr>
		<tr>
            <td>&nbsp;&nbsp;&nbsp;&nbsp;exhibitionUserId</td>
			<td>int</td>
			<td>展厅用户标识</td>
        </tr>
		<tr>
            <td>&nbsp;&nbsp;&nbsp;&nbsp;dataId</td>
			<td>int</td>
			<td>数据唯一标识</td>
        </tr>						
    </tbody>
<table>
----

### <a id="connect"></a> 3、连接人脸识别服务器(外网服务器地址：https://api.clife.cn/)
**接口调用请求说明**

    请求方式： get
    请求url： https://domain/v1/app/face/faceEx/connect

**参数说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">是否必须</th>
			<th width="10%">字段类型</th>
			<th width="60%">参数说明</th>
		</tr>
		<tr>
            <td>serverURL</td>
			<td>是</td>
			<td>String</td>
			<td>人脸识别服务器地址</td>
        </tr>
		<tr>
            <td>deviceNumber</td>
			<td>是</td>
			<td>string</td>
			<td>锁号</td>
        </tr>
		<tr>
            <td>dataServerURL</td>
			<td>是</td>
			<td>string</td>
			<td>数据上传地址</td>
        </tr>		
    </tbody>
<table>

------

**返回结果**

	{
	    "code": 200,
	    "data": true
	}

----

### <a id="disconnect"></a> 4、断开人脸识别服务器(外网服务器地址：https://api.clife.cn/)
**接口调用请求说明**

    请求方式： get
    请求url： https://domain/v1/app/face/faceEx/disconnect

**参数说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">是否必须</th>
			<th width="10%">字段类型</th>
			<th width="60%">参数说明</th>
		</tr>		
		<tr>
            <td>deviceNumber</td>
			<td>是</td>
			<td>string</td>
			<td>锁号</td>
        </tr>				
    </tbody>
<table>

------

**返回结果**

	{
	    "code": 200,
	    "data": true
	}

----


### <a id="data1"></a> 5、模拟设备数据(外网服务器地址：https://api.clife.cn/)
**接口调用请求说明**

    请求方式： get
    请求url： https://domain/v1/app/face/faceEx/data1/{deviceNumber}

**参数说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">是否必须</th>
			<th width="10%">字段类型</th>
			<th width="60%">参数说明</th>
		</tr>		
		<tr>
            <td>deviceNumber</td>
			<td>是</td>
			<td>string</td>
			<td>锁号</td>
        </tr>
		<tr>
            <td>successInfo</td>
			<td>是</td>
			<td>string</td>
			<td>成功标识</td>
        </tr>
		<tr>
            <td>userCode</td>
			<td>是</td>
			<td>string</td>
			<td>用户编码</td>
        </tr>
		<tr>
            <td>userName</td>
			<td>是</td>
			<td>string</td>
			<td>用户名称</td>
        </tr>
		<tr>
            <td>checkTime</td>
			<td>是</td>
			<td>string</td>
			<td>开锁时间（yyyyMMddHHmmss）</td>
        </tr>
		<tr>
            <td>isAdmin</td>
			<td>是</td>
			<td>int</td>
			<td>是否是管理员（true-是 false-否）</td>
        </tr>
		<tr>
            <td>photo</td>
			<td>是</td>
			<td>string</td>
			<td>照片信息</td>
        </tr>						
    </tbody>
<table>

------

**返回结果**

	{
	    "code": 0
	}


------

### <a id="insertLockUser"></a> 6、新增门锁用户
**接口调用请求说明**

    请求方式： post
    请求url： https://domain/v1/web/smarthome/user/lock/insertLockUser

**参数说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">是否必须</th>
			<th width="10%">字段类型</th>
			<th width="60%">参数说明</th>
		</tr>
		<tr>
            <td>appId</td>
			<td>是</td>
			<td>int</td>
			<td>应用标识</td>
        </tr>
		<tr>
            <td>timestamp</td>
			<td>是</td>
			<td>int</td>
			<td>时间戳</td>
        </tr>
		<tr>
            <td>accessToken</td>
			<td>是</td>
			<td>string</td>
			<td>访问凭证</td>
        </tr>
		<tr>
            <td>userCode</td>
			<td>是</td>
			<td>string</td>
			<td>门锁用户编码</td>
        </tr>	
		<tr>
            <td>userName</td>
			<td>是</td>
			<td>string</td>
			<td>用户名</td>
        </tr>	
		<tr>
            <td>sex</td>
			<td>是</td>
			<td>int</td>
			<td>用户性别 0-女 1-男 2-未知</td>
        </tr>	
		<tr>
            <td>accountName</td>
			<td>是</td>
			<td>string</td>
			<td>app账号</td>
        </tr>
		<tr>
            <td>isAdmin</td>
			<td>是</td>
			<td>int</td>
			<td>是否管理员 0-否 1-是</td>
        </tr>
		<tr>
            <td>emotion</td>
			<td>是</td>
			<td>string</td>
			<td>情绪</td>
        </tr>	
    </tbody>
<table>

------

**返回结果**

	{
	    "code": 0
	}

----

### <a id="updateLockUser"></a> 7、编辑门锁用户
**接口调用请求说明**

    请求方式： post
    请求url： https://domain/v1/web/smarthome/user/lock/updateLockUser

**参数说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">是否必须</th>
			<th width="10%">字段类型</th>
			<th width="60%">参数说明</th>
		</tr>
		<tr>
            <td>appId</td>
			<td>是</td>
			<td>int</td>
			<td>应用标识</td>
        </tr>
		<tr>
            <td>timestamp</td>
			<td>是</td>
			<td>int</td>
			<td>时间戳</td>
        </tr>
		<tr>
            <td>accessToken</td>
			<td>是</td>
			<td>string</td>
			<td>访问凭证</td>
        </tr>
		<tr>
            <td>id</td>
			<td>是</td>
			<td>int</td>
			<td>数据标识</td>
        </tr>
		<tr>
            <td>userCode</td>
			<td>否</td>
			<td>string</td>
			<td>门锁用户编码</td>
        </tr>	
		<tr>
            <td>userName</td>
			<td>否</td>
			<td>string</td>
			<td>用户名</td>
        </tr>	
		<tr>
            <td>sex</td>
			<td>否</td>
			<td>int</td>
			<td>用户性别 0-女 1-男 2-未知</td>
        </tr>	
		<tr>
            <td>accountName</td>
			<td>否</td>
			<td>string</td>
			<td>app账号</td>
        </tr>
		<tr>
            <td>isAdmin</td>
			<td>否</td>
			<td>int</td>
			<td>是否管理员 0-否 1-是</td>
        </tr>
		<tr>
            <td>emotion</td>
			<td>否</td>
			<td>string</td>
			<td>情绪</td>
        </tr>			
    </tbody>
<table>

------

**返回结果**

	{
	    "code": 0
	}

----


### <a id="insertUserDeviceNumber"></a> 8、新增用户锁号
**接口调用请求说明**

    请求方式： post
    请求url： https://domain/v1/web/smarthome/user/lock/insertUserDeviceNumber

**参数说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">是否必须</th>
			<th width="10%">字段类型</th>
			<th width="60%">参数说明</th>
		</tr>
		<tr>
            <td>appId</td>
			<td>是</td>
			<td>int</td>
			<td>应用标识</td>
        </tr>
		<tr>
            <td>timestamp</td>
			<td>是</td>
			<td>int</td>
			<td>时间戳</td>
        </tr>
		<tr>
            <td>accessToken</td>
			<td>是</td>
			<td>string</td>
			<td>访问凭证</td>
        </tr>
		<tr>
            <td>deviceNumber</td>
			<td>是</td>
			<td>string</td>
			<td>门锁序列号</td>
        </tr>			
    </tbody>
<table>

------

**返回结果**

	{
	    "code": 0
	}

----
### <a id="updateUserDeviceNumber"></a> 9、修改用户锁号
**接口调用请求说明**

    请求方式： post
    请求url： https://domain/v1/web/smarthome/user/lock/updateUserDeviceNumber

**参数说明**

<table width="100%" style="border-spacing: 0;  border-collapse: collapse;">
    <tbody>
        <tr>
			<th width="20%">参数名称</th>
			<th width="10%">是否必须</th>
			<th width="10%">字段类型</th>
			<th width="60%">参数说明</th>
		</tr>
		<tr>
            <td>appId</td>
			<td>是</td>
			<td>int</td>
			<td>应用标识</td>
        </tr>
		<tr>
            <td>timestamp</td>
			<td>是</td>
			<td>int</td>
			<td>时间戳</td>
        </tr>
		<tr>
            <td>accessToken</td>
			<td>是</td>
			<td>string</td>
			<td>访问凭证</td>
        </tr>
		<tr>
            <td>deviceNumber</td>
			<td>是</td>
			<td>string</td>
			<td>门锁序列号</td>
        </tr>			
    </tbody>
<table>

------

**返回结果**

	{
	    "code": 0
	}

----


**如有问题，请与(April Han)联系**
