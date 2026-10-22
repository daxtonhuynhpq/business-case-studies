<!--
  ════════════════════════════════════════════════════════════════════
  PROJECT README · Daxton Huynh — Business Portfolio
  Ghi chú trong các comment <!-- … --> như thế này KHÔNG hiển thị trên GitHub.
  Đặt file này tại: business-portfolio/zero-cost-operations-system/README.md
  ════════════════════════════════════════════════════════════════════
-->

<p align="center">
  <img src="assets/banner.svg" alt="Streamline End-to-End Operations with a Self-Built Zero-Cost System — AMI Education, Mar 2024 to Aug 2024" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/%E2%9C%93-Information_system_design-FFFF00?style=for-the-badge&labelColor=00003C" alt="Information system design">
  <img src="https://img.shields.io/badge/%E2%9C%93-Workflow_automation-FFFF00?style=for-the-badge&labelColor=00003C" alt="Workflow automation">
  <img src="https://img.shields.io/badge/%E2%9C%93-Resource_optimization-FFFF00?style=for-the-badge&labelColor=00003C" alt="Resource optimization">
</p>

<p align="center">
  <a href="#overview">Overview</a> ·
  <a href="#challenges">Challenges</a> ·
  <a href="#business-values">Business values</a> ·
  <a href="#excel-based-operation-systems">The system</a> ·
  <a href="#inside-the-system">Screenshots</a> ·
  <a href="#other-projects">Other projects</a>
</p>

---

## Overview

AMI Education was founded in March 2024 to bridge the gap in access to high-quality English education in Bac Lieu, a rural province in Vietnam. As the company grew, it faced the challenge of **scaling operations with extremely limited resources**.

With **no budget** for expensive ERP, CRM, or accounting systems, and **no headcount** for specialized staff, the company needed a **zero-cost, Excel-based solution** to automate workflows across **Sales, Academic, HR, and Finance**.

| | |
|---|---|
| **Organization** | AMI Education — English-education startup, Bac Lieu, Vietnam |
| **Timeline** | Mar 2024 – Aug 2024 |
| **My role** | Co-founder & CEO · designed and built the system |
| **Scope** | Sales · Academic · Human Resource · Finance · Support Admin |
| **Tools** | Microsoft Excel <!-- Thêm công cụ cụ thể đã dùng: Power Query, VBA, Data Validation, Google Forms… --> |
| **Software budget** | Zero — no paid systems, no additional headcount |

---

## Challenges

<table>
<tr>
<td width="33%" valign="top">

### Limited resources
As an early-stage startup, AMI could not afford to hire specialized staff. Some employees had to **wear various hats**, making workload reduction essential.

</td>
<td width="33%" valign="top">

### No budget for professional systems
ERP, CRM, and class management tools in Vietnam are **prohibitively expensive** for a small education business.

</td>
<td width="33%" valign="top">

### Fragmented data flows
Manual duplication of data across teams (Sales, Academic, HR, Finance) **consumed time and effort** and created **room for errors**. A single update had to be repeated in multiple places instead of cascading automatically into class assignments, receivables, payroll, and P&L reporting.

</td>
</tr>
</table>

---

## Business values

<p align="center">
  <img src="assets/kpis.svg" alt="Business values: 70% reduced administrative workload through a zero-cost, Excel-based information system that integrates all business functions; 10% saved monthly staffing expenses by enabling real-time, automated reporting of operational data" width="100%">
</p>

| Metric | Result | How |
|---|:---:|---|
| Administrative workload | **↓ 70%** | A zero-cost, Excel-based information system that integrates all business functions |
| Monthly staffing expenses | **↓ 10%** | Real-time, automated reporting of operational data, reducing redundant tasks and optimizing resources across departments |

---

## Excel-based operation systems

- Built **integrated Excel-based systems** covering Sales, Academic, HR, and Finance, enabling **centralized data management and automation**.
- Streamlined operations with **single-input workflows**, automated revenue recognition, payroll, and **dynamic P&L reporting**.

> **Legend** &nbsp; ✅ Automatically updated &nbsp;·&nbsp; ❌ Manual input &nbsp;·&nbsp; dashed arrow = support input

<!-- Sơ đồ được dựng lại từ trang 3 của portfolio. Vui lòng kiểm tra lại các mũi tên cho đúng luồng dữ liệu thực tế. -->

