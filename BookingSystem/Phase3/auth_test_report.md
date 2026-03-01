## Completed List

* Automated ZAP scan 
* Browser Testing
* User Session Testing

## Findings

### Security Vulnerability Assessment

| Category | Result |
|-----------|---------|
| High Risk Vulnerabilities | None detected |
| Medium Risk Vulnerabilities | None detected |
| Low Risk Vulnerabilities | None detected |
| Informational Alerts | 3 |

## Summary of Role Capabilities 

### 🧑‍🦲 **Guest**

---

**✅ Can do**


* “Can access register form — `/register`”
* “Can access login form — `/login`”
* “Can access resources page — `/resources`”

---

**❌ Cannot do**


* “Cannot access reservation form — `/reservation`”
* “Cannot edit reservations — `/reservation?id=1`”
* “Cannot edit resources — `/resources?id=4`”

---

### 🧑‍💼 **Reserver**

---

**✅ Can do**


* “Can access reservation form and book a reservation — `/reservation` + `/api/reservations`”
* “Can access resources form — `/resources`”
* “Can edit and delete resources - `/resources?id=4`”

---

**❌ Cannot do**


* “Cannot modify other reservers reservations — `/reservation?id=1`”
* “Cannot escalate privileges”

---

### 🧑‍💼🛡️ **Administrator**

---

**✅ Can do**


* “Can add a resource — `/admin/resources/new`”
* “Can delete reservations”
* “Can manage all reservations — `/reservation?id=1`”
* “Can view all users (spec 4)”

---

**❌ Cannot do**


---
