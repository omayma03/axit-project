# Axit Landing Page Project

<p align="left">
  <!-- CI/CD Build Status -->
  <a href="https://github.com/omayma03/axit-project/actions/workflows/deploy.yml">
    <img src="https://github.com/omayma03/axit-project/actions/workflows/deploy.yml/badge.svg" alt="Deploy Static Content to Pages Status">
  </a>
  <!-- Lighthouse Performance -->
  <a href="https://pagespeed.web.dev/analysis?url=https://omayma03.github.io/axit-project/">
    <img src="https://img.shields.io/badge/Performance-95%2B-brightgreen?style=flat-square&logo=lighthouse&logoColor=white" alt="Lighthouse Performance">
  </a>
  <!-- Tech Stack Badges -->
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/Bootstrap_5-7952B3?style=flat-square&logo=bootstrap&logoColor=white" alt="Bootstrap 5">
</p>

## Project Idea and Goal
The project consists of converting a professional design (PSD format) into a live, interactive Landing Page. The primary goal is to build a modern and attractive web interface that is responsive across all screen sizes, providing a smooth user experience to showcase services and products in an elegant and organized manner.

---

## Tech Stack
This project was built using core web technologies and helpful libraries:
- **HTML5**: To build and structure the different sections of the page.
- **CSS3 / CSS Grid**: To style colors, typography, and accurately layout the page to match the original design file.
- **JavaScript (Vanilla)**: To add interactivity such as the "Scroll to Top" button and dynamic effects for the Navbar upon scrolling.
- **Bootstrap 5**: To speed up the development of interactive components (like the navbar and menus) and ensure the page is responsive on smart devices.

---

## CI/CD Pipeline & Deployment
We have introduced a pure static **CI/CD Pipeline** using **GitHub Actions**:
1. **HTML Validation (Health Check)**: Runs automatically on every `push` and `pull_request` to the `main` branch. It validates the HTML syntax in `index.html` using `htmlhint` to catch bugs, unclosed tags, or semantic issues.
2. **GitHub Pages Deployment (CD)**: Automatically bundles and deploys the static files directly to **GitHub Pages** whenever changes are successfully merged into the `main` branch.
   - **Live Site URL**: [https://omayma03.github.io/axit-project](https://omayma03.github.io/axit-project)

---

## Static Performance Audit & Optimizations
We conducted a deep static performance check on all assets to analyze loading speed and bandwidth footprint.

### 1. Asset Sizes Audit
| Asset | Current Size | Status | Impact / Optimization Strategy |
|---|---|---|---|
| `images/hero-bg.webp` | **149 KB** | 🟢 Good | Optimal. Compressed from 2.40 MB PNG (94% savings). |
| `images/custom-bg.webp` | **93 KB** | 🟢 Good | Optimal. Compressed from 1.20 MB PNG (92% savings). |
| `images/feature-2.png` | **254 KB** | 🟡 Warning | Heavy asset. Compress using Squoosh. |
| `images/feature-3.png` | **236 KB** | 🟡 Warning | Heavy asset. Compress using Squoosh. |
| `images/feature-1.png` | **39 KB** | 🟢 Good | Acceptable file size. |
| `images/avatar-1.png` | **11 KB** | 🟢 Good | Optimal. |
| `css/style.css` | **6.00 KB** | 🟢 Good | Light and optimized. |
| `js/main.js` | **1.37 KB** | 🟢 Good | Minimal script footprint. |

### 2. Actionable Optimization Recommendations
To boost your performance score above **95+** on mobile and desktop:
* **Background Images Optimized**: Background images `hero-bg.png` and `custom-bg.png` have been successfully converted to `.webp` format and compressed. This reduced their sizes from **3.60 MB** down to **242 KB** combined (a **~93% size reduction**), dramatically improving page load times.
* **Feature Images (Optional)**: `feature-2.png` (254 KB) and `feature-3.png` (236 KB) can be compressed further using [Squoosh.app](https://squoosh.app/) to save an additional ~350 KB if needed.

---

## How to Run the Project Locally
You can easily run and preview the project as follows:
1. Download or clone the project files to your device.
2. Open the `index.html` file directly in your web browser (e.g., Google Chrome).

---

## Known Issues (Postponed)
- **Forms are not connected to a server**: The forms on the page (such as the contact or subscription form) are static and do not send data to any backend server. Connecting them has been postponed until the backend is developed.
- **Performance Optimization**: Background images have been fully optimized. Further optimization can be applied to feature images (`feature-2.png` and `feature-3.png`) using compression tools.
- **Mobile Responsiveness**: The site needs further refinement to adapt better and more smoothly to mobile screens.
- **Sidebar / Mobile Menu**: The mobile-specific sidebar appears but contains no navigation links inside; it requires adding and styling the links.
