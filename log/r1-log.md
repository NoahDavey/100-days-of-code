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
### R1D24
### R1D25
### R1D26
### R1D27
### R1D28
### R1D29
### R1D30
### R1D31
### R1D32
### R1D33
### R1D34
### R1D35
### R1D36
### R1D37
### R1D38
### R1D39
### R1D40