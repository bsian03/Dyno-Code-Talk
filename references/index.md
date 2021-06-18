# References

Here is a list of maybe useful information that you can use in your projects. Please bear in mind that this is not official documentation advice, please make sure you refer to the original documentation.

## Discord Regular Expressions
### Parsed/Mentions

| Description   | Regular Expression                   |
| ------------- | ------------------------------------ |
| Emoji (any)   | `/<a?:(?<name>\w+):(?<id>\d+)>/gi`   |
| Channel       | `/<#(?<id>\d+)>/gi`                  |
| everyone/here | `/@(everyone\|here)/g`               |
| Role          | `/<@$(?<id>\d+)>/gi`                 |
| User          | `/<@!?(?<id>\d+)>/gi`                |
| Timestamp     | `/<t:\d+(?::(?<flag>[tTdDfFR]))?>/g` |

### URLs

| Description      | Regular Expression                                                                                          |
| ---------------- | ----------------------------------------------------------------------------------------------------------- |
| Channel Jump URL | `/https?:\/\/(?:\w+\.)?discord(?:app)?\.com\/channels\/(?<gID>\d+\|@me)\/(?<cID>\d+)/gi`                    |
| Message Jump URL | `/https?:\/\/(?:\w+\.)?discord(?:app)?\.com\/channels\/(?<gID>\d+\|@me)\/(?<cID>\d+)\/(?<mID>\d+)/gi`       |
| Attachment       | `/https?:\/\/cdn\.discordapp\.com\/attachments\/(?<cID>\d+)\/(?<attID>\d+)\/[\w.,;:\?\!\@\^\$-]\.[a-z]+/gi` |
| Invite link      | `/(?:https?:\/\/)?(?:\w+\.)?discord(?:(?:(?:app)?\.com\/invite)\|\.gg)\/(?<code>[a-z0-9-]+)/gi`             |

### Markdown

| Description   | Regular Expression  |
| ------------- | ------------------- |
| Bold          | `/\*\*.+\*\*/g`     |
| Italics       | `/\*.+\*\|_.+_/g`   |
| Strikethrough | `/~~.+~~(?!_)/g`    |
| Underline     | `/__.+__/g`         |
| Spoiler       | `/\|\|.+\|\|/g`     |
| Code string   | ``/`.+`/g``         |
| Code block    | ````/```.+```/g```` |

## Discord Embed Limits

These limits are in characters unless specified

| Location    | Limit      |
| :---------- | :--------- |
| Title       | 256        |
| Description | 2048       |
| Fields      | 25 objects |
| Field name  | 256        |
| Field value | 1024       |
| Footer text | 2048       |
| Author name | 256        |

The total number of characters of the above must also not exceed 6000 characters.
