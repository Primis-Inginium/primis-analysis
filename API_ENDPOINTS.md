# 🛰️ API Endpoints Index

This document lists all active FastAPI router prefixes mapped in `app/main.py`. Use this index to route API triggers accurately.

---

## 🚪 Authentication & Users
| Prefix | Tag | Description |
| :--- | :--- | :--- |
| **`/api/v1/auth`** | `authentication` | Login, Logout, standard verification |
| **`/api/v1/auth`** | `email` | Password resets, account verifies |
| **`/api/v1/users`** | `users` | User-profiles & setup payloads |

---

## 📚 Courses & Attendance
| Prefix | Tag | Description |
| :--- | :--- | :--- |
| **`/api/v1/courses`** | `courses` | Main Course data and metrics |
| **`/api/v1/online-courses`**| `online-courses` | Online-only course links |
| **`/api/v1/attendance`** | `attendance` | Roll-call reporting and stats |

---

## 👥 Roles & Metadata
| Prefix | Tag | Description |
| :--- | :--- | :--- |
| **`/api/v1/students`** | `students` | Student rosters and IDs |
| **`/api/v1/teachers`** | `teachers` | Teacher course metrics |
| **`/api/v1/parents`** | `parents` | Parent relation trees |

---

## 🔔 Communications & Admin
| Prefix | Tag | Description |
| :--- | :--- | :--- |
| **`/api/v1/admin`** | `admin` | Admin dashboard telemetry |
| **`/api/v1/admin`** | `admin-email` | Admin explicitly routing triggers |
| **`/api/v1`** | `materials` | File downloads / static uploads |
| **`/api/v1`** | `notifications` | Internal platform alerts |
| **`/api/v1/support`** | `support` | Ticket submission feeds |

---
*Created automatically to finalize organization on-boarding.*
