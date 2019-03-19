## 2019-02-18

### What did you do this week?

- Rachel: I worked with Ru on the if statements to work on the exceptions in the html scraping and properly building the data frame. In addition, I learned mapping in Data camp in order to implement it in our algorithm. I also wrote an email to Sophie in order to update her on our progress on the project. We felt that it was not necessary to meet virtually and an email would suffice. I also set up an appointment with Albert Kim to work on for loops.

- Ru: I tried working on some if and while statements to scrape the multiple doctors. I also tried getting the code we have so far to automate so we can loop over and move to the next button.  We also sent an update to Sophie and are waiting to hear from her.  

- Maggie: 

### What is it that you're struggling with right now?

- Rachel: We are struggling with putting our outputs together. We can scrape all information from the medical institutions that only have one doctor. Or we can scrape all the information from medical institutions with multiple doctors; however, we still have no combined the two outputs together. We also are having trouble with building a for loop to click the "next" button but we do have a psuedocode of what we could potentially do to solve this problem.

- Ru: I still can't get the if statement to scrape correctly. So far, all it does is get just one of the three doctors' names that are provided. I thought this was because an if statement only runs through once, so I tried using a while loop, but this is also throwing an error. 
Other issue I'm having is automating the 'next' button. For this, I tried putting it in an infinite loop that will run until we reach the last 'next' button but this isn't working. I also realized that the next button has an element/ attribute that says "go-to-page = (the number of the next page)" so I thought this may be put it in a while loop but I don't know how to extract the selector/xpath as it contains a button and some text. 

So far this is what we are using:
  "#populated_addresses > div:nth-child(11) > div > div.next > button"

This is the element I'm trying to work with...if it works: 

<button data-type="pagination-button" data-go-to-page="2" class="uscis-button uscis-button-clear paginate_next" type="button" onclick="$(this).ga_event('', 'click', 'Next Page - Button');">
          Next<span class="fa fa-icon-right fa-chevron-right"></span>
        </button>
        
I'm not sure what the data-go-to-page="2" is but it looks useful. 
  

- Maggie: 

### What are you planning to do next week?

- Rachel: This week, I am planning to still work through the if statements and see if we can get the appropriate output. I am also planning to meet Albert Kim to work on the for loops to hit the "next" button.

- Ru: For this week, I'm just going to focus on trying to get the next button to keep moving. I tried the if statement for extracting the multiple doctors and it's not working, but I think this can be something we can solve later after the basic code is fully functional.  

- Maggie: 



##2019-02-25

### What did you do this week?

- Rachel: As a team, we were able to get docker running on each of our laptops. We met on Friday to discuss the best way to tackle the problem. We discussed switching over to Python because Selenium in Python has more thorough documentation as opposed to R where we only found one pdf where some of the code is defunct although it says it was written on January 3, 2019. I individually worked on the project and was able to interact with the website through R and was working on typing various zipcodes into the search bar to have the entirety of the steps automated. In addition, I was analyzing the various xpaths in the HTML pages that I have scraped in order to figure out how to animate this process.

- Ru: We were able to get Docker running on all of our machines, and we met during the week to find the best ways to proceed. We also briefly spoke about switching to Python as there are more Python tutorials. This week, I decided to break down the problem into chunks in order to solve it. So I created learning goals for myself to get used to RSelenium while solving our issues. So I broke down the issue into:
        1. Open chrome in a web browser --done
        2. Navigate to a certain page and open it  -- done
        3. Find the search element and input a 5 digit zipcode --done
        4. Search. The 10 doctors should pop up --done
        5. Scrape these and put them in dataframe --a few issues joining the dataframe
        6. Click next                             --done
        7. Scrape the next page and put them in dataframe --same as 5

I was able to complete steps 1-4 and 6, albeit in chunks that I think should be made into a function. I used RSelenium for steps 1-4 and can now get my code to search a zipcode and show results. I was also able to get the code to click 'next' and 'scraped' the next 10 doctors. I attached my practice code for reference.


- Maggie: At the beginning of the week, I primarily focused on getting Docker and RSelenium working on my computer, similarly to the rest of my group. While Docker installed without any problems and seems to be working correctly, I, like the rest of my group, was facing some problems when it came to using the code related to RSelenium. I proposed trying to use the Python version of Selenium, because of the errors we encountered using the R version of this program did not have answers available to solve them (problems related to code being out of date, etc), and we were unsure of how to fix this problem. Currently, I am doing research on the Python version of this program and trying to determine its ease of use, and seeing if it is a viable change to make.

### What is it that you're struggling with right now?

- Rachel: The biggest hurdle that I have is just to push through the code errors I have been getting. They have been "easy" fixes but they have been harder to debug since the entire team is unfamiliar with RSelenium. I still have to figure out how to reformat the already scraped data that has exceptions. i.e. when one hospital has multiple authorized doctors. (but that is also an easy fix that just takes time)