```mermaid
%%{init: {"theme": "base", "themeVariables": {"fontSize": "14px", "lineColor": "#8B8BC4"}}}%%
flowchart LR
  subgraph SALES["SALES"]
    CMD[("<b>Customer Master Database</b><br/>CMD ❌")]
    EBD["<b>Enrollment and Billing Database</b> ❌<br/>✅ Class allocation<br/>✅ Payment term (full · 50-30-20 · monthly)<br/>✅ Accounts receivable<br/>✅ Tuition revenue"]
    CMD --> EBD
  end

  subgraph ACADEMIC["ACADEMIC"]
    CAS["<b>Course Administration System</b><br/>❌ Faculty assignment<br/>❌ Course duration and learning schedule"]
  end

  subgraph HR["HUMAN RESOURCE"]
    PMS["<b>Payroll Management System</b><br/>✅ Teaching payroll<br/>✅ Non-teaching payroll"]
  end

  subgraph FINANCE["FINANCE"]
    EMS["<b>Expenses Management System</b><br/>✅ Operating expenses<br/>✅ Staffing expenses"]
    ACC["<b>Accrual-based P&L</b><br/>✅ Deferred revenue<br/>✅ Total expenses"]
    CASH["<b>Cash-based P&L</b><br/>✅ Cashflow recognition<br/>✅ Total expenses"]
  end

  subgraph ADMIN["SUPPORT ADMIN"]
    RM["<b>Receipts Management</b><br/>❌ Receipts generator"]
    WSM["<b>Working Schedule Management</b><br/>❌ Non-academic staff scheduling portal"]
    RS["<b>Reimbursement System</b><br/>❌ Expense reimbursement portal"]
  end

  EBD --> CAS
  CAS --> PMS
  PMS --> EMS
  EBD -- "tuition revenue" --> ACC
  EBD -- "receivables" --> CASH
  EMS --> ACC
  EMS --> CASH
  RM -.-> EBD
  WSM -.-> PMS
  RS -.-> EMS

  classDef sys fill:#3E3A6D,stroke:#3E3A6D,color:#FFFFFF
  class CMD,EBD,CAS,PMS,EMS,ACC,CASH,RM,WSM,RS sys
  style SALES fill:#00003C,stroke:#FFE45C,stroke-width:2px,color:#FFE45C
  style ACADEMIC fill:#00003C,stroke:#6FE3EE,stroke-width:2px,color:#6FE3EE
  style HR fill:#00003C,stroke:#C6F57A,stroke-width:2px,color:#C6F57A
  style FINANCE fill:#00003C,stroke:#3FC8EC,stroke-width:2px,color:#3FC8EC
  style ADMIN fill:#00003C,stroke:#FF6EC7,stroke-width:2px,color:#FF6EC7
  linkStyle default stroke:#8B8BC4,stroke-width:1.5px
```

### Module map

| Department | System | Components | Input |
|---|---|---|:---:|
| 🟨 **Sales** | Customer Master Database (CMD) | Customer records | ❌ |
| | Enrollment & Billing Database (EBD) | Class allocation · Payment term (full package, 50-30-20, monthly) · Accounts receivable · Tuition revenue | ❌ → ✅ |
| 🟦 **Academic** | Course Administration System | Faculty assignment · Course duration & learning schedule | ❌ |
| 🟩 **Human Resource** | Payroll Management System | Teaching payroll · Non-teaching payroll | ✅ |
| 🔷 **Finance** | Expenses Management System | Operating expenses · Staffing expenses | ✅ |
| | Accrual-based P&L | Deferred revenue · Total expenses | ✅ |
| | Cash-based P&L | Cashflow recognition · Total expenses | ✅ |
| 🟪 **Support Admin** | Receipts Management | Receipts generator | ❌ |
| | Working Schedule Management System | Non-academic staff scheduling portal | ❌ |
| | Reimbursement System | Expense reimbursement portal | ❌ |

### How a single input cascades

<!-- Mô tả dưới đây suy ra từ sơ đồ trong portfolio — chỉnh lại cho khớp cách hệ thống thực sự vận hành. -->

1. **Enroll once.** Sales records a student in the CMD and an enrollment in the EBD — class allocation, the payment schedule, receivables, and tuition revenue update automatically.
2. **Teach, then pay.** Academic sets faculty assignments and learning schedules, which feed the payroll system; non-academic schedules arrive from the Support Admin portal.
3. **Close the books automatically.** Payroll and reimbursements roll into the Expenses Management System, which feeds both the **accrual-based P&L** (deferred revenue) and the **cash-based P&L** (cashflow recognition).

