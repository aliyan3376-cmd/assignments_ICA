# 1_attempt.md — Statistical choices and referee's note

 A. Which statistic would I report?

I calculated the mean and median using the Week 1 cleaned teaching file.

| Item | Mean | Median | First-to-last change | Statistic I would report | Reason |
| Oil B | 324.83 | 324.00 | 15.28% | Mean | The mean and median are very close, so the mean gives a reasonable overall average here. |
| Pulse C | 205.92 | 206.00 | 3.69% | Median | The two values are almost identical; I would use the median as a simple measure. |
| Staple A | 111.17 | 111.75 | 12.98% | Median | The median is slightly higher than the mean and is a cautious choice if a recorded price is unusually low or high. |
| Sweetener D | 166.75 | 166.75 | 19.41% | Both are similar | Since they are exactly the same in this dataset, either gives the same central figure. |

The percentage change is based on the average price across the two cities at the first and last dates. The first date is 1 January 2026 and the last date is 19 March 2026.

B. Week 2 Flagged Value sensitivity check (staple A)

I chose Staple A because the Week 2 cleaned file contains a flagged value of 1,250. I kept this value in the first calculation and removed only that observation for the second calculation.

| Staple A | Number of values | Mean | Median |
|---|---:|---:|---:|
| With 1,250 | 24 | 158.71 | 112.50 |
| Without 1,250 | 23 | 111.26 | 112.50 |

The mean decreases by **47.45** when 1,250 is excluded, while the median changes by **0.00**. This shows that the high value has a much stronger effect on the mean than on the median. I cannot say from the number alone that 1,250 is definitely an error, so it should be flagged and checked rather than silently deleted.

C. Referee's note

O — Observation:** In the Week 1 cleaned teaching data, the mean and median are close for all four items.  
O — Observation:** Oil B has a mean of 324.83 and a median of 324.00, while Pulse C has a mean of 205.92 and a median of 206.00.  
O — Observation:** Staple A has a mean of 111.17 and a median of 111.75, and Sweetener D has both a mean and median of 166.75.  
**E — Possible explanation:** Since the two averages are close, neither statistic gives a very different picture of the central price in the Week 1 cleaned file.  
**O — Observation:** Between 1 January and 19 March 2026, the average price across the two cities increased by 15.28% for Oil B, 3.69% for Pulse C, 12.98% for Staple A and 19.41% for Sweetener D.  
**E — Possible explanation:** Sweetener D had the largest first-to-last percentage increase, while Pulse C had the smallest, but these figures only compare the two dates and do not describe every movement in between.  
 D. Limits

The first-to-last percentage change is an endpoint comparison. It does not show the full path of prices during the period. Also, an unusual observation should not be called an error unless it can be checked against a reliable original record.
