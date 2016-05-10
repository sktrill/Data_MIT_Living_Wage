# Data_MIT_Living_Wage

Play with the app here: (link to Shiny app)

<p><b>Background</b></p>
The minimum wage has been a hot button election topic this year with presumptive party nominees espousing diametrically opposiing views on the issue. As the race for the presidential candidates draws to a close, the national dialogue can only increase as campaigns hit the two largest primaries by delegate count. These two states, New York and California, are also the only two states that have passed budget deals to raise the minimum wage to $15 an hour. While the minimum wage sets an earning threshold it fails to account for the basic living expenses of American families. Expenses for food, housing, medicine and child care force minimum wage workers to often hold multiple jobs and/or seek government assistance. This leads to generations of American workers without the financial resources to sustain their livelihood or with the financial freedom to invest in their future. 

<p><b>Purpose</b></p>
This analysis looks to better understand the financial burden of minimum wage Americans, and seeks to predict the states that could see minimum wage hikes in the near future. 

<p><b>Datasets</b></p>
The following datasets were used (scraped in most cases):
<ul>
<li>Living Wage data by state from Dr. Amy K. Glasmeier of MIT, part of the Living Wage Calculator</li>
<li>Percentage of Labour Force in Unions in 2014-2015 from the US Bureau of Labor Statistics</li>
<li>List of Current Governors from the National Governors Association</li>
<li>List of State Legislators from Wikipedia</li>
<li>List of Right to Work states from Wikipedia</li>
</ul>

<p><b>Data Analysis / Understanding the financial burden</b></p>
<ul>
<li> The minimum wage does not sufficiently compensate for the living expenses of American workers. A family of 2 adults and 2 children need to nearly double their income to meet basic needs </li>
<li> The living wage for adults with children in some cases is 2-3 times the minimum wage. A single parent with two kids would need at least 3 other jobs to provide for basic needs </li>
<li> Childcare and housing costs make up the bulk of the expenses for most Americna families. Single parents with two or more children need to work nearly 2-3 jobs just to meet these needs </li>
<li> California, New York, Connecticut and Massachusetts require the highest income to cover basic expenses, as a result living wages in those cities is expectedly higher than the rest </li>
<li> Southern and midwest states have a lower minimum wage than the rest of the country but also a lower living wage </li>
<li> California, New York, Connecticut and Washington have the highest percentage of wage workers in unions </li>
<li> Southern states have right to work laws, Republican control of the state legislature (upper and lower houses), Republican Governors and the lowest percentage of wage workers in unions </li>
<li> The wage multiple (living wage / minimum wage) ranges from 2.9 to 4.3 for single parents with children, demonstrating why multiple jobs are often required. New York and Wisconsin are the worst off </li>
<li> A single parent with 2 children needs to work between 73 and 120 hours a week (equivalent of 1.8 to 3 jobs) to meet base expenses. Even a single adult on minimum wage is required to work between 57 and 91 hours a week at minimum. </li> 
</ul>

<p><b>Prediction / Models to predict the next state to raise wages</b></p>
Since the Living Wage dataset was put together in 2014 we use the fact that a number of states have passed minimum wage hikes via the state legislature to create our training and test sets. The states that have raised minimum wage (not via automated inflation adjustments) are: Arkansas, Connecticut, Delaware, Maryland, Massachusetts, Minnesota, Nebraska, Rhode Island, South Dakota, Vermont and West Virginia. The prediction models use the base expenses (housing, food, medical), minimum wage, party in power in the state legislature, right to work laws and union participation in each state as factors. Comparing the predictions made by decision trees, random forrest and random forrest of inference trees we see that union participation, housing expenses and party in power of state legislature / governorship are the best predictors of which states may enact minimum wage laws. The predicted states are: California, Montana, New York, Ohio, Oregon and Pennsylvania. 

<p><b>Discussion / On lies, damn lies and statistics</b></p>
The predictions are encouraging in that they include California and New York - two states that we know to have enacted minimum wage hikes. Oregon, Montana and Pennsylvania are also somewhat encouraging as there are several cities and counties within those states that have agreed to increase the minimum wage to $15 as of this year. That said there are a number of possible issues to be aware of: 
<ul>
<li> Small Sample Size - this is likely the biggest issue. A more appropriate analysis that would have yielded a larger sample size would have been to use counties in each state as opposed to the state itself</li>
<li> Overfitting - there are a number of factors that can be seen as related, such as food and childcare expenses, union participation and right to work law states (inversely proportional), so its certainly possible that given the small sample size this issue could be exacerbated </li>
<li> Prediction Algorithm - there are other good choices that could have been explored as well, SVM, GBM and adaptive regression splines to name a few </li>
<li> Missing Factors - a large sample size would have allowed for the inclusion of other relevant factors such as historic trends in wage hikes in the state, population of minimum wage workers, state level super pac funding of corporations vs unions etc. </li>
</ul>

<p><b>Conclusion</b></p>
American working class families carry a tremendous financial burden, often having to work 2-3 jobs to provide for basic needs. It seems likely that a number of other states will join New York and California in making bold moves in raising the minimum wage. Sadly the raise in wage falls short of covering the living expenses of most working class families and without federal action it is unlikely that most states (esp. in the deep south) will enact wage increases. 


<p>Further Reading</p>
I'm far from informed about this issue (though interested). If you'd like to learn more here are a few things I came across:
<ul>
<li> An Argument FOR: http://www.bloombergview.com/articles/2012-04-16/u-s-minimum-wage-lower-than-in-lbj-era-needs-a-raise<//li>
<li> An Argument AGAINST: http://www.nytimes.com/2015/10/11/opinion/sunday/the-minimum-wage-how-much-is-too-much.html<//li>
<li> Economic Impact on Families and Businesses: http://laborcenter.berkeley.edu/local-minimum-wage-laws-impacts-on-workers-families-and-businesses/<//li>
<li> Myth-busting with the DOL: https://www.dol.gov/featured/minimum-wage/mythbuster</li>
<li> A Canadian Case Study: https://www.policyalternatives.ca/sites/default/files/uploads/publications/BC%20Office/2015/04/CCPA-BC-Case-for-Incr-Minimum-Wage_0.pdf<//li>
</ul>


<p>Data Sources</p>
<ul>
<li> Living Wage Calculator: http://livingwage.mit.edu/pages/about </li>
<li> Percentage of Labour Force in Unions in 2014-2015, US Bureau of Labor Statistics: 
http://www.bls.gov/news.release/union2.t05.htm </li>
<li> List of Current Governors, National Governors Association: http://www.nga.org/cms/governors/bios </li>
<li> List of State Legislators, Wikipedia: https://en.wikipedia.org/wiki/List_of_United_States_state_legislatures </li>
<li> List of Right to Work stats, Wikipedia: https://en.wikipedia.org/wiki/Right-to-work_law </li>
</ul>

@thekotecha
