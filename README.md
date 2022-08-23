# Passbokning-Sweden 
Python selenium script that can carry out full boking. Date range selection possible. 

  
The script works by pressing "Nästa lediga tid" untill a free date within specified date range is found and then it fulfills the booking. Because of anti bot measures on the website, it uses Anti captcha solver to bypass this problem. The bot can run continually until it books a time without getting booted off the website. 
This script works as of 2022-06-22.  

Anticaptcha used https://anti-captcha.com/. For usage make an account and use API key from website in Main code. 


# Background 
In early 2022 the amount of people looking to make a new passport in Sweden peaked and the wait time was over a year. The only way to find a time fast was to find a time another person unbooked, this is done by pressing the "Nästa lediga tid" button which is both boring and tedious. When I noticed I needed a new passport, I investigated what could be done to speed up the process. What I found was that a simple Selenium script could do all actions. It took afew weeks but then 2022-03-21 the full bot worked and I managed to book a time formyself the same week ( even the same day 😊 ).  

What later conspired was about 4 mounths of booking time for people for free. As of 2022-08-23 about 300 passport times were booked. Many different versions of the script were made to book for up to 5 people, however these versions are unpolished. 

 

# Developments
2022-04-28 

Bot protection added, website searched for ‘’navigator.webdriver’’. Solved in about 4 hrs 

2022-04-31 

Captcha added. Investigated possibilities in making my own captcha solver with tensorflow because the captcha images were simple. Solved by integrating Anti Captcha solver service because price per solved captcha was negible and the time it would take to code and train my own captcha solver would be too long (Will be doing this later when I have time). 

2022-05-02 

Further Bot protection added, website looked for $cds_ in chromdriver files. Rerouted connecting when found. Solved by changing $cds_ string in hex editor. 

2022-05-19  

Bankid added. Solved by sending QR image to people that need the booking, played around with sending SMS however the simplest solution was just sending it on facebook messenger. 
