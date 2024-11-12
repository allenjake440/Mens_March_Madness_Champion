# Team and Player Rating Custom - The Science Behind the Statistic

- **Player Rating Custom**  is a weight based formula that assigns a season score to each player on a 0-100 scale. This rating takes into account the player's average game score within their conference, the average AP Poll ranking (From Pre-Season to the 18th Poll *NOT FINAL*) of their team throughout the season, and the team's average margin of victory. Note that these statistics only include regular season games, both in-conference and out-of-conference.
- **Team Rating Custom** is simply the average of all Player Rating Custom values for players on that team for the given season. This score represents the overall performance level of the team by summarizing individual player contributions.

# The Breakdown of Player Rating Custom

## Game Score (Player Statistic) - The Science Behind the Statistic

The formula for calculating Game Score is as follows:

Game Score = Points + 0.4 × Field Goals Made − 0.7 × Field Goals Attempted − 0.4 × (Free Throws Attempted−Free Throws Made) + 0.7 × Offensive Rebounds + 0.3 × Defensive Rebounds + Steals + 0.7 × Assists + 0.7 × Blocks − 0.4 × Personal Fouls − Turnovers

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

## Methodology - Understanding whats important in the Formula

1. **Weighted Scoring**: Each feature is multiplied by a defined weight (detailed below), determined through insights, trial and error, and domain expertise.
2. **Feature Importance**: To assess feature significance within the player rating metric:
   - First, calculate the average value for each feature.
   - Next, multiply this average by the corresponding weight.
   - Finally, divide each weighted value by the sum of all weighted values to yield the relative importance of each feature.
3. **Pearson Correlation Coefficients**: Whats the PCC for each feature to the result of the metric.

The code and visualizations provided clarify each feature's weight (as a percentage) in calculating the player Season Rating Custom metric. See the `ncaa_champ_data` file for complete code details.

### Feature Weights Breakdown

| Feature                           | Description                                                                                      
|-----------------------------------|---------------------------------------------------------------------------------------------------
| `crs_GMSc`                               | Player's average regular season in-conference game score                                                           
| `MOV`                         | Player's associated teams average margin of victory (in & out of conference regular season games)                                              
| `avg_ap_poll_rank_Pre_18`        | Player's associated teams average AP Poll Rank from pre-season to poll 18                              

### Bar Charts

<div align="center">
  <img src="https://github.com/user-attachments/assets/c04b1608-2d11-40dd-b673-f07d99b15c5a" alt="player_rat_cus">
</div>

<div align="center">
  <img src="https://github.com/user-attachments/assets/24ee9a2a-07d7-4522-906a-3e69e57b394c" alt="player_rat_cus">
</div>

### Code for Player Custom Rating Calculation

```python
all_player_data['player_rating_custom'] = (all_player_data['crs_GmSc'] * 2.5) + all_player_data['MOV'] - (all_player_data['avg_ap_poll_rank_Pre_18'] * .75)
```
