# Avalon
SAAS Avalon analysis code

## Usage

Setup:
```
pip install gspread oauth2client tabulate
git clone https://github.com/yao12310/avalon.git
mkdir avalon/keys
mkdir avalon/data
mv path/to/key/client.json avalon/keys/
```

Updating DB:
```
python -m avalon.main db_write --row {equals sign-separated list of values, optional} --player_write {True/False, optional, default=True}
```

If `--row` is excluded, then the script will prompt you to enter each value one-by-one. (Recommended method.)

Updating README Stats:
```
python -m avalon.main update_stat
```
## Stats

Note: The friends and memories made in this game far outweigh any statistic you will find on this page.In any case, most of these stats are super high variance—especially individual stats, which depend heavily on team composition.

**Good win %:**

Cheesy wins included: 0.4340 (n = 53)

Cheesy wins excluded: 0.3750 (n = 48)

**Good win % w.r.t. # players:**

Cheesy wins included:

|   # Players |   Sample Size |   Good Win % |
|-------------|---------------|--------------|
|           6 |             7 |     0.714286 |
|           7 |             2 |     1        |
|           8 |            16 |     0.375    |
|           9 |            17 |     0.352941 |
|          10 |            11 |     0.363636 |

Cheesy wins excluded:

|   # Players |   Sample Size |   Good Win % |
|-------------|---------------|--------------|
|           6 |             6 |     0.666667 |
|           7 |             1 |     1        |
|           8 |            16 |     0.375    |
|           9 |            15 |     0.266667 |
|          10 |            10 |     0.3      |

**Good win % w.r.t. # Percival claims:**

Cheesy wins included:

|   # Percival Claims |   Sample Size |   Good Win % |
|---------------------|---------------|--------------|
|                   1 |            47 |     0.425532 |
|                   2 |             5 |     0.4      |
|                   3 |             1 |     1        |

Cheesy wins excluded:

|   # Percival Claims |   Sample Size |   Good Win % |
|---------------------|---------------|--------------|
|                   1 |            42 |     0.357143 |
|                   2 |             5 |     0.4      |
|                   3 |             1 |     1        |

**Mean and SD game length by winning team:**

Cheesy wins included:

| Winner   |   Sample Size |   Mean Length |   SD Length |
|----------|---------------|---------------|-------------|
| Bad      |            16 |        39.625 |     19.6159 |
| Good     |            10 |        27.3   |     18.9564 |

Cheesy wins excluded:

| Winner   |   Sample Size |   Mean Length |   SD Length |
|----------|---------------|---------------|-------------|
| Bad      |            16 |       39.625  |     19.6159 |
| Good     |             9 |       29.3333 |     18.9143 |

**Number of carries by player:**

| Player   |   # Carries |
|----------|-------------|
| Abishek  |           3 |
| Brian    |           1 |
| Kate     |           4 |
| Peter    |           2 |
| Rachel   |           1 |
| Sachin   |           1 |

**Win rate leaderboard (minimum 5 games):**

Cheesy wins included:

| Player   |    Win % |   Good Win % |   Bad Win % |   Sample Size |
|----------|----------|--------------|-------------|---------------|
| Ewen     | 0.833333 |     0.666667 |    1        |             6 |
| Brian    | 0.693878 |     0.588235 |    0.933333 |            49 |
| Abishek  | 0.604651 |     0.518519 |    0.75     |            43 |
| Peter    | 0.516129 |     0.421053 |    0.666667 |            31 |
| Kish     | 0.5      |     0.428571 |    0.666667 |            10 |

Cheesy wins excluded:

| Player   |    Win % |   Good Win % |   Bad Win % |   Sample Size |
|----------|----------|--------------|-------------|---------------|
| Ewen     | 0.833333 |     0.666667 |    1        |             6 |
| Brian    | 0.659091 |     0.517241 |    0.933333 |            44 |
| Abishek  | 0.564103 |     0.434783 |    0.75     |            39 |
| Alex     | 0.518519 |     0.357143 |    0.692308 |            27 |
| Jay      | 0.5      |     0.25     |    0.75     |             8 |

**Games played ranking (minimum 5 games):**

| Player   |   Games Played |
|----------|----------------|
| Brian    |             49 |
| Kate     |             45 |
| Abishek  |             43 |
| Sushant  |             38 |
| Rachel   |             34 |
| Peter    |             31 |
| Alex     |             30 |
| Ruhi     |             23 |
| Jai      |             20 |
| Jackie   |             19 |
| Minh     |             14 |
| Kish     |             10 |
| Jay      |              8 |
| Gathenji |              7 |
| Ewen     |              6 |
| Jade     |              5 |

