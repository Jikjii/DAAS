# Dominion Access & Activity System (DAAS)

**DAAS** is a modular, AI-enabled compliance infrastructure platform designed to modernize resident check-in/out procedures and operational accountability within shelters and supportive housing environments. The system integrates smart access control, real-time activity tracking, and AI-powered surveillance auditing to enhance security, streamline staff workflows, and ensure compliance with regulatory mandates.

---

## 🚀 MVP Overview

### ✅ Key Modules
- **Resident Identity & Access Management (IAM)**  
  QR code, badge, or facial recognition-based check-in/out for residents and household members.

- **AI-Powered Entrance Surveillance**  
  Computer vision engine (OpenCV-based) to monitor entry/exit points, flag unauthorized behaviors (tailgating, loitering, unlogged movement), and augment compliance with minimal human oversight.

- **Compliance Dashboard & Audit Logs**  
  Real-time reporting for staff and administrators including check-in history, compliance rates, occupancy alerts, and incident tracking.

---

## ⚙️ System Architecture

- **Frontend:** React.js, Tailwind CSS  
- **Backend API:** Node.js + Express (RESTful), secured with JWT-based auth  
- **Database:** PostgreSQL, modeled with Prisma ORM  
- **AI Engine:** Python (OpenCV), integrated via RESTful microservice  
- **Authentication:** Clerk.dev (multi-role auth for residents & admins)  
- **Hosting & Deployment:** Vercel (frontend), Railway/Render (backend + AI service)  
- **CI/CD:** GitHub Actions for automated testing & deployment

---

## 🧠 Technical Highlights

- Real-time presence logging with biometric fallback (badge/QR/FaceID)
- Resident registry supporting individual and household units with flagging logic (e.g., curfew violation, reentry risk)
- Camera stream analyzer using OpenCV + motion detection to match physical events with digital logs
- Modular microservices design for future scale (e.g., room access, IoT integrations, case management APIs)
- Audit trail and analytics interface for operational transparency and HUD compliance readiness

---

## 🗃️ Database Schema (MVP Scope)

- `Resident` (ID, name, DOB, household ID, unit, status flags)
- `CheckInLog` (resident_id, timestamp, method, location, verified_by)
- `IncidentReport` (event_type, severity, resident_id, AI_match_confidence)
- `AdminUser` (ID, role, permissions, assigned_facility)

---

## 📈 Use Case & Context

Shelters and transitional housing facilities typically rely on manual check-in/out logs, often requiring multiple daily entries per household. This creates operational friction, audit risk, and compliance gaps.

DAAS addresses:
- **Redundant & manual workflows** — digitized and automated
- **Resident noncompliance & circumvention** — AI-enforced accountability
- **Staff burden during peak hours** — asynchronous, AI-audited oversight

The MVP was scoped and developed based on real operational conditions at Westhab, the largest nonprofit developer and operator of supportive housing in Westchester County, NY.

---

## 📸 Screenshots / Demo
_(To be added after initial UI build and deployment.)_

---

## 📌 Future Roadmap (Post-MVP)

- **Biometric validation pipeline (facial recognition matching)**
- **Integration with NYC DHS shelter API or equivalent**
- **Resident-facing mobile app for QR-based check-ins and alerts**
- **Audit compliance export for HUD and city inspections**
- **IoT access control (e.g., smart locks, RFID doors)**

---

## 👤 Author

**Geraldo [Last Name]**  
Founder, DAAS | Developer, Westhab Inc.  
[LinkedIn] • [GitHub] • [YouTube: The Minority Developer]

---

## 📝 License

MIT License. See [LICENSE](./LICENSE) for details.
