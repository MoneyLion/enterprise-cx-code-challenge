# Code Challenge

In this coding challenge, you will be asked to write a program that solves a specific problem. We will use your solution as a starting point for further discussion. Take however much time you feel is appropriate given your interest and availability. There is no right answer there. Good luck, and have fun!

## Instructions

1. Clone this repository to your local machine
2. Create a new **private** repository on GitHub so others can't copy your work
4. Add the `jeromedane` as a viewer along with any additional people requested elsewhere
4. Push your local clone up to your private repository while preserving history
5. Create an application that solves the problem and requirements listed below 
   * Use the [data set](./data.json) from an imaginary 3rd party provider
   * *Simulate* a data loading time of at least 2 seconds due to imaginary network latency
6. Edit the readme of your application to replace only the intro and these instructions with:
   * Instructions on running your code in development and production modes
   * Roughly how much time you decided to spend on this and why 
   * The technologies you chose and you thought process
   * Things you would like to do but didn't have time for                
   * Anything else you would like us to know
7. Submit the URL of your code challenge submission and attach a zip of the final code

## The Problem

> As a consumer, I want to see a list of comparable savings offers so that I can find one meets my needs.

## Requirements 

```
Scenario: The application shall show a list of available offers
  Given a data set of available offers
  When I view the application
  Then the available offers are displayed
```

```
Scenario: Available offers shall show the logo of the offer partner 
  Given a data set of available offers
  When I views the application
  Then each offer displays the partner logo for that offer
```

```
Scenario: Available offers shall show the details of each offer
  Given a data set of available offers
  When I views the application
  Then each offer displays the details for that offer
```

```
Scenario: Available offers shall have a call to action which opens the offer's URL in a new tab when clicked
  Given a data set of available offers
  When I views the application
  And I click on a call to action on an offer
  Then that offer's URL opens in a new tab
```

```
Scenario: Available offers shall be sorted by Annual Percentage Yield by default
  Given a data set of available offers
  When I view the application
  Then offers shown are sorted by Annual Percentage Yield
```

```
Scenario: Available offers shall be sortable by apy and min deposit
  Given a list of available offers
  When I changes the sort input to by <sort> <order>
  Then the available offers are sorted by <sort> <order>

Examples:
  | sort  | apy        |
  | sort  | minDeposit |
  | order | ascending  |
  | order | descending | 
```

```
Scenario: Available offers shall filterable by type
  Given a data set of available offers with at least one <type> offer
  When I change the product type to <type>
  Then only <type> offers are shown

Examples:
  | type | savings-account        |
  | type | money-market           |
  | type | certificate-of-deposit |
```

```
Scenario: All available offers shall be shown when there are no available offers of the selected type
  Given there are no available offers of a selective type
  When I filter for that type of offer
  Then all available offers are shown
```
