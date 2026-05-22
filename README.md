# Axit Landing Page Project

<p align="left">
  <!-- CI/CD Build Status -->
  <a href="https://github.com/omayma03/axit-project/actions/workflows/deploy.yml">
    <img src="https://github.com/omayma03/axit-project/actions/workflows/deploy.yml/badge.svg" alt="Deploy Static Content to Pages Status">
  </a>
  <!-- PageSpeed Insights Performance -->
  <a href="https://pagespeed.web.dev/analysis?url=https://omayma03.github.io/axit-project">
    <img src="https://img.shields.io/pagespeed/insights/v5/performance/https/omayma03.github.io/axit-project?label=Performance&style=flat-square&color=orange" alt="PageSpeed Insights - Performance">
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
| `images/hero-bg.png` | **2.40 MB** | 🔴 Critical | Very slow loading on mobile/slow connections. Needs compression/WebP. |
| `images/custom-bg.png` | **1.20 MB** | 🔴 Critical | Large background image. Needs compression/WebP. |
| `images/feature-2.png` | **254 KB** | 🟡 Warning | Heavy asset. Compress using Squoosh. |
| `images/feature-3.png` | **236 KB** | 🟡 Warning | Heavy asset. Compress using Squoosh. |
| `images/feature-1.png` | **39 KB** | 🟢 Good | Acceptable file size. |
| `images/avatar-1.png` | **11 KB** | 🟢 Good | Optimal. |
| `css/style.css` | **6.00 KB** | 🟢 Good | Light and optimized. |
| `js/main.js` | **1.37 KB** | 🟢 Good | Minimal script footprint. |

### 2. Actionable Optimization Recommendations
To boost your performance score above **95+** on mobile and desktop:
* **Convert Background Images**: Upload `hero-bg.png` and `custom-bg.png` to a free online tool like [Squoosh.app](https://squoosh.app/) or [TinyPNG](https://tinypng.com/) and convert them to `.webp` or highly compressed `.jpg`.
* **Expected Savings**: Converting to WebP will reduce the total website size from **~4.2 MB** down to **~600 KB** (an **85% reduction** in loading time!).
* **Update References**: Once optimized, update references in `index.html` (e.g. change `hero-bg.png` to `hero-bg.webp` in your CSS background or HTML image paths).

---

## How to Run the Project Locally
You can easily run and preview the project as follows:
1. Download or clone the project files to your device.
2. Open the `index.html` file directly in your web browser (e.g., Google Chrome).

---

## Known Issues (Postponed)
- **Forms are not connected to a server**: The forms on the page (such as the contact or subscription form) are static and do not send data to any backend server. Connecting them has been postponed until the backend is developed.
- **Performance Optimization**: Advanced compression strategies for background images have not yet been fully applied (see recommendations in the Performance Audit section).
- **Mobile Responsiveness**: The site needs further refinement to adapt better and more smoothly to mobile screens.
- **Sidebar / Mobile Menu**: The mobile-specific sidebar appears but contains no navigation links inside; it requires adding and styling the links.
