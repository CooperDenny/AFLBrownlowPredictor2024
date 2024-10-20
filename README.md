# AFLBrownlowPredictor2024
This project dives into predicting the 2024 AFL Brownlow Medal votes, using a data I compiled from various sources such as the `fitzRoy` R package, afl.com.au, AFL Tables, and the AFL Coaches Association. By incorporating a range of offensive and defensive statistics, team metrics, AFL Coaches Association votes, as well as variables regarding past recognition such as previous Brownlow performances; my model aims to capture the key aspects of player performance, allowing for a nuanced understanding of what contributes to recognition from the umpires.

The repository contains an R Markdown document and associated files for leveraging an ordinal logistic regression model to predict the 2024 Brownlow Medal votes awarded to players in each AFL game, based on game statistics and other metrics.

## Results
The analysis of the predictions compared to the actual votes for the Brownlow Medal revealed several important insights into the model’s performance. The highlight of the model's output is that it has correctly predicted Patrick Cripps to break the all time vote tally record (not as extreme as he actually did!), as well having Nick Daicos finish second with a high vote count as well.
- When taking a subset of players who I predicted to poll votes and/or actually polled votes (removing players who were predicted to poll 0 votes and also actually polled 0 votes as this would provide a false sense of accuracy), the Mean Absolute Error (MAE) was 2.008, indicating that, on average, the predicted votes differ from the actual votes by about 2.008 votes.
- The model also correctly predicted the player to poll 3 votes in 55.56% of matches (115 out of 207).

## Predicted Leaderboard

The model predicts the following top 20 for the 2024 Brownlow Medal. Predicted votes are pretty close to the actual votes.

| Player                  | Team                | Predicted Votes | Actual Votes | Predicted Rank | Actual Rank |
| :---------------------- | :------------------ | :-------------- | :----------- | :------------- | :---------- |
| Patrick Cripps           | Carlton             | 38              | 45           | 1              | 1           |
| Nick Daicos              | Collingwood         | 34              | 38           | 2              | 2           |
| Isaac Heeney             | Sydney Swans        | 31              | 28           | 3              | 4           |
| Marcus Bontempelli       | Western Bulldogs    | 27              | 19           | 4              | 14          |
| Lachie Neale             | Brisbane Lions      | 26              | 22           | 5              | 12          |
| Zak Butters              | Port Adelaide       | 25              | 29           | 6              | 3           |
| Caleb Serong             | Fremantle           | 24              | 28           | 7              | 4           |
| Errol Gulden             | Sydney Swans        | 23              | 25           | 8              | 8           |
| Zach Merrett             | Essendon            | 23              | 18           | 8              | 16          |
| Noah Anderson            | Gold Coast Suns     | 22              | 14           | 10             | 26          |
| Adam Treloar             | Western Bulldogs    | 21              | 26           | 11             | 7           |
| Chad Warner              | Sydney Swans        | 21              | 23           | 11             | 11          |
| Matt Rowell              | Gold Coast Suns     | 19              | 25           | 13             | 8           |
| Jai Newcombe             | Hawthorn            | 19              | 24           | 13             | 10          |
| Jason Horne-Francis      | Port Adelaide       | 19              | 19           | 13             | 14          |
| Jeremy Cameron           | Geelong Cats        | 18              | 16           | 16             | 19          |
| Sam Walsh                | Carlton             | 18              | 16           | 16             | 19          |
| Tom Green                | GWS Giants          | 17              | 27           | 18             | 6           |
| Jordan Dawson            | Adelaide Crows      | 17              | 18           | 18             | 16          |
| Max Gawn                 | Melbourne           | 16              | 13           | 20             | 28          |

## Contents
- `AFL.Brownlow.Prediction.Model.2024.html`: The knitted html document containing the analysis code.
- `AFL.Brownlow.Prediction.Model.2024.Rmd`: The R Markdown document containing the analysis code.
- `AFLBrownlowPredictor2024.Rproj`: R project file for the AFLBrownlowPredictor project.
- `brownlow_data_2024.csv`: A csv file containing the data required to run the model
- `README.md`: This file providing an overview of the repository.
