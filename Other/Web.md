# Web

## Open Invitation

You have been tasked with finding security loopholes in an organization. You started with mapping the organization's web servers and looking for exposed sensitive information. After a while, you stumbled upon the following knowledge base page. Can you check the source code and find something sensitive that was left behind?

## Solution
This was a simple solution, I spawned the Docker and loaded up the website. In the description it asks to check the source code so that is what I did. 

To get to the source code, I right clicked on the website and clicked on the *Inspect* option. Once opened, I went under the *Inspector* option and began searching the HTML code for the flag. To make searching for the flag easier you can specify what you are looking for within the HTML code.

## sqlme
I think my login panel application might be vulnerable, could you figure it out and try to login as admin? 

This challenge provides a Docker server as well as the source code for the server and the database.

## Solution
Based on the challenge name and the description my brain went to trying to inject sql code to find the flag. 

Before attempting any injections, I downloaded the source code and began inspecting it. There was file named *database.js*, upon further inspection of the code, I found the query that is made to log in the user. This is where a possible SQL injection can happen.

>let query = `SELECT username FROM users WHERE username = '${user}' and password = '${pass}'`;

We can exploit the fact that, in the SQL query we are using the keyword *AND*. The query is asking for the username *AND* the password. 

If we can somehow change the *AND* into an *OR* that means all we will need is the correct username and we will be able to get the flag.

Also, after inspecting the code I determined that the username we will be using to log in as an admin will be **admin**

The text I put into the username box is the following:
`admin' or'`

Making the query look like: 
>`SELECT username FROM users WHERE username = 'admin' or'' and password = '${pass}'`;

As we can see with the way I added single quotes I was able to an OR statement into the SQL query making me only need the correct username to get the flag.




