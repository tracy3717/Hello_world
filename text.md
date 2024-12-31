```python
score = int(input("请输入分数："))
if score >= 90
print("优秀")
```

```mysql
SELECT a.*, b.s_score as score01, c.s_score as score02
FROM student a
INNER JOIN score b ON a.s_id = b.s_id AND b.c_id = '01' #内连接，通过学号连接，指定01
LEFT JOIN score c ON a.s_id = c.s_id AND c.c_id = '02' OR c.c_id IS NULL #指定02，或者c中的c_id 直接不存在；为null的条件不存在，因为左连接中会直接排除c表中不存在的数据，包含null
WHERE b.s_score > c.s_score;
```

考察知识点：子查询、内连接（inner join 、join），左连接（left join），多表连接

1、查询"01"课程比"02"课程成绩高的学生的信息及课程分数

```mysql
SELECT a.*, b.s_score as score01, c.s_score as score02
FROM student a
INNER JOIN score b ON a.s_id = b.s_id AND b.c_id = '01' #内连接，通过学号连接，指定01
LEFT JOIN score c ON a.s_id = c.s_id AND c.c_id = '02' OR c.c_id IS NULL #指定02，或者c中的c_id 直接不存在；为null的条件不存在，因为左连接中会直接排除c表中不存在的数据，包含null
WHERE b.s_score > c.s_score;
```
