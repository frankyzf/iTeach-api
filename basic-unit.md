# Endpoint

`https://n4ii356wm4.execute-api.ap-southeast-1.amazonaws.com/dev/teacher`

## Name Convention

### camelCase style starts with the lowercase

## Basic Info Unit

### CategoryInfo

```javascript
  {
      "id": "main",
      "name": "main",
      "content": [
          {
              "id": "hot",
              "name": "hot"
          },
          {
              "id": "recommend",
              "name": "recommend"
          }
      ]
  }
```

### CourseInfo

```javascript
  {
    "id": "123",
    "name":"class-1",
    "teacherId":"teacher-1",
    "type":"course",
    "location":"",
    "shortDescription":"describe",
    "terms": [{
      "id": "term-id1",
      "name":"term-name1",
      "selfEnrolled":true
    }],
    "introductionType": "",
    "introduction": ""
  }
```

### CourseShortInfo

```javascript
  {
    "id": "123",
    "name":"class-1",
    "teacherId":"teacher-1",
    "teacherBadger": "XXXXX"
    "type":"course",
    "capacity":10,
    "price": 200,
    "enrollment": 9,
    "averateRate": 4.5,
    "location":{
      "address":"xxxx",
      "x":123,
      "y":123
    },
    "shortDescription":"describe"
  }
```


### ClassInfo

```javascript
  {
    "id": "class-id1",
    "startTime":123445,
    "duration": 13,
    "location":{
      "address":"xxxx",
      "x":123.123,
      "y":123.123
    }
  }
```

### TermInfo

```javascript
  {
    "id":"term-id",
    "courseId": "course-id1",
    "teacherId": "teacher-id1",
    "type":"sparse or consecutive",
    "selfEnrolled":true,
    "price": 12.9,
    "capacity":10,
    "enrollment": 9,
    "shortDescription":"describe",
    "startDay":"2018-01-01",
    "endDay":"2018-10-10",
    "location": {
      "address":"xxxx",
      "x": 123,
      "y": 123
    },
    "classes":[ #ClassInfo ]
  }
```

### CommentInfo

```javascript
  {
    "id": "comment-id1",
    "publisherId": "user-id1",
    "publisherInfo": {
      "id": "user-id1",
      "name":"my-name",
      "badge": "badge-pic"
    },
    "content": "",
    "pictures": [{
      "id": "pic-1",
      "url": "url-1"
    }]
  }
```

### TeacherInfo

```javascript
  {
    "id": "teacher-id1",
    "type": "teacher",
    "name": "XXX",
    "phone": "",
    "email": "",
    "badge": "XXXXX",
    "introductionType": "",
    "introduction": ""
  }
```

### UserInfo

```javascript
  {
    "id": "user-id1",
    "familyId": "family-id1",
    "type": "user",
    "name": "XXX",
    "phone": "",
    "email": ""
  }
```

### TraineeInfo

```javascript
  {
    "id": "user-id1",
    "familyId": "family-id1",
    "type": "trainee",
    "name": "XXX",
    "birthday": "1982-1-2",
    "gender": "male"
  }
```

### FamilyInfo

```javascript
  {
    "id": "family-id1",
    "users": [
      #UserInfo
    ],
    "trainee": [
      #TraineeInfo
    ]
  }
```

### EnrollInfo

```javascript
  {
    "user": #UserInfo,
    "number": 2
  }
```

### ComplainInfo

```javascript
{
  "publisher":"xxx",
  "badge": "xxxx",
  "content": "XXXX",
  "picture": "xxxxx"
}
```