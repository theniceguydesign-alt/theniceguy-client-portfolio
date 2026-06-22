# Site Audit: What's Live vs. What's Built

## Audit Date: June 2026
## URL Audited: https://paul-williams-insurance.pages.dev/

---

## PART 1: WHAT'S CURRENTLY LIVE ON CLOUDFLARE

### The Live Site (as of today)

The website at `paul-williams-insurance.pages.dev` is running an **older, incomplete version** of the build. Here is exactly what a visitor sees right now:

#### Navigation Bar
- Logo: "PW." 
- Links: Coverage, About, Quote, Contact
- Phone: **(407) 794-0248**  (old number)
- CTA: "GET A QUOTE" button
- **NO "Intake Form" link**

#### Hero Section
- Headline: "PROTECT WHAT MATTERS MOST"
- Subtext: "Paul Williams Insurance Agency -- serving Mount Dora, FL since 2019. Home, auto, renters, and life insurance. We shop the best rates so you don't have to."
- Phone: **(407) 794-0248**
- **No "Insurance Rebel" branding**

#### Section (01) - Introduction
- Headline: "YOUR LOCAL INSURANCE EXPERTS"
- Generic placeholder text about "trusted insurance partner since 2019"
- Three value propositions: Speed to Lead, Tailored Coverage, Local Expertise
- **NOT Paul's actual "Our Story" content**

#### Section (02) - Coverage Cards
- 6 cards: Auto, Home, Renters, Life, Business, Boat & Recreational
- Cards are present and functional

#### Section (03) - Why Choose
- "14 verified reviews" badge
- "TRUSTED BY MOUNT DORA" headline
- Generic copy about "nearly 100 community recommendations"
- **NOT the 227 Google reviews**
- **NOT the "Insurance Rebel" messaging**

#### Quote Form
- Split-panel design with family image
- Fields: Full Name, Email, Phone, Insurance Type, Message
- Submit button present

#### Footer
- Address: 6551 N Orange Blossom Trl Ste 105, Mount Dora, FL 32757
- Phone: **(407) 794-0248**
- Email: pwilliams3@farmersagent.com
- Hours: **Monday - Saturday 9:00 AM - 6:00 PM** (not "By Appointment Only")
- Copyright: 2025

#### What's MISSING from the live site:
- **/intake** -- Returns **404 Page Not Found**
- **Testimonials section** -- No reviews display at all
- **"Insurance Rebel" branding** -- Nowhere on the site
- **Paul's actual Our Story content** -- Generic placeholder instead
- **Updated phone number** -- Still shows (407) 794-0248
- **Admin dashboard** -- No backend access
- **Intake form navigation link**

---

## PART 2: WHAT'S BUILT AND READY TO DEPLOY

### Feature Comparison: Live vs. Built

| # | Feature | Live Site | Built Version | Impact |
|---|---------|-----------|---------------|--------|
| 1 | **Phone Number** | (407) 794-0248 | **(407) 791-0227** | Correct contact info |
| 2 | **"Insurance Rebel" Branding** | Absent | **Present throughout** | Memorable brand identity |
| 3 | **Our Story Content** | Generic placeholder | **Paul's exact words** | Authentic, personal connection |
| 4 | **Testimonials Section** | Missing | **227 Google reviews, 4.8 stars** | Social proof = conversions |
| 5 | **Intake Form (/intake)** | 404 Not Found | **10-section Acrisure replica** | Complete client data capture |
| 6 | **Intake Form Navigation** | Missing | **In nav bar + mobile menu** | Clients can find the form |
| 7 | **Admin Dashboard (/admin)** | Missing | **3-tab: Overview, Leads, Intakes** | Paul manages his pipeline |
| 8 | **Quote Form Backend** | Unknown | **Connected to MySQL database** | Every lead is stored |
| 9 | **Business Hours** | 9AM-6PM | **By Appointment Only** | Accurate info |
| 10 | **"Trusted By" Headline** | "MOUNT DORA" | **"FLORIDA"** | Statewide positioning |
| 11 | **Review Count** | "14 verified" | **"227+ Google Reviews"** | Actual social proof |
| 12 | **Coverage Descriptions** | Basic | **Expanded (RV, motor home, etc.)** | More lines of business |
| 13 | **Backend Database** | None visible | **MySQL with 4 tables** | Data persistence |
| 14 | **Authentication** | None | **Kimi OAuth + admin roles** | Secure admin access |
| 15 | **Why Choose Content** | Generic | **"That's the Rebel way."** | Brand voice |
| 16 | **Meta Description** | Generic | **SEO-optimized with new branding** | Better search ranking |

---

## PART 3: MAINTENANCE COST BREAKDOWN

### What Paul Needs Help With (He Can't Do Himself)