---

## Inside the system

<!--
  ⚠️ Ẩn danh hoá dữ liệu trước khi đưa lên public: tên học viên, số điện thoại,
  học phí từng người, lương nhân sự. Xuất ảnh khoảng 1600px chiều ngang, lưu vào assets/.
-->

<table>
<tr>
<td width="50%" align="center">
  <img src="assets/sales-pipeline-dashboard.png" alt="AMI Sales Pipeline Dashboard"><br>
  <sub><b>Sales Pipeline Dashboard</b> — executive summary and KPI indicators</sub>
</td>
<td width="50%" align="center">
  <img src="assets/enrollment-billing-database.png" alt="Enrollment and Billing Database worksheet"><br>
  <sub><b>Enrollment & Billing Database</b> — single-input sheet that drives downstream modules</sub>
</td>
</tr>
</table>

---

## Skills demonstrated

| Skill | Evidence |
|---|---|
| **Information system design** | Mapped Sales, Academic, HR, Finance, and Support Admin into one integrated data model with single-input workflows |
| **Workflow automation** | Automated revenue recognition, payroll, and dynamic P&L reporting |
| **Resource optimization** | Cut administrative workload by 70% and saved 10% of monthly staffing expenses |

---

## Other projects

<table>
<tr>
<td width="50%" valign="top">

<sub>JUN 2024 – JUN 2025 · AMI EDUCATION</sub>
### #GO2025 Initiative — Zero-Cost Strategy
☑ Leadership &nbsp; ☑ Operational management &nbsp; ☑ Strategy planning and execution

<a href="../go2025-zero-cost-strategy/"><img src="https://img.shields.io/badge/LEARN_MORE-%C2%BB-FFFF00?style=for-the-badge&labelColor=00003C" alt="Learn more"></a>

</td>
<td width="50%" valign="top">

<sub>JAN 2023 – DEC 2023 · SIEMENS</sub>
### Sustainability @Siemens Vietnam
☑ Leadership &nbsp; ☑ Stakeholder engagement &nbsp; ☑ Market research

<a href="../sustainability-siemens-vietnam/"><img src="https://img.shields.io/badge/LEARN_MORE-%C2%BB-FFFF00?style=for-the-badge&labelColor=00003C" alt="Learn more"></a>

</td>
</tr>
<tr>
<td width="50%" valign="top">

<sub>OCT 2023 – JUL 2024 · SIEMENS</sub>
### Go Digital! B2B Distributors
☑ Partnership management &nbsp; ☑ Content management application (CMA)

<a href="../go-digital-b2b-distributors/"><img src="https://img.shields.io/badge/LEARN_MORE-%C2%BB-FFFF00?style=for-the-badge&labelColor=00003C" alt="Learn more"></a>

</td>
<td width="50%" valign="top">

<sub>SEP 2022 – DEC 2022 · SIEMENS</sub>
### Xcelerator Pitch Competition
☑ Leadership &nbsp; ☑ Innovation and development

<a href="../xcelerator-pitch-competition/"><img src="https://img.shields.io/badge/LEARN_MORE-%C2%BB-FFFF00?style=for-the-badge&labelColor=00003C" alt="Learn more"></a>

</td>
</tr>
</table>

---

<h2 align="center">Thank you for your time!</h2>

<p align="center">
  <!-- Thay YOUR-LINKEDIN-ID bằng đường dẫn LinkedIn thật -->
  <a href="https://www.linkedin.com/in/YOUR-LINKEDIN-ID"><img src="https://img.shields.io/badge/LinkedIn-Connect_with_me-FFFF00?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=00003C" alt="Connect on LinkedIn"></a>
  <a href="mailto:daxton.huypq@gmail.com"><img src="https://img.shields.io/badge/Email-daxton.huypq%40gmail.com-FFFF00?style=for-the-badge&logo=gmail&logoColor=white&labelColor=00003C" alt="Email"></a>
  <img src="https://img.shields.io/badge/Location-Peterborough%2C_Ontario-FFFF00?style=for-the-badge&logo=googlemaps&logoColor=white&labelColor=00003C" alt="Peterborough, Ontario, Canada">
</p>

<p align="center"><a href="../README.md">← Back to portfolio</a></p>
