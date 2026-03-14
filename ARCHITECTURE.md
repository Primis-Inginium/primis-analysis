# 🏗️ Backend System Architecture

This document provides an accurate overview of the **`primis-analysis`** backend, derived directly from the source code entry points.

---

## ⚙️ Core Stack
-   **Framework**: FastAPI (v1.0.0+)
-   **Database ORM**: SQLAlchemy with standard synchronous `SessionLocal`
-   **Table Management**: **Alembic** (Execute `alembic upgrade head` to synchronize).
-   **Static Uploads**: Handles local folders `/uploads` or redirects to **Cloudinary** dynamically based on `.env` configuration keys (`settings.use_cloudinary`).

---

## 🛰️ Middlewares & Policy
To ensure secure and compliant operations, the following are loaded in precedence:

| Middleware | Purpose | Target / Coverage |
| :--- | :--- | :--- |
| **ProxyHeaders** | Trust local proxy headers | Global (Addresses Vercel/Render loops) |
| **Limiter** | Rate-limiting security | Global exception triggers |
| **SecureHeaders**| Secure HTTPS flags set | Excluded on `/docs`, `/redoc` for CDN integrity |
| **CORSMiddleware**| Dynamic Origin allowing | Strictly scoped by `settings.get_cors_origins()` |

---

## 🚀 Environment Dependencies
To boot the cluster successfully, ensure `.env` encompasses:
-   Database connections strings.
-   Cloudinary secrets (if `.use_cloudinary` is truthy).
-   `ENVIRONMENT` (set to `development` for auto-create table streams).

---
*Maintained automatically from ground-truth node inspection.*