- Ru: 
        1. My draft code still needs to be developed. Using what I've used so far, it would be a repetition of the same code over and over again so I am trying to think of the best way I can create a for-loop without breaking the system since the endpoint has no url.Ideally, my pseudocode would have something like "for i in length of pages", but I'm still a little confused on how to do this.

        2. I am having issues pasting the results to each other into a single dataframe because some of the practices have multiple doctors and this is being returned as NA. 
        3. My scraping code: I have been looking for a way to extract multiple classes at once under the div "col-span-10", but these come as individual rows so I need help looking for a better way to scrape the data. Right now, it seems like the code would just be running on the same page over and over again and this would be redundant. I'm also afraid it may also eventually take more time and memory. 
        4. I still need a little more time figuring out how to combine rvest and RSelenium together so at the moment, I just have many  chunks of code. I don't know the best way to piece everything together. 
        5. I forgot how to write functions and for-loops in R, so I need to brush up on that. 


- Maggie: We are still having problems related to getting Selenum to work in R. I think my entire group would rather use this program than the version in Python, because we are all more familiar with R and feel we would likely be able to troubleshoot smaller problems with this program, but the lack of information related to Selenium seems to be causing us problems. As a result, I have encountered some issues with the Python version and I am finding it is taking longer to solve them.

### What are you planning to do next week?

- Rachel: Just carving out time to push through the problems and sit and code. It seems we are in the stage that we know what to do and just need to do it. It would be best if there was a hackathon but self-discipline is the next best thing.

- Ru:  Meet with my partners to finalize which language we are using. I need to merge the chunks of code into a for-loop that iterates through all the pages of the websites. To do this, I will write some kind of steps again, as I noticed this helped this week, create a pseudocode for what my loop should do and how it should run and get the for-loop running. I also need to brush up on R functions, for-loops and find a way to deal with situations where we have multiple doctors so the result ends up being missing.This should probably be the first step so as to create a dataframe for the first twenty doctors.



- Maggie: As others have said, mainly trying to create a final code in order to scrape the website. In addition, I want to decide what program my group would like to use and, whatever our decision is, do more research on what is the problem with what we are attempting to code.




## 2019-02-18

### What did you do this week?

- Rachel: I was working with RSelenium, but in order to interact with the webpages, the Docker needs to be installed. However, my code has been constantly throwing errors. Due to one of our team members being sick this week, we were unable to meet and therefore, I was unable to work with my team mates to problem solve. I also worked on the DataCamp module of Webscraping with XPATHs. It was incredible helpful and will be able to provide a lot of progress once I get the Docker and RSelenium to react with my server. One thing that the web-module discussed is the legal ethics of this but didn't dive into those issues and i would like to discuss that in class

- Ru: Last time, I had been having troubles working with CSS selectors. So this week, I worked on the Datacamp Module(Working with Web Data in R). The module was incredibly helpful and gave me a basic understanding of xpaths, html structure and css selectors. It also gave me a chance to brush up on creating functions so that was an added advantage. Though my partners and I were not able to meet, we were able to create goals for the week and I was able to complete most of the assigned tasks for the week.  

- Maggie: A large part of the week was dedicated to creating our update prsentation, of which I wrote a lot of information on. In addition, I finished the datacamp class regarding webscraping and I feel that I now have a pretty good knowledge of the concepts, at least without any hands-on experience. Also, I did some work on RSelenium and Docker to try and understand the programs and how they work, and how they will work in the context of our project.

### What is it that you're struggling with right now?

- Rachel: I am really struggling with the docker interacting with my server. I have been following along with multiple tutorials but the errors my terminal keeps responding with don't have explanations in the tutorials. I would like to work with Ru to figure out how she got the docker to interact with R with an iOS system.

- Ru: At the moment, nothing? I have a question though...based off of the Working with Web Data in R, one of the instructors said that some websites are designed in the way ours is because the owners of the website may not want people to scrape data. What are the ehical issues regarding what we are doing..especially as this is a government website? 
It could be open to students, but will ProPublica have the legal rights to claim/use the data we obtain? 


- Maggie: Currently I think our largest struggle is getting RSelenium and Docker to work and code it so we can scrape data from the web, but because of our current level of skill in regards to these programs, we are still having some problems.

### What are you planning to do next week?

- Rachel: I am planning on trying to get Rselenium to scrape at least the first two html pages in the uscis.gov site and save it as a file. This way, we can guarentee we can automate the process some how.


- Ru:  Docker is pretty difficult to install so we will be meeting to make sure everyone is up to date with the installation. I also plan to integrate the two tutorials we have learnt and try to get Rselenium and another web scraping package to scrape at least the first two html pages in the uscis.gov site and save it as a dataframe. 

- Maggie: Create a viable program which will begin to scrape the website for data we need, which is the main goal of this project. In order to do this, we will also have to have a firm grasp on these programs and make sure the programs are installed properly.

## 2019-02-11


### What did you do this week?

- Rachel: Our team met Sophie at ProPublica through Zoom. We discussed the scope of the project which was fairly straight forward and discussed the expected turn around time of the project which is 2 weeks to a month from now. Last week, we figured out how to manually scrape the data and noticed the exceptions in the formatting that we have to note. As a group, we decided to focus on using R instead of Python for this scraping project since Ru found Selenium that functions in R. This week, I have worked on understanding the basics of Selenium as well as following through with the manual scraping data method we were exploring last week in order to practice using rvest and other r scraping packages.

