---
title: "Requirements"
id: requirements
sidebar_label: Requirements
custom_edit_url: https://github.com/red-gold/react-social-network/blob/v0.7.0/README.md
---

I recommend that you get to know React before using React Social. React Social has built by [ReactJS](https://reactjs.org/), so understanding how React fits into web development is important.

Current project is based on Single Page Application which has some advantages and disadvantages(If you're not familiar with the concept of Single Page Applications (SPAs), head over to the [here](https://www.codeschool.com/beginners-guide-to-web-development/single-page-applications) for a quick introduction before you read on.

Depends on your back-end solution your requierments would be different. 
Currently React Social only support [Serverless](https://martinfowler.com/articles/serverless.html) solution by [Firebase](https://firebase.google.com/). [Algolia](https://www.algolia.com/) for [Full Text Search](https://en.wikipedia.org/wiki/Full-text_search) solution , send email to users, SMS and some other features using **outbound networking** on firebase cloud functions.
We always try to optimize data read/write to be fast but cheap. With that if you are going to user Firebase we recommend using [Blaze Plan](https://firebase.google.com/pricing/#blaze-calculator) on Firebase pricing set up your social network.