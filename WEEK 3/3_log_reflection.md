Audit Table, Confused Classmate & Reflection
Part 2 & 3: Interpretation Auditor & Colour Check

 AI interpretation
Colour coded clain audit
 How I Checked
  Verdict 


1: "Sweetener D saw the largest relative price surge at 19.41%, rising from PKR 152.00 to PKR 181.50 per kg."
Green
Recomputed "(181.50 - 152.00) / 152.00 * 100 = 19.41%" directly from CSV. 
Accepted

2: "For all four items, the mean and median differ by less than 1 PKR, showing roughly symmetric distributions."
Amber 
Verified absolute differences in Python (all < 0.85 PKR); valid explanation.
Accepted

3: "Oil B's 15.28% increase was driven by global edible oil supply chain disruptions and import tariff hikes." 
Red
Checked dataset columns; no data exists on supply chains, imports, or tariffs.
Rejected

4: "Pulse C remained the most price-stable item, changing by only 3.69% between January 1 and March 19."
Green
Recomputed "(210.50 - 203.00) / 203.00 * 100 = 3.69%" (lowest change). 
Accepted

5: "Because Staple A's mean is below its median, household purchasing power in City 1 dropped faster."
Red
No income or household budget data exists in the file; claim is unsupported. 
Rejected



## 3. Step 4: Confused Classmate Transcript Excerpt
**Role:** AI played a classmate insisting *"The mean is always the typical price"* and asking *"but why?"* until the confusion was resolved.

> **Classmate (AI):** Why shouldn't I just report the mean (`158.71 PKR/kg`) for `Staple A` from our Week 2 file? Isn't the mean always the typical price?
>
> **Aliyan:** The mean is only the typical price when the data are roughly symmetric and free of extreme outliers. In our Week 2 `Staple A` data, 23 of the 24 prices sit between `99.5` and `122.0 PKR/kg`, while one typo was entered as `1,250 PKR/kg`. Because the mean adds every number together before dividing by `24`, that single typo pulls the mean up to `158.71 PKR/kg`—which is higher than every actual price shoppers ever paid.
>
> **Classmate (AI):** But why doesn't the median get pulled up the same way if both use all 24 rows?
>
> **Aliyan:** Because the mean uses **numerical values** (so adding `+1,141 PKR` to one row adds `+1,141 / 24 = +47.54 PKR` to the average), whereas the median uses **rank order**—it lines all 24 prices up from lowest to highest and picks the midpoint between the 12th and 13th values. Whether the 24th value is `122.0` or `1,250.0`, it is still just the single highest slot at the far right end, so the 12th and 13th middle slots stay at `112.50 PKR/kg`.
>
> **Classmate (AI):** Okay, that makes sense for typos—but why wouldn't the mean or median tell us whether prices *went up* over the quarter?
>
> **ALiyan:** Because both the mean and the median collapse all 12 weeks into a single summary number, erasing time order—a dataset rising from `100` to `120` and a dataset falling from `120` to `100` have the exact same mean and median (`110`). To prove prices went up, you need a **change over time** statistic like the first-to-last percentage change (`+12.98%` for `Staple A`), and you pair it with the **median** (`111.75 PKR/kg`) to show the typical level safely.
>
> **Classmate (AI):** Got it—so the mean gets dragged by extreme values because it sums magnitudes, the median resists them because it uses middle rank, and neither shows direction without a start-to-end change metric.

---

## 4. AI Use Log 

 Gate 1 (Before AI): Computed all item means, medians, percentage changes, and the Week 2 flagged-value comparison in Python first, then wrote and hashed `1_attempt.md.

Gate 2 (Role Used):** Used AI strictly as an *Interpretation Auditor* (Part 2) and *Confused Classmate* (Part 4). Did not copy AI-generated prose into `1_attempt.md`.

Gate 3 (Verification): Recomputed every number cited by the AI; flagged and rejected two unsupported causal/external claims.

---

## 5. Reflection

One thing I noticed is that the mean and median can tell a similar story in one dataset but become very different when an extreme value is included. In Week 1, the two measures are close for all four items. In Week 2, the Staple A value of 1,250 changes the mean much more than the median. I should not automatically delete an unusual value because it might be genuine; it needs to be checked against the original source. I also need to be careful not to explain a price increase by blaming inflation or shortages when the dataset does not contain evidence about the cause. The calculations show what changed in the recorded data, not why it changed.

## 6. Data limitations

The teaching file is explicitly labelled as illustrative and not actual PBS observations. 


 show direction over time) with the median (to summarize the typical price level without outlier distortion), noting that these figures reflect illustrative teaching data rather than official PBS releases.
