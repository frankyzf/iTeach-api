# Endpoint

`https://n4ii356wm4.execute-api.ap-southeast-1.amazonaws.com/dev`

## /teacher/my-courses _[GET, Authorized]_

### Response

```javascript
{
    "success": true,
    "errorCode": 0,
    "errorMsg": "",
    "seq": 1548042899,
    "data": [
        #CourseShortInfo
    ]
}
```

## /course/{courseId} _[GET, UnAuthorized]_

Fetch a course info

Response

```javascript
{
    "success": true,
    "errorCode": 0,
    "errorMsg": "",
    "data": #CourseInfo
}
```

## /course/{courseId} _[POST, Authorized]_

Update a course

Request

```javascript
{

  "data": #CourseInfo
}
```

Response

```javascript
{
    "success": true,
    "errorCode": 0,
    "errorMsg": "",
    "data": #CourseInfo
}
```

## /course/{courseId} _[PUT, Authorized]_

Create a new course

Request

```javascript
{

  "data": #CourseInfo
}
```

Response

```javascript
{
    "success": true,
    "errorCode": 0,
    "errorMsg": "",
    "data": #CourseInfo
}
```

## /term/{termId} _[GET, UnAuthorized]_

Fetch a term info

Response

```javascript
{
    "success": true,
    "errorCode": 0,
    "errorMsg": "",
    "data": #TermInfo
}
```

## /term/{termId} _[POST, Authorized]_

Update a term

Request

```javascript
{

  "data": #TermInfo
}
```

Response

```javascript
{
    "success": true,
    "errorCode": 0,
    "errorMsg": "",
    "data": #TermInfo
}
```

## /term/{termId} _[PUT, Authorized]_

Create a new term

Request

```javascript
{

  "data": #TermInfo
}
```

Response

```javascript
{
    "success": true,
    "errorCode": 0,
    "errorMsg": "",
    "data": #TermInfo
}
```

## /teacher/term/add-enrolls _[POST, Authorized]_

add users to a term

Request

```javascript
{

  "data": {
    "termId": "XXXX",
    "users": [{
      "phone": "XXXXX",
      "number": 1,
      "status": "paid"
    }]
  }
}
```

Response

```javascript
{
    "success": true,
    "errorCode": 0,
    "errorMsg": "",
    "data": {
      "enrolls": [#EnrollInfo]
    }
}
```


## /teacher/term/remove-enrolls _[POST, Authorized]_

remove a user from a term

Request

```javascript
{

  "data": {
    "termId": "XXXX",
    "user": {
      "id": "user-id1",
      "phone": "XXXXX",
      "number": 1,
      "status": "paid"
    }
  }
}
```

Response

```javascript
{
    "success": true,
    "errorCode": 0,
    "errorMsg": "",
    "data": {
      "enrolls": [#EnrollInfo]
    }
}
```