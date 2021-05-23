# #100DaysOfCode Log - Round 1 - Noah Davey

The log of my #100DaysOfCode challenge. Started on [24th of January 2021].

## Log

### R1D1 
Today I created a personal access token with the github API and used it to read repo details from my github account. I also used it to read commit details for specific repos. This was relatively easy to achieve, however I still have some questions around how exactly OAuth2 works and what is different between an implementation using a personal access token and OAuth. Feel happy that I sat down and did this today, a good first step towards this challenge. Turns out sitting down and just starting to code does work decently well

### R1D2
Today I created a webhook throught the github UI for my GithubAccountability Repo. I initially set it up so that whenever a comment on a commit is received that an event would be sent to me. I was able to successfully receive the payload and view the data which was sent to me. Tomorrow I plan on extending the functionlaity of this endpoint so that it does something useful when someone pushes to a repo. Likely I will do something like sending a message to telegram or signal etc. This was a good day and I feel like I better grasp the idea of Webhooks now.

### R1D3
Today I connected to the telegram API using a bot. I struggled a bit here in trying to make the bot send me an individual method. But was successful in setting up the connection. Hopefully tomorrow I will be able to get some messages getting sent back and forth. Once that is achieved I will be able to connect up the webhook implementation and send through commit details when the webhook is hit.

### R1D4
Today I was able to get my telegram bot to send me messages and in turn I was able to send it messages. I can either call the getUpdates function to or setup a webhook where they ping me with updates. Not sure of the implementation I want yet. But i think this bot will be more used for pushing out updates and not listening to what people say. So likely will just use the 'getUpdates' for now to find out the chatID where I should be sending messages to. Tomorrow I will hopefully be able to connect the github webhook stuff and send a telegram message based off that. Im getting close now

### R1D5
Today I managed to setup a full loop of sorts. When a commit is pushed to my accounability repository (and hopefully this one when I test it shortly), a webhook on my express server is hit which in turn shoots a message off through the telegram bot. I plan on trying to launch this small app on heroku tomorrow. Which will mean i can ideally have it sit there in perpetuity and ping off the alarm when I do my daily commit. I do have concern about the requirement of this to sit waiting for updates all day and having to run a webserver for that which obviously isn't free. I guess i will have to see. Worst case maybe I setup something which logs on daily and checks my Github account and does a similar sort of thing. We'll see

### R1D6
Today I setup my heroku app and changed the urls in my github webhook setup. I have concerns about if this will work or not when it hasn't been up for a few hours (supposedly on the free tier the dynos sleep after an hour of inactivity). However a good win is that on a github push my heroku app went and send a telegram message! Woohoo, today feels like a great success 

### R1D7
Today didn't feel very productive. I have been sick and mistakenly left this till the end of my day when I was pretty recked. I did check that the heroku app works as expected and i think overall the accountability tracker worked decently. Will expand upon it in the future but for now I should move onto something else. I did a bid of work on my scoreboard app today and made it so that when you submit a ping pong match, that is recorded in the db. So a small win 

### R1D8
Today I did some work on my scoreboard app. Managed to populate a dropdown with all the users I have stored in my db. This is a good step forwards in terms of functionality and tomorrow I look forwards to playing around with then referencing that detail in entries made to the match collection

### R1D9
Today I wasn't really feeling like doing work on my scoreboard app so did an exercism problem. Solved for the prime factors of a number which wasn't too hard and a nice problem to look at this eve. Tomorrow or soon i kind of want to look at improving my accountability app somehow to allow people to link up repos via the telegram bot? Or similar, will think about this more

### R1D10
Today I did anotther exercism challenge on flattening array's. Think i will leave the github accountability planner till i have a bit more energy. Still happy with today though, came up with a decent enough solution to the problem

### R1D11
Bit of a late one tonight. I made the stupid decision of not doing my coding earlier in the day and that meant i had to do my coding now. I am not in the best state to do my coding so as a result have been pretty inefficient. Tried some exercism problems, but pretty slow on the mark overall -.- 

### R1D12
Worked on a couple exercism problems today, nothing much to report though...

### R1D13
Attempted to do minesweeper challenge and still struggling with it. But made some decent steps forward today which was good

