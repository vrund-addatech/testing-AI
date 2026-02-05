# Speaker Notes: Stored Procedure Logging Initiative

## Slide 1: Summary & Ask
**Key Message:** We're proposing a lightweight, safe, and data-driven approach to identify and fix the worst stored procedure performance issues.

**Talking Points:**
- This is a minimal-overhead logging solution focused only on reporting stored procedures
- No customer data will be stored—only aggregate performance metrics
- Data is automatically purged after 30 days to minimize storage and maintenance
- We're asking for approval to implement this logging and prioritize fixing the top offenders

---

## Slide 2: The Problem (Business Impact)
**Key Message:** Performance issues are hurting our customers and our team, but we lack the data to fix them effectively.

**Talking Points:**
- Customers are experiencing frustrating wait times when generating reports
- Peak hours create system stress with high CPU and I/O, risking overall stability
- We're constantly firefighting issues reactively instead of proactively
- Without production metrics, we can't confidently prioritize which issues to tackle first

---

## Slide 3: Proposed Approach (Simple & Safe)
**Key Message:** The solution is simple, safe, and focused—log only what matters, with built-in safeguards.

**Talking Points:**
- We'll capture essential performance metrics: execution count, CPU time, duration, and logical reads
- Scope is limited to reporting stored procedures only—no impact on transactional workflows
- Automatic 30-day retention means minimal storage costs and maintenance
- Privacy and safety are built-in: no customer data, minimal overhead, read-only metrics

---

## Slide 4: Why This Works
**Key Message:** This approach gives us the data we need to make smart decisions and measure success.

**Talking Points:**
- Data-driven prioritization ensures we fix the issues with the biggest impact first
- Measurable outcomes let us track improvements and prove the value of our work
- Proactive optimization reduces firefighting and reactive escalations
- The approach scales naturally as we grow our product and customer base

---

## Slide 5: Case Study (Real Production Example)
**Key Message:** Here's a real example of what we're dealing with—a stored procedure that's crushing performance.

**Talking Points:**
- This SP, "RptGetValidationEndOfDaySalesByInvoicePaymentDate," is a production offender
- It's consuming 94 seconds of CPU time and reading 90 million logical pages per execution
- Real customer impact: OT Works Clinic experienced 1.20-minute wait times just for this report
- This is the kind of issue that logging will help us discover and prioritize

---

## Slide 6: Root Cause Identified
**Key Message:** We found the problem—a missing index causing millions of unnecessary database lookups.

**Talking Points:**
- The execution plan revealed an Index Spool + Key Lookup pattern on AcctInvoiceLines
- A non-covering index forced the database to perform 21.7 million repeated lookups for InvoiceId
- This directly explains the excessive logical reads, CPU time, and duration
- Finding this required investigation time—logging will make these discoveries automatic

---

## Slide 7: Verified Fix (Proof of Value)
**Key Message:** We tested a fix and proved it works—execution time dropped from 80 seconds to 9 seconds.

**Talking Points:**
- We simulated the solution using temporary pre-calculation in our test environment
- Execution time dropped by ~89%—from 80 seconds to just 9 seconds
- The permanent fix is straightforward: update the existing index to include InvoiceId
- This eliminates the repeated base table lookups entirely

---

## Slide 8: Before vs After (Metrics Snapshot)
**Key Message:** The improvement is dramatic—89% faster execution, massively reduced reads and CPU.

**Talking Points:**
- Duration improvement: 80 seconds down to 9 seconds (−89%)
- Logical reads: reduced from 90 million to a fraction (no repeated lookups)
- CPU time: reduced from 94 seconds in line with the lower reads
- Bottom line: customers get their reports faster, and the system experiences less strain

---

## Slide 9: Implementation Plan
**Key Message:** We have a clear, phased rollout plan that starts delivering value in Week 2.

**Talking Points:**
- Week 1: Stand up the logging infrastructure with auto-purge and no customer data
- Week 2: Build a dashboard showing the top 10 offenders and start optimizing (beginning with our case study)
- Ongoing: Weekly reviews to track improvements, discover new hotspots, and feed into release planning
- This is a sustainable, continuous improvement process

---

## Slide 10: Decision & Next Steps
**Key Message:** We need your approval to move forward, and here's exactly what happens next.

**Talking Points:**
- **Decision needed:** Approve logging for reporting SPs and prioritize the case study fix
- **Next steps:** Assign an owner for the logging implementation, schedule the index fix, and set up monthly reviews
- **Important context:** This investigation was done outside normal work hours to avoid impacting delivery—we're passionate about solving this customer pain
- With your approval, we can turn this proof-of-concept into real, measurable improvements for our customers and our system

---

## General Presentation Tips
- Keep the tone collaborative and solution-focused
- Emphasize the low risk and high return of this approach
- Be ready to answer questions about overhead, scope, and timelines
- Highlight the customer impact and business value throughout
- Show confidence in the data and the proposed solution
