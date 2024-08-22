![NCAA Champion Art](https://github.com/allenjake440/Mens_March_Madness_Champion/assets/134075534/9c552d90-6d45-4b71-bf29-6838626cf0e9)

## Using Machine Learning in preparation to predict the NCAA Men's March Madness Champion for every up-coming year!

### ![Medium Article](https://allenjake440.medium.com/predicting-the-mens-march-madness-champion-with-machine-learning-892bd78997ca)

#### Acquired Data since 2003 from ![realgm](https://basketball.realgm.com/ncaa/) and ![Men's College Basketball Reference](https://www.sports-reference.com/cbb/seasons/men/2023-polls.html).

##### Project About:
- Since my NBA champion project is fully end-to-end (web scraped -> transformed -> analyzed) in python, this project is NOT web scraped by code entirely. 
##### How to setup/run the Project:
- For predicting new seasons in the future, for example 2025, 2026 you'll have to hand copy the new season data from website using my given links to find the approriate tables, then format as follows in each file (via excel/python/whatever).
- Then run python file ncaa_champ_data then run ncaa_champ_ml for results.

##### CSV's | website location links
- all_coach_data (https://www.sports-reference.com/cbb/seasons/men/2024-coaches.html)
- all_player_cf_tour_avg_data (https://basketball.realgm.com/ncaa/stats/2024/Averages/Qualified/All/Conference_Tournament/All/points/desc/1/) All pages, Qualified Checked
- all_player_crs_avg_data (https://basketball.realgm.com/ncaa/stats/2024/Averages/Qualified/All/Conference_Regular_Season/All/points/desc/1/) All pages, Qualified Checked
- all_player_mm_tour_avg_data (https://basketball.realgm.com/ncaa/stats/2024/Averages/Qualified/All/Post-Season_NCAA_Tournament/All/points/desc/1/) All pages, Qualified Checked
- all_team_ap_poll_data (https://www.sports-reference.com/cbb/seasons/men/2024-polls.html)
- all_team_crs_advanced_data (https://basketball.realgm.com/ncaa/team-stats/2024/Advanced_Stats/Team_Totals/4)
- all_team_crs_average_data (https://basketball.realgm.com/ncaa/team-stats/2024/Averages/Team_Totals/4)
- all_team_crs_misc_data (https://basketball.realgm.com/ncaa/team-stats/2024/Misc_Stats/Team_Totals/4)
- all_team_kenpom_data (https://kenpom.com/)
- all_team_ncrs_advanced_data (https://basketball.realgm.com/ncaa/team-stats/2024/Advanced_Stats/Team_Totals/2)
- all_team_ncrs_average_data (https://basketball.realgm.com/ncaa/team-stats/2024/Averages/Team_Totals/2)
- all_team_ncrs_misc_data (https://basketball.realgm.com/ncaa/team-stats/2024/Misc_Stats/Team_Totals/2)
- all_team_tournament_data (This is not pre-set on any website the was together from wiki scraping, coding, and personal research with said, its 100% correct. All Men's NCAA D1 bball teams since 2003 tournament seed, tournament wins, and bracket region.)
- team_index_custom 
- team_index_season (https://basketball.realgm.com/ncaa/teams)
  
   
