# The Analysis 
## 2.How are in_demand skills trending for Data Analysis 

~~~~python
from matplotlib.ticker import PercentFormatter
df_plot=df_DA_US_percent.iloc[:,:5]

sns.lineplot(df_plot,dashes=False,palette='tab10')
sns.set_theme(style='ticks')
sns.despine()
plt.title("Trending Top skills for data analyst in the US")
plt.ylabel('Likelihood in Job Postings')
plt.xlabel('2023')
plt.legend().remove()
ax=plt.gca()
ax.yaxis.set_major_formatter(PercentFormatter(decimals=0))


for i in range(5):
         plt.text(11.2,df_plot.iloc[-1,i],df_plot.columns[i])
~~~~

### Results
![Trending Top skills for Data Analysts in the US](3_Project\Images\img2.png)

*Bar graph visualizing the trending top skills for data analysts in the US in 2023.*

### Insights:

## Trending Top Skills for Data Analyst in the US (2023)

- **SQL**: Remains the top skill, showing slight decline but still in high demand (~60%).
- **Excel**: Stable demand, trending upwards toward the end of the year (~50%).
- **Python**: Moderate demand, fluctuating around 30-40% throughout the year.
- **Tableau**: Steady in the 30% range, slightly decreasing towards the end.
- **Power BI**: Least demanded skill but showing growth, hovering around 20-30%.

The chart showcases the trending likelihood of these key skills being requested in US job postings for data analysts throughout 2023.


view my notebook with detailed steps here:
[3_skills_trend..ipynb](3_Project\3_skill_Trend.ipynb)