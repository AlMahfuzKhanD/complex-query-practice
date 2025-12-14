# 🧠 SQL & Laravel Query Mastery Roadmap (with Exercises)

> **Goal:** Regain the ability to write complex SQL & Laravel queries independently — without relying on AI.

This roadmap is designed for **Laravel + MySQL developers** and is based on **real-world reporting problems** (like Loan Demand, Season-wise Reports, Excel exports, Yajra DataTables, etc.).

**Duration:** 8–10 weeks  
**Daily Time:** 60–90 minutes

---

## 🔑 Golden Rules (Very Important)

Before writing *any* query, always answer:

1. **What does ONE row represent?**
2. **What is the base table?**
3. **Do I need aggregation?**
4. **JOIN or subquery?**
5. **Is there a duplication risk?**

➡️ **Always write RAW SQL first**  
➡️ Then convert to **Laravel Query Builder**

---

## 🔰 PHASE 1 – SQL CORE (Week 1–2)

### Week 1: Data Retrieval Basics

#### Day 1 – SELECT & WHERE
**Learn**
- SELECT
- WHERE
- AND / OR

**Exercises**
- Get all customers
- Customers from Dhaka
- Customers created after `2024-01-01`

---

#### Day 2 – ORDER BY & LIMIT
**Exercises**
- Latest 10 bookings
- Oldest 5 customers
- Top 10 highest loan bookings

---

#### Day 3 – LIKE, IN, BETWEEN
**Exercises**
- Customers whose name starts with `A`
- Orders between two dates
- Bookings with status in (`active`, `pending`)

---

#### Day 4 – NULL & COALESCE
**Exercises**
- Bookings without delivery
- Loan amount showing `0` instead of NULL

---

#### Day 5 – Laravel Conversion
Convert **all previous queries** into:

```php
DB::table('table_name')->where(...)->get();
```

---

### Week 2: Aggregation (Most Important)

#### Day 6 – COUNT & SUM
**Exercises**
- Total bookings
- Total loan amount
- Total loan per season

---

#### Day 7 – GROUP BY
**Exercises**
- Total loan per customer
- Booking count per company
- Loan per season

---

#### Day 8 – HAVING
**Exercises**
- Customers with loan > 1,000,000
- Seasons with total loan > 10 crore

---

#### Day 9 – AVG, MIN, MAX
**Exercises**
- Average loan per booking
- Maximum loan per season

---

#### Day 10 – Mini Report
**Build:**
> Season-wise loan summary  
(season, total_loan, avg_loan)

---

## 🧩 PHASE 2 – MULTI TABLE THINKING (Week 3–4)

### Week 3: JOIN Fundamentals

#### Day 11 – INNER JOIN
**Exercises**
- Orders with customer name
- Booking with company name

---

#### Day 12 – LEFT JOIN
**Exercises**
- Bookings even if no loan exists
- Customers without orders

---

#### Day 13 – JOIN + Aggregation (Trap Zone)
**Exercises**
- Total loan per booking
- Identify duplicate row problem

---

#### Day 14 – Fix Duplication
**Exercises**
- Fix wrong totals caused by JOIN
- Explain why duplication happens

---

#### Day 15 – Laravel JOIN Practice
Convert all JOIN queries into Laravel Query Builder.

---

### Week 4: Subqueries (Senior-Level Skill)

#### Day 16 – Aggregate Before JOIN
**Exercises**
- Loan sum per booking (subquery)
- Recovery sum per booking

---

#### Day 17 – LEFT JOIN Subqueries
**Exercises**
- Booking + total loan
- Booking + total recovery

---

#### Day 18 – Multiple Subqueries
**Exercises**
- Booking + loan + recovery
- Outstanding calculation

---

#### Day 19 – Conditional Aggregation
**Exercises**
- Seed loan vs fertilizer loan
- Loan by type in single query

---

#### Day 20 – Mini Report
> Loan Demand Report (simplified version)

---

## 🏗 PHASE 3 – REPORT DESIGN THINKING (Week 5–6)

### Week 5: Analytical Thinking

#### Day 21 – Define Report Structure
**Exercises**
- Define what ONE row means
- Select correct base table

---

#### Day 22 – Multi-Season Comparison
**Exercises**
- Current vs previous season loan
- Self-join booking table

---

#### Day 23 – Historical Comparison
**Exercises**
- Year-over-year growth
- Season-wise trends

---

#### Day 24 – Calculated Fields
**Exercises**
- Outstanding amount
- Average loan per bag

---

#### Day 25 – Full Report (Raw SQL)
> Loan Demand Report (raw SQL only)

---

### Week 6: Laravel Production Patterns

#### Day 26 – Yajra DataTables
- Server-side processing
- Computed columns

---

#### Day 27 – Excel Export
- Same query as DataTable
- No duplication
- Correct totals

---

#### Day 28 – Totals & Footer Logic
**Exercises**
- SQL totals
- Excel totals

---

#### Day 29 – Refactoring
**Exercises**
- Extract reusable query logic
- Share logic between DataTable & Excel

---

#### Day 30 – Final Challenge
Rebuild a complete report **from scratch**

❌ No AI  
✔ Pure thinking

---

## ⚙️ PHASE 4 – PERFORMANCE & MASTERY (Week 7–8)

### Week 7: Performance Optimization
- Indexing strategy
- `EXPLAIN` query plan
- Query optimization

### Week 8: Advanced SQL
- CASE WHEN
- Window functions
- Financial reporting patterns

---

## 🧪 Daily Practice Rule

Before executing a query, write this as comments:

```sql
-- One row represents:
-- Base table:
-- Aggregation needed:
-- Join or subquery:
-- Duplication risk:
```

---

## 🚀 How to Use This Repo

- Practice **one day at a time**
- Save your SQL solutions
- Convert them to Laravel Query Builder
- Track improvements weekly

---

## 💡 Final Advice

> "SQL skill is not memorization — it is structured thinking."

If you can **explain your query**, you truly understand it.

Happy querying 🚀

