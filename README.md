# Challenges_SQL

/*Challenges*/
/* The organization always posts on social media to promote the content of its contributors. The head of the company was
working on a presentation for investors and asked me to extract the insights from the post from the database. 
He wants to see how the post is performing on Facebook, especially the first*/

SELECT created_time, engaged_fans, post_clicks, reach, impressions
	FROM "PostInsights"
	ORDER BY created_time DESC
	
/* Top countries that where we have the highest number of fans */

SELECT "CountryCode","NumberOfFans"
   FROM "FansPerCountry"
   ORDER BY "NumberOfFans" DESC
   LIMIT 10
  
  /*Days when we witnessed a greater number of average new likes in a day in a sorted order */
  
  SELECT DISTINCT date,new_likes
  	FROM "GlobalPage"
	ORDER BY new_likes DESC
  
  /*We are doing a gender-based analysis. What is the latest split of fans by gender in percentage 
  
SELECT gender, SUM(number_of_fans),
ROUND(SUM(num_of-fans)*100 / (SELECT SUM(num_of_fans) FROM "FansPerGenderAge"
						Where "date" = '2018-10-16'),
FROM "FansPerGenderAge"
WHERE "date"  = '2018-10-16'
GROUP BY "Gender"
	  */