**Kate Good Theorem statistics:**
| Weak Success   |   Count |   Good Win % |
|----------------|---------|--------------|
| No             |       3 |            0 |
| Yes            |       7 |            0 |

| Strong Success   |   Count |   Good Win % |
|------------------|---------|--------------|
| No               |       4 |            0 |
| Yes              |       6 |            0 |

| Weak KGT Applied   |   Sample Size |   Good Win % |
|--------------------|---------------|--------------|
| No                 |            39 |     0.538462 |
| Yes                |            10 |     0        |

| Strong KGT Applied   |   Sample Size |   Good Win % |
|----------------------|---------------|--------------|
| No                   |            39 |     0.538462 |
| Yes                  |            10 |     0        |


**Player/role counts/percentages (minimum 5 games):**

Total count:

| Player   |   Merlin |   Percival |   Assassin |   Morgana |   Mordred |   Oberon |   Minion #1 |   Loyal Servant |   Sample Size |
|----------|----------|------------|------------|-----------|-----------|----------|-------------|-----------------|---------------|
| Abishek  |        4 |          7 |          4 |         5 |         4 |        3 |           0 |              16 |            43 |
| Alex     |        2 |          4 |          7 |         6 |         2 |        0 |           0 |               9 |            30 |
| Brian    |        5 |         10 |          2 |         8 |         5 |        0 |           0 |              19 |            49 |
| Ewen     |        0 |          1 |          1 |         0 |         0 |        2 |           0 |               2 |             6 |
| Gathenji |        0 |          0 |          0 |         1 |         0 |        0 |           0 |               6 |             7 |
| Jackie   |        2 |          4 |          3 |         1 |         0 |        1 |           0 |               8 |            19 |
| Jade     |        2 |          0 |          0 |         0 |         0 |        0 |           0 |               3 |             5 |
| Jai      |        4 |          1 |          3 |         3 |         1 |        0 |           0 |               8 |            20 |
| Jay      |        1 |          2 |          3 |         0 |         1 |        0 |           0 |               1 |             8 |
| Kate     |        5 |          3 |          4 |         7 |         4 |        1 |           0 |              21 |            45 |
| Kish     |        0 |          3 |          0 |         1 |         2 |        0 |           0 |               4 |            10 |
| Minh     |        3 |          2 |          3 |         1 |         1 |        0 |           0 |               4 |            14 |
| Peter    |        5 |          4 |          6 |         2 |         4 |        0 |           0 |              10 |            31 |
| Rachel   |        7 |          3 |          3 |         3 |         6 |        0 |           0 |              12 |            34 |
| Ruhi     |        1 |          2 |          2 |         4 |         2 |        1 |           0 |              11 |            23 |
| Sushant  |        8 |          3 |          3 |         4 |         4 |        0 |           1 |              15 |            38 |

Normalized by role (i.e. divided by occcurrences for each role):

*Columns will not necessarily sum to 1 due to players with < 5 games not being included.*

| Player   |   Merlin |   Percival |   Assassin |   Morgana |   Mordred |   Oberon |   Minion #1 |   Loyal Servant |   Sample Size |
|----------|----------|------------|------------|-----------|-----------|----------|-------------|-----------------|---------------|
| Abishek  |     0.08 |       0.14 |      0.083 |     0.106 |     0.105 |    0.273 |           0 |           0.103 |            43 |
| Alex     |     0.04 |       0.08 |      0.146 |     0.128 |     0.053 |    0     |           0 |           0.058 |            30 |
| Brian    |     0.1  |       0.2  |      0.042 |     0.17  |     0.132 |    0     |           0 |           0.122 |            49 |
| Ewen     |     0    |       0.02 |      0.021 |     0     |     0     |    0.182 |           0 |           0.013 |             6 |
| Gathenji |     0    |       0    |      0     |     0.021 |     0     |    0     |           0 |           0.038 |             7 |
| Jackie   |     0.04 |       0.08 |      0.062 |     0.021 |     0     |    0.091 |           0 |           0.051 |            19 |
| Jade     |     0.04 |       0    |      0     |     0     |     0     |    0     |           0 |           0.019 |             5 |
| Jai      |     0.08 |       0.02 |      0.062 |     0.064 |     0.026 |    0     |           0 |           0.051 |            20 |
| Jay      |     0.02 |       0.04 |      0.062 |     0     |     0.026 |    0     |           0 |           0.006 |             8 |
| Kate     |     0.1  |       0.06 |      0.083 |     0.149 |     0.105 |    0.091 |           0 |           0.135 |            45 |
| Kish     |     0    |       0.06 |      0     |     0.021 |     0.053 |    0     |           0 |           0.026 |            10 |
| Minh     |     0.06 |       0.04 |      0.062 |     0.021 |     0.026 |    0     |           0 |           0.026 |            14 |
| Peter    |     0.1  |       0.08 |      0.125 |     0.043 |     0.105 |    0     |           0 |           0.064 |            31 |
| Rachel   |     0.14 |       0.06 |      0.062 |     0.064 |     0.158 |    0     |           0 |           0.077 |            34 |
| Ruhi     |     0.02 |       0.04 |      0.042 |     0.085 |     0.053 |    0.091 |           0 |           0.071 |            23 |
| Sushant  |     0.16 |       0.06 |      0.062 |     0.085 |     0.105 |    0     |           1 |           0.096 |            38 |

