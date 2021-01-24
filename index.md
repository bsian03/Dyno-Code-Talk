# Welcome to Dyno's #code-talk channel!
## Rules
1. All [Dyno Server](https://discord.com/channels/203039963636301824/203039963636301824) rules apply! No invites, no advertising, no spam!
2. Please only use this channel if you have any **code** issues, questions or conversations. Anything else should go in their respective channels.
3. Do not ping anyone for help/support in this channel.
4. We appreciate everyone's help and contribution here, however please do not start any useless arguments if it's something that is minor.
5. Do not ask people to make stuff/do code for you, whether it be bots, websites etc.

You will be moderated as usual if you cause any arguments or issues.

## What is #code-talk?
Simply put it, it's a channel where developers, both beginners and professionals, can share, help and have conversations in. Whilst primarily aimed at Discord Bot development, you can also get help regarding development outside of Discord, e.g. APIs, frontend and hardware, applications etc as well as resources/information regarding development. The community here are mostly comprised of people who are knowledgable at JavaScript and TypeScript, however there are also users who are proficient at other languages as well.

## I need help with my code!
This is where the community come in - you included! We have some general guidelines for you to help us understand what the issue is and what you're working with. 

1. Do your job
    - Look at the documentation
    - Read the error
    - Google the issue you're having
2. Ask for help nicely and give appropriate information
    - The language used
    - Library/tech used
    - Expected behaviour
    - Actual behaviour
    - Error message
    - The section of code where you need help with

**General tips**
- We need context
- Try to log everything to the console/terminal to debug what/where the issue is first
- Read the error, try to understand what it's saying
- Google the error/issue you're having

We can, for instance, help you identify errors if you are stuck, give you tips on how to do something or the best way of achieving something.

## How to read JavaScript errors (example)
```js
TypeError: Cannot read property 'replace' of undefined
    at Object.usergame (/path/to/project/misc/utils.js:281:49)
    at Command.bot.registerCommand [as execute] (/path/to/project/commands/info/status.js:11:31)
    at Command.executeCommand (/path/to/project/node_modules/eris/lib/command/Command.js:384:26)
    at Command.process (/path/to/project/node_modules/eris/lib/command/Command.js:344:25)
    at CommandClient.onMessageCreate (/path/to/project/node_modules/eris/lib/command/CommandClient.js:154:50)
    at CommandClient.emit (events.js:193:13)
    at Shard.emit (/path/to/project/node_modules/eris/lib/gateway/Shard.js:1928:26)
    at Shard.wsEvent (/path/to/project/node_modules/eris/lib/gateway/Shard.js:425:26)
    at Shard.onWSMessage (/path/to/project/node_modules/eris/lib/gateway/Shard.js:1767:26)
    at WebSocket.ws.onmessage (/path/to/project/node_modules/eris/lib/gateway/Shard.js:1645:33)
```
Let's break this down line by line. 
```js
TypeError: Cannot read property 'replace' of undefined
```
This is the error that has occured.
- `TypeError` tells you what kind of error has occured. In JavaScript, the defaults are `Error`, `EvalError`, `InternalError`, `RangeError`, `ReferenceError`, `SyntaxError`, `TypeError` and `URIError`. You can read more about types of errors [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error/).
- `Cannot read property 'replace' of undefined` is the error message. This tells you that JavaScript is trying to access the property `replace` from something that is undefined, aka something that doesn't exist.

```js
at Object.usergame (/path/to/project/misc/utils.js:281:49)
```
This is where the error originated from. The first line after the error message is always where the error originated from. 
- `at Object.usergame` This tells you the section of code where the error occured. In this case it is the `usergame` property of an object.
- `##(/path/to/project/misc/utils.js:281:49)` This tells you exactly where the error is located. In this case, it is located in the file at `##/path/to/project/misc/utils.js` on line 281, character 49. Your code/text editor should show you where that is.

```js
at Command.bot.registerCommand [as execute] (/path/to/project/commands/info/status.js:11:31)
```
This line tells you what referenced the line above.
- `at Command.bot.registerCommand`, similarly above, tells you what section of code referenced the line above. In this case it is the `registerCommand` property of the `bot` object, which is a property of the `Command` object.
- `[as execute]` This may or may not show in your error, depending on the context. This is the name of a parameter. This more than likely does not matter and you can ignore this.
- `##(/path/to/project/commands/info/status.js:11:31)` Again, this tells you exactly where the error is located.

This pattern repeats until there is nothing more to reference from. In the case of JavaScript, if the origin of the error is somewhere in the `node_modules` folder, it is more than likely that it is not an issue in that location, and you should keep going down the list of locations until you get to your project code, and see what is causing the error to occur.