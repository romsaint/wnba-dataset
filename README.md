# WNBA Historical Dataset (1997–2025)

## Overview
This dataset contains **26 million rows** of WNBA game, player, and team data from 1997 to 2025. Perfect for analytics, machine learning, fantasy sports, or fan projects. It includes basic stats (PTS, REB, AST), advanced metrics (GmSc, VORP, TENDEX), and game context (scores, attendance, arenas).

## Data Structure
- **Format**: JSON, CSV, SQLite (Premium tier).
- **Rows**: ~26M (per player, per game).
- **Source**: Aggregated from public WNBA data (verified against WNBA.com, ESPN).

### Key Fields
| Field | Description | Type | Example |
|-------|-------------|------|---------|
| Game ID | Unique game identifier | Integer | 8054 (Aces @ Sky, Aug 25, 2025) |
| Player ID | Unique player identifier | Integer | 751 (Chelsea Gray) |
| Name | Player full name | String | "Chelsea Gray" |
| PTS | Points scored | Integer | 14 |
| GmSc | Game Score (efficiency metric) | Float | 11.3 |
| VORP | Value Over Replacement Player | Float | 0.514 |
| Season | Game season | Integer | 2025 |
| Start Timestamp | Game date/time | ISO Date | 2025-08-25T20:00:00.000Z |
| Home Team Score | Home team points | Integer | 74 |
| Attendance | Game attendance | Integer | 9103 |


## Use Cases
- **Analytics**: Track player efficiency trends (e.g., Chelsea Gray’s 2025 GmSc).  
- **ML Models**: Predict game outcomes or player performance.  
- **Fantasy Sports**: Build WNBA fantasy apps with advanced metrics.  
- **Research**: Analyze historical trends (e.g., rookie impact since 1997).


### Python (pandas): Average GmSc by Team
```python
import pandas as pd
df = pd.read_csv("wnba_all_1997_2025.json")
team_gmsc = df[df["Season"] == 2025].groupby("Team ID")["GmSc"].mean()
print(team_gmsc)
```


## Usage Notes
- **For educational/non-commercial use only**.  
- **Sample**: Preview 1k rows at [GitHub](https://github.com/romsaint/wnba-dataset).  
- **Contact**: x - [X account](https://x.com/romsayia), telegram - [@romloevu](https://web.telegram.org/a/#1617948483)

*Data sourced from public WNBA aggregates; use responsibly.*
