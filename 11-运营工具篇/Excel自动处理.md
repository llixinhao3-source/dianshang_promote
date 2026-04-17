# Excel自动处理

> 数据清洗、分析、报表自动化

---

## 常用场景

| 场景 | 工具 | 说明 |
|------|------|------|
| 数据清洗 | Python/Pandas | 去重/补全/格式化 |
| 数据分析 | Excel/Python | 统计/透视/图表 |
| 报表生成 | Python/ReportLab | 自动生成日报/月报 |
| 数据同步 | Python/openpyxl | 多表合并/关联 |

---

## Python处理示例

```python
import pandas as pd

# 读取
df = pd.read_excel('data.xlsx')

# 清洗
df = df.drop_duplicates()
df = df.fillna('')

# 分析
result = df.groupby('类目').agg({
    '销量': 'sum',
    '利润': 'mean'
})

# 导出
result.to_excel('report.xlsx')
```

---

## 常用库

| 库 | 用途 |
|-----|------|
| pandas | 数据处理 |
| openpyxl | Excel读写 |
| xlwings | Excel操作 |
| reportlab | PDF报表 |