Normalized by player (i.e. divided by games played for each player):

*Row values should sum to 1.*

| Player   |   Merlin |   Percival |   Assassin |   Morgana |   Mordred |   Oberon |   Minion #1 |   Loyal Servant |   Sample Size |
|----------|----------|------------|------------|-----------|-----------|----------|-------------|-----------------|---------------|
| Abishek  |    0.093 |      0.163 |      0.093 |     0.116 |     0.093 |    0.07  |       0     |           0.372 |            43 |
| Alex     |    0.067 |      0.133 |      0.233 |     0.2   |     0.067 |    0     |       0     |           0.3   |            30 |
| Brian    |    0.102 |      0.204 |      0.041 |     0.163 |     0.102 |    0     |       0     |           0.388 |            49 |
| Ewen     |    0     |      0.167 |      0.167 |     0     |     0     |    0.333 |       0     |           0.333 |             6 |
| Gathenji |    0     |      0     |      0     |     0.143 |     0     |    0     |       0     |           0.857 |             7 |
| Jackie   |    0.105 |      0.211 |      0.158 |     0.053 |     0     |    0.053 |       0     |           0.421 |            19 |
| Jade     |    0.4   |      0     |      0     |     0     |     0     |    0     |       0     |           0.6   |             5 |
| Jai      |    0.2   |      0.05  |      0.15  |     0.15  |     0.05  |    0     |       0     |           0.4   |            20 |
| Jay      |    0.125 |      0.25  |      0.375 |     0     |     0.125 |    0     |       0     |           0.125 |             8 |
| Kate     |    0.111 |      0.067 |      0.089 |     0.156 |     0.089 |    0.022 |       0     |           0.467 |            45 |
| Kish     |    0     |      0.3   |      0     |     0.1   |     0.2   |    0     |       0     |           0.4   |            10 |
| Minh     |    0.214 |      0.143 |      0.214 |     0.071 |     0.071 |    0     |       0     |           0.286 |            14 |
| Peter    |    0.161 |      0.129 |      0.194 |     0.065 |     0.129 |    0     |       0     |           0.323 |            31 |
| Rachel   |    0.206 |      0.088 |      0.088 |     0.088 |     0.176 |    0     |       0     |           0.353 |            34 |
| Ruhi     |    0.043 |      0.087 |      0.087 |     0.174 |     0.087 |    0.043 |       0     |           0.478 |            23 |
| Sushant  |    0.211 |      0.079 |      0.079 |     0.105 |     0.105 |    0     |       0.026 |           0.395 |            38 |

**Percentage of times two players are on the same team (minimum 5 games both played, else -1):**