### R1D14
Today worked on extending my github accountability tracker a bit. Managed to get all public repos via the github API. Also was able to create a webhook for that repo. Began working on sending a message from the telegram bot. And tomorrow will try to finish off this functionality. The main thing i was lacking today was being able to detect when the user has sent a message vs a response. Perhaps i will need to address this via the commands endpoint however. Not sure atm

### R1D15
Feeling pretty tired today as I had to stay back at work sorting out some automatic deposits stuff. But still sat down and did some code. Managed to add a command to the Telegram bot and hook that up to the github API so that when the user types /subscript_to_repo they get a custom keyboard where they can select the repo they would like to follow. Tomorrow I will try to set up the webhook integration wherein the user will be able to click one of the options and have the webhook created for them. Will need some way of remembering who to send updates for the repo to though...

### R1D16
Today I was able to get my telegram bot to set a github webhook upon response from a user. This feels like good progress. Slowly getting somewhere and building some useful functionality. Attempting to do some minor refactoring of the code as i go as well since it is kind of gross atm. But overall pretty happy with performance so far!

### R1D17 
Today worked on a bit of refactoring and sending some form of error/success message when the webhook was set. Also was attempting to improve the github webhook where it is based off the event type however didn't get very far with that aspect

### R1D18
Today managed to make a little bit or progress on the diamond exercism problem. But felt too tired to do anything productive. Hopefully tomorrow I can get a bit more done

### R1D19
Today I added eslint and typescript to my project. Didn't really any features yet but overall feels like a good move for code cleanliness and what not

### R1D20
Today I converted most of the files in my project to Typescript. I think next time I start a project I will start off with Typescript. This will hopefully reduce the amount of backtracking I have to do. Feels cleaner now though which is good

### R1D21
Didn't have a whole bunch of direction today. But begun the process of creating a VS Code plugin. Going to attempt to make a Cyclomatic Complexity Calculator. Which will involve some static analysis of code and presenting of data to users.

### R1D22
Feeling very sick and headachy today. Managed to add really basic codeLens functionality to the plugin. But not much overall progress. The extension world seems somewhat daunting. But will see how I go 

### R1D23
Almost didn't do my coding today again but managed to get an exercism problem finished which feels good even though it wasn't project related. Glad im keeping the streak alive

### R1D24
Worked on doing a binary search tree today. Was going well until I had to be able to sort it... Which is kind of the point. I think sleeping on the problem will help me with this one

### R1D25
Was feeling in a more productive mood today but got derailed by not putting myself in a place where I couldn't be distracted. I should probably do this coding in my room where I can enter a flow state or at least approach it. Though was able to play around with some hover funcitonality in vscode plugins

### R1D26
### R1D27
I didn't do my coding yesterday which I was annoyed at myself for. Though I have been going very well up until that point and will just have to make up for it on other days. It was a small misstep but hopefully not a recurring one. Today I made some good progress on my VSCode plugin which was cool. Figuring out how to make code lens appear on multiple keywords dynamically. Got to make it dissapear when the keyword is no longer there tomorrow. But so far so good!

### R1D28
Quite unproductive today, had a weak attempt at trying to make the codelens dissapear when the function keyword was moved. Will have to try again tomorrow

### R1D29
Today felt productive which was nice. Managed to come up with a decent way of calculating complexity of functions via regular expressions. Currently only using the if/else if/else branching statements, but plan on testing it using this method and then extendint the functionality to include things like switch statements later. Tomorrow I think i will need to take a look at how I can pull out a function from the users document in VS Code

### R1D30
Today managed to make recogition of function keyword better via a regex as well. Though still exhibits some weird behaviour when moving text around so will need to address that. All good though feels like im making some pregesss slowy but surely...

### R1D31
Worked on the Binary Search Tree Exercism problem today which went well once I figured out how to print out the ordered tree. Then moved onto working on an anagram problem

### R1D32
Yesterday just did a little work on the anagram task. I only did 30mins though...

### R1D33
Finished the Anagram problem today, also worked on the circular buffer problem. I think I am doing these exercism problems as a way to procrastinate doing more involved projecct type work. Tomorrow I think I will force myself to work on the VS Code Extension

### R1D34
Did some work on the extension yesterday working on trying to improve the detection of keywords. I feel there should be an easier way of doing this but potentially it is always custom built by people

