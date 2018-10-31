---
title: Installing on Firebase
id: version-0.7.0-install_firebase
sidebar_label: Firebase Client
custom_edit_url: https://github.com/red-gold/react-social-network/blob/v0.7.0/README.md
original_id: install_firebase
---

[![Firestore](https://raw.githubusercontent.com/Qolzam/react-social-network/next/docs/app/firestore2.png)](firebase.google.com/cloud/firestore)
    **Video tutorial**
    
    [![Install React Social Network](https://img.youtube.com/vi/zrqDE82Eny8/0.jpg)](https://www.youtube.com/watch?v=zrqDE82Eny8)
   #### With [Firestore](https://github.com/Qolzam/firestore-social-backend)
   * Configure firebase:
        * If you don't have firebase account, follow [Create firebase account](https://firebase.google.com/)
        * Create Project open the [Firebase Console](https://console.firebase.google.com/) and create a new project.
        * [Enable Firestore](https://firebase.google.com/docs/firestore/quickstart)
        * [Enable firebase storage](https://firebase.google.com/docs/storage/) Go to [firebase console](https://console.firebase.google.com). Click on your `project name`. In `DEVELOP` menu choose `Storage`. Click on `GET STARTED`. In `dialog` click on `GOT IT`.
        * Get [firebase config](https://firebase.google.com/docs/web/setup) Go to [firebase console](https://console.firebase.google.com). Click on your `project name`. In `Project Overview` page click on `Add Firebase to your web app`. In dialog box copy `var config = <copy this area>` configuration key/value. Open config file `react-social-network` root directory in `src/config/environment.dev.ts`. Pate your config in `firebase : <paste here>`.
        * [Enable Email/Password Authentication](https://firebase.google.com/docs/auth/web/password-auth) sign-in on firebase:
            * In the Firebase console, open the Auth section.
            * On the Sign in method tab, enable the Email/password sign-in method and click Save.
        * [Enable OAuth](https://firebase.google.com/docs/auth/) We are supporting sign-in with [Github](https://medium.com/@endactiongroup/enable-github-sign-in-oauth-with-firebase-38b93960e8db), Google and [Facebook](https://medium.com/@endactiongroup/enable-facebook-sign-in-oauth-with-firebase-af7a6651b60c). Following [firebase document](https://firebase.google.com/docs/auth/) you can enable each one you need.
        * [Install Firestore Social Backend](https://github.com/Qolzam/firestore-social-backend) Follow instruction of [Firestore Social Backend](https://github.com/Qolzam/firestore-social-backend)
      * Enable firestore dependencies
        * Go to React Social Network folder in `src/socialEngine.ts` write `useFirestore(provider)` to enable firestore dependencies!