| Player   |   Rachel |   Ewen |   Peter |   Minh |   Jai |   Kate |   Sushant |   Abishek |   Ruhi |   Brian |   Jackie |   Kish |   Alex |   Jade |   Jay |   Gathenji |
|----------|----------|--------|---------|--------|-------|--------|-----------|-----------|--------|---------|----------|--------|--------|--------|-------|------------|
| Rachel   |    -1    |    0.4 |    0.5  |   0.5  |  0.6  |   0.46 |      0.52 |      0.4  |   0.46 |    0.4  |     0.36 |   0.71 |   0.56 |   -1   |  0.4  |       0.86 |
| Ewen     |     0.4  |   -1   |   -1    |  -1    | -1    |  -1    |     -1    |     -1    |  -1    |   -1    |    -1    |  -1    |  -1    |   -1   | -1    |      -1    |
| Peter    |     0.5  |   -1   |   -1    |  -1    |  0.42 |   0.37 |      0.41 |      0.52 |   0.4  |    0.6  |     0.64 |   0.67 |   0.31 |   -1   |  0.8  |      -1    |
| Minh     |     0.5  |   -1   |   -1    |  -1    |  0.6  |   0.42 |      0.55 |      0.5  |   0.67 |    0.42 |     0.64 |  -1    |   0.14 |   -1   | -1    |      -1    |
| Jai      |     0.6  |   -1   |    0.42 |   0.6  | -1    |   0.56 |      0.44 |      0.35 |   0.17 |    0.53 |     0.71 |  -1    |   0.45 |   -1   | -1    |      -1    |
| Kate     |     0.46 |   -1   |    0.37 |   0.42 |  0.56 |  -1    |      0.56 |      0.46 |   0.45 |    0.57 |     0.56 |   0.38 |   0.4  |   -1   |  0.38 |       0.57 |
| Sushant  |     0.52 |   -1   |    0.41 |   0.55 |  0.44 |   0.56 |     -1    |      0.5  |   0.44 |    0.51 |     0.43 |   0.44 |   0.41 |   -1   |  0.38 |       0.5  |
| Abishek  |     0.4  |   -1   |    0.52 |   0.5  |  0.35 |   0.46 |      0.5  |     -1    |   0.41 |    0.54 |     0.47 |   0.43 |   0.5  |   -1   |  0.62 |       0.29 |
| Ruhi     |     0.46 |   -1   |    0.4  |   0.67 |  0.17 |   0.45 |      0.44 |      0.41 |  -1    |    0.45 |     0.29 |   0.67 |   0.69 |   -1   |  0.4  |      -1    |
| Brian    |     0.4  |   -1   |    0.6  |   0.42 |  0.53 |   0.57 |      0.51 |      0.54 |   0.45 |   -1    |     0.74 |   0.4  |   0.38 |    0.6 |  0    |       0.5  |
| Jackie   |     0.36 |   -1   |    0.64 |   0.64 |  0.71 |   0.56 |      0.43 |      0.47 |   0.29 |    0.74 |    -1    |  -1    |   0.27 |   -1   | -1    |      -1    |
| Kish     |     0.71 |   -1   |    0.67 |  -1    | -1    |   0.38 |      0.44 |      0.43 |   0.67 |    0.4  |    -1    |  -1    |  -1    |   -1   | -1    |      -1    |
| Alex     |     0.56 |   -1   |    0.31 |   0.14 |  0.45 |   0.4  |      0.41 |      0.5  |   0.69 |    0.38 |     0.27 |  -1    |  -1    |   -1   | -1    |       0.4  |
| Jade     |    -1    |   -1   |   -1    |  -1    | -1    |  -1    |     -1    |     -1    |  -1    |    0.6  |    -1    |  -1    |  -1    |   -1   | -1    |      -1    |
| Jay      |     0.4  |   -1   |    0.8  |  -1    | -1    |   0.38 |      0.38 |      0.62 |   0.4  |    0    |    -1    |  -1    |  -1    |   -1   | -1    |      -1    |
| Gathenji |     0.86 |   -1   |   -1    |  -1    | -1    |   0.57 |      0.5  |      0.29 |  -1    |    0.5  |    -1    |  -1    |   0.4  |   -1   | -1    |      -1    |

**Percentage of times two players win, given that they are on the same team (minimum 5 games, else -1):**

Cheesy wins included:

