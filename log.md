# 100 Days Of Code - Log

### Day 1: Tuesday, July 30, 2019

**Today's Progress**: I forked this repository and made my first entry in this log. I worked on the qryuser.go file, where I spent 15 minutes trying to figure out how to run SQL queries using the go-sql-driver. After writing half the query I needed to find users, I decided to change direction and work on my first commit where I follow the Hello Service tutorial that @daved wrote for us. I spent more than an hour this first day, but I got my [first PR](https://github.com/OpenEugene/openboard/pull/48/commits/612ba1b87df560e82af7fc49c224f5ff58a9b863) submitted. I also gave some feedback on @mckelveygreg's [PR](https://github.com/OpenEugene/openboard/pull/42#pullrequestreview-268759359).

**Thoughts** Since coming back from #GopherCon 2019, I've been pumped about keep up with my Go studies and projects. When @mckelveygreg challenged me to 100 Days of Code, I readily accepted. What I've wanted to work on lately has been the OpenBoard project. I haven't been making much progress because I've been distracted by Netflix and games on my smart phone. This coding challenge should put me on a more productive track. I'm so glad to have such encouraging friends!

**Link(s) to Work**
1. [OpenEugene OpenBoard](https://github.com/OpenEugene/openboard)

### Day 2: Wednesday, July 31, 2019

**Today's Progress**: Got a few more commits in for openboard user service. I'm back at the place I left from yesterday when I was in the middle of the find users query. I wasn't able to proceed any further in the query because I don't know how users are being found. Are we finding them with their email addresses? Their roles? Any of the above? There were a few segways I took from the main code. I installed libsecret on my machine so I can store credentials with git. I also adjusted a keyboard shortcut setting in VS Code so it acts more like Sublime.

**Thoughts** I noticed that Daved had built the go code (maybe with `go build`?), and that go.mod and go.sum were generated, which were in the Hello Service commits. I'll go ahead and run that command after I'm finished writing the queries.

**Link(s) to Work**
1. [OpenEugene OpenBoard](https://github.com/OpenEugene/openboard)

### Day 3: Thursday, August 1, 2019

**Today's Progress**: Since I didn't know what information was going to be used to find users, I asked the other devs in the openboard channel in our Slack. Meanwhile, I made up a query using my best guess, given what was in the user.proto file. I also asked where I type `go build` because I can't remember how to do that. Tomorrow, I can work on the roles. I'll first need to make a migration for the tables before writing the queries. Once the roles table is put in, I'll be able to add JOIN to the find users query to find by roleIDs.

**Thoughts** I introduced someone to #100DaysOfCode by explaining what it was.

**Link(s) to Work**
1. [OpenEugene OpenBoard](https://github.com/OpenEugene/openboard)

### Day 4: Friday, August 2, 2019

**Today's Progress**: No response to my questions on Slack, but I have my guesses. I created a roles table migration because we have a function to add roles. Not sure how roles and users are linked, but I'll ask Tuesday when we have our OpenBoard Meetup meeting. I finished the add/update and fine roles query. 

I noticed the go.mod and go.sum files in openboard/back/internal, so I ran `go build -o /home/frankie/code/bin` as per my understanding of Daved's instructions in the [Readme](https://github.com/OpenEugene/openboard/tree/master/back). I got this error:
```can't load package: package .: no Go files in /home/frankie``` Strange, because there are a few .go files in the subdirectories. I sent a Go developer friend a DM on Slack to see if he can help.

I read [Golang 101 Hacks](https://nanxiao.gitbooks.io/golang-101-hacks/content/posts/go-build-vs-go-install.html) to try to understand how to use `go build`, but it was too simplistic, giving an example of how to build one file, hello.go, in one directory.

I ran `go get` where my userdb.go file was, and it showed a lot of errors. I didn't know I couldn't split a long query string into multiple lines. It makes me wonder how we can make the code more readable. Do I just use word wrap with my text editor? 

**Thoughts** Feeling a bit lost with the `go build` stuff, but hopefully whatever someone tells me, I can just repeatedly use that command for a while. Next step will be to fix the errors that show up with `go get` and try to build the program so I can run it.

**Link(s) to Work**
1. [OpenEugene OpenBoard](https://github.com/OpenEugene/openboard)

### Day 5: Saturday, August 3, 2019

**Today's Progress**: Alex observed that our code was using Go dependencies pre-Go 1.11. Now that Go uses Modules, maybe we can switch. Daved said he'll be back in town on Monda and would be able to help with the modules question then. 

Meanwhile, I ran `go get` and there were a lot of errors I had to fix. My latest commit was making those fixes.

**Thoughts** Alex showed me his personal website on GitHub and it looked really professional, skillfully made, and sleek. I was really impressed. He said all he used were static HTML files. Of course, this mean that I want to make a website. I'm not sure what to put in it, but that might be something I do for Day 6.

**Link(s) to Work**
1. [OpenEugene OpenBoard](https://github.com/OpenEugene/openboard)
