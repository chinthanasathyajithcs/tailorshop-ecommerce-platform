<div align="center">

# 🧵 TailorShop
### *Full-Stack Bespoke E-Commerce & Custom Tailoring Web Platform*

[![Java 21](https://img.shields.io/badge/Java_21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://openjdk.org/projects/jdk/21/)
[![Spring Boot 3](https://img.shields.io/badge/Spring_Boot_3-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)](https://spring.io/projects/spring-boot)
[![Hibernate](https://img.shields.io/badge/Hibernate_ORM-59666C?style=for-the-badge&logo=hibernate&logoColor=white)](https://hibernate.org/orm/)
[![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Cloudinary](https://img.shields.io/badge/Cloudinary_CDN-3448C5?style=for-the-badge&logo=cloudinary&logoColor=white)](https://cloudinary.com/)
[![Apache Maven](https://img.shields.io/badge/Apache_Maven-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white)](https://maven.apache.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

<br/>

### 🎓 University Coursework Project
**Academic Module:** 2nd Year — Enterprise Java Development & Object-Oriented Programming (OOP)  
**Core Competencies:** Full-stack layered architecture, RESTful API design, domain-driven entity modeling, Spring Data JPA, responsive frontends, and resilient cloud media integration.

<br/>

**A full-stack enterprise web application engineered in Java 21 and Spring Boot 3, bridging traditional bespoke tailoring with modern digital retail—featuring custom dimension measurement orders, real-time order tracking pipelines, and an administrative inventory control center.**

<br/>

</div>

---

## 📸 Platform Visual Showcase

<div align="center">
  <table border="0" style="width:100%; text-align:center;">
    <tr>
      <td width="50%" align="center" valign="top">
        <h3>🌐 Digital Storefront & Service Portal</h3>
        <img src="frontend/images/first4.png" alt="Digital Storefront Showcase" width="100%" style="border-radius:8px; margin-top:8px; box-shadow:0 4px 12px rgba(0,0,0,0.12);" /><br/><br/>
        <p align="center"><b>Brand & Customer Journey:</b> Modern hero landing page, brand story, bespoke tailoring measurement service catalog, and customer contact intake.</p>
      </td>
      <td width="50%" align="center" valign="top">
        <h3>🛒 Retail Shopping, Checkout & Tracking</h3>
        <img src="frontend/images/last4.png" alt="Retail & Order Tracking Showcase" width="100%" style="border-radius:8px; margin-top:8px; box-shadow:0 4px 12px rgba(0,0,0,0.12);" /><br/><br/>
        <p align="center"><b>E-Commerce & Fulfillment:</b> Dynamic product grid, persistent shopping cart with live tax/shipping computation, multi-stage visual order tracking, and role-based auth.</p>
      </td>
    </tr>
  </table>
</div>

---

## 📌 Executive Summary

Custom tailoring businesses operate with complex workflows: off-the-rack garment sales, raw fabric sales per meter, bespoke custom measurement intake, and time-sensitive order tracking. 

**TailorShop** unifies these operations into a single cohesive, high-performance web platform:
1. **Readymade Retail & Raw Materials Store**: Browse fashion collections, purchase fabrics per meter, configure standard sizing, and manage cart state.
2. **Bespoke Custom Tailoring Engine**: Submit millimeter-precise custom measurements (chest, waist, inseam, sleeve, and shoulder) for handcrafted suits, blazers, and shirts.
3. **Transparent Order Lifecycle**: Live status updates across all stages (*Confirmed → In Tailoring → Quality Check → Out for Delivery*).
4. **Administrative Back-Office Control**: Full inventory lifecycle management, Cloudinary-powered drag-and-drop media ingestion, and order status progression.

---

## ✨ Key System Features

| Category | Capability | Description |
| :--- | :--- | :--- |
| 📏 **Bespoke Tailoring** | **Custom Measurement Engine** | Dedicated order flow capturing precise body measurements (chest, waist, sleeve, inseam, length) for custom garments. |
| 🛍️ **E-Commerce Catalog** | **Dynamic Product Grid** | Responsive product catalog supporting standard garments, custom items, and raw fabrics sold per meter. |
| 🛒 **Cart & Pricing Engine** | **Persistent Shopping Cart** | Real-time dynamic tax (2%) calculations, automated delivery fees, and free-shipping thresholds for qualifying orders. |
| 🚚 **Order Pipeline** | **Visual Tracking Pipeline** | Live multi-stage visual tracking interface for customers to monitor fulfillment progress via unique order IDs. |
| ⚙️ **Admin Dashboard** | **Inventory Management** | Administrative console for product CRUD operations, automated image optimization, and order fulfillment updates. |
| ☁️ **Media Infrastructure** | **Resilient Cloud Storage** | Cloudinary Global CDN integration with automatic image resizing and fail-safe local disk fallback (`uploads/`). |

---

## 🏗️ Architecture & Technology Stack

```
┌─────────────────────────────────────────────────────────────┐
│                       Client Frontend                       │
│    HTML5  •  CSS3  •  JavaScript (ES6+)  •  Bootstrap 4     │
│   (Storefront  •  Custom Tailor Kiosk  •  Admin Dashboard)  │
└──────────────────────────────┬──────────────────────────────┘
                               │ RESTful JSON APIs (Multipart)
┌──────────────────────────────▼──────────────────────────────┐
│                    Spring Boot REST Layer                   │
│   ProductController • OrderController • CartController     │
│   CustomProductController • UserController • AdminController │
└──────────────────────────────┬──────────────────────────────┘
                               │
┌──────────────────────────────▼──────────────────────────────┐
│                     Service & Media Layer                   │
│         OrderService  •  CartService  •  ImageService       │
│               (Cloudinary CDN + Local Fallback)             │
└──────────────────────────────┬──────────────────────────────┘
                               │
┌──────────────────────────────▼──────────────────────────────┐
│                 Data Access & ORM (JPA)                     │
│         Spring Data JPA Repositories  •  Hibernate          │
└──────────────────────────────┬──────────────────────────────┘
                               │
┌──────────────────────────────▼──────────────────────────────┐
│                     Persistence Layer                       │
│      Embedded H2 File Database  •  MySQL Production Mode    │
└─────────────────────────────────────────────────────────────┘
```

| Component | Technology | Rationale |
|---|---|---|
| **Language & Runtime** | Java 21 (LTS) | Modern language features, pattern matching, records, and virtual thread readiness. |
| **Framework** | Spring Boot 3.2.5 | Enterprise-grade dependency injection, Spring MVC, and automated configuration. |
| **Data Layer** | Spring Data JPA / Hibernate | Object-Relational Mapping (ORM) and declarative repository queries. |
| **Database** | Embedded H2 / MySQL | Zero-configuration file database (`./data/tailorshopdb`) for instant local evaluation + MySQL support. |
| **Media Delivery** | Cloudinary Java SDK & CDN | Automatic WebP/AVIF format optimization, thumbnail generation, and global CDN delivery. |
| **Build Tool** | Apache Maven | Deterministic multi-platform builds via bundled Maven Wrapper (`mvnw`). |

---

## 💡 Architectural Evolution & Design Decisions (ADR)

* **🗄️ Database Modernization (MySQL Server ➔ Zero-Setup Embedded H2):**  
  The system was originally built against an external MySQL service (`localhost:3307`). To eliminate environment hurdles for evaluators, teammates, and CI runners, the primary profile was refactored to an embedded file-based **H2 Database** (`jdbc:h2:file:./data/tailorshopdb;AUTO_SERVER=TRUE`). Users can clone and launch immediately without installing database engines, while MySQL remains toggleable via `application.properties`.
* **☁️ Cloud Storage Evolution (AWS S3 ➔ Cloudinary CDN with Local Fallback):**  
  Remote asset storage originally targeted AWS S3. To optimize delivery speed, real-time image compression, and responsive dimension scaling, media handling was refactored to **Cloudinary CDN**. A resilient **local disk fallback** (`uploads/products/`) was also engineered to guarantee that image uploads function seamlessly even during offline development.

---

## 👨‍💻 My Role & Key Contributions

As a core architect and full-stack developer on this project, I designed and implemented foundational layers across both backend and frontend:

* **Spring Boot Application Architecture & Configuration**:
  * Set up the core project foundation, Maven build dependencies, package organization, and Spring Boot 3 bootstrapping.
  * Formulated `WebConfig.java` to handle CORS security headers and static resource handler mappings for `/uploads/**`.
* **Catalog Management & Product APIs (`ProductController.java`, `Product.java`)**:
  * Engineered the product management REST endpoints supporting multipart image upload ingestion.
  * Integrated Cloudinary CDN image upload pipelines with automated fallback to local disk storage.
* **Order Processing & User Management (`OrderController.java`, `UserController.java`)**:
  * Formulated customer registration, authentication, and order lifecycle persistence workflows.
  * Built database transactions linking line items, custom measurements, and order summaries.
* **Administrative Management Console (`admin-dashboard.html`, `admin-products.html`)**:
  * Architected the admin dashboard frontend interface for product catalog controls, category allocations, and stock management.
* **Customer Storefront & Checkout Flow**:
  * Built dynamic product card rendering using JavaScript (`shop.html`).
  * Implemented client-side shopping cart state management (`cart.html`).
  * Engineered the interactive Track Order status pipeline (`trackorder.html`) and responsive login portals (`login.html`, `login-admin.html`).

---

## 🚀 Getting Started

### Prerequisites
* **Java Development Kit (JDK) 21** or higher installed and configured on your `PATH`.
* Modern Web Browser (Chrome, Firefox, Edge, Safari).

### Quickstart Guide

1. **Clone the repository:**
   ```bash
   git clone https://github.com/chinthanasathyajithcs/tailorshop-ecommerce-platform.git
   cd tailorshop-ecommerce-platform
   ```

2. **Configure Application Properties:**
   ```bash
   cd backend
   cp src/main/resources/application.properties.example src/main/resources/application.properties
   ```
   *(The default settings use the embedded H2 file database, requiring zero configuration).*

3. **Start the Spring Boot Backend:**
   * **Linux / macOS:**
     ```bash
     ./mvnw spring-boot:run
     ```
   * **Windows:**
     ```cmd
     mvnw.cmd spring-boot:run
     ```
   * *The server will start on `http://localhost:8080`.*
   * *H2 Console can be accessed at `http://localhost:8080/h2-console` (JDBC URL: `jdbc:h2:file:./data/tailorshopdb`).*

4. **Launch the Frontend:**
   * Simply open `frontend/index.html` in your web browser (or serve the `frontend/` directory using VS Code Live Server or Python `python3 -m http.server 3000`).

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) - see the LICENSE file for details.