| Player   |   Rachel |   Ewen |   Minh |   Peter |   Jai |   Kate |   Sushant |   Abishek |   Ruhi |   Brian |   Jackie |   Kish |   Alex |   Jade |   Jay |   Gathenji |
|----------|----------|--------|--------|---------|-------|--------|-----------|-----------|--------|---------|----------|--------|--------|--------|-------|------------|
| Rachel   |    -1    |     -1 |   0.6  |    0.22 |  0.11 |   0.42 |      0.29 |      0.6  |   0.17 |    0.5  |     0.6  |    0.4 |   0.44 |     -1 |  -1   |       0.17 |
| Ewen     |    -1    |     -1 |  -1    |   -1    | -1    |  -1    |     -1    |     -1    |  -1    |   -1    |    -1    |   -1   |  -1    |     -1 |  -1   |      -1    |
| Minh     |     0.6  |     -1 |  -1    |   -1    | -1    |   0.4  |      0.33 |      0.33 |  -1    |    0.4  |     0.14 |   -1   |  -1    |     -1 |  -1   |      -1    |
| Peter    |     0.22 |     -1 |  -1    |   -1    |  0.4  |   0.5  |      0.22 |      0.77 |  -1    |    0.72 |     0.57 |   -1   |   0.2  |     -1 |  -1   |      -1    |
| Jai      |     0.11 |     -1 |  -1    |    0.4  | -1    |   0.4  |      0.12 |      0.5  |  -1    |    0.4  |     0.2  |   -1   |   0.2  |     -1 |  -1   |      -1    |
| Kate     |     0.42 |     -1 |   0.4  |    0.5  |  0.4  |  -1    |      0.35 |      0.58 |   0.3  |    0.68 |     0.5  |   -1   |   0.5  |     -1 |  -1   |      -1    |
| Sushant  |     0.29 |     -1 |   0.33 |    0.22 |  0.12 |   0.35 |     -1    |      0.47 |   0.25 |    0.53 |     0.33 |   -1   |   0.44 |     -1 |  -1   |      -1    |
| Abishek  |     0.6  |     -1 |   0.33 |    0.77 |  0.5  |   0.58 |      0.47 |     -1    |   0.44 |    0.77 |     0.5  |   -1   |   0.57 |     -1 |   0.6 |      -1    |
| Ruhi     |     0.17 |     -1 |  -1    |   -1    | -1    |   0.3  |      0.25 |      0.44 |  -1    |    0.6  |    -1    |   -1   |   0.56 |     -1 |  -1   |      -1    |
| Brian    |     0.5  |     -1 |   0.4  |    0.72 |  0.4  |   0.68 |      0.53 |      0.77 |   0.6  |   -1    |     0.57 |   -1   |   0.82 |     -1 |  -1   |      -1    |
| Jackie   |     0.6  |     -1 |   0.14 |    0.57 |  0.2  |   0.5  |      0.33 |      0.5  |  -1    |    0.57 |    -1    |   -1   |  -1    |     -1 |  -1   |      -1    |
| Kish     |     0.4  |     -1 |  -1    |   -1    | -1    |  -1    |     -1    |     -1    |  -1    |   -1    |    -1    |   -1   |  -1    |     -1 |  -1   |      -1    |
| Alex     |     0.44 |     -1 |  -1    |    0.2  |  0.2  |   0.5  |      0.44 |      0.57 |   0.56 |    0.82 |    -1    |   -1   |  -1    |     -1 |  -1   |      -1    |
| Jade     |    -1    |     -1 |  -1    |   -1    | -1    |  -1    |     -1    |     -1    |  -1    |   -1    |    -1    |   -1   |  -1    |     -1 |  -1   |      -1    |
| Jay      |    -1    |     -1 |  -1    |   -1    | -1    |  -1    |     -1    |      0.6  |  -1    |   -1    |    -1    |   -1   |  -1    |     -1 |  -1   |      -1    |
| Gathenji |     0.17 |     -1 |  -1    |   -1    | -1    |  -1    |     -1    |     -1    |  -1    |   -1    |    -1    |   -1   |  -1    |     -1 |  -1   |      -1    |

Cheesy wins excluded:

| Player   |   Rachel |   Ewen |   Minh |   Peter |   Jai |   Kate |   Sushant |   Abishek |   Ruhi |   Brian |   Jackie |   Kish |   Alex |   Jade |   Jay |   Gathenji |
|----------|----------|--------|--------|---------|-------|--------|-----------|-----------|--------|---------|----------|--------|--------|--------|-------|------------|
| Rachel   |    -1    |     -1 |    0.6 |    0.22 |  0.12 |   0.42 |      0.31 |      0.6  |  -1    |    0.45 |     0.6  |     -1 |   0.5  |     -1 |  -1   |       0.17 |
| Ewen     |    -1    |     -1 |   -1   |   -1    | -1    |  -1    |     -1    |     -1    |  -1    |   -1    |    -1    |     -1 |  -1    |     -1 |  -1   |      -1    |
| Minh     |     0.6  |     -1 |   -1   |   -1    | -1    |  -1    |      0.2  |      0.2  |  -1    |   -1    |     0    |     -1 |  -1    |     -1 |  -1   |      -1    |
| Peter    |     0.22 |     -1 |   -1   |   -1    | -1    |   0.44 |      0.22 |      0.73 |  -1    |    0.69 |     0.57 |     -1 |   0.2  |     -1 |  -1   |      -1    |
| Jai      |     0.12 |     -1 |   -1   |   -1    | -1    |   0.4  |      0.12 |      0.4  |  -1    |    0.33 |     0.2  |     -1 |  -1    |     -1 |  -1   |      -1    |
| Kate     |     0.42 |     -1 |   -1   |    0.44 |  0.4  |  -1    |      0.32 |      0.53 |   0.3  |    0.65 |     0.44 |     -1 |   0.5  |     -1 |  -1   |      -1    |
| Sushant  |     0.31 |     -1 |    0.2 |    0.22 |  0.12 |   0.32 |     -1    |      0.44 |   0.25 |    0.5  |     0.2  |     -1 |   0.44 |     -1 |  -1   |      -1    |
| Abishek  |     0.6  |     -1 |    0.2 |    0.73 |  0.4  |   0.53 |      0.44 |     -1    |   0.38 |    0.72 |     0.43 |     -1 |   0.54 |     -1 |   0.6 |      -1    |
| Ruhi     |    -1    |     -1 |   -1   |   -1    | -1    |   0.3  |      0.25 |      0.38 |  -1    |    0.5  |    -1    |     -1 |   0.67 |     -1 |  -1   |      -1    |
| Brian    |     0.45 |     -1 |   -1   |    0.69 |  0.33 |   0.65 |      0.5  |      0.72 |   0.5  |   -1    |     0.54 |     -1 |   0.8  |     -1 |  -1   |      -1    |
| Jackie   |     0.6  |     -1 |    0   |    0.57 |  0.2  |   0.44 |      0.2  |      0.43 |  -1    |    0.54 |    -1    |     -1 |  -1    |     -1 |  -1   |      -1    |
| Kish     |    -1    |     -1 |   -1   |   -1    | -1    |  -1    |     -1    |     -1    |  -1    |   -1    |    -1    |     -1 |  -1    |     -1 |  -1   |      -1    |
| Alex     |     0.5  |     -1 |   -1   |    0.2  | -1    |   0.5  |      0.44 |      0.54 |   0.67 |    0.8  |    -1    |     -1 |  -1    |     -1 |  -1   |      -1    |
| Jade     |    -1    |     -1 |   -1   |   -1    | -1    |  -1    |     -1    |     -1    |  -1    |   -1    |    -1    |     -1 |  -1    |     -1 |  -1   |      -1    |
| Jay      |    -1    |     -1 |   -1   |   -1    | -1    |  -1    |     -1    |      0.6  |  -1    |   -1    |    -1    |     -1 |  -1    |     -1 |  -1   |      -1    |
| Gathenji |     0.17 |     -1 |   -1   |   -1    | -1    |  -1    |     -1    |     -1    |  -1    |   -1    |    -1    |     -1 |  -1    |     -1 |  -1   |      -1    |

**Percentage of times two players win, given that they are on opposite teams (minimum 5 games, else -1):**


*Win percentages are presented as row player vs column player.*

Cheesy wins included:

