![NCAA Champion Art](https://github.com/allenjake440/Mens_March_Madness_Champion/assets/134075534/9c552d90-6d45-4b71-bf29-6838626cf0e9)

## Using Machine Learning in preparation to predict the NCAA Men's March Madness Champion for every up-coming year!

### ![Medium Article](https://allenjake440.medium.com/predicting-the-mens-march-madness-champion-with-machine-learning-892bd78997ca)

#### Acquired Data since 2003 from ![realgm](https://basketball.realgm.com/ncaa/) and ![Men's College Basketball Reference](https://www.sports-reference.com/cbb/seasons/men/2023-polls.html).
##### Since the entire the database file is too large to share on github, here is a step-by-step contruction log overview of the database.
##### Database Construction:
1. WebScraped and Hand Copied Data Tables:
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
   - NCAA kenpon (via kenpon.com/subscription) all pre-tourney data

2. The RawData file was created in Excel, by collecting all of this data.

3. Custom Features:
   
