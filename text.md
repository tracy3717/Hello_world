```python
score = int(input("请输入分数："))
if score >= 90
print("优秀")
```

```mysql
SELECT a.*, b.s_score as score01, c.s_score as score02
FROM student a
INNER JOIN score b ON a.s_id = b.s_id AND b.c_id = '01'
LEFT JOIN score c ON a.s_id = c.s_id AND c.c_id = '02' OR c.c_id IS NULL 
WHERE b.s_score > c.s_score;
```
