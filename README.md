# Predicting the NCAA Men's March Madness Champion Using Machine Learning

<div align="center">
  <img src="https://github.com/allenjake440/Mens_March_Madness_Champion/assets/134075534/9c552d90-6d45-4b71-bf29-6838626cf0e9" alt="NCAA Champion Art">
</div>

## Overview

Predicting the NCAA Men's March Madness Champion using machine learning based on historical data.

### [Read the Medium Article](https://allenjake440.medium.com/predicting-the-mens-march-madness-champion-with-machine-learning-892bd78997ca)

---

## Data Sources (Since 2003)

- [RealGM](https://basketball.realgm.com/ncaa/)
- [Men's College Basketball Reference](https://www.sports-reference.com/cbb/seasons/men/2023-polls.html)

---

## Project Details

This project is a continuation of my NBA champion project. While that project uses full web scraping, much of the data for this NCAA project was hand-collected over time.

The project uses machine learning techniques to predict the NCAA Men's March Madness champion for upcoming years.

### How to Set Up and Run the Project

1. For predicting future seasons (e.g., 2025, 2026), manually copy the new season data from the websites linked below.
2. Format the data (using Excel, Python, or other tools) according to the required structure.
3. Run the Python file `ncaa_champ_data.py` to load the data.
4. Run `ncaa_champ_ml.py` to generate predictions.

---

## CSV Files and Data Sources

Below is a list of the required CSV files and their corresponding sources:

- **all_coach_data**: [Sports Reference Coaches](https://www.sports-reference.com/cbb/seasons/men/2024-coaches.html)
- **all_player_cf_tour_avg_data**: [RealGM Conference Tournament Player Stats](https://basketball.realgm.com/ncaa/stats/2024/Averages/Qualified/All/Conference_Tournament/All/points/desc/1/) (All pages, "Qualified" checked)
- **all_player_crs_avg_data**: [RealGM Conference Regular Season Player Stats](https://basketball.realgm.com/ncaa/stats/2024/Averages/Qualified/All/Conference_Regular_Season/All/points/desc/1/) (All pages, "Qualified" checked)
- **all_player_mm_tour_avg_data**: [RealGM NCAA Tournament Player Stats](https://basketball.realgm.com/ncaa/stats/2024/Averages/Qualified/All/Post-Season_NCAA_Tournament/All/points/desc/1/) (All pages, "Qualified" checked)
- **all_team_ap_poll_data**: [Sports Reference AP Poll Data](https://www.sports-reference.com/cbb/seasons/men/2024-polls.html)
- **all_team_crs_advanced_data**: [RealGM Conference Regular Season Advanced Team Stats](https://basketball.realgm.com/ncaa/team-stats/2024/Advanced_Stats/Team_Totals/4)
- **all_team_crs_average_data**: [RealGM Conference Regular Season Team Averages](https://basketball.realgm.com/ncaa/team-stats/2024/Averages/Team_Totals/4)
- **all_team_crs_misc_data**: [RealGM Conference Regular Season Miscellaneous Stats](https://basketball.realgm.com/ncaa/team-stats/2024/Misc_Stats/Team_Totals/4)
- **all_team_kenpom_data**: [KenPom](https://kenpom.com/)
- **all_team_ncrs_advanced_data**: [RealGM Non-Conference Regular Season Advanced Stats](https://basketball.realgm.com/ncaa/team-stats/2024/Advanced_Stats/Team_Totals/2)
- **all_team_ncrs_average_data**: [RealGM Non-Conference Regular Season Team Averages](https://basketball.realgm.com/ncaa/team-stats/2024/Averages/Team_Totals/2)
- **all_team_ncrs_misc_data**: [RealGM Non-Conference Regular Season Miscellaneous Stats](https://basketball.realgm.com/ncaa/team-stats/2024/Misc_Stats/Team_Totals/2)
- **all_team_tournament_data**: This data was gathered from various sources, including scraping Wikipedia and personal research. It includes data on all Men's NCAA D1 basketball teams' tournament seeds, wins, and bracket regions since 2003.
- **team_index_custom**: Update this for new school name changes if necessary for future seasons.
- **team_index_season**: [RealGM Teams](https://basketball.realgm.com/ncaa/teams)

---

## Notes

- The data for this project was hand-collected. For future seasons, data should be manually collected and formatted appropriately.
- The project involves machine learning techniques using Python to predict NCAA champions based on various statistical data sources.

