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

We provide some actions to authorize a user. The authorize actions include signup, login, logout and update password for a user.


----

```js
dbLogin = (email , password) => {}
```
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
dbUpdatePassword = (newPassword, confirmPassword) => {}
```

This action is responsible to change user password on the server. `newPassword` parameter is the password that user wants to replace with current password. `confirmPassword` parameter is the password which is the same as `newPassword`.

```js
dbSendEmailVerfication = () => {}
```
This action is responsible to send a email verification on the server

```js
dbResetPassword = (email) => {}
```
This action is responsible to reset the password on the server.  `email` parameter is the email corresponding to the the account that user wants to reset. 

```js
dbLoginWithOAuth = (OAuthType) => {}
```
This action is responsible to login with OAuth on server. `OAuthType` is a OAuth object with OAuth information

```js
login = (user) => {}
```

This action is responsible to change user state to login state on reducer. `user` is the user object with user information such as `uid`, `email`, `displayName`,`avatarUrl`.

```js
logout = () => {}
```

This action is responsible to change user state to logout state on reducer.

```js
signup = (user) => {}
```

This action is responsible to create new user state on reducer. `user` parameter is a user object with user information.

```js
updatePassword = () => {}
```

This action is responsible to fire reducer method on update password.

## Circle

We provide some actions to manipulate user circle. The circle actions include add circle, add user to a circle, update circle and user to circle, delete circle and user in circle, get circle and get follower.

---

```js
dbAddCircle = (circleName) => {}
```

This action is responsible to add a circle on the database on server. `circleName` is the name of the circle.

```js
dbFollowUser = (followingCircleId, userFollowing) => {}
```
This action is responsible to add referer user to the following circle of current user on server. `followingCircleId` is the id of circle and `userFollowing` is an object of referer user information.

```js
dbUpdateUserInCircles = (circleIdList, userFollowing) => {}
```
This action is responsible to update user in circle/circles on server. `userFollowing` is an object of referer user information and `circleIdList` is a list of circles which will be updated.


```js
dbDeleteFollowingUser = (userFollowingId) => {}
```
This action is responsible to delete following user on server. `userFollowingId` is the id of following user.

```js
dbUpdateCircle = (newCircle) => {}
```
This action is responsible to update circle on server. `newCircle` is the object of circle which will be updated

```js
dbDeleteCircle = (circleId) => {}
```
This action is responsible to delete a circle from database on server. `circleId` is the id of circle which will be deleted

```js
dbGetCircles = () => {}
```
This action is responsible to get all circles from data base belong to current user on server

```js
dbGetUserTies = () => {}
```
This action is responsible to get all user ties from data base on server

```js
 dbGetFollowers = () => {}
