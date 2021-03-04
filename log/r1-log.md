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
### R1D12
### R1D13
### R1D14
### R1D15
### R1D16
### R1D17 
### R1D18
### R1D19
### R1D20