### R1D35
Worked on extension today and mainly did 'busy' work refactoring and what not. I need to wake up and do this coding in the morning to have some problem solving left in me i think

### R1D36
This was a good day, managed to reorganise the structure of some of the stuff i had been working on into a way that better made sense. Today i will hopefully be able to polish some of it, but feeling good about it

### R1D37
Missed today because I didn't take my laptop with me to Livs. Somewhat dissapointing but oh well just gotta move on and try not slip up again

### R1D38
Today managed to make some headway in the space of extracting functions in their entirety. Still got some work to do on it, but think i have some decent direction with it so far

### R1D39
Worked on the extension today and am really close with it. Have it providing the function complexity on hover. For some reason though the hover is being janky atm and displaying all hovers on one line so need to fix that. Also been working on app W/Matt which is cool

### R1D40
Worked on mine and matts project today which was good, managed to setup ESLint, typescript and nodemon for a new project. Tomorrow think I will focus on hooking up a database and how we will manage that connection effectively

### R1D41
I worked on trying to start building out the DB and connecting to TypeORM today, there was a few hiccups but managed to get a better idea of what direction it would be taking

### R1D42
Managed to put some data into the database using TypeORM today which was cool. Still need to improve the structure within the code but looking good so far

### R1D43
Today managed to make the structure of the code a bit nicer and resolve some issues with the tsconfig which were causing things to crash

### R1D44
I forgot to write my log for this day, but i did code... Think i did something on mine and matts project

### R1D45
I did some work for Tommy at Swyftx today. Adding in functionality for different high value customer levels in intercom. Still a bit off but just need to test it works now

### R1D46
Forgot to write this log - Pretty sure i just fixed a few small typeorm issues while liv was on the phone for her survey

### R1D47
Was at the parents on this day. Just spent some time working on the db stuff 

### R1D48
I worked on expanding out the repository functionality in our database library. Managed to get a few queries working as expected with the query builder which was cool.  

### R1D49
I'm really bad at keeping these logs now. But on saturday I did something with our data structure i think?

### R1D50
Yesterday I kind of faffed about and didn't get much done, was trying to figure out types and create a generic XOR type where i could apply that to entity types so it would be more effective when inserting data in a specific way. But think i found a work around

### R1D51
Today I worked on starting our express backend. It turned out me more researching how to make an effectively structured backend in nodeJS but glad with the progress that was made and tomorrow can hopefully crack on with making some routes. Though also leaning towards implementing a graphQL API so that might change some things? I'm not sure yet

### R1D52
Worked on implementing the graphQL stuff yesterday. Managed to get some endpoints returning data which was good

### R1D53
This day managed to make an endpoint return a collection of trades associated with a given user

### R1D54
I missed this day

### R1D55
I missed this day too 🤦‍♂️

### R1D56
Alright, so i haven't done this logging for a week. But i have been coding daily. Think i will just continue as if i was only on this day and go with that. Was stuck for most of today trying to figure out a problem, but was able to fix it. Was struggling to get the most recent record from a table given an assetId, userId and timestamp. Though i am suspecting some of my problems came from typeorm calling its columns `id` and the SQL command `MAX(columnName)` also having its own id columns... Might investigate this tomorrow. Don't want to run into other funky issues later down the line. Also wondering if i should be swapping do doucment storage through something like mongo, at thiagos suggestion? 

### R1D57
Today managed to get two core things working. One was the ability to get historical balance data for a user's asset up to a specific date. The other was the general flow of registering a user via the graphQL endpoint. Which involved connecting the resolver, to the userService, through to the DB. Might go for another layer of separation here but for now is good. Want to make the repositories get exported directly from the DB library, rather than having to call `getCustomRepository` every time i want to use them. Also had a play with the SQL issue i ran into yesterday. Seems that when you call `MAX(columnName)` it generates another table or something,resulting in that weird behaviour with IDs. Changing the column names of my tables seemed to have no effect on the behaviour. I ran across the HAVING keyword, but couldn't remember exactly how it worked, so might have to explore that further

### R1D58
A day late as i have been doing, but managed to help sort out some of the unit testing stuff with matt today come up with some generally better structure for the project and how data will flow through it. Managed to add in the ability to get repositories directly from the DB lib. This makes the code in other libs more simplified as they don't have to worry about the DB connection itself

