1. Gender distribution of respondents from India:\n
--- SELECT Gender, COUNT(*) AS Count
FROM Dataset
WHERE Country = 'India'
GROUP BY Gender;

2. Percentage of respondents from India interested in education abroad and sponsorship:
--- SELECT
(COUNT(CASE WHEN Interest_in_Education_Abroad = 'Yes' AND Sponsorship_Required = 'Yes' THEN 1 END) * 100.0 / COUNT(*)) AS Percentage
FROM Dataset
WHERE Country = 'India';

3. Top 6 influences on career aspirations for respondents in India:
--- SELECT Career_Influence, COUNT(*) AS Count
FROM Dataset
WHERE Country = 'India'
GROUP BY Career_Influence
ORDER BY Count DESC
LIMIT 6;

4. How career aspiration influences vary by gender in India:
--- SELECT Gender, Career_Influence, COUNT(*) AS Count
FROM Dataset
WHERE Country = 'India'
GROUP BY Gender, Career_Influence
ORDER BY Gender, Count DESC;

5. Percentage of respondents willing to work for a company for at least 3 years:
--- SELECT
(COUNT(CASE WHEN Willing_To_Work_3_Years = 'Yes' THEN 1 END) * 100.0 / COUNT(*)) AS Percentage
FROM Dataset;

6. How many respondents prefer to work for socially impactful companies:
--- SELECT COUNT(*) AS Count
FROM Dataset
WHERE Social_Impact_Company_Preference = 'Yes';

7. Preference for socially impactful companies by gender:
--- SELECT Gender, COUNT(*) AS Count
FROM Dataset
WHERE Social_Impact_Company_Preference = 'Yes'
GROUP BY Gender;

8. Distribution of minimum expected salary in the first three years:
--- SELECT Minimum_Expected_Salary_3_Years, COUNT(*) AS Count
FROM Dataset
GROUP BY Minimum_Expected_Salary_3_Years;

9. Expected minimum monthly salary in hand:
--- SELECT MIN(Minimum_Monthly_Salary) AS Minimum_Monthly_Salary, MAX(Minimum_Monthly_Salary) AS Maximum_Monthly_Salary
FROM Dataset;

10. Percentage of respondents who prefer remote working:
--- SELECT
(COUNT(CASE WHEN Remote_Work_Preference = 'Yes' THEN 1 END) * 100.0 / COUNT(*)) AS Percentage
FROM Dataset;

11. Preferred number of daily work hours:
--- SELECT Preferred_Work_Hours, COUNT(*) AS Count
FROM Dataset
GROUP BY Preferred_Work_Hours;

12. Common work frustrations among respondents:
--- SELECT Work_Frustration, COUNT(*) AS Count
FROM Dataset
GROUP BY Work_Frustration
ORDER BY Count DESC;

13. Need for work-life balance interventions by gender:
--- SELECT Gender, COUNT(*) AS Count
FROM Dataset
WHERE Work_Life_Balance_Intervention = 'Yes'
GROUP BY Gender;

14. Number of respondents willing to work under an abusive manager:
--- SELECT COUNT(*) AS Count
FROM Dataset
WHERE Willing_To_Work_Under_Abusive_Manager = 'Yes';

15. Distribution of minimum expected salary after five years:
--- SELECT Minimum_Expected_Salary_5_Years, COUNT(*) AS Count
FROM Dataset
GROUP BY Minimum_Expected_Salary_5_Years;

16. Remote working preferences by gender:
--- SELECT Gender, COUNT(*) AS Count
FROM Dataset
WHERE Remote_Work_Preference = 'Yes'
GROUP BY Gender;

17. Top work frustrations for each gender:
--- SELECT Gender, Work_Frustration, COUNT(*) AS Count
FROM Dataset
GROUP BY Gender, Work_Frustration
ORDER BY Gender, Count DESC;

18. Factors that boost work happiness and productivity for respondents:
--- SELECT Work_Happiness_Boosters, COUNT(*) AS Count
FROM Dataset
GROUP BY Work_Happiness_Boosters;

19. Percentage of respondents needing sponsorship for education abroad:
--- SELECT
(COUNT(CASE WHEN Sponsorship_Required = 'Yes' THEN 1 END) * 100.0 / COUNT(*)) AS Percentage
FROM Dataset;