- Ru: We talked to Sophie, our new contact for this project last week Wednesday to go over the project and hear her expectations for the project. I also looked at various web scraping packages in R, including rvest, xml2, httr and RSelenium in order to find out which may be better suited for our project. Sophie had suggested using Selenium in R, but I found that R has its own version(RSelenium) so I have been learning how to use it. I  managed to install Docker in order to virtually interact with the webpage and have been playing around with        Docker and RSelenium to have a feel of this package. At the moment, I have been using other tutorials online instead of Datacamp as it seems Datacamp may not have enough information for what we need.  

- Maggie: Worked on a method of web scraping that could work with the
    task on hand, but was problematic because it was largely manual.
    Talked to our contact at ProPublica and determined what our goals
    were with her and what her expectations were of us. Worked on a
    datacamp course regarding webscraping, which we believe will be our
    main task after talking to our contact. Particularly, I worked on
    trying to understand Selenium for R, because that was suggested to
    us by our contact, and tried to determine if this would work with
    our project.

### What is it that you're struggling with right now?

- Rachel: I am struggling the most with gaining enough knowledge and skill to deliver this project in the suggested time frame. Since we are so new to all these tools, its really hard to get basic footing to even build a basic algorithm. It's also really difficult because it feels like the group is running in circles because we don't know where to start so a lot of false starts seem to keep occuring. Also, (this is entirely my personal preference which should be discussed with the group) I would like to meet with the team more times during the week because I feel like I learn the most with group work and having other people in live time to help me through a problem or logic that I am struggling with. However, our schedules are generally conflicting so we will need to sort this discrepancy out.

- Ru: Getting started. I understand our webpage is interactive, and has no endpoint url. Though I now know how to navigate it using RSelenium, I haven't quite found the best way to find the elements in page using CSS selectors. I think this may be because we have a lot of classes within a div? and divs within divs? I feel this may be easier to understand once I understand selection of different elements so I'm still looking for tutorials on this.  

- Maggie: Right now, I am trying to determine a better way of web
    scraping the website containing the names of doctors that works with
    the formatting of the website, because our current method is based
    mostly around the manual collection and input of data.

### What are you planning to do next week?

- Rachel: Learn as much as we can about the tools that can potentially help us to solving how to get around the static url and automating the scraping process. I think that we need to devise a strategy to solve this problem one way before we keep searching for new avenues to solve the problem.

- Ru: I'm planning to learning more about css selection in RSelenium and find out if I can pull out a few doctor's names and their addresses from the website using RSelenium and possibly rvest.  

- Maggie: Do more research on Selenium and start working with it or a
    similar program to try to scrape the website for relevant data for
    our client.

## 2019-02-05

### What did you do this week?

- Rachel: I worked through the DataCamp module Working with Web Data in R in regards to the first three chapters: Downloading Files and Using API Clients, Using httr to interact with APIs directly, Handling JSON and XML. I also looked through the USCIS.gov and tried to use the techniques taught in the DataCamp course. I found the company that hosts the data for the search for a doctor; however, have not figured if the public has access to the data in CSV format.

- Ru: I watched the first three DataCamp videos for Working with Web Data in R and learnt how to download files from the web, using API clients and interacting with APIs. I also briefly looked at the USCIS website and read briefly about selenium package our client advised us to use. I found that there is a similar package in R, and hopefully it will be efficient enough to use for our project.  We also got in touch with our contact and are will be having our first meeting this week through Zoom on Wednesday. 

- Maggie: I did a lot of background research on Brady violations before our topic changed. I also did a bit of research on malpractice as well as laws regarding immigration to the United States, and did a bit of self-teaching on web scraping and Github. I, along with everyone else, also planned a meeting with our contact at ProPublica.

### What is it that you're struggling with right now?

- Rachel: I am struggling to figure which coding language we will end up using for the data scraping. Our client, Sarah, provided us with a resource Selenium which works best in python but my coding strength is in R. In addition, it’s difficult to find the resources that are most applicable to our project rather than generalized Data scraping courses.


- Ru: I’m still looking for the best way to scrape data from the USCIS website (Python vs R) as the page is responsive and does not necessarily have different endpoints for the url. It looks like the preferred method might end up being Python, but as I am more familiar with R, I've been trying to look for other packages we can use in R that will be helpful.  

- Maggie: trying to find out the best way to find data in the USCIS.gov, so that it can be scraped in the best way possible. We are also currently still trying to determine how this project’s trajectory as we recently had to change topics.

### What are you planning to do next week?

- Rachel: Planning to work through the rest of the applicable DataCamp courses in regard to webscraping in HTML, since that appears to be the language the site is coded in, and begin to code some basic data scraping techniques. In addition, we need to figure out the best way to organize the data set for our code to eventual compile the data into our data set structure.

- Ru: Planning to start using the skills used in DataCamp to scrape data from the website. We are meeting the client on Wednesday to talk more about the project.  

- Maggie: more research on web scraping and how to best implement it, and trying to navigate the website from which we will be getting our data.




