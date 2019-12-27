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

**Thoughts** I could have used a bigger library to parse the website data, but it was simple enough, I was willing to go through the process of figuring out how to parse it myself.
 
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

**Today's Progress** I learned about more strings package functions like Join, Split, Replace, and ReplaceAll. I used these to try to clean up the text that goquery sent back, but they didn't work as well as I wanted. I ended up using the regexp package to remove excessive white space.

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
(*pm)[:2] // good
```
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

### Day 51: Tuesday, October 1, 2019

**Today's Progress** I decided to take on a challenge presented by an acquaintance. It was to multiply two fractions and return the reduced form of the product as a fraction, which I completed. The challenge also includes having to do a unit test as well as implement parallel processing, so I'm not done yet. I made the repo private since we should be coming up with the answers on our own.

**Thoughts** I thought the challenge would have been easy to finish within an hour, since it's just multiplying two fractions. What ended up taking up all my time was writing out how to get the greatest common factor, which involved finding prime numbers. It was tricky to do the prime factor tree as an algorithm, as opposed to drawing it out on a piece of paper. But, I got through it, and I'll be looking at what Go tests are, for the first time, tomorrow.

**Link(s) to Work** 
* https://github.com/codegold79/aruku

### Day 52: Wednesday, October 2, 2019

**Today's Progress** I wrote some tests (table test) with some examples of edge cases for fractions. I was so good at coming up with scenarios, I had to rewrite my function to get my tests to pass.

**Thoughts** Thank you again to @daved for writing the test tutorial and example so I can quickly get up to speed on how to write a Go test and how to follow some basic conventions.

**Link(s) to Work** 
* https://github.com/codegold79/aruku

### Day 53: Saturday, October 5, 2019

**Today's Progress** I read a couple chapters of Go In Action by William Kennedy (https://www.amazon.com/Go-Action-William-Kennedy/dp/1617291781) regarding testing (Chp 9) and concurrency (Chp 6). Very helpful in establishing the basic concepts, and then going into best practices, as well as give examples of what code would be utilized in real life.

**Link(s) to Work** 
* https://github.com/codegold79/aruku

### Day 54: Sunday, October 6, 2019

**Today's Progress** I continued working on retrieving route information and associating them with the service alerts to send in the alert emails. The email also has some minor formatting. 

**Thoughts** There appears to be a bug where the route_id for my user gets overwritten. Something to deal with next time.

**Link(s) to Work** 
* https://github.com/codegold79/bael

### Day 55: Monday, October 7, 2019

**Today's Progress** I was curious as to the difference between Docker Containers, Kubernetes, VirtualBox, and VMWare. I read a few sites, with one of the more interesting ones being https://blogs.vmware.com/cloudnative/2017/10/25/kubernetes-introduction-vmware-users/ Who knew that K8 works well to run on VMWare's vSphere? Now, I wonder, what sorts of companies have a need for orchestration of massive numbers of servers and apps using containers and virtualization? I imagine Google, Amazon, and Facebook, but how about smaller companies? 

### Day 56: Wednesday, October 9, 2019

**Today's Progress** I worked on the first of my assigned issues. Created a branch and started working on creating a User type in the proto file, and using that to define Item(s). Unfortunately, the service is also called "User", so I have to change the service name to "UserSvc". No problem (I think). After the changes, I generated the pb files, then tried to build openboard server, but it said it couldn't find the postsvc migrations. I tried go generate, but it couldn't find the mysql module. Things to work on tomorrow. 

**Link(s) to Work** 
* https://github.com/OpenEugene/openboard/pulls

### Day 57: Thursday, October 10, 2019

**Today's Progress** I didn't realize I hadn't tried to run the program with the latest postsvc changes. There were a lot of errors. I fixed them all, as well as the errors that came from the usersvc changes yesterday. Submitted two PRs. I can start work on the second issue (create a client that can be used to test all the db functions) tomorrow.

**Link(s) to Work** 
* https://github.com/OpenEugene/openboard/pulls

### Day 58: Saturday, October 12, 2019

**Today's Progress** Tried to set up test client by initializing pb.NewUserSvcClient, but it couldn't find the function (undefined), despite my being able to see the function in the pb package. And yet, my tooltip indicated the old pb.NewUserClient was there (I can't see it there), so I used that instead. But, the weird thing is, when I tried to run pb.FndRoleReq on the client, it had more parameters in the function than the proto file's FndRoleReq had. Not sure what's going on.

**Link(s) to Work** 
* https://github.com/OpenEugene/openboard/pulls

### Day 59: Sunday, October 13, 2019

**Today's Progress** I got stuck again with my integration test client not being able see the protobuf generated files. I asked @daveddev for help, and he not only got me unstuck by telling me about using "replace" in go.mod. He also made use of a library he made (github.com/codemodus/relay) to help me manage my errors so they're more readable. Super thankful for all his help--it saved me so much time!

**Link(s) to Work** 
* https://github.com/OpenEugene/openboard/pulls

### Day 60: Monday, October 14, 2019

**Today's Progress** Had a nice conversation with Michael Gasch at VMWare about #Golang. He recommended reading Bill Kennedy's four part blog post that ends with Design Philosophy On Data And Semantics (https://www.ardanlabs.com/blog/2017/05/language-mechanics-on-stacks-and-pointers.html) I read parts 1 and 2 today, and reviewed Bill's chapter on concurrency. 

**Thoughts** I'm so thankful for people like Bill who can not only break concepts down to their most simplest ideas, and teach people difficult concepts by building up from the foundation. For the first time, I think I finally understand pointers, why we need pointer types (the addresses might be 8 bytes, but they need to point to different data types), and why you should return the pointer and not just declare a variable as a pointer. It's so much readable when you do that. Also, loved learning about how to see the decisions the garbage collector made by using `go build -gcflags "-m -m"`. Fascinating stuff!

### Day 61: Wednesday, October 16, 2019

**Today's Progress** I read a paper regarding Application Platforms and how VMWare will provide the solution to the difficulty of scaling by use of a Hybrid Cloud Runtime. It's fascinating to find similarities between increasing the scaling of applications and the increasing of production volumes in a manufacturing setting. Failing to identify the correct bottlenecks in each case can lead to incurring unsustainable cost due to throwing more resources in areas that aren't needed. The strength of VMWare is they have the people who can bring a wholistic understanding of the system and its problems.

### Day 62: Friday, October 18, 2019

**Today's Progress** I completed the first of two PRs in this sprint for openboard and @daved approved it after some fixups. We decided on Nathan Youngman and Roger Peppe's book, Get Programming with Go for our Go Book Club. I read through two lessons (chapters), completed the exercises for them, and pushed up the code in a new repository.

**Link(s) to Work** 
* https://github.com/OpenEugene/openboard/pulls
* https://github.com/codegold79/get-programming-with-go

### Day 63: Saturday, October 19, 2019

**Today's Progress** I read and did the exercises for lessons 3 and 4 in Get Programming With Go. I thought these initial chapters wouldn't have anything new for me, but they did. I learned
* only short variable declarations can be in `for` loops and `if` statements
* each `case` in `switch` has its own variable scope
* the `fallthrough` keyword in `switch`
* there are only 25 keywords to learn in Go
* math/rand package's handy `Intn()` function 

**Link(s) to Work** 
* https://github.com/codegold79/get-programming-with-go

### Day 64: Monday, October 21, 2019

**Today's Progress** I completed the lesson 5 capstone exercise in Get Programming With Go. I totally forgot about using hyphen followed by numbers to control spacing in fmt.Printf. One thing I'm guessing happens, that I didn't think of before, was that if you use short variable declaration inside a for loop, that it won't try to redeclare the variable again if it's going to be used. It will ignore the colon, and treat any iteration after the first as a regular equal sign.

**Link(s) to Work** 
* https://github.com/codegold79/get-programming-with-go

### Day 65: Friday, October 25, 2019

**Today's Progress** With Daved's lesson on pointers and receiver arguments for methods, I was able to get passed all the errors and successfully run one test each for the user and post services.

**Link(s) to Work** 
* https://github.com/OpenEugene/openboard/pulls

### Day 66: Saturday, October 26, 2019

**Today's Progress** Learned about construction functions in Go, and how they're used so that zero value structs won't break a package because it can't deal with them. Refactored the openboard integration test program so that the user and post service tests would be in their own functions.

**Link(s) to Work** 
* https://github.com/OpenEugene/openboard/pulls
* https://golangbot.com/structs-instead-of-classes/

### Day 67: Saturday, October 29, 2019

**Today's Progress** Tried to write another function in the integration test to add a user, but I keep getting rpc errors. Not sure how to get passed them.

**Link(s) to Work** 
* https://github.com/OpenEugene/openboard/pulls

### Day 68: Saturday, November 3, 2019

**Today's Progress** Finally got passed the pointer as a structure field error for integration test. Added user through test successfully. Added more tests for finding users, removing a user, and updating a user. Also changed how we query finding users.

**Link(s) to Work** 
* https://github.com/OpenEugene/openboard/pulls

### Day 69: Sunday, November 10, 2019

**Today's Progress** I've decided to go back to my service alert project and see what all still needs to be done with that project. Most of today was reading what was already done and trying to figure out what was not working right. I created issues when I found any notes on problems or for the ones I encountered. I ended up fixing one small bug that affected formatting of emailed messages. 

**Thoughts** It's difficult to QA this project since the interaction with Firestore is so slow. I might have to add in functionality to skip sections of code, or get used to inserting/removing comment slashes.
 
**Link(s) to Work** https://github.com/codegold79/bael

### Day 70: Friday, November 15, 2019

**Today's Progress** I've been so used to using integers for table keys, and didn't know there was a better way until I worked on Openboard. Turns out a randomized string, or UID, can be used for keys and it obscures a little how to access an item. A neat feature of the UID we're using is it is generated in an ordered manner so our MariaDb database doesn't have to spend a lot of time adding to the end of a unique key set. So today, I updated all the integer IDs to be strings, or varchar(26) in our migrations. Since that didn't take much time, I also studied up on the Slack API. I found out from my research I would like to make a slash command.

**Link(s) to Work** https://github.com/OpenEugene/openboard/pulls

### Day 71: Saturday, November 16, 2019

**Today's Progress** Continued work on converting the queries to use string IDs instead of uint32. I mostly struggled with GitHub.com workflow, but got through it with @daveddev's help. 

**Thoughts** I was trying to overcomplicate things. Hopefully, tomorrow I can start working on integration tests.

**Link(s) to Work** https://github.com/OpenEugene/openboard/pulls

### Day 72: Monday, November 18, 2019

**Today's Progress** Read chapters 6 and 7 of Get Programming With Go and completed exercises for 6. 

**Link(s) to Work** https://github.com/codegold79/get-programming-with-go/tree/master/lesson06

### Day 73: Tuesday, November 19, 2019

**Today's Progress** I followed a GCP tutorial for using Cloud Functions and Go to make a Slack slash command: https://cloud.google.com/functions/docs/tutorials/slack. It was a lot of fun to build and test out, but the final response is interpreted as a string and doesn't look at the json I sent. Reading Slack's documentation, it looks like they might have changed the response message structure. I think I need a block property and get rid of the response_type property.

**Link(s) to Work** https://github.com/codegold79/daekath

### Day 74: Wednesday, November 20, 2019

**Today's Progress** I found the reason for my woes yesterday was because I had "Content-Type:" instead of "Content-Type". That colon was the only difference between Slack API interpreting the JSON and not. With that working, I wanted to see how different it would be running the same code on Lambda. AWS was more difficult to navigate, given that the roles are hard to select permissions for, and I had to manually set up the API Gateway trigger. In GCP, I didn't have to set the role and the API Gateway was simply selecting "HTTP" from a drop-down menu. I make a couple minor changes such as storing the SLACK_TOKEN in an environmental variable and generating a door code, instead of inspirational quotes.

**Link(s) to Work** https://github.com/codegold79/daekath

### Day 75: Monday, November 21, 2019

**Today's Progress** Read chapters 8 and 9 of Get Programming With Go and completed exercises for 8. 

**Link(s) to Work** https://github.com/codegold79/get-programming-with-go/tree/master/lesson08

### Day 76: Sunday, December 1, 2019

**Today's Progress** Had an OpenBoard meeting with @DavedDev last Tuesday. He made some helpful comments on PR#57. After going over what needed to be done, we agreed it would be better to redo the changes given my new understanding. Plus, what I had done was a huge mess. Today, I completely redid the code changes for the integration test client in a more orderly manner. Making the changes the second time was easier, made much more sense, and is hopefully, much more readable.

**Link(s) to Work** https://github.com/OpenEugene/openboard/pulls

### Day 77: Monday, December 2, 2019

**Today's Progress** Finished chapter 9 exercises, read chapter 10 and completed its exercise in Get Programming with Go.

**Link(s) to Work** 
* https://github.com/codegold79/get-programming-with-go/tree/master/lesson09
* https://github.com/codegold79/get-programming-with-go/tree/master/lesson10

### Day 78: Tuesday, December 3, 2019

**Today's Progress** Wrote a couple more integration tests for openboard user and post services. While trying to add FndUser test, it seems there are some old dependencies that didn't have the fixes I had made. Strange. Will have to look into it another day.

**Link(s) to Work** https://github.com/OpenEugene/openboard/pulls

### Day 79: Friday, December 6, 2019

**Today's Progress** Fixed the go.mod file to replace a path to an internal dependency. Fixed the find user queries until the new find user integration test worked.

**Link(s) to Work** https://github.com/OpenEugene/openboard/pulls

### Day 80: Saturday, December 7, 2019

**Today's Progress** Did yet another refactoring of the integration test file. Made the existing tests more robust by adding more roles and users and doing a search on an existing user and another not. Had to modify the queries in the main code to make the results closer to what is intended.

**Link(s) to Work** https://github.com/OpenEugene/openboard/pulls

### Day 81: Sunday, December 8, 2019

**Today's Progress** I wanted to work on openboard on my MacBook while traveling, which means I needed to install the backend software. However, MariaDb is proving difficult to install (again). After nearly an hour of working on errors and searching for solutions on Google, I removed MariaDb and will be trying again, maybe within a Docker container next time.

**Link(s) to Work** https://github.com/OpenEugene/openboard/pulls

### Day 82: Monday, December 9, 2019

**Today's Progress** I didn't know the first thing about running MariaDb on Docker, so I completed a few beginners' tutorials on the default bridge network for containers and how to access a running MariaDb server instance. After being able to log into the MySQL server, I looked into the OpenBoard database code to see how the program was accessing the database. I couldn't figure it out, but I saw that Daved had created a Docker compose manifest as well as two docker images. Next step for me will be to figure out how to run the compose file.

**Link(s) to Work** https://github.com/OpenEugene/openboard/pulls

### Day 83: Tuesday, December 10, 2019

**Today's Progress** Worked on getting the docker-compse.yml file by exporting variables in shell, getting the command right (it's docker-compose, not docker compose, at least on Catalina), editing the Dockerfiles, removing images and containers to get the changes to catch. I probably could have saved some time and used docker-compose build or docker-compose up --build. I spent a little time trying to figure out how to get google.golang.org/grpc to be recognized by VS Code, but finally gave up when there was nothing to clone into the src directory. I also had to get the author back to my personal github account details (instead of work), so had to rebase my log entries there. Still more to go with Docker tomorrow.

**Link(s) to Work** https://github.com/OpenEugene/openboard/pulls

### Day 84: Wednesday, December 11, 2019

**Today's Progress** After trying some more to get docker-compose to work, the script failed to connect to the mysql server. I finally gave up and spent some time cleaning up the mysql/mariadb installation. I reinstalled with brew and one website revealed that running mysql_secure_installation only works with sudo. If I had known that from the beginning, I wouldn't have gone through all this hassel. Ah well. Tomorrow, I'll be able to get openboard to work on my work computer, hopefully.

**Thoughts** There's enough days in the year that I can finish #100DaysOfCode before 2020, and there are three days where I can take a break.

**Link(s) to Work** https://github.com/OpenEugene/openboard/pulls

### Day 85: Thursday, December 12, 2019

**Today's Progress** Went as far as I could with user service tests by adding a delete user test. Added an issue regarding not actually deleting data, but marking them as deleted. Added another issue regarding linking users and posts. Continued post service test by adding types and another post. There is no find types yet in postdb.go, but I wrote the test anyway and commented it out. Finding posts is causing gRPC errors so I have not pushed up those changes yet.

**Link(s) to Work** https://github.com/OpenEugene/openboard/pulls

### Day 86: Friday, December 13, 2019

**Today's Progress** Spent over an hour finding errors caused by having wildcards in the query statement, instead of concatenating the percent symbols to the variables bound to the MySQL query parameters. Learned that I don't need quotes around query parameters as the mysql driver will handle those automatically. I didn't make any commits because more errors are happening. More to do tomorrow.

**Link(s) to Work** https://github.com/OpenEugene/openboard/pulls

### Day 87: Sunday, December 15, 2019

**Today's Progress** Errors are getting easier to figure out and fix. I had to ensure that slug field needed to be saved as a blank string to be consistent with the Go strict data types that require it to be a string or nil, not MySQL's NULL value. The fix enabled me to find posts. I added an edit post test as well. There are two tests remaining: delete post and find types.

**Thoughts** Had to miss a day yesterday, ironically because Go Bootcamp took all day. Now, I only have two days I can miss to be able to finish 100 Days of Code by the end of the year.

**Link(s) to Work** https://github.com/OpenEugene/openboard/pulls

### Day 88: Monday, December 16, 2019

**Today's Progress** Added delete post test. Find types was added to the post.proto file as well as added to the post service interface and queries. The find types test was added.

**Thoughts** I had miscalculated how many days I can miss. I can miss three (not two as I originally thought) to have the last #100DaysOfCode challenge day and the last day of the year to be the same.

**Link(s) to Work** https://github.com/OpenEugene/openboard/pulls

### Day 89: Tuesday, December 17, 2019

**Today's Progress** I thought I understood strings in Go, but after an hour, I still couldn't figure out how to decipher text encoded with a Vigenère Cipher. That was one of the two exercises for the capstone lesson 11 in Get Programming with Go. Tomorrow, I'll have to go over chapter 9 again and see what I'm missing.

### Day 90: Wednesday, December 18, 2019

**Today's Progress** I tried to do the arithmetic of the Vigenère cipher in my head, but after failing after an hour to get anything other than gibberish for an answer, I think I need to get out a paper and pencil and solve this the old fashioned way first. Then, maybe I can finish writing the program. The fact that bytes are unsigned int8s makes this problem particularly difficult for me to work around.

### Day 91: Thursday, December 19, 2019

**Today's Progress** With the help of pen and paper, I figured the arithmetic required to decipher the Vigenère message. Using the equations I figured out, I came up with two solutions. The first decoded using strings package and no range keyword. The second decoded using range but no other package except fmt.

For the third way, which the book mentioned should not use if statements, but rather modulo, I had to look up the Wikipedia article. I'm afraid I'm losing patience for this capstone chapter, so I didn't want to figure it out.

**Thoughts** After all that, there's still the encryption part of the capstone to complete. Hopefully, encryption will be faster than decryption.

**Link(s) to Work** 
* https://github.com/codegold79/get-programming-with-go/lesson11

### Day 92: Friday, December 20, 2019

**Today's Progress** Ciphering was much easier than deciphering. I completed the exercise with time to spare. I spent the remainder of the hour reading chapter 12.

**Thoughts** Today, I submitted a PR for OpenFaaS/FaaS-Cli contribution. It was a simple one, but I had included a table test, and I felt accomplished. Hopefully, I can get out of the beginner level and get into the intermediate one. It is nice to have some knowledge of bash (thanks to my Ubuntu machine at IDX, thanks to Daved for teaching me some basics, thanks to having my personal computer--this one--be an Ubuntu), and basic knowledge of git (thanks to IDX having me rebase so much).

**Link(s) to Work** 
* https://github.com/codegold79/get-programming-with-go/lesson11

### Day 93: Saturday, December 21, 2019

**Today's Progress** Finished reading chapter 12, did the exercise, and started to read chapter 13.

**Thoughts** Tuesday is next OpenBoard meetup day, when I anticipate getting more assignments. I anticipate continuing with the book Sunday, Monday, and even Tuesday (since it's Xmas eve and there's no work that day).

**Link(s) to Work** 
* https://github.com/codegold79/get-programming-with-go/lesson12

### Day 94: Sunday, December 22, 2019

**Today's Progress** Finished reading chapter 13 on methods, did the exercise, and finished reading chapter 14. Chapter 14 covered first class functions, which was a nice review for me because a couple weeks ago, I had studied Dave Cheney's article, https://dave.cheney.net/2016/11/13/do-not-fear-first-class-functions (thanks @daved for finding that). Doing the exercise (tomorrow) will help to solidify first class functions in my mind.

**Thoughts** Regarding the methods chapter 13, I didn't like how methods were not considered a different kind of function. It was classified as not a kind of function, but only like a function and something different. So, the statement on page 107 was misleading to me, "A package can only have a single function with a given name, and it can’t be the same name as a type, so a celsius function that returns a celsius type isn’t possible." 

If I were to re-write the concept of method, I would use the wording in GoTour. On the page https://tour.golang.org/methods/1, it says, "A method is a function with a special receiver argument." 

On the next page, https://tour.golang.org/methods/2, it emphasizes, "Remember: a method is just a function with a receiver argument."

And I would rewrite the Get Programming With Go sentence to say, "A package can only have a single (non-method) function with a given name, and it can't be the same name as a type. However, if the function is a method, it too cannot have the same name as another function, however, it can have the same name as a type."

**Link(s) to Work** 
* https://github.com/codegold79/get-programming-with-go/lesson13

### Day 95: Monday, December 23, 2019

**Today's Progress** @daved reviewed my #OpenBoard PR and I fixed what I could. The rest will be discussed tomorrow during our meeting. Completed lesson 14 exercise, and finished lesson 15 capstone exercise. That capstone is messier than the answer in the appendix, so it can do with some refactoring.

**Thoughts** I think a countdown can begin--only 5 days remaining in the challenge!

**Link(s) to Work** 
* https://github.com/OpenEugene/openboard/pulls
* https://github.com/codegold79/get-programming-with-go/lesson14
* https://github.com/codegold79/get-programming-with-go/lesson15

### Day 96: Wednesday, December 25, 2019

**Today's Progress** Completed lesson 16 reading and exercise, and lesson 17 reading. I'm able to go quickly through these chapters because array and slice syntax is review for me.

**Thoughts** Four days remaining in the challenge!

**Link(s) to Work** 
* https://github.com/codegold79/get-programming-with-go/lesson16

### Day 97: Thursday, December 26, 2019

**Today's Progress** Completed lesson 17 exercise, and lesson 18 reading and exercise. I learned that append can modify the original underlying array if the capacity was large enough to hold the additional element. However, a new array will be created (with double the previous capacity), if the added element does not fit in the slice. It was also interesting to learn that when taking a slice of an array that has values, the slice capacity will be however many elements of the array was added, plus the rest of the array that wasn't used.

**Thoughts** Three days remaining in the challenge!

**Link(s) to Work** 
* https://github.com/codegold79/get-programming-with-go/lesson17
* https://github.com/codegold79/get-programming-with-go/lesson18