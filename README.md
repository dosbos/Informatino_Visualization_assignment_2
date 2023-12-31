    ---
    The provided data was taken from 
    https://www.kaggle.com/datasets/martj42/international-football-results-from-1872-to-2017

    In this assignment I have designed an interface that shows visualization interactive techniques like brushing, painting, scaling and linking.
    I have included more than one filtering option
    ---

1. The "results.csv" file contains columns with the following names: "date," "home_team," "away_team," "home_score," "away_score," "tournament," "city," "country," and "neutral."
The "date" column represents the date when the game took place, using the format "YYYY-MM-DD" (e.g., 1872-11-30). The "home_team" column indicates the team hosting the game (e.g., Scotland), while the "away_team" column denotes the opposing team (e.g., England). The "home_score" column represents the number of goals scored by the home team (e.g., 2), and the "away_score" column represents the number of goals scored by the away team (e.g., 3). The "tournament" column provides the name of the tournament, specifically indicating if it was a friendly match. The "city" column indicates the location where the match was conducted (e.g., Glasgow), while the "country" column specifies the country where the city is situated (e.g., Scotland). The "neutral" column denotes whether the match was played in a neutral country, with a value of "FALSE" or "TRUE."

2. The first graph utilizes a global map to allow users to select a country. When a user hovers over a specific country, the country name is displayed in a tooltip, and the corresponding country is highlighted in red.

3. Located at the bottom of the global map, users can find two input fields for specifying a minimum and maximum date interval. By default, these fields are populated with the minimum and maximum dates from the CSV file, obtained using the d3.max and d3.min functions, respectively, by mapping the data to the "date" column. Upon selecting a country, the second graph is displayed, presenting two bar charts. These charts simultaneously function as line graphs and bar charts. They provide a valuable means of evaluating a country's progress in soccer. The upper directed bar chart showcases the selected country's scores, while the bottom directed bar chart illustrates the scores of the opposing countries in each match.

4. To facilitate interval changes, a confirmation button has been incorporated. When the user wishes to modify the interval, triggering the button captures the selected interval and communicates it to the bar chart graph. This process involves removing the previous graph and generating a new one. Since the initial country selection already filters the data, this approach ensures efficiency.

5. Due to the extensive dataset, the bar charts may appear narrow. However, if the selected interval is smaller or if no information is available for the specified years, the charts expand to accommodate the data accordingly.

6. Hovering over the bar chart triggers the appearance of an outline, revealing a tooltip with details about the corresponding match. This information includes the number of goals scored by the specified country, the name of the country, and the date when the game took place.

7. Users have the option to input the desired interval manually or select it from a calendar interface for added convenience.

8. For enhanced interpretability, a third graph in the form of a pie chart has been provided. This choice is particularly suitable given that only two teams are involved. The pie chart illustrates the distribution of scores based on the outcome of the selected match. Notably, the chart also includes additional information such as the tournament name and the location where the game was played.