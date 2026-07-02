# Week 2 - Notes & Observations
## Percentage Retention Rate & Documentation

---

## What I Did
Calculated the percentage retention rate for each cohort by 
dividing the absolute retained users by the original cohort 
size (Month 0) and multiplying by 100.

---

## Issues Encountered & How I Fixed Them

### Issue 1: Validation Returned False
**Problem:**
When validating that all retention values fall within 0-100%, 
the check returned False.

**Cause:**
The retention matrix contains NaN values for months where 
cohorts have no data yet (e.g. a cohort from December 2011 
cannot have Month 12 data). NaN values failed the <= 100 
condition causing the validation to return False.

**Fix:**
Used .fillna(0) to replace NaN values with 0 before 
validating, since 0% retention is a valid value:
```python
valid = (retention_rate.fillna(0) <= 100).all().all()
print("All values within 0-100%:", valid)
