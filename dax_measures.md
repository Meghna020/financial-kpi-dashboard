# Core DAX Measures

```DAX
Actual Amount = SUM(FinanceData[Actual])

Budget Amount = SUM(FinanceData[Budget])

Variance = [Actual Amount] - [Budget Amount]

Variance % = DIVIDE([Variance], [Budget Amount])

Revenue = CALCULATE([Actual Amount], FinanceData[Category] = "Revenue")

Gross Profit =
    CALCULATE([Actual Amount], FinanceData[Category] = "Revenue")
    - CALCULATE([Actual Amount], FinanceData[Category] = "COGS")

EBITDA =
    [Gross Profit]
    - CALCULATE([Actual Amount], FinanceData[Category] = "Operating Expense")

EBITDA Margin = DIVIDE([EBITDA], [Revenue])

YTD Actual = TOTALYTD([Actual Amount], Calendar[Date])

YTD Budget = TOTALYTD([Budget Amount], Calendar[Date])
```

