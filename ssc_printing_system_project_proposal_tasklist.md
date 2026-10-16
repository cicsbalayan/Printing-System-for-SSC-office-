# Supreme Student Council (SSC) Printing System Project Plan & Requirements

**Institution:** Batangas State University - The National Engineering University  
**Campus:** Balayan Campus  
**Office:** Supreme Student Council (SSC) Office  
**Period / Context:** 2023 – 2026 Operational Framework  

---

## 1. Executive Summary & Historical Context (2023–2026)

From 2023 through 2026, the Batangas State University Balayan Campus Supreme Student Council has experienced significant growth in student-led initiatives, organizational events, and academic advocacy campaigns.

* **2023 Phase (The Baseline):** Operations relied heavily on manual tracking of printing requests, resulting in paper wastage, queuing bottlenecks during midterm and finals weeks, and unstructured financial transparency reports.
* **2024–2025 Phase (The Transition):** Introduction of basic digital submission channels (Google Forms, manual messaging). However, accountability gaps, lack of quota tracking per student organization, and maintenance tracking for office printing hardware became prominent operational challenges.
* **2026 Target Phase (The Automated Solution):** Implementation of a centralized, web-based SSC Printing System designed to streamline document queuing, automate quota management for affiliated student organizations, ensure budget transparency, and integrate robust hardware monitoring.

---

## 2. Project Requirements

### A. Functional Requirements

1. **User Authentication & Role-Based Access Control (RBAC):**
   * *Standard Student / Org Member:* Can upload documents for printing, check queue status, and view remaining print credits/quota.
   * *SSC Officer / Print Manager:* Can approve/reject print requests, manage pricing/paper size tiers, adjust quotas, and oversee the job queue.
   * *System Administrator:* Manages user accounts, system logs, hardware configurations, and database backups.

2. **Document Upload & Pre-processing:**
   * Support for standard file formats (`.pdf`, `.docx`, `.xlsx`, `.pptx`, `.png`, `.jpg`).
   * Automated page-count estimation and cost calculation prior to final submission.
   * Options for configuration (grayscale/color, single/double-sided, paper size: A4, Short, Long).

3. **Queue & Status Management:**
   * Real-time queue dashboard showing job status (*Pending, Approved, Printing, Completed, Rejected*).
   * Estimated wait time notifications and token/reference code generation for claim verification.

4. **Reporting & Transparency Dashboard:**
   * Monthly generation of printing logs, paper consumption analytics, and expense reports addressing historical auditing needs (carrying over accountability standards from 2023–2025).
   * Exportable reports in PDF and CSV format for audit by the Office of the Student Affairs and Services (OSAS).

### B. Non-Functional Requirements

1. **Usability:** Intuitive, mobile-responsive user interface accessible via campus Wi-Fi or mobile data.
2. **Performance:** Page load times under 2 seconds; document processing and queue updates in real-time.
3. **Security:** Secure password hashing (bcrypt), HTTPS encryption, and role verification middleware to prevent unauthorized job approvals.
4. **Reliability & Privacy:** Daily automated database backups and auto-deletion of raw files from server storage 24 hours after print completion to maintain student privacy.

---

## 3. Technical Requirements

### A. Technology Stack

* **Frontend:** HTML5, CSS3 / Tailwind CSS, JavaScript (React.js or vanilla JS for modular interactivity).
* **Backend:** Node.js with Express.js (or Python Flask/FastAPI depending on team proficiency).
* **Database:** PostgreSQL or MySQL for structured relational data storage (users, print logs, quotas).
* **File Storage:** Secure local server storage or cloud bucket (e.g., Supabase Storage / AWS S3) with automated purging policies.
* **Hardware Integration:** CUPS (Common Unix Printing System) integration or local print spooler API for direct network printer communication (targeting standard campus office network printers like Epson L-series or Brother multi-function units).

### B. Infrastructure & Deployment

* Hosted locally on an SSC dedicated office machine or lightweight cloud instance (e.g., Render, Railway, or local campus server).
* Local network (LAN) accessibility within the SSC office and designated printing station.

---

## 4. Project Task List & Implementation Timeline

### Phase 1: Requirements Gathering & System Design (Weeks 1–2)
* [ ] Review historical printing logs and bottlenecks from 2023–2025 operations.
* [ ] Finalize database schema design (Users, Orgs, Print Jobs, Logs, Pricing).
* [ ] Create UI/UX wireframes for student portal and admin dashboard.

### Phase 2: Core Development (Weeks 3–6)
* [ ] Set up project repository and environment configuration.
* [ ] Implement user authentication and RBAC modules.
* [ ] Develop document upload module with format validation and page counter.
* [ ] Build queue management backend and real-time dashboard UI.

### Phase 3: Hardware Integration & Testing (Weeks 7–8)
* [ ] Connect software queue to office network printer/spooler via CUPS/Node-Printer.
* [ ] Conduct end-to-end testing (load testing, file format rendering tests).
* [ ] Perform security audit on user access permissions.

### Phase 4: Deployment, Training, and Handover (Weeks 9–10)
* [ ] Deploy system to local server / hosting environment.
* [ ] Conduct orientation and training for incoming 2026–2027 SSC officers.
* [ ] Roll out pilot testing phase with selected student organizations.
* [ ] Official launch and handover of documentation.