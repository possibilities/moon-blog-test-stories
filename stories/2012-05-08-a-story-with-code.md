---
title: "A Story With Code"
date: 2012-05-08 09:22
---

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

    Meteor.publish('stories', function() {
      var query = {
        publishedAtStamp: {
          $exists : true
        }
      };
      var params = {
        sort: {
          publishedAtStamp: -1
        }
      };
      return Stories.find(query, params);
    });