### R1D59
Today and yesterday i managed to add functionality around refreshing a users balances. This seems pretty core and definitely something which will need to be revisited down the line. But for now happy with it. Need to spend some time hashing out what our other endpoints and what not look like. Might do that tomorrow morning. But also should probably code if im gonna do anything in particular

### R1D60
Missed the day yesterday but cracked on today. Spent some time better structuring some elements of the project and was also trying to figure out how to import modules correctly using TS. Seems to be a bit of a pain. But hopefully tomorrow might have some more ideas to work with

### R1D61
Wasn't super productive today, but overall managed to make progress with TSConfig stuff and managed to allow us to use absolute imports now! Tomorrow keen to work on fleshing out the coingecko integration stuff

### R1D62
Today was a bit of a shit day in terms of getting stuff done. Mainly spent my hour looking for solutions to the TSConfig module resolution stuff. Turns out the config i thought worked yesterday just allows the TS compiler to know where to look for those modules. But when they get transpiled, the absolute paths don't get changed to valid paths and so the modules then fail to get located. There seemed to be very mixed opinions everywhere about how to fix and address this issue. I am going to go to bed now, but think i will use a plugin called `module-alias` but will see how i go. Honestly just keen to solve this one now

### R1D63
Today spent some more time struggling with the absolute path stuff until i just put it aside so i could make some actual progress with the project. Annoyed i spend the time on trying to figure it out and getting nowwhere. Will likely have to come back at some point in the future and resolve this issue properly. But for now onwards and upwards. Spend some time creating a 1:1 table today to keep track of coin gecko asset mappings as they will likely differ from our internal asset ids etc. Will hopefully help longterm

### R1D64
Yesterday i didn't get a tonne done. Was overall pretty tired and my brain wasn't there. Added some stuff to the coin gecko class. And did some testing around with the api. But nothing solid. Today gonna work on creating a function which i can call with a given assetId in our DB which will also get a few relevant exchange rates and put those into the db

### R1D65
Managed to get coingecko setup today so that i am able to retreive coin price data for each asset in my binance portfolio and store that alongside it in the db. Tomorrow i would like to improve this slightly by getting multiple coin prices in one call rather than individual ones. This will help reduce rate limiting issues early on. Though i imagine it will still be a problem...

### R1D66
Was working on the bulk getting of price data from coingecko today. Though struggled to make progress as i ran into a roadblock when trying to identify the assetInfo from the database for each balance object returned from binance. Not the biggest issue in the world. But i wonder if it is a sign of some key architechture decisions i will need to make... Also making a note that the balance service should probably call an 'exchangeIntegrationService' or similar which would get all integrated exchange data in a consistent format

### R1D67
I missed yesterday but that was because of mine and livs 2 year so ill give myself that one aha. Managed to get the bulk balance getting from CoinGecko today. Took me a bit to sort out a few issues, mainly around linting not liking code and having to figure out ways around it. Was overall a good thought exercise though and glad it is done now. Might spend some time tomorrow trying to figure out how we can abstract away the 'getPricingData' like calls 

### R1D68
Today i removed the binance api key & secret key from the users table, managed to abstract it away so they would be slightly more secure and more scalable for adding new exchanges etc. Overall seems like a good solution. Tomorrow will probably need to add in functionality around an 'exchangeService' which you would call too, and that might go to all exchanges a user has integrated with and make calls to their apis to get current balance data

### R1D69
I actually ended up working on the pricing service today since i think it would be best to wait a little on the exchange service for matts stuff to be merged in. Managed to decently abstract away the logic behind getting prices. Not sure if i like how the interface is atm though, involves alot of array searching, maybe a map would be a better approach...

### R1D70
### R1D71
### R1D72
### R1D73
### R1D74
### R1D75
### R1D76
### R1D77
### R1D78
### R1D79
### R1D80
### R1D81
### R1D82
### R1D83
### R1D84
### R1D85
### R1D86
### R1D87
### R1D88
### R1D89
### R1D90
### R1D91
### R1D92
### R1D93
### R1D94
### R1D95
### R1D96
### R1D97
### R1D98
### R1D99
### R1D100
