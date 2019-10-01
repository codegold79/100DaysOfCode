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

### Day 6: Sunday, August 4, 2019

**Today's Progress**: I started a static webpage on GitHub with some HTML, CSS, and a lot of time trying to figure out GIMP. It looks terrible, but I have some ideas as to how to fix it. I have my code on a branch that hasn't been merged yet. I'll merge to master when I'm ready to show it. Thankfully, because it's a static site, it's easy to test.

**Thoughts** It's tough to have to consider how to make a page look nice. I'm glad I'm a backend dev.

**Link(s) to Work**
1. [Codegold Personal Webpage](https://codegold79.github.io/)

### Day 7: Monday, August 5, 2019

**Today's Progress**: Made a lot of formatting changes to the site, but it still looks terrible. I think I might need help from someone artistic as well as maybe follow a tutorial to figure out how to make this page mobile responsive. Front end development is hard. Alex (@appins) completely configured my laptop to run i3. It looks and runs amazingly. I still have a few tweaks to make like the light-locker.

**Thoughts** Thanks to Alex, i3 is so much less daunting. I can start, close, and quit apps, open them with horizontal or vertical split, log out of i3, open a terminal...Feels pretty good.

**Link(s) to Work**
1. [Codegold Personal Webpage](https://codegold79.github.io/)

### Day 8: Tuesday, August 6, 2019

**Today's Progress**: Greg suggested I use grid instead of floating divs to make my page more responsive. After adding some more pictures and making some more adjustments, I pushed changes to master. After all, how can I get helpful feedback unless someone sees it? I did all this while using i3--pretty nifty! I printed out the cheat sheet which was helpful. I'm doing more and more from the command line like resizing images. I even used `>>` in bash to append the output of `cat` from one file to another. I learned that trick from a Linux systems admin at GohperCon 2019.

**Thoughts** I love that I'm becoming more comfortable with the command line. I am so appreciative of the people around me who are there to help and make my projects more fun and less stressful.

**Link(s) to Work**
1. [Codegold Personal Webpage](https://codegold79.github.io/)

### Day 9: Wednesday, August 7, 2019

**Today's Progress**: Made the text readable and adjusted the colors. Final re-alignment. I think I'm done with my webpage for the time being. 

**Thoughts** None

**Link(s) to Work**
1. [Codegold Personal Webpage](https://codegold79.github.io/)


### Day 10: Thursday, August 8, 2019

**Today's Progress**: Now that I'm using i3wm, my touchpad two-finger click didn't work so I followed instructions at https://cravencode.com/post/essentials/enable-tap-to-click-in-i3wm/ to get that working again. Fun thing is, it also told me how to get 3 finger click as middle click to work, so that's a plus. I also found the settings Alex put in place for switching keyboard layout languages and i3lock screen. For the latter, it was interfering with my vim, so I set the language toggle to something different. As for the latter, there was a blank screen, so I put my own wallpaper up. Of course, the wallpaper was the not the proper dimension, so I looked up how to resize image with ImageMagick from the command line.

**Thoughts** My work today started with Alex's advice that I install the repo light-locker. It's a bit confusing because I already have light-locker, but there are other repos with the same name, but different author. Alex's suggestions for continuing configuration on the config he gave me was, 
> you need light-locker from the repos. And haikarainen/light and Stark/siji. Light locker is for locking your computer when you close your lid. Light is for the backlight. And siji is an icon font.

**Link(s) to Work**


### Day 11: Friday, August 9, 2019

**Today's Progress**: The goal was to get the function keys to be able to adjust the backlight levels on my screen. I followed the instructions from (FOSS Fix Brightness Control)[https://itsfoss.com/fix-brightness-ubuntu-1310/] but it didn't work. I commented out `bindsym XF86MonBrightnessUp exec light -A 5` because in the CLI, `light -A 5` doesn't change the setting (displayed when typing just `light`). I followed other instructions such as the one (here)[https://askubuntu.com/questions/47364/laptop-brightness-problem-on-toshiba-portege-r705-p35], but to no avail. 

**Thoughts** I guess my 100 days of code can be spent configuring Ubuntu as there is so much that can be done.

**Link(s) to Work**

### Day 12: Saturday, August 10, 2019

**Today's Progress**: I read through chapter 1 again of The Go Programming Language by Donovan and Kernighan, as well as the first two chapters of Learn Linux in a Month of Lunches by Ovadia.

**Thoughts** The reads were more fun as the words made much more sense, now that I know the basics.

**Link(s) to Work**

### Day 13: Sunday, August 11, 2019

**Today's Progress**: I Read through ch7 of Ovadia's Linux book. Now I understand the difference between a codec and a driver, and what a kernal does. So, I was able to find out today, using lspci, that my audio, whose controls aren't working in i3, use the snd_hda_intel driver. I tried to find what driver controls the screen, but there didn't seem to be one. Maybe it's controlled by something else.

**Thoughts** I read more than an hour today, given how interesting and useful the topics were.

**Link(s) to Work**

### Day 14: Monday, August 12, 2019

**Today's Progress** I am in the middle of ch14 in Ovadia's Linux book now where it is describing the Linux directory structure. I've only known that certain commands, in the form of binaries were in /bin, but never new what /sbin held, and other directories. Very glad to get the rest of the picture.

**Thoughts** Today was very busy, an we need to take a nap before heading out to catch a flight. Thank goodness reading a book counts as coding. If it weren't for being able to read on the subway or on the bus, I don't think I could have made any progress in this 100DayOfCode challenge.

**Link(s) to Work**

### Day 15: Tuesday, August 13, 2019

**Today's Progress** Made it to ch20  of Learn Linux in a Month of Lunches. I'm continuing to learn useful commands and best practices regarding upgrading, security, encryption, transferring files, and so forth.

**Thoughts** 

**Link(s) to Work**

### Day 16: Wednesday, August 14, 2019

**Today's Progress** I finished Ovadia's book earlier than I thought. It only had 23 chapters when I expected between 28-31. Ch23 mentioned Git, making me think I should read a Git book. I started Ry's Git Tutorial, available for free at https://www.amazon.com/Rys-Git-Tutorial-Ryan-Hodson-ebook/dp/B00QFIA5OC. I just finished ch4.

**Thoughts** I should probably think about what I want to do in terms of coding next, instead of just reading books.

**Link(s) to Work** https://github.com/codegold79/ry-git-tutorial.git

### Day 17: Thursday, August 15, 2019

**Today's Progress** I was itching to get some Go code written and I thought I'd put my energies to writing a parser for a huge log file (over 1 gb) that can parse out certain text using the regexp package and store the info into a map. So far, I was able to use bufio to read a tiny version of the log file, match substrings from each line, and store the strings into a map that counts how many times the matched string showed up in the log.

**Thoughts** The part that I don't even know how to get started on is how to break up my main function, which has all the code, into smaller functions that do small things. I guess that will come later.

**Link(s) to Work** https://github.com/codegold79/laravel-log-parser.git

### Day 18: Friday, August 16, 2019

**Today's Progress** I copied over lines from the actual laravel.log so I can work with real data. I set up the regular expressions such that three important lines of text would match. Then, I made a switch statement with the three different matches being each a case. I wrote out skeleton code for which slices they should be creating and/or populating, if any.

**Thoughts** I'm not sure when I'll need to use a pointer, but it seems if three different functions will need to refer to the same slices, then maybe those might need to be passed pointers? I'll just go with that for now.

**Link(s) to Work** https://github.com/codegold79/laravel-log-parser.git

### Day 19: Saturday, August 17, 2019

**Today's Progress** I did some studying on slices and arrays and it turns out I can't use them to store times, counts, and strings all in one place. I'll need to use three different maps instead. Then, for the imageSpeeds information, I'll need to make another map that holds an array of four items. These items all have to be the same type, so I'll try to make them all integers. I had to research how Go processes time and it seems the "time" package has what I need. The most unusual part of that package is how I use January 2, 2006 to make the time formats.

**Thoughts** I think I'll try to do what Daved did in openBoard HelloService tutorial regarding setting the maps. I'll just save information in separate functions without passing the maps as arguments. They'll exist outside the functions and so can be saved directly, since they all have access to it.

**Link(s) to Work** https://github.com/codegold79/laravel-log-parser.git

### Day 20: Monday, August 19, 2019

**Today's Progress** I fleshed out most of the remaining functions. What is left is the last function, the image processing time summary, because I can't seem to change the values in the array in the map. The error I get is that it cannot assign to the array item. The strange thing is, I can print the value of the array item, but I can't change it. This is what's causing the error: 
```
func main() {
	mapp := map[string][4]int{"one": {1, 2, 3, 4}}
	mapp["one"][0]++
}
```

**Thoughts** Hopefully, I'm missing something small in the syntax. Otherwise, what is the use of maps if I can't change the values in them?

**Link(s) to Work** https://github.com/codegold79/laravel-log-parser.git

### Day 21: Tuesday, August 20, 2019

**Today's Progress** Two devs showed how I could increment array items in a map in #Golang. Alex treated the arrays as pointers and Daved retrieved the values, saved them to a variable, changed it, and saved it in the map. I had some panics in the code as I didn't anticipate some of the log entries to be what they were. But, I have my first working version of the program now.

**Thoughts** I didn't think I missed a day, but I realize I didn't have a Twitter entry for Sunday, August 18. I swear I thought I had done coding that day, but I guess not. I heard from Greg that if it wasn't tweeted, it didn't happen. Oh well.

**Link(s) to Work** https://github.com/codegold79/laravel-log-parser.git

### Day 22: Wednesday, August 21, 2019

**Today's Progress** I formatted the map using Sprintf, including a couple calculations. I used WriteString to newly created file that would sever as a CSV report. I added a few issues to work on in GitHub.

**Thoughts** After spending this week writing this code, I don't think it's really that helpful. Before I spend a lot of work making this production ready, I might demonstrate it to Nik and see if he finds it to be useful.

**Link(s) to Work** https://github.com/codegold79/laravel-log-parser.git

### Day 23: Thursday, August 22, 2019

**Today's Progress** I added incomplete counts that weren't counted previously due to missing jobID to the idx map. I found out how to cross compile to a windows/amd64 executable. I think I'm done with this project for now.

**Thoughts** There are a couple projects I can work on next. I can work on the post service in openboard. The other one is working on learning Kubernetes since companies that are looking for Go devs seem to also want people who know K8. If I run out of things to do, I can go back to going through Ry's Git Tutorial. There certainly is plenty to do.

**Link(s) to Work** https://github.com/codegold79/laravel-log-parser.git

### Day 24: Friday, August 23, 2019

**Today's Progress** I switched back to the openboard project and submitted five commits on the back/postsrv-build-the-post-service branch. I followed the helosvc tutorial very closely.

**Thoughts** My coworker tested out the laravel.log parser and found an error. I'll have to go back and debug it. Daved would not be pleased I had such poor error handling.

**Link(s) to Work** https://github.com/OpenEugene/openboard.git, https://github.com/OpenEugene/openboard/pull/49/commits

### Day 25: Saturday, August 24, 2019

**Today's Progress** I submitted two more commits on the back/postsrv-build-the-post-service branch. Today I did work on sql migrations and having the sql migration interfaces implement postsvc.

**Thoughts** I'm realizing I should go back and redo the usersvc. I'm looking to it for references to see what I should do for postsvc, but some of it is incorrect. For example, not all columns in the user table need to be NOT NULL. I'll go back and fix those after postsvc. On another note, I listened to three episodes (95, 94, 93, 92) of the Go Times podcast. Now I'm curious about using Buffalo for rapid web development. It'd be nice if I could make a React.js website using Buffalo and Go.

**Link(s) to Work** https://github.com/OpenEugene/openboard.git, https://github.com/OpenEugene/openboard/pull/49/commits

### Day 26: Sunday, August 25, 2019

**Today's Progress** I submitted one commit to the open PR to wire the postsvc to the http and grpc servers. I started to work on another commit for the db queries, which takes the longest. I won't push that commit til I'm done. A few issues came up.

I wasn't sure how to bind parameters for when we are searching for a word that matches, so I ended preparing a statement that had `like '%?%' in it. I spent a short time looking it up, but I couldn't find it easily. I'll wait for the error message to help with my search for the fix. 

I'll also need to go back and set up the search for multiple keywords, not just one keyword. 

Finally. the hello service tutorial had a slight discrepenacy. When AddHelo is called, part of the response to that request is a bunch of timestamps. Yet, there are no timestamps returned in the response by the helloqry. I wonder if that's on purpose.

**Thoughts** According to a comment made in Go Time podcast, you should be making a test file for every file you write. I haven't written a single test in go yet. I suppose I should get on that...later.

**Link(s) to Work** https://github.com/OpenEugene/openboard.git, https://github.com/OpenEugene/openboard/pull/49/commits

### Day 26: Sunday, August 25, 2019

**Today's Progress** I submitted one commit to the open PR to wire the postsvc to the http and grpc servers. I started to work on another commit for the db queries, which takes the longest. I won't push that commit til I'm done. A few issues came up.

I wasn't sure how to bind parameters for when we are searching for a word that matches, so I ended preparing a statement that had `like '%?%' in it. I spent a short time looking it up, but I couldn't find it easily. I'll wait for the error message to help with my search for the fix. 

I'll also need to go back and set up the search for multiple keywords, not just one keyword. 

Finally. the hello service tutorial had a slight discrepenacy. When AddHelo is called, part of the response to that request is a bunch of timestamps. Yet, there are no timestamps returned in the response by the helloqry. I wonder if that's on purpose.

**Thoughts** According to a comment made in Go Time podcast, you should be making a test file for every file you write. I haven't written a single test in go yet. I suppose I should get on that...later.

**Link(s) to Work** https://github.com/OpenEugene/openboard.git, https://github.com/OpenEugene/openboard/pull/49/commits

### Day 27: Tuesday, August 27, 2019

**Today's Progress** I submitted the last commit for postsvc queries. It only took 30 minutes to complete. For the rest of the time, I watched videos at https://kubernetes.academy, shared by an employee at VM Ware in the Women Who Go Slack. 

**Thoughts** There are a lot of errors in my postsvc code because I don't have the post.proto and the generated proto buffer files. I don't know how to get those changes into my local branch until those branches are merged to mater. Maybe what I should try to do next time is try to get multiple branches merged into a local branch, so I can try to build and run the code. It'd be great to try out what's been written so far.
 
**Link(s) to Work** https://github.com/OpenEugene/openboard.git, https://github.com/OpenEugene/openboard/pull/49/commits

### Day 28: Friday, August 30, 2019

**Today's Progress** I continued Ry's Git Tutorial and practiced more git commands. I didn't know until today that a merge commit is a merge of 3 commits and that the most recent commit still points to the two parent commits.

**Thoughts** It was a very busy week, so I had to skip a couple of days in the challenge. The upcoming week is a lot less busy.
 
**Link(s) to Work** https://github.com/codegold79/ry-git-tutorial

### Day 29: Saturday, August 31, 2019

**Today's Progress** I read about consensus protocols that are used in blockchain technology. Bitcoin uses Proof of Work, but it's very energy intensive. It's also slow. Another consensus protocol used (by Ethereum's Casper) is Proof of State. But, the one I spent the most time learning about was Raft, a protocol that was made with ease of understanding in mind. The most useful graphic I saw was at http://thesecretlivesofdata.com/. I also liked the talk done by Diego Ongaro (the person who wrote the paper on Raft) which can be seen here: https://www.youtube.com/watch?v=LAqyTyNUYSY

**Thoughts** It's crazy how little I know about the problems out there and what people are doing to solve them.
 
**Link(s) to Work** 

### Day 30: Sunday, September 1, 2019

**Today's Progress** Today, I finally got to starting to learn about Docker. I went through the docs to install Docker on my computer, downloaded and ran the hello-world container, downloaded and ran busy-box (a non-latest version), and looked around in the container. I incidentally found out that Ubuntu root user is locked down and you can't ever log in as root.

**Thoughts** I've got a long way to go learning about Docker, and it will certainly have to include learning about Kubernetes.
 
**Link(s) to Work** 

### Day 31: Monday, September 2, 2019

**Today's Progress** I learned more about Docker, how to commit changes to image layers, how to build it from an existing image, or build from scratch. I also learned a few commands that can be used in the docker file, and how to save images to docker hub public repository.

**Thoughts** 
 
**Link(s) to Work** 

### Day 32: Tuesday, September 3, 2019

**Today's Progress** I worked more on my laravel.log parser. I fixed a division by zero bug, made the output more readable using the text/language and text/message packages, and made the time durations more precise by converting them to float32 (previously integers).

**Thoughts** Next step in this project is to edit the report live, while the log is being written.
 
**Link(s) to Work** https://github.com/codegold79/laravel-log-parser.git

### Day 33: Wednesday, September 4, 2019

**Today's Progress** I started another repository where I will be putting Go practice code. So far, I've created a webpage scraper that scrapes the contents of one webpage using *net/http*. I parsed the data with the help of *golang.org/x/net/html* and *string*, and saved the data to a file using *os*. 

**Thoughts** I could have used a bigger libary to parse the website data, but it was simple enough, I was willing to go through the process of figuring out how to parse it myself.
 
**Link(s) to Work** https://github.com/codegold79/bael

### Day 34: Thursday, September 5, 2019

**Today's Progress** It wasn't the easiest thing to do, but I finally set up my Google Cloud Platform account, got authenticated from the CLI (including my app), figured out how to save and edit entries in the Firestore database, copied my work from yesterday to a Cloud Function, got it to run, set up a cloud repository, pushed my code up to there, deployed from the repo, and decided my entire project needs to be changed up. So, I'll re-write everything tomorrow. Instead of scraping one page, I need to scrap multiple pages for the same data because it's very difficult to figure out which routes the service alerts come from. At least if I go to a route's page, I know which route to assign the alerts.

**Thoughts** I know that global variables are terrible, but how about global structs? I'll look at some code from the veterans and see what they're doing.
 
**Link(s) to Work** https://source.cloud.google.com/ltd-sched-mon/ltd-sched-mon

### Day 35: Friday, September 6, 2019

**Today's Progress** I'm finding that I'm still not grasping the concepts behind maps and points completely yet. So I created yet another repository on GitHub that is just for Sandbox play tests. It's basically my own Go Playground, except all my code is collected in a repo. Some findings for today were (1) map keys cannot just be anything. So far, I know map keys can be strings and integers. They cannot be structs, (2) Interfaces can have at least one of their items be another interface. In that case, the outer interface takes all the methods of the inner interface.

**Thoughts** This service alerts project is going to take a lot longer than I initially thought.
 
**Link(s) to Work** https://github.com/codegold79/cai

### Day 36: Saturday, September 7, 2019

**Today's Progress** I continued playing around in my sandbox repo and was able to modify variables with pointers to slices of structs. I changed the way my website scraper worked. I gave in and used goquery instead of golang.org/x/net/http. It's so much easier to be able to select elements on a page. I also changed how I save alerts. Previously, I used maps, but now, I use slices.

**Thoughts** 
 
**Link(s) to Work** 
* https://github.com/codegold79/cai
* https://github.com/codegold79/bael

### Day 37: Sunday, September 8, 2019

**Today's Progress** I learned about more strings package functions like Join, Split, Replace, and ReplaceAll. I used these to try to clean up the text that goquery sent back, but they didn't work as well as I wanted. I endedup using the regexp package to remove excessive white space.

**Thoughts** Next will be saving the alerts to Firestore.
 
**Link(s) to Work** 
* https://github.com/codegold79/bael
* https://github.com/codegold79/cai

### Day 38: Monday, September 9, 2019

**Today's Progress** I wrote the next function to save the alerts to Firestore. While working on that, I learned about the empty interface and how it can represent other types, as long as they don't implement methods. That's an interesting way to go about being more flexible about types.

**Thoughts** I haven't finished testing the code, so hopefully it's not too buggy.
 
**Link(s) to Work** 
* https://github.com/codegold79/bael

### Day 39: Tuesday, September 10, 2019

**Today's Progress** Daved looked through my pull requests through Openboard and taught me new concepts. Commit messages should start with a capital letter and not end in punctuation. They should be a certain length. According to https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html, the messages should be less than 50 characters for the summary and the description should have at most 72 characters per line. He also taught me that `go generate` in the mysql folder will generate the migration file. Building and executing the code from cmd/openbsrv will generate the go.mod and go.sum files. He explained how go.mod/sum files are packaged with libraries in directories that are to be exported, either externally or internally. Also, go files inside directories called "internal" are not to be exported externally. Daved made me aware of having different versions of dependencies for different projects, and this happens by temporarily setting the go path to the project directory when running the project. For next time, he said we can talk about my last question, which was, how to I send requests to the user and post services I created and check that they're sending back the intended messages. He hinted that we will be writing code to send the requests (as opposed to using something like Postman).

**Thoughts** I'm so fortunate to have been introduced to Daved who inspired me to learn Go and now he's spending the time to teach me how to be a developer at a higher level. It's up to me now to work hard on my Go studies and projects.
 
**Link(s) to Work** 
* https://github.com/OpenEugene/openboard/pulls

### Day 40: Wednesday, September 11, 2019

**Today's Progress** I followed the protobuffer tutorial for go, but ended up getting a bunch of errors when I ran protoc. I tried to build without running protoc, but I encountered issues there too, where the user.proto variables did not get carried over to the go code. I was able to change the database fields in a table, though, and generate a migration file.

**Thoughts** I'll have to figure out protobuf tomorrow.
 
**Link(s) to Work** 
* https://github.com/OpenEugene/openboard/pulls

### Day 41: Saturday, September 14, 2019

**Today's Progress** I couldn't get passed the same error I encountered last time with protobuf: ```google/api/annotations.proto: File not found.
msgs/proto/user.proto:16:1: Import "google/api/annotations.proto" was not found or had errors``` I asked on Slack for help, then went back to work on my service alert from Google Cloud project. I found a bug that incorrectly set a db doc as outdated. I found another bug that can be fixed if I saved only unique alerts from the LTD site.

**Thoughts** 
 
**Link(s) to Work** 
* https://github.com/OpenEugene/openboard/pulls
* https://github.com/codegold79/bael

### Day 42: Sunday, September 15, 2019

**Today's Progress** I got annoyed when I encountered a "does not support indexing" error. Why should I add parenthesis for pointers to make indexing possible? Why not just make it easier on us and let us get away without parenthesis?
```
pm := make([]Members, 5)
pm := &m

m[:2]     // good
pm[:2]    // bad
(*pm)[:2] // good ```
Source: https://stackoverflow.com/questions/25290956/go-update-slice-iterating-error-does-not-support-indexing 

I fixed the bugs with the data injesting part of the service alerts code. Now, I probably should take that out of the main package and start putting some logical structure to my code. Not that I know how to do that at the moment. I've never made packages outside of main.

**Thoughts** This site seems promising in regard to helping with code structure: https://www.sohamkamani.com/blog/2017/09/13/how-to-build-a-web-application-in-golang/
 
**Link(s) to Work** 
* https://github.com/codegold79/bael

### Day 43: Monday, September 16, 2019

**Today's Progress** Daved shared an article and several code snippets, which I read. They were about arrays, slices, and finally about empty interfaces. I still need more time with the interfaces, but my understanding of slices might be solidifying. I still am not sure how to use a struct and slice to my advantage at the moment. Here were what Daved shared:
* https://blog.golang.org/go-slices-usage-and-internals#TOC_4
* https://play.golang.org/p/Ki_zmYudzaQ
* https://play.golang.org/p/my6l2JOmmsL
* https://play.golang.org/p/58epBVn-21p

**Thoughts** Hopefully, tomorrow, I can delve more into the questions I had tomorrow.
 
**Link(s) to Work** 
* 

### Day 44: Thursday, September 19, 2019

**Today's Progress** With @daved's help, I got the updated proto file to compile. I even built and executed the OpenBoard application--yay! I'm ready for our OpenBoard meeting on Tuesday. 

Having read some of chapter 2 of Go In Action by William Kennedy, I was able to figure out how to restructure my code for my service alert project. It looks so much better now. I started to replace the slice pointers in function parameters, but I broke the code, so I haven't committed that change yet. 

**Thoughts** I'm really liking the Go In Action book; it seems to cover how to use the Go language I've spent the last few months learning. I'm familiar with syntax and grammer, but now I need to learn how to compose and write idiomatically.
 
**Link(s) to Work** 
* https://github.com/codegold79/bael
* https://github.com/OpenEugene/openboard/pulls

### Day 45: Friday, September 20, 2019

**Today's Progress** I converted the pointers to slices and just passed the slices themselves to functions in my service alerts project. After that, I started working on the user data, by outlining what I wanted the functions to do. I wrote out the function that retrieved all the user keys.

**Thoughts** I still don't understand all of the function calls I need to do to retrieve data from Firestore. Maybe one day, it'll make sense. But for now, I don't know what context is, what closing the client does, and such.
 
**Link(s) to Work** 
* https://github.com/codegold79/bael

### Day 46: Saturday, September 21, 2019

**Today's Progress** I added the functionality to remove the outdated alerts from a user's stored alert keys in the service alerts project. It looks at a stored_alert's outdated_at timestamp. If it has one, it is outdated, and the alert key is removed from the user's collection.

**Thoughts** It took a lot longer than I thought, because I got stuck there for a while retrieving an array using Get and DataAt(). When I used DataTo() and a struct per instructions at https://godoc.org/cloud.google.com/go/firestore
 
**Link(s) to Work** 
* https://github.com/codegold79/bael

### Day 47: Friday, September 27, 2019

**Today's Progress** Progress has been made for the service alerts app. New service alerts are identified and sent back for each userkey. I can tell that I'll need to construct the client in the package, instead of creating a variable and storing client for almost every function in the package. 
 
**Link(s) to Work** 
* https://github.com/codegold79/bael

### Day 48: Saturday, September 28, 2019

**Today's Progress** Today, I figured out how to send an email using a Cloud Function written in Go and SendGrid email libraries. Send Grid has some easy documentation to follow (https://app.sendgrid.com/guide/integrate/langs/go).

**Thoughts** I stored the Send Grid API key in an environmental variable with Google Cloud function, but it seems that is not recommended, according to https://cloud.google.com/functions/docs/env-var#setting_environment_variables. I guess I'll have to deal with that later.
 
**Link(s) to Work** 
* https://source.cloud.google.com/ltd-sched-mon/ltd-sched-mon

### Day 49: Sunday, September 29, 2019

**Today's Progress** I added the functionality in the alerts project to send out alerts if they are new to the database.

**Thoughts** After the backend is set up, I still need to figure out how to have users choose routes they'd like to (un)subscribe to. I'd like to set up email verification so we don't get erroneous subscriptions.

**Link(s) to Work** 
* https://github.com/codegold79/bael

### Day 50: Monday, September 30, 2019

**Today's Progress** I finished up updating the user alerts and worked on the email content. It's going to take a lot of work to try to get the route IDs and the links to the service alert pages. Most of the re-arranging of the functions is done.

**Link(s) to Work** 
* https://github.com/codegold79/bael