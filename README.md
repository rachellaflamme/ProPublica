# ProPublica

How to replicate code:

1. Download RSelenium from github. This code can be found here: https://github.com/ropensci/RSelenium

2. Download Docker. This program is needed to save data from scraped pages. This software can be found here: https://www.docker.com/get-started

3. Run the lines "docker run -d -p 4445:4444 selenium/standalone-chrome" and "docker ps" in the terminal. This checks that R and Docker are connected.

4. Run code.