| Player   |   Peter |   Minh |   Rachel |   Ewen |   Jai |   Kate |   Sushant |   Abishek |   Ruhi |   Brian |   Jackie |   Kish |   Alex |   Jade |   Jay |   Gathenji |
|----------|---------|--------|----------|--------|-------|--------|-----------|-----------|--------|---------|----------|--------|--------|--------|-------|------------|
| Peter    |   -1    |  -1    |     0.44 |     -1 |  0.43 |   0.59 |      0.62 |      0.42 |   1    |    0.25 |    -1    |  -1    |   0.82 |     -1 |  -1   |       -1   |
| Minh     |   -1    |  -1    |     0.2  |     -1 | -1    |   0.14 |      0.2  |      0.33 |  -1    |    0.14 |    -1    |  -1    |   0.33 |     -1 |  -1   |       -1   |
| Rachel   |    0.56 |   0.8  |    -1    |     -1 |  0.5  |   0.43 |      0.54 |      0.33 |   0.57 |    0.33 |     0.56 |  -1    |   0.14 |     -1 |  -1   |       -1   |
| Ewen     |   -1    |  -1    |    -1    |     -1 | -1    |  -1    |     -1    |     -1    |  -1    |   -1    |    -1    |  -1    |  -1    |     -1 |  -1   |       -1   |
| Jai      |    0.57 |  -1    |     0.5  |     -1 | -1    |   0.25 |      0.5  |      0.27 |   0.4  |    0.33 |    -1    |  -1    |   0.17 |     -1 |  -1   |       -1   |
| Kate     |    0.41 |   0.86 |     0.57 |     -1 |  0.75 |  -1    |      0.62 |      0.36 |   0.67 |    0.26 |     0.62 |   0.4  |   0.5  |     -1 |   0.2 |       -1   |
| Sushant  |    0.38 |   0.8  |     0.46 |     -1 |  0.5  |   0.38 |     -1    |      0.24 |   0.6  |    0.22 |     0.62 |   0.4  |   0.23 |     -1 |   0.2 |       -1   |
| Abishek  |    0.58 |   0.67 |     0.67 |     -1 |  0.73 |   0.64 |      0.76 |     -1    |   0.77 |    0.42 |     0.67 |  -1    |   0.5  |     -1 |  -1   |        0.8 |
| Ruhi     |    0    |  -1    |     0.43 |     -1 |  0.6  |   0.33 |      0.4  |      0.23 |  -1    |    0.08 |     0.4  |  -1    |  -1    |     -1 |  -1   |       -1   |
| Brian    |    0.75 |   0.86 |     0.67 |     -1 |  0.67 |   0.74 |      0.78 |      0.58 |   0.92 |   -1    |     0.8  |   0.83 |   0.72 |     -1 |   0.5 |       -1   |
| Jackie   |   -1    |  -1    |     0.44 |     -1 | -1    |   0.38 |      0.38 |      0.33 |   0.6  |    0.2  |    -1    |  -1    |   0.5  |     -1 |  -1   |       -1   |
| Kish     |   -1    |  -1    |    -1    |     -1 | -1    |   0.6  |      0.6  |     -1    |  -1    |    0.17 |    -1    |  -1    |  -1    |     -1 |  -1   |       -1   |
| Alex     |    0.18 |   0.67 |     0.86 |     -1 |  0.83 |   0.5  |      0.77 |      0.5  |  -1    |    0.28 |     0.5  |  -1    |  -1    |     -1 |  -1   |       -1   |
| Jade     |   -1    |  -1    |    -1    |     -1 | -1    |  -1    |     -1    |     -1    |  -1    |   -1    |    -1    |  -1    |  -1    |     -1 |  -1   |       -1   |
| Jay      |   -1    |  -1    |    -1    |     -1 | -1    |   0.8  |      0.8  |     -1    |  -1    |    0.5  |    -1    |  -1    |  -1    |     -1 |  -1   |       -1   |
| Gathenji |   -1    |  -1    |    -1    |     -1 | -1    |  -1    |     -1    |      0.2  |  -1    |   -1    |    -1    |  -1    |  -1    |     -1 |  -1   |       -1   |

Cheesy wins excluded:

| Player   |   Peter |   Minh |   Rachel |   Ewen |   Jai |   Kate |   Sushant |   Abishek |   Ruhi |   Brian |   Jackie |   Kish |   Alex |   Jade |   Jay |   Gathenji |
|----------|---------|--------|----------|--------|-------|--------|-----------|-----------|--------|---------|----------|--------|--------|--------|-------|------------|
| Peter    |   -1    |  -1    |     0.38 |     -1 |  0.43 |   0.59 |      0.58 |      0.42 |   1    |    0.25 |    -1    |  -1    |   0.8  |     -1 |  -1   |       -1   |
| Minh     |   -1    |  -1    |    -1    |     -1 | -1    |   0.14 |      0.2  |      0.33 |  -1    |    0.14 |    -1    |  -1    |   0.2  |     -1 |  -1   |       -1   |
| Rachel   |    0.62 |  -1    |    -1    |     -1 |  0.6  |   0.46 |      0.58 |      0.38 |   0.57 |    0.38 |     0.62 |  -1    |   0.14 |     -1 |  -1   |       -1   |
| Ewen     |   -1    |  -1    |    -1    |     -1 | -1    |  -1    |     -1    |     -1    |  -1    |   -1    |    -1    |  -1    |  -1    |     -1 |  -1   |       -1   |
| Jai      |    0.57 |  -1    |     0.4  |     -1 | -1    |   0.29 |      0.5  |      0.3  |   0.4  |    0.38 |    -1    |  -1    |   0.17 |     -1 |  -1   |       -1   |
| Kate     |    0.41 |   0.86 |     0.54 |     -1 |  0.71 |  -1    |      0.62 |      0.38 |   0.67 |    0.28 |     0.62 |   0.4  |   0.47 |     -1 |   0.2 |       -1   |
| Sushant  |    0.42 |   0.8  |     0.42 |     -1 |  0.5  |   0.38 |     -1    |      0.25 |   0.56 |    0.24 |     0.62 |  -1    |   0.17 |     -1 |   0.2 |       -1   |
| Abishek  |    0.58 |   0.67 |     0.62 |     -1 |  0.7  |   0.62 |      0.75 |     -1    |   0.73 |    0.42 |     0.67 |  -1    |   0.42 |     -1 |  -1   |        0.8 |
| Ruhi     |    0    |  -1    |     0.43 |     -1 |  0.6  |   0.33 |      0.44 |      0.27 |  -1    |    0.1  |    -1    |  -1    |  -1    |     -1 |  -1   |       -1   |
| Brian    |    0.75 |   0.86 |     0.62 |     -1 |  0.62 |   0.72 |      0.76 |      0.58 |   0.9  |   -1    |     0.8  |   0.83 |   0.69 |     -1 |   0.5 |       -1   |
| Jackie   |   -1    |  -1    |     0.38 |     -1 | -1    |   0.38 |      0.38 |      0.33 |  -1    |    0.2  |    -1    |  -1    |   0.43 |     -1 |  -1   |       -1   |
| Kish     |   -1    |  -1    |    -1    |     -1 | -1    |   0.6  |     -1    |     -1    |  -1    |    0.17 |    -1    |  -1    |  -1    |     -1 |  -1   |       -1   |
| Alex     |    0.2  |   0.8  |     0.86 |     -1 |  0.83 |   0.53 |      0.83 |      0.58 |  -1    |    0.31 |     0.57 |  -1    |  -1    |     -1 |  -1   |       -1   |
| Jade     |   -1    |  -1    |    -1    |     -1 | -1    |  -1    |     -1    |     -1    |  -1    |   -1    |    -1    |  -1    |  -1    |     -1 |  -1   |       -1   |
| Jay      |   -1    |  -1    |    -1    |     -1 | -1    |   0.8  |      0.8  |     -1    |  -1    |    0.5  |    -1    |  -1    |  -1    |     -1 |  -1   |       -1   |
| Gathenji |   -1    |  -1    |    -1    |     -1 | -1    |  -1    |     -1    |      0.2  |  -1    |   -1    |    -1    |  -1    |  -1    |     -1 |  -1   |       -1   |

**3+1 vs 2+1 strategy success rate:**

Cheesy wins included:

|    Win % |   Sample Size |
|----------|---------------|
| 0.333333 |             6 |
| 0.44     |            25 |

Cheesy wins excluded:

|    Win % |   Sample Size |
|----------|---------------|
| 0.2      |             5 |
| 0.391304 |            23 |

**Good win rate w.r.t. R1 fail (filtered for cases where bad guy on R1):**

Cheesy wins included:

|    Win % |   Sample Size |
|----------|---------------|
| 0.428571 |             7 |
| 0.36     |            25 |

Cheesy wins excluded:

|    Win % |   Sample Size |
|----------|---------------|
| 0.428571 |             7 |
| 0.333333 |            24 |

**Flip statistics for different # bad guys and mission index:**


*Excludes Oberon in 10-person games.*

*Overall:*

|   # Fails |   Count |        % |   Good Win % |
|-----------|---------|----------|--------------|
|         0 |       9 | 0.346154 |     0.444444 |
|         1 |      11 | 0.423077 |     0.181818 |
|         2 |       6 | 0.230769 |     0.666667 |

*2 bad guys on mission 1:*

|   # Fails |   Count |   % |   Good Win % |
|-----------|---------|-----|--------------|
|         0 |       3 | 0.6 |            0 |
|         1 |       2 | 0.4 |            0 |

*2 bad guys on mission 2:*

|   # Fails |   Count |        % |   Good Win % |
|-----------|---------|----------|--------------|
|         0 |       5 | 0.555556 |          0.6 |
|         1 |       2 | 0.222222 |          0.5 |
|         2 |       2 | 0.222222 |          0.5 |

*2 bad guys on mission 3:*

|   # Fails |   Count |   % |   Good Win % |
|-----------|---------|-----|--------------|
|         0 |       1 | 0.1 |     1        |
|         1 |       6 | 0.6 |     0.166667 |
|         2 |       3 | 0.3 |     0.666667 |

*3 bad guys on mission 2:*

|   # Fails |   Count |   % |   Good Win % |
|-----------|---------|-----|--------------|
|         1 |       1 | 0.5 |            0 |
|         2 |       1 | 0.5 |            1 |
