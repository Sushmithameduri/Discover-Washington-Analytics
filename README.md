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
- [Key Metrics Summary](#key-metrics-summary)
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

<img width="591" height="630" alt="image" src="https://github.com/user-attachments/assets/450543dc-8198-4f3e-bbcf-d8923ed7ca88" />


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

The site used Google Analytics 4 (GA4) with a custom Google Looker Studio dashboard to track performance against five defined goals.

### KPI Framework

| # | Goal | KPI | Metric |
|---|---|---|---|
| 1 | Maximize Student Participation | Daily Active Students | Active Users |
| 2 | Improve Resource Engagement | Views per Session | Views per Session |
| 3 | Track Content Effectiveness | Average Session Duration | Average Session Duration |
| 4 | Ensure Consistent Access | Returning Visitor Rate | % Returning Users |
| 5 | Validate Navigation Clarity | Bounce Rate | Bounce Rate |

### Looker Studio Dashboard

The Google Looker Studio report included four panels:

1. **Top Viewed Guides** — Page-level view counts to identify most popular content
2. **User Engagement Chart** — Time-series of average session duration vs. views per session
3. **New vs. Returning Users Pie Chart** — Audience retention overview
4. **Daily Active Visitors Line Chart** — Day-over-day traffic trends (March 12–18, 2025)

> 📊 Dashboard : <img width="905" height="679" alt="image" src="https://github.com/user-attachments/assets/b9175f6d-9153-4258-b71c-f9ba1b6afbc8" />

### Key Metrics (Phase 3 Reporting Period)

| Metric | Value |
|---|---|
| Total Page Views | 958 |
| Most Viewed Page | Discover Washington Homepage (384 views) |
| Average Time on Site | 8 min 59 sec |
| Bounce Rate | 38% |
| Daily Active Users (recent week) | ~5 |
| New vs. Returning Split | 33.3% / 33.3% / 33.3% |
| Peak Views per Session | 8.32 (March 10, 2025) |
| Active User Growth | +82.4% |
| New User Growth | +66.7% |
| Event Count Growth | +26.5% (946 events) |

### Traffic Patterns

- **Peak day:** Thursday (13 users), followed by Sunday (11) and Saturday (10)
- **Lowest traffic:** Tuesday (1 user)
- **Browser breakdown:** Chrome ~80%, Edge and Safari minimal
- **Publishing strategy:** Content published Wed/Thu to index before peak weekend traffic

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

*Built with ❤️ by Team 4 — IS5320 Web Analytics Course*
