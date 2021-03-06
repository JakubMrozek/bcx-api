Topics
========

> <Clever topics quote>

Topics are anything in Basecamp that can have comments: Messages, Calendar Events, Uploads, Todos. Messages will appear in the topics index even before they have any comments, but any other topicable type will only appear if there's at least one comment posted.


Get topics
----------

* `GET /projects/1/topics.json` shows topics for this project. We will return 50 topics per page. If the result set has 50 topics, it's your responsibility to check the next page to see if there are any more topics -- you do this by adding `&page=2` to the query, then `&page=3` and so on.
* `GET /topics.json` shows topics for all projects.

```json
[
  {
    "id": 1028592764,
    "title": "Prep the materials before the board meeting with Bezos",
    "excerpt": "I'll be there!",
    "created_at": "2012-03-24T09:53:35-05:00",
    "updated_at": "2012-03-24T09:53:35-05:00",
    "attachments": 0,
    "private": false,
    "trashed": false,
    "last_updater": {
      "id": 149087659,
      "name": "Jason Fried"
    },
    "topicable": {
      "id": 174886926,
      "type": "CalendarEvent",
      "url": "https://basecamp.com/999999999//api/v1/projects/605816632-bcx/calendar_events/174886926-prep-the-materials.json"
    }
  },
  {
    "id": 936075699,
    "title": "Welcome!",
    "excerpt": "Yeah, really, welcome!",
    "created_at": "2012-03-24T09:53:35-05:00",
    "updated_at": "2012-03-24T09:53:35-05:00",
    "attachments": 1,
    "private": false,
    "trashed": false,
    "last_updater": {
      "id": 149087659,
      "name": "Jason Fried"
    },
    "topicable": {
      "id": 936075699,
      "type": "Message",
      "url": "https://basecamp.com/999999999//api/v1/projects/605816632-bcx/messages/936075699-welcome.json"
    }
  }
]
```

The `title` is the original title of the topicable and the `excerpt` is from the latest comment. If a message does not have any comments, the `last_updater` is the creator of the message.
