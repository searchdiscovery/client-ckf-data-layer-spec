# Login

Fire whenever a user logs in to an account.

## Javascript Code

```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ event_data: null, user_data: null });  // Clear the previous event_data object.
dataLayer.push({
  event: "login",
  event_data: {
    method: "<method>",
  },
  page_data: {
    user_login_state: '<user_login_state>',
    franchise_id: '<franchise_id>'
  },
  user_data: {
    user_id: "<user_id>",
  }
});
```

## Variable Definitions

|Field|Type|Required|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|method|string|recommended|The method used to login.|google, linkedin, email and password|
|user_id|string|recommended|The user identifier|1234567890|
|user_login_state|string|contextual|Set on all events with the authentication status of the visitor.|authenticated, anonymous|
|franchise_id|integer|optional|Set on all events that can be tied back to a franchise.|143, 576, 1134|
