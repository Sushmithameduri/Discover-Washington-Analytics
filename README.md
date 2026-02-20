# 🌲 Discover Washington – Explore, Experience, and Enjoy!

> A WordPress-based travel guide website built for Washington State, developed as part of a Web Analytics & Content Strategy course project (IS5320)
> <img width="1045" height="588" alt="image" src="https://github.com/user-attachments/assets/0186e2b1-e066-47be-849f-fa60dcffca6e" />


---

## 🛠️ Tech Stack

![WordPress](https://img.shields.io/badge/WordPress-21759B?style=for-the-badge&logo=wordpress&logoColor=white)
![AWS](https://img.shields.io/badge/Amazon_AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![Google Analytics](https://img.shields.io/badge/Google%20Analytics-E37400?style=for-the-badge&logo=google-analytics&logoColor=white)
![Google Maps](https://img.shields.io/badge/Google%20Maps-4285F4?style=for-the-badge&logo=google-maps&logoColor=white)
![Looker Studio](https://img.shields.io/badge/Looker%20Studio-4285F4?style=for-the-badge&logo=looker&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

---

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Tech Stack Details](#tech-stack-details)
- [Site Architecture](#site-architecture)
- [Content Strategy](#content-strategy)
- [Design Strategy](#design-strategy)
- [Analytics & KPIs](#analytics--kpis)
- [Development Phases](#development-phases)
- [WordPress Plugins Used](#wordpress-plugins-used)
- [Server Infrastructure](#server-infrastructure)
- [Lessons Learned & Future Work](#lessons-learned--future-work)

---

## Project Overview

**Discover Washington – Explore, Experience, and Enjoy** is a WordPress website designed to serve as a comprehensive digital travel guide for Washington State. The site covered everything from Seattle tourism and national parks to food & drink, hiking trails, tech hubs, and universities.

**Mission Statement:**
> *"Discover Washington – Explore, Experience, and Enjoy aims to be the ultimate digital guide, providing insightful and engaging content to help visitors and locals explore the best of Washington's cities, nature, food, and culture."*

The site was hosted on an AWS EC2 instance (`http://18.118.179.231/`) and tracked with Google Analytics 4 (GA4) and Google Looker Studio for performance reporting.

---


## Tech Stack Details

| Category | Technology |
|---|---|
| **CMS** | WordPress (self-hosted) |
| **Theme** | Palawan (lightweight, mobile-responsive) |
| **Hosting** | AWS EC2 (Ubuntu) |
| **Containerization** | Docker + Docker Compose |
| **Analytics** | Google Analytics 4 (GA4) |
| **Dashboard Reporting** | Google Looker Studio |
| **Maps** | Google My Maps (custom embedded maps) |
| **Domain** | Elastic IP (AWS) — `18.118.179.231` |

---

## Site Architecture

The site was built around a multi-level navigation system designed for intuitive content discovery.

### Main Navigation Menu

```
Home
├── Tourism Places in Seattle
│   ├── Chihuly Garden and Glass
│   ├── Pike Place Market
│   └── Seattle Art Museum (SAM)
├── Nature & Adventure
│   ├── Parks
│   │   ├── Mount Rainier National Park
│   │   ├── Olympic National Park
│   │   └── North Cascades National Park
│   └── Beaches
│       └── Best Beaches in Washington
├── Hiking & Trekking
│   └── Hiking at Rattlesnake Ledge
├── Food & Drink
│   ├── Wineries & Breweries
│   └── Pike Place Market: A Must-Visit Spot for Food Lovers
├── Events & Festivals
│   ├── Annual Events in Washington
│   └── Celebrate the Seasons: Best Seasonal Festivals
└── Innovation & Universities
    ├── Washington's Universities: Where Innovation Meets Opportunity
    └── Tech Offices & Headquarters: Driving Innovation in Washington
```



### Content Hierarchy Pattern

Each section followed a consistent three-tier structure:

1. **Main Menu Page** — Introduces the theme (e.g., "Nature & Adventure") with an overview and call to action

<img width="605" height="442" alt="image" src="https://github.com/user-attachments/assets/a7d54f56-e857-4482-b6d4-cf3e460fcecb" /><img width="606" height="271" alt="image" src="https://github.com/user-attachments/assets/c70d9be2-2378-4bae-840e-29afaf2d6510" />

2. **Subcategory Page** — Drills into a sub-topic (e.g., "Parks") with summaries and links to individual posts

<img width="633" height="287" alt="image" src="https://github.com/user-attachments/assets/037c90d4-043c-4b36-a230-1b9f755ed320" />

3. **Individual Post** — Detailed guide for a specific attraction, including hero image, structured sections, embedded maps, and references

<img width="298" height="682" alt="image" src="https://github.com/user-attachments/assets/fb7f393b-2678-4444-9e38-4dbf5283ebcf" />



---

## Content Strategy

### Post Structure

Every post was built on a consistent template to maximize readability and engagement:

- **Hero Image** — High-resolution, visually striking photo that captures the location's essence
- **Intro Section** — Brief, evocative overview of the destination
- **Structured Sections** — Organized using clear headings and subheadings (e.g., "Epic Hiking Trails," "Wildlife & Natural Wonders," "Stay & Camp in the Wild")
- **Checkmark Bullet Points** — Easy-to-scan lists of key attractions and activities
- **Practical Details** — Trail difficulty, seasonality, family-friendliness tips
- **Call-to-Action** — "Your Adventure Starts Here" section with a "Ready to Explore?" prompt
- **Embedded Google My Maps** — Custom interactive map for route planning
- **References** — Citations from authoritative sources (National Park Service, Wikipedia, official resort sites)

### Content Categories

| Category | Focus |
|---|---|
| Tourism Places in Seattle | Cultural landmarks, art, iconic Seattle spots |
| Nature & Adventure | National parks, wilderness, beaches |
| Hiking & Trekking | Trail guides, difficulty levels, best seasons |
| Food & Drink | Restaurants, wineries, breweries, food markets |
| Events & Festivals | Seasonal events, festivals, local celebrations |
| Innovation & Universities | Tech companies, universities, STEM ecosystem |

### Content Inspiration

The site drew inspiration from leading travel platforms:
- [Incredible India](https://www.incredibleindia.gov.in/en) — High-quality visuals, structured regional navigation
- [VisitScotland](https://www.visitscotland.com) — Clean design, strong destination storytelling
- [Lonely Planet](https://www.lonelyplanet.com/) — Well-structured travel guides with practical detail
- National Geographic Travel — Immersive imagery, engaging long-form content

### Interactive Elements

- **Custom Google My Maps** — Created a shared map with layers for Seattle Attractions, Hiking Spots, and Tech Headquarters, embedded across relevant posts so users can plan routes geographically [Custom Maps](https://www.google.com/maps/d/u/0/edit?mid=16iY4FRBluleKx2XL2kmZpe7WUCDzLBs&ll=47.35848409374252%2C-121.0207488&z=7)
- **Smart Slider 3** — Dynamic homepage hero image slider showcasing Washington's landscapes
- **Tag Cloud** — Visual taxonomy powered by the Cool Tag Cloud plugin, allowing keyword-based navigation

---

## Design Strategy

### Visual Identity

- **Theme:** Palawan WordPress theme — chosen for fast performance, mobile responsiveness, and clean aesthetics
- **Color Palette:** Greens and earth tones reflecting Washington's forests, mountains, and coastline
- **Typography:** Clear, readable fonts with strong visual hierarchy

### Layout Principles

- Full-width hero images on the homepage and key landing pages
- Sidebar with Tag Cloud, Recent Posts, Recent Comments, and Categories for multi-pathway navigation
- Dropdown mega-menus for deep content discovery without overwhelming the user
- Mobile-first design — tested primarily on Chrome (which accounted for ~80% of traffic)

### Design Decisions Informed by Analytics

- **Chrome optimization prioritized** after GA4 data showed ~25–30 of all users on Chrome vs. minimal Edge/Safari usage
- **Nature & Adventure content expanded** after analytics showed it was the second most-visited category (44 views), with Mount Rainier and Olympic National Park pages performing strongly
- **Homepage spotlights updated** to surface popular categories in the sidebar, reducing bounce rate
- **High-quality images added** to visually rich pages like Chihuly Garden and Mount Rainier after engagement data showed higher session durations on image-heavy pages

---

## Analytics & KPIs

### KPI Framework

| # | Goal | KPI | Metric |
|---|---|---|---|
| 1 | Maximize Student Participation | Daily Active Students | Active Users |
| 2 | Improve Resource Engagement | Views per Session | Views per Session |
| 3 | Track Content Effectiveness | Average Session Duration | Average Session Duration |
| 4 | Ensure Consistent Access | Returning Visitor Rate | % Returning Users |
| 5 | Validate Navigation Clarity | Bounce Rate | Bounce Rate |

---

### 📊 Looker Studio Dashboard


<img width="904" height="677" alt="image" src="https://github.com/user-attachments/assets/26fcc2b1-c2d1-4c9c-b6c3-348a9daa56e1" />


---

### 📈 Growth Metrics (Phase 3)

| Metric | Value |
|---|---|
| 📈 Active User Growth | **+82.4%** (reached 31 users in 7 days) |
| 👤 New User Growth | **+66.7%** |
| ⚡ Event Count Growth | **+26.5%** (946 recorded events) |
| ⏱️ Avg. Time on Site | **8 min 59 sec** |
| 🔁 Bounce Rate | **38%** |
| 👁️ Total Page Views | **958** |
| 📅 Peak Views/Session | **8.32** (March 10, 2025) |


<img width="723" height="353" alt="image" src="https://github.com/user-attachments/assets/444007fe-b24f-48c0-98b1-1f87b29c4593" />

---

### 🔥 GA4 Dashboard

<img width="690" height="352" alt="image" src="https://github.com/user-attachments/assets/3e461e00-7e55-4e4f-82c2-a403112ee2ac" />

---

### 📄 Top Pages by Views

| Page | Views | Events |
|---|---|---|
| Discover Washington – Homepage | 299 | 774 |
| Chihuly Garden and Glass | 65 | 123 |
| Nature & Adventure | 44 | 90 |
| Mount Rainier National Park | 28 | 60 |
| Pike Place Market | 22 | 50 |
| IS5320-T4 | 21 | 52 |
| Washington's Universities | 19 | — |
| Olympic National Park | 13 | — |

---

### ⏱️ Per-Page Engagement Time

| Page | Active Users | Avg. Engagement | Views |
|---|---|---|---|
| Discover Washington (Home) | 39 | 36s | 299 |
| Nature & Adventure | 8 | 16s | 44 |
| Pike Place Market | 7 | 10s | 22 |
| Hiking at Rattlesnake Ledge | 6 | 38s | 15 |
| Mission Statement | 6 | 10s | 18 |
| Mount Rainier National Park | 6 | 29s | 28 |
| Chihuly Garden and Glass | 6 | 18s | 65 |
| Celebrate the Seasons | 5 | 29s | 6 |
| IS5320-T4 | 5 | **1m 52s** | 21 |

<img width="794" height="347" alt="image" src="https://github.com/user-attachments/assets/ac561d75-4606-4f28-91b8-8252a22418b3" />


---

### 📅 Traffic by Day of Week

| Day | Users | Traffic Level |
|---|---|---|
| Thursday | 13 | 🔥🔥🔥 Peak |
| Sunday | 11 | 🔥🔥🔥 High |
| Saturday | 10 | 🔥🔥🔥 High |
| Friday | 6 | 🔥🔥 Medium |
| Wednesday | 5 | 🔥🔥 Medium |
| Monday | 3 | 🔥 Low |
| Tuesday | 1 | ⬇️ Lowest |

> **Strategy:** New content was published on **Wednesdays & Thursdays** to index before the weekend traffic surge.

<img width="292" height="321" alt="image" src="https://github.com/user-attachments/assets/ec476d6b-067d-4a89-814e-9edb61a90e7f" />

---

### 🌐 Browser Usage

| Browser | Users |
|---|---|
| Chrome | ~25–30 (~80%) |
| Edge | Minimal |
| Safari | Minimal |

> **Impact:** Chrome optimization was prioritized in all design and testing decisions.

<img width="269" height="304" alt="image" src="https://github.com/user-attachments/assets/ac8a6efc-433e-446a-97f1-0641484001e3" />

---

### 👥 User Activity Over Time

```
30 days  ████████████████████████  42 users
 7 days  ███████████████           31 users
  1 day  ██                         3 users
```
<img width="329" height="208" alt="image" src="https://github.com/user-attachments/assets/3162c790-f38c-4fd8-96ac-21748897f636" />


---

### 🔄 New vs. Returning Users

| Segment | Share |
|---|---|
| New | 33.3% |
| Returning | 33.3% |
| Not Set | 33.3% |

<img width="174" height="167" alt="image" src="https://github.com/user-attachments/assets/0bd36c8f-cc55-4b08-877d-ff249d542209" />

---
---

## Development Phases

### Phase 1 — The Beginning

**Goal:** Establish the site foundation and publish prototype posts.

- Provisioned AWS EC2 instance and associated Elastic IP
- Installed Docker, Docker Compose, and WordPress
- Configured the Palawan theme and initial navigation structure
- Published 3 prototype posts to establish the content template:
  - *Chihuly Garden and Glass: A Dazzling Art Experience*
  - *Pike Place Market: A Must-Visit Spot for Food Lovers*
  - *Hiking at Rattlesnake Ledge*
- Defined content strategy and design direction
- Assigned team roles across IA, UX/UI, Web Dev, Server Admin, Content, PM, and QA

### Phase 2 — Expansion

**Goal:** Build out the full content and navigation architecture.

- Developed complete menu system with all six main categories
- Created main category pages, subcategory pages, and individual attraction posts
- Integrated Google My Maps across relevant posts
- Added Smart Slider 3 homepage image slider
- Installed and configured all WordPress plugins
- Published posts across all content categories
- Connected GA4 for analytics tracking

### Phase 3 — The Enlightenment

**Goal:** Analyze data, refine strategy, and present findings.

- Conducted full preliminary analytics review using GA4 and Looker Studio
- Identified top-performing content and adjusted publishing schedule accordingly
- Created custom Google My Maps for all Phase 3 content
- Built and published KPI Everyday Dashboard in Looker Studio
- Added submenus and deepened content in high-traffic categories
- Produced final project documentation and client-ready presentation

---

## WordPress Plugins Used

| Plugin | Purpose |
|---|---|
| **Smart Slider 3** | Dynamic homepage hero image slider |
| **TaxoPress** | Manages tags, taxonomies, and categories |
| **WPCode Lite** | Adds and manages custom PHP snippets |
| **YYDevelopment Tag Manager** | Integrates GA4 / Tag Manager tracking codes |
| **Cool Tag Cloud** | Displays a styled tag cloud in the sidebar |

---

## Server Infrastructure

- **Platform:** Amazon Web Services (AWS)
- **Instance:** EC2 (Ubuntu)
- **Networking:** Elastic IP for stable public access
- **Port Configuration:** HTTP (port 80) opened on launch
- **Stack:** Docker + Docker Compose for WordPress deployment
- **Uptime:** Monitored throughout all three phases — zero reported downtime

---

## Lessons Learned & Future Work

### ✅ What Worked Well
- Three-tier content hierarchy made navigation intuitive
- Custom Google My Maps significantly improved site utility for trip planning
- Publishing on Wed/Thu aligned well with peak Thursday traffic
- High-quality hero images correlated with longer session durations

### ⚠️ Challenges
- Low daily active users (1–3/day in final weeks) — needs broader promotion and SEO
- Session duration declined over time — content refresh cadence needs attention
- Limited team bandwidth restricted multimedia depth (no videos or virtual tours)

### 🚀 Future Improvements
- **SEO optimization** — Keyword research and on-page SEO for Washington travel queries
- **Social media integration** — Auto cross-posting to Instagram, Pinterest, and Facebook
- **User-generated content** — Allow travelers to submit experiences and photos
- **Virtual tours** — 360° embedded views for key attractions
- **Email newsletter** — Capture returning visitors with weekly Washington travel tips
- **Expanded multimedia** — YouTube embeds, additional image sliders per post
- **Multilingual support** — Spanish and Mandarin versions for Washington's diverse visitor base

---

## References

- Lonely Planet. n.d. *Lonely Planet*. https://www.lonelyplanet.com/
- Ministry of Tourism, Government of India. n.d. *Incredible India*. https://www.incredibleindia.gov.in/en
- U.S. National Park Service. 2021. *Mount Rainier National Park*. https://cdn.recreation.gov/
- Wikipedia contributors. 2025. *Mount Rainier*. https://en.wikipedia.org/wiki/Mount_Rainier
- Crystal Mountain Resort. 2025. *Mt. Rainier Gondola – Activities*. https://www.crystalmountainresort.com/

---

