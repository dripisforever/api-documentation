Views API
==================

Making a request
----------------

All URLs start with **`http://api.views.ly/v1/`**. The path is prefixed with the account ID, but no `/api/v1` API prefix. Also, note the different domain!

``` shell
curl -H "Authorization: Token $ACCESS_TOKEN" -H 'User-Agent: MyApp (yourname@example.com)' https://3.basecampapi.com/999999999/projects.json
```

To search users, it's the same idea, but you also have to include the `Content-Type` header and the JSON data:

``` shell
curl -H "Authorization: Token $ACCESS_TOKEN" \
  -H 'Content-Type: application/json' \
  -H 'User-Agent: MyApp (yourname@example.com)' \
  -d '{ "name": "My new project!" }' \
  https://api.views.ly/v1/users/search?q=salam
```

Throughout the Basecamp 3 API docs, we include "Copy as cURL" examples. To try the examples in your shell, copy your OAuth 2.0 access token into your clipboard and run:

``` shell
export ACCESS_TOKEN=PASTE_ACCESS_TOKEN_HERE
export ACCOUNT_ID=999999999
```

Then you should be able to copy/paste any example from the docs. After pasting a cURL example, you can pipe it to a JSON pretty printer to make it more readable. Try [jsonpp](https://jmhodges.github.io/jsonpp/) or `json_pp` on OSX:

``` shell
curl -s -H "Authorization: Token $ACCESS_TOKEN" https://3.basecampapi.com/999999999/projects.json | json_pp
```


API endpoints
-------------
<!-- START API ENDPOINTS -->

- [Comments](https://github.com/strivemag/api-documentation/blob/master/sections/comments.md#comments)
- [Follow Suggestions](https://github.com/strivemag/api-documentation/blob/master/sections/documents.md#documents)
- [Followers](https://github.com/strivemag/api-documentation/blob/master/sections/events.md#events)
- [Following](https://github.com/strivemag/api-documentation/blob/master/sections/forwards.md#forwards)
- [Likers](https://github.com/strivemag/api-documentation/blob/master/sections/inboxes.md#inboxes)
- [Likes](https://github.com/strivemag/api-documentation/blob/master/sections/message_boards.md#message-boards)
- [Locations](https://github.com/strivemag/api-documentation/blob/master/sections/messages.md#messages)
- [Notification counts](https://github.com/strivemag/api-documentation/blob/master/sections/message_types.md#get-message-types)
- [Notifications](https://github.com/strivemag/api-documentation/blob/master/sections/people.md#people)
- [Posts](https://github.com/strivemag/api-documentation/blob/master/sections/projects.md#projects)
- [Public Profiles](https://github.com/strivemag/api-documentation/blob/master/sections/question_answers.md#question-answers)
- [Relationships](https://github.com/strivemag/api-documentation/blob/master/sections/questionnaires.md#questionnaires)
- [Search](https://github.com/strivemag/api-documentation/blob/master/sections/questions.md#questions)
- [Users](https://github.com/strivemag/api-documentation/blob/master/sections/recordings.md#recordings)
- [Schedule entries](https://github.com/basecamp/bc3-api/blob/master/sections/schedule_entries.md#schedule-entries)
- [Schedules](https://github.com/basecamp/bc3-api/blob/master/sections/schedules.md#schedules)
- [Templates](https://github.com/basecamp/bc3-api/blob/master/sections/templates.md#templates)
- [To-do lists](https://github.com/basecamp/bc3-api/blob/master/sections/todolists.md#to-do-lists)
- [To-dos](https://github.com/basecamp/bc3-api/blob/master/sections/todos.md#to-dos)
- [To-do sets](https://github.com/basecamp/bc3-api/blob/master/sections/todosets.md#to-do-sets)
- [Uploads](https://github.com/basecamp/bc3-api/blob/master/sections/uploads.md#uploads)
- [Vaults](https://github.com/basecamp/bc3-api/blob/master/sections/vaults.md#vaults)
- [Webhooks](https://github.com/basecamp/bc3-api/blob/master/sections/webhooks.md#webhooks)

<!-- END API ENDPOINTS -->

License
-------

These API docs are licensed under [Creative Commons (CC BY-SA 4.0)](http://creativecommons.org/licenses/by-sa/4.0/). Please share, remix, and distribute as you see fit.
