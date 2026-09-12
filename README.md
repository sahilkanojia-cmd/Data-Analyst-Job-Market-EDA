# Data Analyst Job Market Analysis

Exploratory data analysis of ~62,000 "Data Analyst" job postings, aimed at understanding salary trends, in-demand skills, hiring companies, locations, and work arrangements in the current job market.

## Objective

Analyze job postings to answer:
- What are the most common Data Analyst job titles?
- Which companies and locations offer the most opportunities?
- What is the typical advertised salary?
- Which skills are most in demand, and which are associated with higher pay?
- How common are remote and contract roles?
- What should an aspiring Data Analyst prioritize learning?

## Dataset

- **File:** `data/Data_Analyst_Jobs_Cleaned.csv`
- **Size:** 61,953 rows × 35 columns
- **Fields include:** job title, company, location, salary (raw and standardized), schedule/employment type, remote-work flag, posting source, and boolean skill flags (`skill_sql`, `skill_python`, `skill_excel`, `skill_tableau`, `skill_power_bi`, `skill_r`, `skill_aws`, `skill_spark`, `skill_hadoop`).

## Tools

Python · Pandas · NumPy · Matplotlib · Seaborn (Jupyter Notebook)

## How to Run

```bash
git clone https://github.com/sahilkanojia-cmd/Data-Analyst-Job-Market-EDA.git
cd Data-Analyst-Job-Market-EDA
pip install pandas numpy matplotlib seaborn
jupyter notebook Data_Analyst_Job_Market_EDA.ipynb
```

Make sure `Data_Analyst_Jobs.csv` stays in the `data/` folder — the notebook reads it via a relative path.

## Key Insights

1. **Salary data is sparse** — only ~16% of postings (10,088 of 61,953) disclose a standardized salary; treat pay findings as directional, not exhaustive.
2. **Median salary is $88,400** (mean $92,289), with the middle 50% falling between $62,400–$117,500. The distribution is right-skewed with outliers up to $624,000.
3. **"Data Analyst" is the top title** (~10% of postings), but the dataset also captures adjacent roles like Data Scientist, Data Engineer, and BI Analyst.
4. **Top "hiring companies" are mostly staffing/freelance platforms** (Upwork, Talentify.io, Dice) rather than direct employers — Walmart is the largest genuine direct employer in the top 10.
5. **72% of postings have no specific city** ("Anywhere" or "United States"); among city-specific roles, the Midwest leads — Oklahoma City, Kansas City, and Denver top the list.
6. **At least 45% of postings are explicitly remote-eligible**, likely an undercount since the remote flag has no explicit "False" value.
7. **SQL is the single most in-demand skill**, appearing in 51.5% of postings, followed by Excel (32.6%), Python (31.4%), Tableau (28.0%), and Power BI (26.5%).
8. **Niche technical skills pay the most** — Spark ($122,493), Hadoop ($118,985), and AWS ($114,830) top the average-salary ranking despite appearing in under 7% of postings.
9. **The most common skills pay the least** — Excel ($83,695) and Power BI ($91,994) sit at the bottom of the salary ranking, suggesting they're baseline expectations rather than differentiators.
10. **Remote vs. onsite pay is close on average** (~$92K mean either way) but remote postings have a lower median (~$85K vs. ~$92K), pointing to wider pay variance among remote listings.
11. **Full-time dominates** (~73% of postings), but contract/temp work is a substantial secondary path (~20%+ combined).
12. **LinkedIn is the dominant posting source** (~33%), followed by gig/freelance marketplaces like Upwork — confirming this market blends traditional and gig-style hiring.
13. **Standardized salary is a genuinely derived metric** — it correlates only moderately (r ≈ 0.40) with the raw min/max/avg salary fields rather than duplicating them.

## Bottom Line

For an aspiring Data Analyst: **SQL is non-negotiable**, pair it with **Excel, Python, Tableau, and Power BI** for baseline hireability, then differentiate with a **cloud or big-data skill (AWS, Spark)** to reach the top of the salary range.

## Caveats

- Salary figures are based on the subset of postings that disclosed pay (~16%) and may not represent the full market.
- Company and location breakdowns include staffing platforms and unspecified locations, which can obscure direct-employer and city-level trends.
- This is exploratory analysis, not a causal study — skill-salary associations are correlational.

## License

Feel free to fork and adapt for your own analysis or portfolio.
