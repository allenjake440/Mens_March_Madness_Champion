# Team and Player Rating Custom - The Science Behind the Statistic

**Player Rating Custom** is a regression-based, scaled formula that assigns a season score to each player on a 0-100 scale. This rating takes into account the player's average game score within their conference, the average AP Poll ranking (From Pre-Season to the 18th Poll *NOT FINAL*) of their team throughout the season, and the team's average margin of victory. Note that these statistics only include regular season games, both in-conference and out-of-conference.
**Team Rating Custom** is simply the average of all Player Rating Custom values for players on that team for the given season. This score represents the overall performance level of the team by summarizing individual player contributions.

# The Breakdown of Player Rating Custom

## Game Score (Player Stat) - The Science Behind the Statistic

The formula for calculating Game Score is as follows:

\[
\text{Game Score} = \text{Points} + 0.4 \times \text{Field Goals Made} - 0.7 \times \text{Field Goals Attempted} - 0.4 \times (\text{Free Throws Attempted} - \text{Free Throws Made}) + 0.7 \times \text{Offensive Rebounds} + 0.3 \times \text{Defensive Rebounds} + \text{Steals} + 0.7 \times \text{Assists} + 0.7 \times \text{Blocks} - 0.4 \times \text{Personal Fouls} - \text{Turnovers}
\]

### Explanation

In simpler terms, the formula combines both positive and negative elements of a player's performance, giving a weighted score to various actions they take on the court:

- **Positive Contributions**:
  - Points scored, field goals made, rebounds (offensive and defensive), steals, assists, and blocks all add to the Game Score, as they represent positive contributions.
  
- **Penalties**:
  - Missed field goals, missed free throws, personal fouls, and turnovers subtract from the Game Score, as they are typically detrimental to the team’s performance.

This combination provides a quick summary of a player's impact, allowing fans and analysts to assess their performance in a single number.

### Code for Game Score

```python
all_player_data['crs_GmSc'] = (
    all_player_data['crs_PPG'] +
    0.4 * all_player_data['crs_FGM'] -
    0.7 * all_player_data['crs_FGA'] -
    0.4 * (all_player_data['crs_FTA'] - all_player_data['crs_FTM']) +
    0.7 * all_player_data['crs_ORB'] +
    0.3 * all_player_data['crs_DRB'] +
    all_player_data['crs_SPG'] +
    0.7 * all_player_data['crs_APG'] +
    0.7 * all_player_data['crs_BPG'] -
    0.4 * all_player_data['crs_PF'] -
    all_player_data['crs_TOV']
)
```

## Methodology 

1. **Feature Scaling**: Each feature is absoluated min-max scaled.
2. **Weighted Scoring**: Features are multiplied by specific weights (detailed below) based on insights, trial and error, and domain expertise.

The code and visualizations provided clarify each feature's weight (as a percentage) in calculating the QB Season Rating Custom metric. See the `nfl_champ_data` file for complete code details.

### Feature Weights Breakdown

| Feature                           | Description                                                                                       | Weight (%) |
|-----------------------------------|---------------------------------------------------------------------------------------------------|------------|
| `crs_GMSc`                               | Player's average regular season in-conference game score                                                           | 53.32     |
| `TD`                         | Player's associated teams average margin of victory (in & out of conference regular season games)                                                       | 29.63      |
| `sum_mvp_shares_L4S_cs`        | Player's associated teams average AP Poll Rank from pre-season to poll 18                              | 17.05      |

### Bar Chart Feature Weights Breakdown

<div align="center">
  <img src="https://github.com/user-attachments/assets/6cf9db5d-21de-43c6-98ba-452a304bd4bd" alt="player_rat_cus">
</div>

### Code for Player Custom Rating Calculation

```python
all_player_data['player_rating_custom'] = (all_player_data['crs_GmSc'] * 2.5) + all_player_data['MOV'] - (all_player_data['avg_ap_poll_rank_Pre_18'] * .75)
```
