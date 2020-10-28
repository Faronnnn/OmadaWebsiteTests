# OmadaWebsiteTests
 
This is an example project how to use SpecFlow and SpecFlow+Runner to run Selenium Web Tests of Omada.com Website using different Browsers (Chrome, Firefox).

## Attension 
In order to run SpecFlow+Runner on desired machine the Visual Studio Account have to be linked to SpecFlow+Runner account.
If runing test from Test Explorer won't start the browser please check the Test Output and follow the link with description how to link accounts

## TimeTable of work
# 1 week: 
Getting to know the Omada's website and figuring out what is worth testing. After all this website general purpouse is giving people informations about company.
# 2 week: 
Writing PageObjects, test scenarios and implementation of these tests. Omada's website has almost no ID's so creating selectors were quite time consuming.
# 3 week:
In order to give as simple as possible ability to pick Browsers in which tests are running I decided to change adapter to SpecFlow+Runner which required to gave up NUnit. Last 2 days I had to figureout the correct configurations for the Browsers (firefox was not willing to cooperate with files downloading).

## Tests
# General info:
I order to pick different browser for the specific test all you need to do is to add tag that points to this browser before desired test: @Browser_Chrome or @Browser_Firefox

# Test 1:
Test is checking responsiveness of contact form on the website. This form has attached Captcha so I could only fill the form fields and check if they are keeping the values. Contact form is loaded inside iframe which creates small delay in loading. Also comboboxes are unusual because they don't act as fields and aloow to type values. Also the hold values, sometimes in "Value" and sometimes in "value".

# Test 2:
Checking if jobs offers are accessible through external website. This test simply checks if there is an offer with specific name on the website where Omada tries announces their work offers.

# Test 3:
