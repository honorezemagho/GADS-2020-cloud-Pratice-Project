# Exploring a BigQuery Public Dataset

## Here a the Steps:

1. Log in Your Google Cloud Account. > In the Cloud Console, on the Navigation menu, click BigQuery. The Welcome to BigQuery in the Cloud Console message box opens. This message box provides a link to the quickstart guide and lists UI updates.

Click Done.
2. In the left pane, click ADD DATA > Explore public datasets. (In this example we are going to explore USA Names public DataSet)

3. In the searchbox, type USA Names then press ENTER.

4. Click on the USA Names tile you see in the search results.

5. Click View dataset.
BigQuery opens in a new browser tab. The project bigquery-public-data is added to your resources and you see the dataset usa_names listed in the left pane in your Resources tree.

6. Query bigquery-public-data.usa_names.usa_1910_2013 for the name and gender of the babies in this dataset, and then list the top 10 names in descending order.

9. Copy and paste the following query into the Query editor text area:
` SELECT
  name, gender,
  SUM(number) AS total
FROM
  `bigquery-public-data.usa_names.usa_1910_2013`
GROUP BY
  name, gender
ORDER BY
  total DESC
LIMIT
  10`

10. Click Run. The query results opens below the Query editor. At the top of the Query results section, BigQuery displays the time elapsed and the data processed by the query. Below the time is the table that displays the query results. The header row contains the name of the column as specified in GROUP BY in the query.