| Task | Frequency | Time Required | Monthly Cost |
|------|-----------|---------------|--------------|
| **Hosting & Uptime** | Continuous | -- | Included in base |
| **Security Patches** | As needed (1-2x/month) | 30 min each | Included |
| **Database Backups** | Monthly | 15 min | Included |
| **Content Updates** (text changes) | 2x/month | 30 min each | $60/mo |
| **Phone/Email Support** | As needed | -- | $40/mo |
| **Lead Export** (CSV for his CRM) | Weekly | 15 min | $25/mo |
| **Admin Dashboard Training** | Initial + refreshers | 2 hrs initial | $120 one-time |
| **SSL Certificate Renewal** | Annual | 15 min | Included |
| **DNS Management** | As needed | 15 min | Included |
| **Form Submission Alerts** | Setup | 30 min | $15/mo |

---

### Recommended Service Tiers

#### Tier 1: Basic Hosting -- $79/month
**What's included:**
- Website hosting (always online)
- Uptime monitoring
- Monthly database backups
- Security patches
- SSL certificate management
- Quarterly check-in (15 min call)

**What Paul pays extra for:**
- Content updates: $50 each
- Phone support: $40/hr
- Lead exports: $25 each

#### Tier 2: Professional -- $149/month (RECOMMENDED)
**What's included:**
- Everything in Basic
- Up to 2 content updates/month
- Phone/email support (up to 2 hrs/month)
- Weekly lead exports (CSV)
- Monthly analytics report
- Priority response (within 4 hours)

**What Paul pays extra for:**
- Additional content updates: $40 each
- Extra support hours: $50/hr
- New feature development: quoted separately

#### Tier 3: Premium -- $249/month
**What's included:**
- Everything in Professional
- Unlimited content updates
- Up to 5 hrs/month phone/email support
- Weekly analytics + insights call
- SEO monitoring & recommendations
- Priority response (within 1 hour)
- Semi-annual strategy review

---

### One-Time Setup Fees

| Service | Price | Notes |
|---------|-------|-------|
| **Website Build** (already done) | $3,500 - $5,000 | One-time project fee |
| **Domain DNS Setup** | Included | Pointing to new deployment |
| **Admin Account Setup** | Included | Creating Paul's login |
| **Initial Training Session** | $120 | 1-hour walkthrough of dashboard |
| **Email Alert Configuration** | $50 | Notifications for new leads |

---

### Annual Option (Recommended for Paul)

**Professional Annual: $1,490/year** (2 months free)
- Saves $298 vs. monthly
- Includes everything in Professional tier
- One invoice per year
- Lock in the rate for 12 months

---

## PART 4: WHAT PAUL CAN'T DO HIMSELF

These are the tasks that **require technical expertise** and are the reason ongoing maintenance has a cost:

| # | Task | Why Paul Can't Do It | What Happens If Neglected |
|---|------|---------------------|---------------------------|
| 1 | **Database Management** | No SQL knowledge | Lost leads, data corruption |
| 2 | **Security Patches** | Doesn't know what to patch | Site hacked, client data exposed |
| 3 | **SSL Renewal** | Doesn't know what SSL is | Site shows "Not Secure" warning |
| 4 | **DNS Changes** | Doesn't know what DNS is | Site goes offline |
| 5 | **Backend API Changes** | No programming knowledge | Can't fix broken forms |
| 6 | **Code Updates** | No coding experience | Site breaks, features stop working |
| 7 | **Database Backups** | Doesn't know how to export | If server fails, all leads are gone |
| 8 | **Form Debugging** | Can't read error logs | Intake forms stop submitting |
| 9 | **Auth/User Management** | Doesn't understand OAuth | Can't add/remove admin users |
| 10 | **Deployment/Updates** | Doesn't know how to deploy | Stuck with current version forever |

---

## PART 5: SUMMARY FOR PAUL

### What He's Getting

A **complete digital command center** that does four things his current site cannot:

1. **Captures Leads** -- Every quote request is stored in a database, not lost in an email
2. **Collects Intake Data** -- Clients fill out comprehensive Acrisure forms online
3. **Tracks Pipeline** -- Admin dashboard shows new > contacted > quoted > bound
4. **Builds Trust** -- 227 reviews, "Insurance Rebel" branding, professional presence

### What It Costs

| Item | Price |
|------|-------|
| **One-Time Build** | $4,000 |
| **Monthly Hosting & Support** (Professional) | $149/month |
| **Annual** (2 months free) | $1,490/year |

### What You Do for Him Monthly

- Keep the site online and secure
- Back up his leads and intake data
- Help him update content when needed
- Answer his questions about the dashboard
- Export leads for his call list
- Make sure forms keep working
- Handle all technical issues

**He focuses on selling insurance. You focus on the technology.**
