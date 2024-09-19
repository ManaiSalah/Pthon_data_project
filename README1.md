# The Analysis

## 1.What are the most demanded skills for the top 3 most popular data roles?

To find the most demanded skills for the top3 most popular dara roles.I filtered out these positions by wich ones were the most popular,and got the top 5 skills for these top 3 roles.this query highlights the most popular job titles and their top skills, showing which skills I shouldpay attention to depending on the role I'm targeting.

view my notebook with detailed steps here:
[2_skill_demand.ipynb](3_Project\2_Skills_count.ipynb)


## Visualize Data

~~~python

fig,ax=plt.subplots(len(job_titles),1)
for i,job_title in enumerate(job_titles):
    df_plot=df_skills_perc[df_skills_perc['job_title_short']==job_title].head(5)
    df_plot.plot(kind='barh',x='job_skills',y='skill_percent',ax=ax[i],title=job_title)
    ax[i].invert_yaxis()
    ax[i].set_ylabel('')
    ax[i].legend().set_visible(False)
    fig.tight_layout(h_pad=0.5)
    fig.suptitle('Likelihood of skills requested in US Job postings',fontsize=15)


plt.show()
~~~~

### Results 

![Visualiszation of top skills for data nerds](3_Project\Images\skill_demand.png)

## Insights 

### Key Skills for Data Roles

### Data Analyst:
- **SQL**: Core skill for querying databases.
- **Excel**: Essential for data manipulation and analysis.
- **Tableau**: Frequently used for data visualization.
- **Python**: Popular for data analysis and automation.
- **SAS**: Used for statistical analysis and data management.

### Data Engineer:
- **SQL**: Crucial for managing and optimizing databases.
- **Python**: Key programming language for data manipulation.
- **AWS**: In-demand for cloud computing and data storage solutions.
- **Azure**: Cloud platform used for data engineering and storage.
- **Spark**: Required for big data processing and real-time analytics.

### Data Scientist:
- **Python**: Widely used for machine learning, statistical analysis, and data manipulation.
- **SQL**: Needed for querying and managing databases.
- **R**: Popular for statistical computing and data visualization.
- **SAS**: Utilized for statistical analysis in data science.
- **Tableau**: Important for creating data visualizations and storytelling.


