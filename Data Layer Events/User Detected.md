# User Detected

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "User Detected",
    "user": {
        "custKey": "<custKey>",
        "hashedEmail": "<hashedEmail>",
        "loginStatus": "<loginStatus>",
        "segment": "<segment>",
        "type": "<type>",
        "userHandle": "<userHandle>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|user.custKey|string|Unique identifier of a customer. Any id's considered PII must be hashed.||||||||
|user.hashedEmail|string|The email address of a given user \(pre-hashed in the data layer with hashing algorithm of choice, such as MD5 or SHA-2\).|b642b4217b34b1e8d3bd915fc65c4452|||||||
|user.loginStatus|string|Describes the login state of the user|logged in, logged out, guest|||||||
|user.segment|string|Describes the type of the user. Often used to differentiate customers from employees or associates.|individual, team, employee|||||||
|user.type|string|Determines whether the user is a Customer or Non-Customer based on their login status and purchase history.|customer, prospect|||||||
|user.userHandle|string|captures b2C\_userhandle that is created during the digital cart checkout|11af3885-d055-450e-ade8-2fa78ec4b622|||||||




