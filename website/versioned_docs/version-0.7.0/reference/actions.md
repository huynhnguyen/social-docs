---
title: Actions
id: version-0.7.0-actions
sidebar_label: Actions
custom_edit_url: https://github.com/red-gold/react-social-network/blob/v0.7.0/README.md
original_id: actions
---

This layer is responsible for implementing actions for entities. [Actions](http://redux.js.org/docs/basics/Actions.html) are payloads of information that send data from your application to your store. They are the only source of information for the store.

----

## Authorize

We provide some actions to authorize a user. The authorize actions include singup, login, logout and update password for a user.


----

This action check a user by `email` and `password` to authorize a user to login website. 

```js
dbLogout = () => {}
```

This action is responsible to logout the user.

```js
dbSignup = (user) => {}
```

This action is responsible to register user on the server. `user` parameter is a user object with user information.

```js
dbUpdatePassword = (newPassword) => {}
```

This action is responsible to change user passwaord on the server. `newPassword` parameter is the password that user wants to replace with current password.

```js
login = (uid) => {}
```

This action is responsible to change user state to login state on reducer. `uid` is the user identifire.

```js
logout = () => {}
```

This action is responsible to change user state to logout state on reducer.

```js
signup = (user) => {}
```

This action is responsible to create new user state on reducer.

```js
updatePassword = () => {}
```

This action is responsible to fire reducer method on update password.

## Circle

We provide some actions to authorize a user. The authorize actions include singup, login, logout and update password for a user.

---

```js
dbAddCircle = (circleName) => {}
```

Add a circle on the database. `circleName` is the name of the circle.

```js
dbAddFollowingUser = (cid, userFollowing) => {}
```

Add a user in a circle on the server. `cid` is the identifier of that circle. `userFollowing` is an object of the user which we want to add in a circle.

```js
dbDeleteFollowingUser = (cid, followingId) => {}
```

Delete a user from a circle on the server. `cid` is the identifier of that circle. `userFollowing` is an object of the user which we want to from a circle.

```js
dbUpdateCircle = (newCircle) => {}
```

Update a circle. `newCircle` is a circle object which should be updated.

```js
dbDeleteCircle = (id) => {}
```

Update a circle on the server. `id` is the circle identifier.

```js
dbGetCircles = () => {}
```

Get all circles of current user from server.

```js
dbGetCirclesByUserId = (uid) => {}
```

Get all circles of a specific user from server. `uid` is the user identifier.

```js
addCircle = (uid, circle) => {}
```

Add a circle in redux store. `uid` is the user identifier which we want to add `circle` to, from redux store.

```js
updateCircle = (uid, circle) => {}
```

Add a circle in redux store. `uid` is the user identifier which we want to update `circle` for, from redux store.

```js
deleteCircle = (uid, id)}
```

Delete a circle with `id` identifier which the user with `uid` identifier is the owner of that circle, from redux store.

```js
addCircles = (uid, circles) => {}
```

Add a list of `cricles` for the user with `uid` identifier on redux store.

```js
openCircleSettings = (uid, id) => {}
```

Indicate a circle with `id` identifier for a user with `uid` identifier should be open.

```js
closeCircleSettings = (uid, id) => {}
```

Indicate a circle with `id` identifier for a user with `uid` identifier should be close.

```js
addFollowingUser = (uid, cid, followingId, userCircle) => {}
```

Add a user in a circle.
Add a user with `followingId` identifier in a circle with `cid` identifier belong to the user with `uid` identifier. `userCircle` is an object of user information which we want to add in a circle.

```js
deleteFollowingUser = (uid, cid, followingId) => {}
```

Delete a user from a circle.
Delete a user with `followingId` identifier from a circle with `cid` identifier belong to the user with `uid` identifier. `userCircle` is an object of user information which we want to delete from a circle.

## Comment

---

```js
dbAddComment = (newComment, callBack) => {}
```

Add a comment on a post. `newComment` is an object of comment. `callBack` is a function callback which will be fired when comment add successfully.

```js
dbGetComments = () => {}
```

Get whole comments of current user who is logged in.

```js
dbUpdateComment = (id, postId, text) => {}
```

Update a comment content with `id` identifier on a post with `postId` identifier. `text` is the new content of the comment.

```js
dbDeleteComment = (id, postId) => {}
```

Delete a comment content with `id` identifier on a post with `postId` identifier.

```js
addComment = (data) => {}
```

Add a comment on redux store. Data is an object with comment information.

```js
updateComment = (data) => {}
```

Update a comment on redux store. Data is an object with updated comment information.

```js
addCommentList = (postComments) => {}
```

Add a list of comment on redux store. `postComments` is a list of comments.

```js
deleteComment = (id, postId) => {}
```

Delete a comment with `id` identifier on a post with `postId` identifier on redux store. Data is an object with comment information.

```js
clearAllData = () => {}
```

Delete all comments from redux store.

```js
openCommentEditor = (comment) => {}
```

Open comment editor of a comment. `comment` include comment information.

```js
closeCommentEditor = (comment) => {}
```

Comment comment editor of a comment. `comment` include comment information.

## globalActions

### Global Action Functions

```js
progressChange = (percent, visible) => {}
```

Changes progress bar percentage. `percent` is a number of percentage. `visible` indicate if progress bar should be visible or not.

```js
defaultDataEnable = (status) => {}
```

Sets dafault data loaded.

```js
defaultDataDisable = () => {}
```

Sets dafault data has not loaded.

```js
showNotificationRequest = () =>  {}
```

Show a notification popup that request has been sent.

```js
showNotificationSuccess = () =>  {}
```

Show a notification popup that request has been processed successfully.

```js
hideMessage = () => {}
```

Hide notification popup.

```js
showErrorMessage = (message) => {}
```

Show notification popup with error `message`.

```js
setHeaderTitleOpt = (opt,payload) => {}
```

Sets the title of site header. According `opt` we can set the title. `payload` is an object depend on `opt`.

```js
setHeaderTitle = (text) => {}
```

Sets the title of site header. `text` is the text of title.

```js
openPostWrite = () => {}
```

Show the dialog of writing post.

```js
closePostWrite = () => {}
```

Close the dialog of writing post.

```js
showTopLoading = () => {}
```

Show top loading popup.

```js
hideTopLoading = () => {}
```

Hide top loading popup.

```js
temp = (data) => {}
```

Stor temprory data on redux store.

```js
loadDataGuest = () => {}
```

Execute some procedure like load essential data the time user is unauthorized.

## imageGalleryActions

### Image Gallery Action Functions

## notifyActions

### Notify Action Functions

## postActions

### Post Action Functions

## userActions

### User Action Functions

## voteActions

### Vote Action Functions


> ⭐️ This page needs help. Please help with your contribution. To start click on edit button.
