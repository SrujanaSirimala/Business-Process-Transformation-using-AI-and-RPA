## **Business Process Transformation using AI & RPA**

**Course:** CIS8010 | **Project:** 8010 Lending Co. — Mortgage Underwriting Process Innovation

## Business Context

**Who is Lending Co.?**
- A **direct residential mortgage lender** (mid-size company)
- Recently entered a partnership with a **fintech platform** that recommends home loan companies to prospective homebuyers
- This partnership would dramatically **increase the volume of loan applications** coming in

**The Core Challenge:**
- Their existing underwriting process was **labour-intensive** and relied on **basic scripting**
- It simply could **not handle the scale** of applications the fintech partnership would bring
- They needed to **innovate their business process** to stay competitive and profitable

**Key KPIs the company tracked:**
- Proportion of loans exceeding conforming loan limits
- Underwriting Process Lead Time
- Cost of Underwriting Process per application
- Document Verification Cycle Time
- Loan Funding Turnaround Time

## AS-IS Business Process (The Current State)

*"The As-Is process is how the company was operating before our proposed changes."*

The mortgage underwriting process started when Lending Co. **received a loan application** from an applicant. Here is how it flowed:

1. **Application Received** — A loan application comes in (via the fintech platform referral)
2. **Document Collection** — Staff manually checked whether the applicant had submitted the correct documentation
3. **Document Verification** — Employees manually verified that documents matched the data in the application
4. **Data Correction** — If discrepancies were found, they went back to the applicant for corrections
5. **Affordability Calculation** — Only at this late stage did the team calculate whether the applicant could actually afford the loan (Debt-to-Income ratio)
6. **Property Appraisal** — An appraisal was ordered and the value was compared to the purchase price
7. **Insurance & Tax Estimation** — Property tax and insurance tax were estimated (these were done one after the other)
8. **Final Decision** — A manager/underwriter reviewed everything and either approved or declined the loan

### As-Is Pain Points (Why It Was Broken)

| Pain Point | What It Meant |
|---|---|
| **No customer interaction touchpoints** | Applicants were left in the dark; no updates or reminders sent |
| **Heavy reliance on human intervention** | Every verification and decision step required a person, making it slow and error-prone |
| **Affordability checked too late** | The team spent time processing documents for applicants who couldn't even afford the loan |
| **Tasks executed sequentially** | Steps like estimating property tax and insurance were done one at a time, adding unnecessary delays |

## TO-BE Business Process (The Improved Future State)

*"The To-Be process is what we designed to fix those pain points."*

Our team proposed four key innovations:

### 1. Pre-Check Affordability Upfront
- **What changed:** Move the affordability check to the **very beginning** of the process — before any documents are collected
- **How:** Calculate the applicant's **Debt-to-Income (DTI) Ratio** using basic financial data (income, existing loan EMIs, assets, soft credit score check)
- **Rule:** DTI must be **< 43%** (industry standard) to proceed
- **Why it matters:** Eliminated wasted effort processing unqualified applicants — saving time and cost per application

### 2. AI-Powered Document Processing (Amazon Textract)
- **What changed:** Replaced manual document verification with **Amazon Textract**
- **How it works:** Textract uses OCR (Optical Character Recognition), Natural Language Processing, and Intelligent Document Processing to automatically:
  - Extract text from uploaded documents
  - Match document data against application data
  - Flag discrepancies without human review
- **Why it matters:** Dramatically reduced **document verification cycle time** and removed a major source of human error

### 3. Parallel Task Execution
- **What changed:** Tasks that were previously done sequentially are now done **simultaneously**
- **Example:** Estimating Property Tax and Insurance Tax happen at the same time instead of one after the other
- **Why it matters:** Directly reduces **underwriting lead time**

### 4. RPA for Human Tasks (UiPath)
- **What changed:** Routine decision-support tasks previously done by humans are now automated using **UiPath RPA (Robotic Process Automation)**
- **Tasks automated:**
  - Checking if appraisal value is less than purchase price
  - Checking if appraisal has been received
  - Triggering loan approval or rejection workflows
- **Why it matters:** Frees up underwriters and managers for complex judgment calls only

### 5. Automated Document Reminder
- **New step added:** If an applicant hasn't submitted required documents after **5 days**, an automated reminder is sent
- **Why it matters:** Reduces application drop-off and keeps the pipeline moving without manual follow-up

## Critiques & Impediments We Addressed


| Challenge | How We Addressed It |
|---|---|
| **Cost of Amazon Textract** ($50/1,000 pages for forms) | Justified by reduction in lead time and verification costs — net positive ROI |
| **Employee impact from automation** | Proposed a **4-week training program** for staff on the new process |
| **RPA errors replacing manual tasks** | Retained human swim lanes (LPC, Manager, Underwriter) for oversight and escalations |
| **Pre-check DTI may be inaccurate** | A full affordability check is still done later after verified documents and appraisal are received |
