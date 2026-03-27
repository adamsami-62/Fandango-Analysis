# Fandango Rating Analysis

Description: A data analysis project built to recreate the findings of a FiveThirtyEight investigation into Fandango's movie rating system. The original article raised concerns that Fandango was artificially inflating ratings. Built using Python, primarily Pandas and Seaborn.

Original Article: https://fivethirtyeight.com/features/fandango-movies-ratings/

About the dataset: Dataset obtained from [here](https://github.com/fivethirtyeight/data/tree/master/fandango). Contains Fandango's star ratings and displayed ratings, alongside aggregated scores scraped from Rotten Tomatoes, Metacritic, and IMDB.

The data was imported, cleaned, and analyzed in Python, with visualizations built to compare Fandango's ratings against other platforms. [Full process is outlined here.](https://github.com/adamsami-62/Fandango-Analysis/blob/main/FandangoDataAnalysisProject.ipynb)

**Example Code**
```python
def move_legend(ax, new_loc, **kws):
    old_legend = ax.legend_
    handles = old_legend.legendHandles
    labels = [t.get_text() for t in old_legend.get_texts()]
    title = old_legend.get_title().get_text()
    ax.legend(handles, labels, loc=new_loc, title=title, **kws)
```
```python
fig, ax = plt.subplots(figsize=(15,6),dpi=150)
sns.kdeplot(data=norm_scores,clip=[0,5],shade=True,palette='Set1',ax=ax)
move_legend(ax, "upper left")
```

**Example Visualization**
![Example Visualization](assets/example_visualization.png)
