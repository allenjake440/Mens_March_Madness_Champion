![NCAA Champion Art](https://github.com/allenjake440/Mens_March_Madness_Champion/assets/134075534/9c552d90-6d45-4b71-bf29-6838626cf0e9)

## Using Machine Learning in preparation to predict the 2024 NCAA Men's March Madness Champion right before the tournament (3/17/2024).

### ![Medium Article](https://allenjake440.medium.com/predicting-the-mens-march-madness-champion-with-machine-learning-892bd78997ca)

#### Acquired Data since 2003 from ![realgm](https://basketball.realgm.com/ncaa/) and ![Men's College Basketball Reference](https://www.sports-reference.com/cbb/seasons/men/2023-polls.html).
##### Since Entire DataBase is too much data to have I file for github, here is a step-by-step contruction log overview of the database.
##### Database Construction:
1. WebScrapped and Hand Copied Data Tables:
   ###### Team Stats:
   - Conference Advanced Team Totals
   - Conference Misc Stats Team Totals
   - Conference Average Stats Team Totals
   - Non-Conference Advanced Team Totals
   - Non-Conference Misc Stats Team Totals
   - Non-Conference Average Stats Team Totals
   ###### Player Stats:
   - Player Conference Average Stats
   - Player Conference Tournament Stats
   - Player March Madness Tournament Stats
   - Player Height and Weight Stats
   ###### Other Stats:
   - Men's College Basketball AP Polls (reverse polls values) (via MCBR)
   - NCAA Div 1 Tournament Bracket (via Wikipedia)

2. Merged (joined) Data Tables:
   
   ###### Team Database:
    - Merged all team datatables and stats
      
   ###### Player Database:
    - Merged all player datatables and stats
  
3. Info on all Custom Calculated Features:
   - Visit the NCAA DataBase Feature Overview file
   
