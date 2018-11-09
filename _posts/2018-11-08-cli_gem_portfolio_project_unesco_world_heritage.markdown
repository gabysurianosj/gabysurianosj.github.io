---
layout: post
title:      "CLI Gem portfolio project: UNESCO World Heritage"
date:       2018-11-08 18:28:10 -0500
permalink:  cli_gem_portfolio_project_unesco_world_heritage
---


The 'UNESCO World Heritage Finder' was created to help you find any world heritage site listed in [UNESCO's website](http://whc.unesco.org/en/list/). You can pick which site you are interested in learning more about - maybe it will lead to your next travel destination!

![](https://external-preview.redd.it/7LZhh3eXfHte1UR2ft_OeL1VuyK8k5w7SbIFctXi8FU.jpg?auto=webp&s=077fc4adf20bc82d175106951805ae44ddc46df1)

With 1,092 sites listed, we hope this app facilitates the process of narrowing down your search to learn more about the World Heritage sites. 

The below is the process I took to create this app: 
* Chose a website to scrape. I decided I was going to focus on something related to travel/culture because that's something I love 
* I used this [link](https://bundler.io/v1.12/guides/creating_gem.html) provided on the project guidelines to help me start creating my ```gem``` using ```Bundler``` 
* Once my scaffold directory was created, I went into my ```Gemfile``` and made sure all the gems I was going to need where included in my file 
* Then, I started creating the files I was going to need to follow the initial logic, which went as follows: I need a CLI class that would be responsible for getting the input from the user and displaying information. I also need a Scraper class that would be responsible for scraping information from the webpage. And finally, I would also need a class that pulled the scraping and creating-new-objects functionality together. 
* I first created the executable file - the [CLI Applications in Ruby lesson](https://learn.co/tracks/full-stack-web-development-v5/intro-to-ruby-development/command-line-applications/cli-applications-in-ruby#running-cli-applications) were very helpful as I started to move forward with the process
* The Controller class is responsible to welcome the user and prompt the user with questions to use the application
* As the user progresses through the app, the Controller class calls for the Site and Scraper classes when required - the Site class is responsible for inheritig from the... and the Scraper class is responsible to scrape the website and return the site name and description asked for by the User 
* Then it was time for testing. I had an issue here because I had forgotten to grant the file execute permissions so I kept getting the following message: ```bash: bin/cli: Permission denied```. Again, the CLI Application in Ruby lesson was helpful and I used ```sudo chmod +x bin/cli``` to grant it access 
* Finally, I worked on styling my gem. While testing, I noticed it was hard for the User to differentiate what text was what so I wanted to make sure I could create something easy to follow so I installed ```gem 'colorize'``` and used it to color code the messages on the app 

I hope you enjoy it as much as I have! 





