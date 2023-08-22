<div align="center">
  <img height="150" src="https://camo.githubusercontent.com/62da68eb62b1e5f175f7d1f0191dd89a653d7908feb22d37d4a0ab07365d6791/68747470733a2f2f6d656469612e67697068792e636f6d2f6d656469612f4d3967624264396e6244724f5475314d71782f67697068792e676966"  />
</div>

###

<div align="center">
  <a href="https://www.linkedin.com/in/ali-kerem-simsek/" target="_blank">
    <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="linkedin logo"  />
  </a>
</div>

###

<h1 align="center">Comprehensive Power BI Report</h1>

###

<h2 align="left">My Aim</h2>

###

<p align="left">My purpose here is to tell you how I did this project and what I paid attention to. I hope it will be very instructive for you.</p>

###

<h2 align="left">Summary</h2>

###

<p align="left">Automating the monthly analysis a dealer basis due to the complexity and difficulties of dealing with big data.<br>My goal is to avoid the unnecessary workload. Thanks to this report, we can reach analysed data for 7 different dealers in just one report.</p>

###

<h2 align="left">Screens</h2>

###

<div align="center">
  <img height="500" src="https://github.com/krmsmsk/Resimler/blob/main/2/Screenshot_1.png?raw=true"  />
</div>

###

<p align="left">- I have the main panel on the left side. Above this are filters and transition buttons between pages.<br>- Again, at the top of this panel, there is the title of "Dealer Name and Sales Analysis". The "Dealer Name" here takes the name of the dealer we selected from the filter. I designed this with a measure.<br>- There is a date measure on this top of the right panel. This date was again automated with a measure. It trigger with my main data table 's max transaction date. In this way, i can reach last time that i need to get a time, refreshed data.<br>- On the other hands, you can see Summary table and Detail tables on the right panel. Summary table created with measures what data for business lines need. Detail tables created with measures like Summary. But as an extra, in detail tables have a structure that changes as you choose. I made this structure with measure. In the screenshot below, I used the formula I used for a similar structure as an example. Don't worry, the logic is the same.</p>

###

<div align="center">
  <img height="300" src="https://github.com/krmsmsk/Resimler/blob/main/2/Screenshot_4.png?raw=true"  />
</div>

###

<p align="left">- Why i use just measure for fill the tables? Why not i use nested tables?<br>- If I use nested tables, report loading time will take too long. So, maybe report will crash when it will every schedule process. Also, we need to think what we will add more for this report. I mean, we should not create hunderets of tables for a raport. This will be effect that performance.</p>

###

<div align="center">
  <img height="500" src="https://github.com/krmsmsk/Resimler/blob/main/2/Screenshot_2.png?raw=true"  />
</div>

###

<div align="center">
  <img height="500" src="https://github.com/krmsmsk/Resimler/blob/main/2/Screenshot_3.png?raw=true"  />
</div>

###

<p align="left">- In this section, my purpose getting rid of the complex image and accessing the detail data quickly without waiting for the tables to load.</p>

###

<div align="center">
  <img height="500" src="https://github.com/krmsmsk/Resimler/blob/main/2/Screenshot_7.png?raw=true"  />
</div>

###

<p align="left">- Finally, one of the most important parts is modeling the data.<br>- The rule we should pay attention to here is the legibility of the model. Star schema is generally used in PoweBI, but my model has turned into a snowflake schema because of the extra detail tables I need to create. There are some minor differences between these two schemes, let me talk about them a little bit.</p>

###

<h3 align="left">★ What is differences between Star Schema and Snowflake Schema?</h3>

###

<p align="left">1. A star schema has denormalized dimension tables, while a snowflake schema has normalized dimension tables.<br>2. A star schema is easier to design and implement than a snowflake schema.<br>3. A star schema can be more efficient to query than a snowflake schema, because there are fewer JOINs between tables.<br>4. A star schema can require more storage space than a snowflake schema, because of the denormalized data.<br>5. A star schema can be more difficult to update than a snowflake schema, because of the denormalized data.<br>6. A star schema can be more difficult to troubleshoot than a snowflake schema, because of the denormalized data.</p>

###

<h3 align="left">✔ What is Star Schema?</h3>

###

<p align="left">This schema consists of a central table, called the "fact table," and a number of directly connected other tables, called "dimension tables." The fact table contains information about metrics or measures, while the dimension tables contain information about descriptive attributes.</p>

###

<div align="center">
  <img height="500" src="https://github.com/krmsmsk/Resimler/blob/main/1690419880-starschema.jpg?raw=true"  />
</div>

###

<h3 align="left">✔ What is Snowflake Schema?</h3>

###

<p align="left">The snowflake schema consists of a central table, which is called the "fact table," and a number of other tables, which are called "dimension tables." As with other schemas, the fact table contains information about events or facts, while the dimension tables contain information about the dimensions of those events or facts.</p>

###

<div align="center">
  <img height="500" src="https://github.com/krmsmsk/Resimler/blob/main/1690420374-snowflakeschema.jpg?raw=true"  />
</div>

###

<h3 align="left">⁉ Why we should use a schema when we create a PowerBI report or something else like that?</h3>

###

<p align="left">If we dont use a schema and upload all our data with just one or two tables, our system will work unnecessarily. This mean is unnecessarily cost, time and errors. With a schema, we use more dimension table and so that our data load more quickly than the other one. Thanks to that, we won't need to wait for load and probably we won't get errors. Also, in this way anyone who look at our report, will understand our report and datas easly.</p>

###
