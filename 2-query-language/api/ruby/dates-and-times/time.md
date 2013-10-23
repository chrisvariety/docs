---
layout: api-command 
language: Ruby
permalink: api/ruby/time/
command: time 
github_doc: https://github.com/rethinkdb/docs/edit/master/2-query-language/api/ruby/dates-and-times/time.md
related_commands:
    now: now/
    epoch_time: epoch_time/
    iso8601: iso8601/
---

{% apibody %}
r.time(year, month, day[, hour, minute, second], timezone) &rarr; time
{% endapibody %}

Create a time object for a specific time.

__Example:__ Update the birthdate of the user "John" to November 3rd, 1986 UTC.

```rb
r.table("user").get("John").update(:birthdate => r.time(1986, 11, 3, 'Z')).run(conn)
```