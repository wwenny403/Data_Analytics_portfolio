# Day 1 Exercises — Pandas merge & pivot_table

完成以下练习，暂时不要查答案，自己尝试写代码。

---

# Exercise 1 — DataFrame 创建

使用 Pandas 创建以下两个 DataFrame。

用户表 users

| user_id | name |
|-------|------|
| 1 | Alice |
| 2 | Bob |
| 3 | Cindy |

订单表 orders

| user_id | product |
|-------|------|
| 1 | Book |
| 1 | Pen |
| 2 | Laptop |

任务：

1. 使用 `pd.DataFrame()` 创建两个表
2. 打印两个 DataFrame

---

# Exercise 2 — 数据表合并（merge）

使用 **Exercise 1 的两个表**。

任务：

1. 使用 `merge()` 合并 users 和 orders  
2. 按 `user_id` 进行合并  
3. 输出合并后的 DataFrame

思考：

如果某个用户没有订单，会发生什么？

---

# Exercise 3 — left join

在 Exercise 2 的基础上：

任务：

1. 使用 `how="left"` 重新合并两个表  
2. 观察输出结果  
3. 与默认 merge 结果进行比较

思考：

为什么有些值会出现 `NaN`？

---

# Exercise 4 — pivot_table 统计

创建以下 DataFrame：

| city | population |
|-----|------|
| Beijing | 100 |
| Beijing | 120 |
| Shanghai | 90 |
| Shanghai | 110 |

任务：

使用 `pivot_table()` 统计：

每个城市的 **总人口**

---

# Exercise 5 — 多维数据统计

创建以下数据：

| city | gender | population |
|-----|------|------|
| Beijing | M | 100 |
| Beijing | F | 120 |
| Shanghai | M | 90 |
| Shanghai | F | 95 |

任务：

使用 `pivot_table()` 生成统计表：

城市 × 性别 的人口统计。

输出结构类似：

| city | F | M |
|----|----|----|

---

# Challenge（可选）

创建以下订单数据：

| city | product | sales |
|-----|------|------|
| Beijing | Book | 30 |
| Beijing | Pen | 20 |
| Shanghai | Book | 25 |
| Shanghai | Pen | 15 |

任务：

用 `pivot_table()` 统计：

每个城市每种产品的 **销售总量**。
