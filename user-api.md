# Endpoint

`https://n4ii356wm4.execute-api.ap-southeast-1.amazonaws.com/dev`

## /user/category _[GET, UnAuthorized]_

### Response

```javascript
{
    "success": true,
    "errorCode": 0,
    "errorMsg": "",
    "seq": 1548042899,
    "data": [
        #CategoryInfo
    ]
}
```

### /user/category-course/{mainCategory}/{subCategory} _[GET, Unauthorized]_

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": [
    #CourseShortInfo
  ]
}
```

## Course

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

## /user/enroll/term _[POST, Authorized]_

Enroll a term

Request

```javascript
{

  "data": {
    "termId": "term-id1",
    "trainees": [#TraineeInfo]
  }
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

## /user/cancel/term/{termId} _[POST, Authorized]_

Enroll a term

Request

```javascript
{

  "data": {
    "termId": "term-id1",
    "trainee": #TraineeInfo
  }
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


## /user/enroll/class _[POST, Authorized]_

Enroll a class

Request

```javascript
{

  "data": {
    "termId": "term-id1",
    "classId": "class-id1",
    "trainees": [#TraineeInfo]
  }
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

## /user/cancel/class/{classId} _[POST, Authorized]_

Enroll a term

Request

```javascript
{

  "data": {
    "termId": "term-id1",
    "classId": "class-id1",
    "trainee": #TraineeInfo
  }
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


## /user/enroll/term/{termId} _[POST, Authorized]_

Enroll a term

Request

```javascript
{

  "data": {
    "termId": "term-id1",
    "trainees": [#TraineeInfo]
  }
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

## /course-comment/{courseId} _[GET, UnAuthorized]_

Get the comment of a course

Response

```javascript
{
    "success": true,
    "errorCode": 0,
    "errorMsg": "",
    "data": {
      "comments": [#CommentInfo]
    }
}
```

## /course-comment/{courseId} _[POST, Authorized]_

Get the comment of a course

Request

```javascript
{
  "data": #CommentInfo
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

### /complain/[course-code] _[POST, Authorized]_

Request

```javascript
{
  "data": #ComplainInfo
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
  "data": #UserInfo
}
```

### /user/payer _[GET, Authorized]_

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": {
    "users": [#UserInfo]
  }
}
```

### /user/payer _[POST, Authorized]_

Request

```javascript
{
    "data": #UserInfo
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

### /user/trainee _[GET, Authorized]_

Response

```javascript
{
  "success": true,
  "errorCode": 0,
  "errorMsg": "",
  "data": {
    "trainees":[#TraineeInfo]
  }
}
```


### /user/trainee _[POST, Authorized]_

Request

```javascript
{
    "data": #TraineeInfo
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
