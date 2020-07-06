
- クエリの実行に実行プランを含めるには

https://docs.microsoft.com/ja-jp/sql/relational-databases/performance/display-an-actual-execution-plan?view=sql-server-ver15


```
USE [hogehoge]

SELECT 'ALTER INDEX ' + '[' + C.name + ']' + ' ON [' + D.name + '].[' + B.name + '] REORGANIZE' AS 'reorganize command'
      ,D.name AS schemaname
      ,B.name AS table_name
      ,C.name AS index_name
      ,A.avg_fragmentation_in_percent
      ,A.page_count
FROM sys.dm_db_index_physical_stats (DB_ID(),null,null,null,null) AS A 
LEFT OUTER JOIN  sys.objects AS B 
ON  A.object_id = B.object_id 
LEFT OUTER JOIN  sys.indexes AS C 
ON  A.object_id = C.object_id  AND A.index_id = C.index_id 
LEFT OUTER JOIN  sys.schemas AS D 
ON  B.schema_id = D.schema_id 
WHERE B.type = 'U'
AND   C.index_id > 0 
AND   A.avg_fragmentation_in_percent > 30 
ORDER BY A.avg_fragmentation_in_percent DESC;
```
