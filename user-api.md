## Endpoint

`https://api.alphachain.com/v1`

## Main page

### /main/catagorize _[GET, Unauthorized]_

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": [
    {
      "code":"code-1",
      "name":"catagory-1",
      "icon":"base-64 encode"
    }
  ]
}
```

### /main/hot _[GET, Unauthorized]_

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": [
    {
      "name":"class-1",
      "teacher":"teacher-1",
      "type":"course",
      "capacity":10,
      "price": 12.9,
      "enrollment": 9,
      "avg-rate": 4.5,
      "short-description":"describe"
    }
  ]
}
```

### /main/slide _[GET, Unauthorized]_

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": [
    {
      "name":"class-1",
      "url":"http://abc.123.com/aaaa.pic"
    }
  ]
}
```

### /main/search _[POST, Unauthorized]_

Request

```javascript
{

  "keyword": "XXXX"
}
```

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": [
    {
      "code":"codeXXX",
      "name":"class-1",
      "teacher":"teacher-1",
      "type":"course",
      "capacity":10,
      "price": 12.9,
      "enrollment": 9,
      "avg-rate": 4.5,
      "short-description":"describe"
    }
  ]
}
```

## catagory

### /catagory/sub-catagory _[GET, Unauthorized]_

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": [
    {
      "code":"xxx",
      "name":"sub-catagory-1",
    }
  ]
}
```

### /catagory/sub-catagory/[code]/highest-rate _[GET, Unauthorized]_

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": [
    {
      "code":"codeXXX",
      "name":"class-1",
      "teacher":"teacher-1",
      "type":"course",
      "price": 12.9,
      "capacity":10,
      "enrollment": 9,
      "avg-rate": 4.5,
      "short-description":"describe"
    }
  ]
}
```

### /catagory/sub-catagory/[code]/nearest _[GET, Unauthorized]_

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": [
    {
      "code":"codeXXX",
      "name":"class-1",
      "teacher":"teacher-1",
      "type":"course",
      "capacity":10,
      "price": 12.9,
      "enrollment": 9,
      "avg-rate": 4.5,
      "short-description":"describe"
    }
  ]
}
```

### /catagory/sub-catagory/[code]/search _[POST, Unauthorized]_

Request

```javascript
{

  "keyword": "XXXX"
}
```

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": [
    {
      "code":"codeXXX",
      "name":"class-1",
      "teacher":"teacher-1",
      "type":"course",
      "capacity":10,
      "price": 12.9,
      "enrollment": 9,
      "avg-rate": 4.5,
      "short-description":"describe"
    }
  ]
}
```

## Course

### /course/introduction/[code] _[GET, Unauthorized]_

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": [
    {
      "code":"codeXXX",
      "name":"class-1",
      "teacher":"teacher-1",
      "type":"course",
      "self-enrolled": true,
      "avg-rate": 4.5,
      "short-description":"describe",
      "large-pic":"xxxx",
      "small-pic":"XXXX",
      "terms":[
        {
          "code":"XXX",
          "name":"cccc",
          "capacity":10,
          "enrollment": 9,
          "price": 12.9
        }
      ]
    }
  ]
}
```

### /course/rate/[course-code] _[GET, Unauthorized]_

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": [{
      "user": "XXXX",
      "comment":"XXXXX",
      "video": [{
        "code":"",
        "name" :"XXX",
        "url":""
      }]
      "picture": [{
        "code":"",
        "name" :"XXX",
        "url":""
      }]
    }]
}
```

### /course/complain/[course-code] _[POST, Authorized]_

Request

```javascript
{

  "complain": "XXXX"
}
```

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": {}
}
```

### /course/consultant/[course-code] _[POST, Authorized]_

Request

```javascript
{

  "consultant": "XXXX"
}
```

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": {}
}
```

### /course/terms/try-cancel _[POST, Authorized]_

Request

```javascript
{
  "course-code":"XXX",
  "term-code":"YYY",
  "enroller":[
    {
      "id":"XXX",
      "name":"XXXX"
    }
  ]
}
```

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": {
      "cancel-fee": 12.9,
      "refund":10,
      "total-fee": 9,
      "token":"XXXXXX"
    }
}
```

### /course/terms/confirm-cancel _[POST, Authorized]_

Request

```javascript
{
  "course-code":"XXX",
  "term-code":"YYY",
  "action-token":"XXXXX"
}
```

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": {}
}
```

### /course/terms/class/[course-code]/[term-code] _[GET, Authorized]_

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": {
      "price": 12.9,
      "capacity":10,
      "enrollment": 9,
      "short-description":"describe",
      "start-time":"xxxx",
      "end-time":"XXXX",
      "classes":[
        {
          "code":"XXX",
          "name":"cccc",
          "datetime":123445,
          "location":{
            "x":123.123,
            "y":123.123
          }
        }
      ]
    }
}
```

### /course/terms/class/try-cancel _[POST, Authorized]_

Request

```javascript
{
  "course-code":"XXX",
  "term-code":"YYY",
  "class-code":"ZZZ",
  "enroller":[
    {
      "id":"XXX",
      "name":"XXXX"
    }
  ]
}
```

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": {
      "cancel-fee": 12.9,
      "refund":10,
      "total-fee": 9,
      "token":"XXXXXX"
    }
}
```

### /course/terms/class/confirm-cancel _[POST, Authorized]_

Request

```javascript
{
  "course-code":"XXX",
  "term-code":"YYY",
  "class-code":"ZZZZ",
  "action-token":"XXXXX"
}
```

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": {}
}
```

## user

### /user/myself _[GET, Authorized]_

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": {
    "id":"XXXX",
    "name":"XXXX",
    "phone":"ZZZZ"
  }
}
```

### /user/family-supervisor _[GET, Authorized]_

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": [{
    "id":"XXXX",
    "name":"XXXX",
    "phone":"ZZZZ"
  }]
}
```

### /user/trainee _[GET, Authorized]_

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": [{
    "id":"XXXX",
    "name":"XXXX",
    "birthday":1233333
  }]
}
```

### /user/add-trainee _[POST, Authorized]_

Request

```javascript
{
    "name":"XXXX",
    "birthday":1233333
}
```

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": {}
}
```
