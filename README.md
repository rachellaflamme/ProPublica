# ProPublica

This code allows us to scrape the United States Citizenship and Immigration Services website, which contains all of the doctors recommended by the government for screenings before immigrants are granted greencards. This research is being done for the news website ProPublica. These are instructions on how to properly run this code, as numerious software packages are required.

# Installation

1. Install the following packages into R if you already have not done so.
-`install.packages("RSelenium")` This code can be found here: https://github.com/ropensci/RSelenium
-`install.packages("xml2")`
-`install.packages("rvest")`
-`install.packages("dplyr")`
-`install.packages("purr")`
-`install.packages("tidyverse")`

2. Download Docker. This program is needed to save data from scraped pages. This software can be found here: https://www.docker.com/get-started

3. Run the lines "docker run -d -p 4445:4444 selenium/standalone-chrome" and "docker ps" in the R terminal. This checks that R and Docker are connected.

4. Run code.
