# Figure Friday 2024 - week 34
Music sets the tone for our mornings, days, and nights, whether we're washing dishes or partying. The following [data set](https://github.com/plotly/Figure-Friday/blob/main/2024/week-34/dataset.csv) explores various parameters of songs in the Spotify library, including genre, danceability, and tempo.

Things to consider:
- how can the [facet plot](https://plotly.com/python/facet-plots/) be improved?
- how can [the trendline](https://plotly.com/python-api-reference/generated/plotly.express.scatter.html#plotly.express.scatter) be improved?
- is there a better way to show the correlations between energy and danceability of songs?
- are there other interesting correlations to discover?
- what [other graphs](https://plotly.com/python/) can we use to analyze the data set?

Sample Figure below.
Code:
```
import plotly.express as px
import pandas as pd

df = pd.read_csv('https://raw.githubusercontent.com/plotly/Figure-Friday/main/2024/week-34/dataset.csv')
fig = px.scatter(df, x="energy", y="danceability", facet_col="explicit", trendline='ols',
                 labels={"explicit": "Has explicit lyrics"})
fig.show()
```

## Participation Instructions:
Create - use the weekly data set to build your own Plotly visualization or Dash app. Or, enhance the sample figure provided in this post, using Plotly or Dash.
Submit - post your creation to LinkedIn or Twitter with the hashtags #FigureFriday and #plotly by midnight Thursday, your time zone.Please also submit your visualization in the Figure Friday channel: ⁠⁠figure-friday
Celebrate - join the [Figure Friday sessions](https://www.addevent.com/event/qK22258533) to showcase your creation and receive feedback from the community.

Thank you to [Abhi](https://www.linkedin.com/in/abhiniti-abhi-wagh-ms-0b6024228/) for suggesting this data set and thank you to [MaharshiPandya on Kaggle](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset/data) for the data.