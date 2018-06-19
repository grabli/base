# API for Grabli.ml (v1)

The entry point https://grabli.ml/api/v1/{methodName}

For understanding authorization mechanic, please learn https://github.com/kahmali/meteor-restivus#default-authentication

## Functions

<dl>
<dt><a href="#clientDataRow/add/_id_Script">clientDataRow/add/:id_Script([name], [content], [rewrite])</a></dt>
<dd><p>Api for client data row list</p>
</dd>
<dt><a href="#clientDataRowDownload/_id/_format">clientDataRowDownload/:id/:format()</a></dt>
<dd><p>Api for client data row downloading</p>
</dd>
<dt><a href="#clientScript/_id_script">clientScript/:id_script([content], [public])</a></dt>
<dd><p>Api for client script</p>
</dd>
<dt><a href="#clientScriptPatch/_id_script/_field">clientScriptPatch/:id_script/:field([schedule], [autoloading], [proxy])</a></dt>
<dd><p>Api for client script patching</p>
</dd>
<dt><a href="#downloadScheduleOutput/_id_script">downloadScheduleOutput/:id_script()</a></dt>
<dd><p>Api for client script schedule output</p>
</dd>
</dl>

<a name="clientDataRow/add/_id_Script"></a>

## clientDataRow/add/:id_Script([name], [content], [rewrite])
Api for client data row list

**Kind**: global function  
**Summary**: <br/>
Api for client data row list <br/>
You can add data rows to script  
**Authrequired**: yes  
**Urlparam**: <code>String</code> :id_Script - id script  

| Param | Type | Description |
| --- | --- | --- |
| [name] | <code>string</code> | name for row |
| [content] | <code>string</code> | data for row |
| [rewrite] | <code>string</code> | flag for rewriting |

**Example**  
```js
POST
curl https://grabli.ml/api/v1/clientDataRow/add/werhg34hrf -X POST -H "X-Auth-Token: f2KpRW7KeN9aPmjSZ" -H "X-User-Id: fbdpsNf4oHiX79vMJ" -d "name=test&content=123"
```
<a name="clientDataRowDownload/_id/_format"></a>

## clientDataRowDownload/:id/:format()
Api for client data row downloading

**Kind**: global function  
**Summary**: <br/>
Api for client data row downloading  
**Authrequired**: yes  
**Urlparam**: <code>String</code> :id - id row  
**Urlparam**: <code>String</code> :format - download|email  
**Example**  
```js
GET
curl https://grabli.ml/api/v1/clientDataRowDownload/324dfdsfew/download -X GET -H "X-Auth-Token: f2KpRW7KeN9aPmjSZ" -H "X-User-Id: fbdpsNf4oHiX79vMJ"
```
<a name="clientScript/_id_script"></a>

## clientScript/:id_script([content], [public])
Api for client script

**Kind**: global function  
**Summary**: <br/>
Api for client script <br/>
You can get script by id <br/>
You can update or insert by id script  
**Authrequired**: yes  
**Urlparam**: <code>String</code> :id_script - id script  

| Param | Type | Description |
| --- | --- | --- |
| [content] | <code>string</code> | Code in HEX format |
| [public] | <code>string</code> | If parameter set "on", then script will be public, all other values will be used as negative condition. |

**Example**  
```js
GET
curl https://grabli.ml/api/v1/clientScript/hdfger34734 -X POST -H "X-Auth-Token: f2KpRW7KeN9aPmjSZ" -H "X-User-Id: fbdpsNf4oHiX79vMJ"
```
**Example**  
```js
POST
curl https://grabli.ml/api/v1/clientScript/hdfger34734 -X POST -H "X-Auth-Token: f2KpRW7KeN9aPmjSZ" -H "X-User-Id: fbdpsNf4oHiX79vMJ" -d "content=inHEXFormat&public=on"
```
**Example**  
```js
DELETE
curl https://grabli.ml/api/v1/clientScript/hdfger34734 -X DELETE -H "X-Auth-Token: f2KpRW7KeN9aPmjSZ" -H "X-User-Id: fbdpsNf4oHiX79vMJ"
```
<a name="clientScriptPatch/_id_script/_field"></a>

## clientScriptPatch/:id_script/:field([schedule], [autoloading], [proxy])
Api for client script patching

**Kind**: global function  
**Summary**: <br/>
Api for client script patching <br/>
You can set up auto loading script by id <br/>
You can set up schedule for script by id  
**Authrequired**: yes  
**Urlparam**: <code>String</code> :id_script - id script  
**Urlparam**: <code>String</code> :field - autoloading|schedule  

| Param | Type | Description |
| --- | --- | --- |
| [schedule] | <code>string</code> | Schedule description in cron format |
| [autoloading] | <code>string</code> | If parameter set "on", then script will be public, all other values will be used as negative condition. |
| [proxy] | <code>string</code> | Proxy URL in format protocol://username:password@host:port. |

**Example**  
```js
POST
curl https://grabli.ml/api/v1/clientScriptPatch/hdfger34734/autoloading -X POST -H "X-Auth-Token: f2KpRW7KeN9aPmjSZ" -H "X-User-Id: fbdpsNf4oHiX79vMJ" -d "autoloading=on"
```
<a name="downloadScheduleOutput/_id_script"></a>

## downloadScheduleOutput/:id_script()
Api for client script schedule output

**Kind**: global function  
**Summary**: <br/>
Api for client script schedule output  
**Authrequired**: yes  
**Urlparam**: <code>String</code> :id_script - id script  
**Example**  
```js
GET
curl https://grabli.ml/api/v1/downloadScheduleOutput/hdfger34734/autoloading -X POST -H "X-Auth-Token: f2KpRW7KeN9aPmjSZ" -H "X-User-Id: fbdpsNf4oHiX79vMJ"
```

* * *

&copy; Viktorov Konstantin and grabli team https://grabli.ml