```
This action is responsible to get all followers on server.

```js
dbGetCirclesByUserId = (uid) => {}
```
This action is responsible to get all user circles from data base by user id on server. `uid` is id of user

```js
addCircle = (circle) => {}
```
This action is responsible to create a new circle state on reducer. `circle` is an object of circle information

```js
updateCircle = (circle) => {}
```
This action is responsible to update a circle state on reducer. `circle` is an object of circle information

```js
deleteCircle = (circleId) => {}
```
This action is responsible to delete a circle state on reducer. `circleId` is an id of circle which will be deleted

```js
addCircles = (circles) => {}
```
This action is responsible to add a list of `cricles` state on reducer. `circles` is an object of each circle's information

```js
clearAllCircles = () => {}
```
This action is responsible to clear all data in circle state on reducer. 

```js
openCircleSettings = (circleId) => {}
```

This action is responsible to open circle settings. `circleId` is id of circle.

```js
closeCircleSettings = (circleId) => {}
```
This action is responsible to close opened circle settings.  `circleId` is id of circle.

```js
addFollowingUser = (userTie) => {}
```
This action is responsible to add a user in a circle on reducer. `userTie` is an iterable object of user.

```js
updateUserTie = (userTie) => {}
```
This action is responsible to update the user tie on reducer. `userTie` is an object of user information.


```js
addUserTies = (userTies) => {}
```
This action is responsible to to add user ties on reducer. `userTie` is an object of list of user information.

```js
addUserTieds = (userTieds) => {}
```
This action is responsible to add users who send tie request for current user on reducer. `userTieds` is an object of user information

```js
deleteUserFromCircle = (userId, circleId) => {}
```
This action is responsible to delete the user from a circle on reducer. `userId` is id of user and `circleId` is id of a circle that user will be deleted.

```js
deleteFollowingUser = (userId) => {}
```
This action is responsible to delete a user from a circle on reducer. `userId` is id of user

```js
showSelectCircleBox = (userId) => {}
```
This action is responsible to show the box to select circle. `userId` is id of user

```js
hideSelectCircleBox = (userId) => {}
```
This action is responsible to hide the box to select circle. `userId` is id of user

```js
showFollowingUserLoading = (userId) => {}
```
This action is responsible to show loading on following user. `userId` is id of user

```js
setSelectedCircles = (userId, circleList) => {}
```
This action is responsible to set current user selected circles for referer user on reducer. `userId` is id of user and `circleList` is list of circles.

```js
removeSelectedCircles = (userId) => {}
```
This action is responsible to remove current user selected circles for referer user on reducer. `userId` is id of user

```js
openSelectCircleBox = (userId) => {}
```
This action is responsible to open select circle box. `userId` is id of user

```js
closeSelectCircleBox = (userId) => {}
```
This action is responsible to close select circle box. `userId` is id of user

```js
hideFollowingUserLoading = (userId) => {}
```
This action is responsible to hide loading on following user. `userId` is id of user

## Comment
We provide some actions to manipulate user comment. The comment actions include get comments, update comments, delete comments

---

```js
dbAddComment = (ownerPostUserId, newComment, callBack) => {
```

This action is responsible to add a comment on a post on server. `ownerPostUserId` is id of the owner of the post. `newComment` is an object of comment. `callBack` is a function callback which will be fired when comment add successfully.

```js
dbFetchComments = (ownerUserId, postId) => {}
```

This action is responsible to get all comments from database of the post on server. `ownerPostUserId` is id of the owner of the post while `postId` is id of the post

```js
dbUpdateComment = (comment) => {}
```
This action is responsible to update a comment from database on server. `comment` is an object with comment information


```js
dbDeleteComment = (id, postId) => {}
```

This action is responsible to delete a comment from database on server. `id` is an id of the comment which will be deleted, `postId` is id of the post contains the comment which will be deleted

```js
addComment = (comment) => {}
```

This action is responsible to  add a comment on reducer. `comment` is an object with comment information.

```js
updateComment = (comment) => {}
```

This action is responsible to  update a comment on reducer. `comment` is an object with comment information.

```js
addCommentList = (postComments) => {}
```

This action is responsible to add a list of comment on reducer. `postComments` is a list of comment objects.

```js
deleteComment = (id, postId) => {}
```

This action is responsible to delete a comment on reducer. `id` is id of the comment, `postId` is id of the post

```js
clearAllData = () => {}
```

This action is responsible to delete all comments on reducer.

```js
openCommentEditor = (comment) => {}
```

This action is responsible to open comment editor of a comment. `comment` is an object with comment information.

```js
closeCommentEditor = (comment) => {}
```

This action is responsible to close comment editor of a comment. `comment` is an object with comment information.


## globalActions

We provide some actions to manipulate some frequently used function. The global actions include send newFeed, showNotification

----

```js
dbSendFeed = (newFeed) => {}
```
This action is responsible to add a normal feed on server. `newFeed` is an object with feed information.

```js
showNotificationRequest = () => {}
```
This action is responsible to show notification request on server.

```js
showNotificationSuccess = () => {}
```
This action is responsible to show notification request of success on server.

```js
setSearchRequest = (percent, visible) => {}
```
This action is responsible to set search request on reducer. `percent` is the percentage of search, `visible` indicate if progress bar should be visible or not.

```js
progressChange = (percent, visible) => {}
```

This action is responsible to change progress bar percentage on reducer. `percent` is a number of percentage. `visible` indicate if progress bar should be visible or not.


```js
progressChangeWithKey = (percent, visible, progressKey, meta) => {}
```
This action is responsible to change multiple progress bar percentage with key on reducer.`percent` is a number of percentage. `visible` indicate if progress bar should be visible or not. `progressKey` is the key of the progress. `meta` is the metadata corresponding to the progess

```js
dbLoadTwitterMedia = (accessToken) => {}
```
This action is responsible to load twitter media on server. `accessToken` is token to connect to twitter

```js
initLocale = () => {}
```
This action is responsible to initialize the locale on reducer.

```js
defaultDataEnable = () => {}
```
This action is responsible to set the default data has loaded.

```js
defaultDataDisable = () => {}
```
This action is responsible to set default data has not loaded.

```js
clearLoadedData = () => {}
```

This action is responsible to delete all loaded data on reducer.

```js
loadInitialData = () => {}
```
This action is responsible to load initial data

```js
hideMessage = () => {}
```
This action is responsible to hide the global message pop-up.

```js
showMessage = () => {}
```
This action is responsible to show the `message` pop-up.

```js
setHeaderTitleOpt = (callerKey,payload) => {}
```

This action is responsible to set the title of site header. According `opt` we can set the title. `payload` is an object depend on `opt`.

```js
setHeaderTitle = (text) => {}
```

This action is responsible to set the title of site header. `text` is the text of title.

```js
openPostWrite = () => {}
```

This action is responsible to show the dialog of writing post.

```js
closePostWrite = () => {}
```

This action is responsible to close the dialog of writing post.

```js
showTopLoading = () => {}
```

This action is responsible to show top loading popup.

```js
hideTopLoading = () => {}
```

This action is responsible to hide top loading popup.

```js
showMasterLoading = () => {}
```

This action is responsible to show master loading.

```js
showSendFeedback = () => {}
```
This action is responsible to show feedback

```js
hideSendFeedback =() => {}
```
This action is responsible to hide feedback

```js
temp = (data) => {}
```

This action is responsible to store temprory data on reducer.

```js
loadDataGuest = () => {}
```

This action is responsible to to execute some procedure like load essential data the time user is unauthorized.

```js
openDialog = (type) => {}
```
This action is responsible to open a dialog. `type` is an object of dialog type information which will be opened

```js
 closeDialog = (type) => {}
```
This action is responsible to close a dialog. `type` is an object of dialog type information which will be closed

## imageGalleryActions
We provide some actions to manipulate images and videos in gallery. The imageGallery actions includes get, update delete images and videos.

```js
dbGetImageGallery = () => {}
```

This action is responsible to fetch images for image gallery on server.

```js
dbGetVideoGallery = () => {}
```

This action is responsible to Fetch video for video gallery on server.

```js
dbUploadVideo = (file, fileName, videoThumbnails) => {}
```

This action is responsible to upload video on server. `file` is video file updated to database. `filename` is name of video file. `videoThumbnails` is an object of video thumbnails information.

```js
dbDeletedVideo = (videoId) => {}
```

This action is responsible to delete video on server. `videoId` is the id of video on database.

```js
dbSaveImage = (imageURL) => {}
```

This action is responsible to save image URL to database on server. `imageUrl` is the url of image.

```js
dbDeleteImage = (fileId, folderName, fileName) => {}
```

This action is responsible to delete an image from database on server. `fileId` is id of the image file. `folderName` is the name of folder which contain image file. `fileName` is the name of image file.

```js
 dbUploadImage = (file, fileName) => {}
```

This action is responsible to upload image to database on the server.  `file` is the image file which will be uploaded. `fileName` is the name of uploaded image file.

```js
dbUploadAvatar = (file, fileName) => {}
```

This action is responsible to upload avatar to database on the server. `file` is the image file of avatar which wil be uploaded. `fileName` is the name of uploaded image file.

```js
dbUploadCover = (file, fileName) => {}
```

This action is responsible to upload cover to database on the server.`file` is the image file of cover which wil be uploaded. `fileName` is the name of uploaded image file.

```js
dbDownloadImage = (fileName) => {}
```

This action is responsible to download image from database on server. `fileName` is the name of downloaded image file.


```js
dbFetchAlbumImages = (userId, albumId) => {}
```

This action is responsible to get images in an album on server. `userId` is the id of the user. `albumId` is the id of album which contains images.

```js
dbFetchAvatarImages = (userId) => {}
```

This action is responsible to get avatar of user on server. `userId` is the id of the user that the avatar belongs to.

```js
dbFetchCoverImages = (userId) => {}
```

This action is responsible to get cover images of user on server. `userId` is the id of the user that the cover belongs to.

```js
dbCreateAlbum = (albumPost ,images) => {}
```
This action is responsible to create album in database on server. `albumPost` is an object of album information. `images` is list of object of image information

```js
addImageList = (entities) => {}
```

This action is responsible to dd image list to image gallery on reducer. `entities` is an object of image list information

```js
addAlbumIds = (albumIds) => {}
```

This action is responsible to add album list on reducer. `albumIds` is a list of album id.

```js
 addAlbumImages = (albumId, imageIds) => {}
```

This action is responsible to add album image list id on reducer. `albumId` is the id of the album. `imageIds` is list of image id. 

```js
addAvatarImages = (userId , imageIds: Map<string, boolean>) => {
```

This action is responsible to add avatar images of user on reducer. `userId` is the id of user which own the avatar. `imageIds` is a list of avatar image id.

```js
addCoverImages = (userId, imageIds) => {}
```

This action is responsible to add cover images of user on reducer. `userId` is the id of user which own the cover. `imageIds` is a list of cover image id.


```js
addImage = (image) => {}
```

This action is responsible to add image to gallery on reducer. `image` is an object of image information in gallery.

```js
albumHasMoreImage = (albumId) => {}
```

This action is responsible to indicate more image in album on reducer. `albumId` is the id of album.

```js
albumHasNoMoreImage = (albumId) => {}
```

This action is responsible to indicate no more image in album on reducer. `albumId` is the id of album.

```js
setLastAlbumImage = (albumId, imageId) => {}
```

This action is responsible to indicate the last image in album on reducer. `album` is the id of album. `imageId` is the id of the last image in the album.

```js
deleteImage = (imageId) => {}
```

This action is responsible to delete the image on reducer. `imageId` is the id of the image.

```js
setImageURL = (name, url) => {}
```

This action is responsible to set the image url of the image on reducer. `name` is the image name. `url` is the url of that image. 

```js
addVideo = (video) => {}
```

This action is responsible to add a video to gallery on reducer. `video` is the added video file

```js
addVideoList = (videos) => {}
```

This action is responsible to add list of video to gallery on reducer. `videos` is the video file list.

```js
deleteVideo = (id) => {}
```

This action is responsible to delete a video on reducer. `id` is the id of the video which will be deleted.

```js
clearAllData = () => {}
```

This action is responsible to clear all data in gallery on reducer.

```js
addUploadingPhoto = (photoId ) => {}
```

This action is responsible to add an uploaded photo on reducer. `photoId` is the id of the photo which will be added.

```js
deleteUploadingPhoto = (photoId ) => {}
```

This action is responsible to delete an uploaded photo on reducer. `photoId` is the id of the photo which will be deleted.

```js
clearUploadingPhoto = () => {}
```

This action is responsible to clear an uploading photo on reducer.


```js
sendImageRequest = (name) => {}
```

This action is responsible to send an image request on reducer. `name` is the name of the image request.

## notifyActions
We provide some actions to manipulate with notification. The notify actions includes add, get, delete, seen notifications.

```js
dbAddNotification = (newNotify) => {}
```

This action is responsible to add notification to database on server. `newNotify` is an object of notification information.

```js
dbGetNotifications = () => {}
```

This action is responsible to get all notifications from database on server.

```js
dbDeleteNotification = (id) => {}
```

This action is responsible to delete notification in database on server. `id` is the id of notification. 

```js
dbSeenNotification = (id) => {}
```

This action is responsible to make seen notification in database on server. `id` is the id of notification.

```js
addNotify = () => {}
```

This action is responsible to add notification on reducer.

```js
addNotifyList = (userNotifies) => {}
```

This action is responsible to add list of notification on reducer. `userNotifies` is an object of list of notification information of user

```js
deleteNotify = (id) => {}
```

This action is responsible to delete notification on reducer. `id` is id of notification.

```js
seenNotify = (id) => {}
```

This action is responsible to change notification to has seen status on reducer. `id ` is id of notification. 

```js
clearAllNotifications = () => {}
```

This action is responsible to clear all the notification on reducer.



## postActions
We provide some actions to manipulate with post. The post actions includes add, get, delete, search post/posts

```js
dbAddPost = (newPost, callBack) => {}
```

This action is responsible to add a new normal post to database on server. `newPost` is an object of post information. `callback` is callback function after adding a post. 


```js
dbUpdatePost = (updatedPost, callBack) => {}
```

This action is responsible to update a post to database on server. `updatedPost` is an object of updated post information. `callback` is callback function after adding a post.


```js
dbDeletePost = (id) => {}
```

This action is responsible to delete post from database on server.


```js
dbGetPosts = (page, limit) => {}
```

This action is responsible to get posts from database on server. `page` is number of post pages to get and `limt` is the limitation of post for each page. Default value of `page` is 0 and `limit` is 10.


```js
dbSearchPosts = (query, page, limit) => {}
```

This action is responsible to search posts in database on server. `query` is the keyword of search.`page` is number of post pages to get and `limt` is the limitation of post for each page. Default value of `page` is 0 and `limit` is 10.


```js
dbGetPostsByUserId = (userId, page, limit) => {}
```

This action is responsible to get posts based on each user from database on server. `userId` is the id of user.`page` is number of post pages to get and `limt` is the limitation of post for each page. Default value of `page` is 0 and `limit` is 10.


```js
dbGetPostById = (uid, postId) => {}
```

This action is responsible to get all users post by postId from database on server. `uid` is user id. `postId` is the id of post.


```js
 dbGetPostSearchKey = () => {}
```

This action is responsible to get post by search key from database on server.


```js
setPostSearchKey = (searchKey) => {}
```

This action is responsible to set post by key on reducer. `searchKey` is the searching keyword.


```js
addPost = (post) => {}
```

This action is responsible to add a post on reducer. `post` is an object of post information.


```js
updatePost = (post) => {}
```

This action is responsible to update a post on reducer. `post` is an object of post information.


```js
updatePostComments = (post) => {}
```

This action is responsible to update post comments on reducer. `post` is an object of post information.


```js
updatePostVotes = (post) => {}
```

This action is responsible to update post votes on reducer. `post` is an object of post information.


```js
deletePost = (uid, id) => {}
```

This action is responsible to delete post on reducer. `uid` is the id of user. `id` is post id.


```js
 addPosts = (entities) => {}
```

This action is responsible to add a list of post on reducer. `entities`  is a list of post information.


```js
addStreamPosts = (postIds) => {}
```

This action is responsible to add a list of post for stream on reducer. `postIds` is a list post information.


```js
addSearchPosts = (postIds, overwrite) => {}
```

This action is responsible to add a list of post for search on reducer. `postIds`  is a list of post information.`overwrite` is post searching attribute.


```js
addInstagramPosts = (posts) => {}
```

This action is responsible to add a list of Instagram post on reducer. `posts`  is a list of post information.


```js
 clearAllData = () => {}
```

This action is responsible to clear all data in post store on reducer. 


```js
addImagePost = (uid, post) => {}
```

This action is responsible to add a image post on reducer. `uid` is user id. `post` is an object of post information.


```js
hasMoreDataStream = () => {}
```

This action is responsible to indicate stream has more data on reducer.


```js
notMoreDataStream = () => {
```

This action is responsible to indicate stream has no more data on reducer.


```js
hasMorePostSearch = () => {}
```

This action is responsible to indicate there are more post to search on reducer.


```js
notMorePostSearch = () => {}
```

This action is responsible to indicate there is no more post to search on reducer.



```js
setPageStream = (page) => {}
```

This action is responsible to set the page request of stream  on reducer. `page` is the page to request.


```js
increasePageStream = () => {}
```

This action is responsible to increase page count of stream on reducer.


```js
lastPostStream = (lastPostId) => {}
```

This action is responsible to set last post id of stream on reducer. `lastPostId` is the id of the last post


```js
lastPostSearch = (lastPostId ) => {}
```

This action is responsible to set last post id of search on reducer. `lastPostId` is the id of the last post


```js
hasMoreDataProfile = () => {}
```

This action is responsible to indicate profile posts has more data on reducer.


```js
notMoreDataProfile = (userId ) => {}
```

This action is responsible to  indicate profile posts has no more data on reducer. `userId` is user id.



```js
requestPageProfile = (userId , page: number) => {}
```

This action is responsible to set the page request of profile posts. `userId` is id of user. `page` is page nubmer of request.


```js
lastPostProfile = (userId, lastPostId) => {}
```

This action is responsible to set the last post of profile posts. `userId` is id of user. `lastPostId` is the id of the last post.


## userActions
We provide some actions to manipulate with user. The post actions includes add, get, delete, search post/posts

```js
dbGetUserInfo = () => {}
```

This action is responsible to get user info from database on server.


```js
dbGetUserInfoByUserId = (uid, callerKey) => {}
```

This action is responsible to get user info by user id from database on server. `uid` is id of the user. `callerKey` is key in user profile


```js
 dbUpdateUserInfo = (newProfile) => {}
```

This action is responsible to update user info to database on server. `newProfile` is an object of user profile information


```js
dbGetPeopleInfo = (page, limit) => {}
```

This action is responsible to get people information from database on server. `page` is the people information page, `limit` is number of people information for each page.

```js
dbFetchFindPeople = (page, limit) => {}
```

This action is responsible to get user list fron database on server.`page` is the people information page, `limit` is number of people information for each page. The default value for `page` is 0 and for `limit` is 10

```js
fetchUserSearch = (query, page, limit) => {}
```

This action is responsible to get user list with query key from database on server. `query` is query key. `page` is the people information page, `limit` is number of people information for each page. The default value for `page` is 0 and for `limit` is 10

```js
addUserInfo = (uid, info) => {}
```

This action is responsible to add user information on reducer. `uid` is id of the user. `info` is an object of user information which will be updated.

```js
addFindPeople = (userIds) => {}
```

This action is responsible to add people information on reducer. `userIds` is a list of user id.

```js
setPostSearchKey = (searchKey) => {}
```

This action is responsible to set post search key on reducer. `searchKey` is key for searching.


```js
addUserSearch = (userIds, overwrite) => {}
```

This action is responsible to add user to search list. `userIds` is list of user id. `overwrite` is to overwrite the user if it existed in the search list.

```js
addPeopleInfo = (infoList) => {}
```

This action is responsible to add people informations on reducer. `infoList` is a list of people information.


```js
updateUserInfo = (uid , info: Map<string, any>) => {}
```

This action is responsible to update user informations on reducer. `uid` is user id. `info` is a list of user information.


```js
clearAllData = () => {}
```

This action is responsible to clear all user data on reducer.


```js
openEditProfile = () => {}
```

This action is responsible to open edit profile pop-up.


```js
 closeEditProfile = () => {}
```

This action is responsible to close edit profile pop-up.


```js
addProfilePosts = ( userId, postIds) => {}
```

This action is responsible to add a list of posts for profile users on reducer. `userId` is user id. `postIds` is list of post id which will be added.


```js
 addProfileAlbums = ( userId , albumIds) => {{}
```

This action is responsible to add a list of albums for profile users on reducer. `userId` is user id. `albumIds` is list of albums id which will be added.

```js
hasMoreFindPeople = () => {}
```

This action is responsible to indicate that there are more people in findPeople to show.


```js
notMoreFindPeople = () => {}
```

This action is responsible to indicate that there is no more people in findPeople to show.


```js
hasMoreSearchPeople = () => {}
```

This action is responsible to indicate that there are more people in SearchPeople to show.


```js
notMoreSearchPeople = () => {}
```
This action is responsible to indicate that there is no more people in searchPeople to show.

```js
setFindPagePeoplePage = (page) => {}
```

This action is responsible to set page request of profile posts on reducer. `page` is the page of profile posts.


```js
fetchAlbums = (userId, page, limit) => {}
```

This action is responsible to set page request of user's album on reducer. `userId` is user id. `page` is the page of albums. `limit` is number of ablums for each page.


```js
increasePageAlbum = (userId) => {}
```

This action is responsible to increase album page count of album on reducer. `userId` is user id.


```js
hasMoreDataAlbum = (userId) => {}
```

This action is responsible to indicate that there are more more data to show in profile album posts. `userId` is user id.


```js
notMoreDataAlbum = (userId ) => {}
```

This action is responsible to indicate that there is no more more data to show in profile album posts. `userId` is user id.


```js
requestPageAlbum = (userId, page) => {}
```

This action is responsible to set album page request of profile posts. `userId` is user id. `page` is the request page.


```js
lastPostAlbum = (userId , lastPostId ) => {}
```

This action is responsible to set last album post identification of profile posts. `userId` is user id. `lastPostId` is the id of the last post.


```js
increaseFindPagePeoplePage = () => {}
```

This action is responsible to increase page request of find people page on reducer.


```js
lastUserPeople = (lastUserId ) => {}
```

This action is responsible to set last user identification of find people page.

```js
increaseFollowCountUser = (userId ) => {}
```

This action is responsible to increase user follow count on reducer. `userId` is user id.


```js
decreaseFollowCountUser = (userId) => {}
```

This action is responsible to decrease user follow count on reducer. `userId` is user id.


```js
increaseShareCountUser = (userId ) => {}
```

This action is responsible to increase user share count on reducer. `userId` is user id.


```js
decreaseShareCountUser = (userId ) => {}
```

This action is responsible to decrease user share count on reducer. `userId` is user id.


```js
increaseVoteCountUser = (userId ) => {}
```

This action is responsible to increase user vote count on reducer.
`userId` is user id.

```js
decreaseVoteCountUser = (userId ) => {}
```

This action is responsible to decrease user vote count on reducer.
`userId` is user id.


```js
increasePostCountUser = (userId ) => {}
```

This action is responsible to increase user post count on reducer.
`userId` is user id.

```js
decreasePostCountUser = (userId ) => {}
```

This action is responsible to decrease user post count on reducer.
`userId` is user id.

## userSettingActions
We provide some actions to manipulate with userSetting. The userSetting actions includes get, update and clear userSetting.

```js
dbFetchUserSetting = () => {}
```

This action is responsible to get user setting from database on server.

```js
 dbUpdateUserSetting = (setting) => {}
```

This action is responsible to update user setting in database on server. `setting` is an object of user setting information.


```js
updateUserSetting = (userSetting: Map<string, any>) => {}
```
This action is responsible to update user setting in database on reducer. `setting` is an object of user setting information.


```js
getUserSetting = () => {}
```

This action is responsible to get user setting on reducer.

```js
clearAllUserSetting = () => {}
```

This action is responsible to clear user setting on reducer.

## voteActions
We provide some actions to manipulate with vote. The vote actions includes add, get and delete vote.
------

```js
dbAddVote = (postId ,ownerPostUserId ) => {}
```

This action is responsible to add vote to a post in database on server. `postId` is post id. `ownerPostUserId` is user id of the user who own that post.

```js
dbGetVotes = (userId , postId ) => {}
```

This action is responsible to get vote of a post in database on server. `userId` is user id. `postId` is post id.

```js
dbDeleteVote = (postId , ownerPostUserId ) => {}
```

This action is responsible to delete a vote of a post in database on server. `postId` is post id. `ownerPostUserId` is user id of the user who own that post.

```js
 addVote = (vote) => {}
```

This action is responsible to add a vote to a post on reducer. `vote` is an object of vote information.

```js
 deleteVote = (userId , postId ) => {}
```

This action is responsible to delete a vote of a post on reducer. `postId` is post id. `userId` is user id of the user who vote that post.



```js
addVoteList = (votes) => {}
```

This action is responsible to add a list of vote on reducer. `votes` is an object of vote list information.

```js
 clearAllvotes = () => {}
```

This action is responsible to clear all vote data on reducer.

This action is responsible to
> ⭐️ This page needs help. Please help with your contribution. To start click on edit button.
