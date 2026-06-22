# Paul Williams Insurance Website — Pricing & Deployment Guide

## 1. RECOMMENDED SERVICE PRICING (What to Charge Paul)

Below is a fair, professional pricing structure for a fullstack website with hosting, maintenance, and ongoing support. These rates reflect the actual value of the infrastructure and ongoing labor.

---

### ONE-TIME SETUP FEE

| Item | Price | Notes |
|------|-------|-------|
| **Complete Website Build** | $3,500 - $5,000 | Full design + development + backend + forms + dashboard |
| **Domain DNS Setup** | Included | Pointing domain to new deployment |
| **Admin Account Setup** | Included | Creating Paul's login credentials |
| **Initial Content Load** | Included | All copy, forms, images, reviews |

**Recommended one-time fee for Paul: $4,000**

(Agencies charge $16,500-$36,500 for this level of work. You are delivering massive value at a fraction.)

---

### MONTHLY HOSTING & MAINTENANCE

| Tier | Monthly Price | What's Included |
|------|--------------|-----------------|
| **Basic** | $79/month | Hosting, uptime monitoring, monthly backups, security patches |
| **Professional** | $149/month | Everything in Basic + content updates (up to 2/month), phone/email support, lead export |
| **Premium** | $249/month | Everything in Professional + priority support, weekly analytics reports, SEO monitoring, unlimited content updates |

**Recommended for Paul: Professional Tier at $149/month**

This tier is appropriate because:
- He'll need help updating content as he rebuilds his book
- He needs support learning the admin dashboard
- Lead exports for his CRM/call list
- Phone/email support when he has questions

---

### OPTIONAL ADD-ONS

| Service | Price | Notes |
|---------|-------|-------|
| Email Notification on New Leads | $25/month | SMS + email alerts when intake forms are submitted |
| Custom Domain Email (@paulwilliamsagency.com) | $15/month | Professional email through the platform |
| Additional Coverage Pages | $200/page | If he wants dedicated pages for Boat, RV, Commercial, etc. |
| CRM Integration (Salesforce/HubSpot) | $500 setup + $50/month | Auto-sync leads to his CRM |
| Review Widget Auto-Update | $30/month | Pulls latest Google reviews automatically |

---

### ANNUAL DISCOUNT

Offer Paul: **2 months free** if he pays annually
- Professional annual: $1,490/year (saves $298)

---

## 2. STEP-BY-STEP CLOUDFLARE DEPLOYMENT GUIDE

Follow these steps in order to get Paul's site live on his Cloudflare domain.

---

### STEP 1: Publish the Website (Get the Live URL)

```
1. Open the project in the platform
2. Click "Deploy" or "Publish"
3. Copy the deployment URL (it will look like: https://paul-williams-abc123.platform.app)
4. This is your LIVE URL — save it
```

**Result:** You now have a live website at a temporary platform URL.

---

### STEP 2: Log Into Cloudflare

```
1. Go to https://dash.cloudflare.com
2. Log in with the credentials Paul gave you (or your own if you manage his account)
3. Select the domain: paul-williams-insurance.pages.dev
```

---

### STEP 3: Configure DNS to Point to the New Site

In Cloudflare Dashboard:

```
1. Click on the domain "paul-williams-insurance.pages.dev"
2. Go to the "DNS" tab on the left sidebar
3. Look for existing A records or CNAME records
4. Delete any existing A records pointing to the old site
5. Add a NEW CNAME record:
   
   Type: CNAME
   Name: @  (this means the root domain)
   Target: [paste your deployment URL from Step 1, WITHOUT https://]
   TTL: Auto
   Proxy Status: Click the orange cloud to turn it OFF (gray cloud) 
                 — you can turn it back ON after confirming it works

6. Add a NEW CNAME record:
   
   Type: CNAME
   Name: www
   Target: [paste your deployment URL from Step 1, WITHOUT https://]
   TTL: Auto
   Proxy Status: OFF (gray cloud)

7. Click "Save"
```

**Result:** The domain now points to your new website.

---

### STEP 4: Wait for DNS Propagation

```
DNS changes can take anywhere from:
- A few minutes (if proxy is off)
- Up to 24-48 hours (worst case, rare)

You can check if it's working by:
1. Opening an incognito/private browser window
2. Going to https://paul-williams-insurance.pages.dev
3. If you see YOUR new site (not the old one), DNS has propagated
```

---

### STEP 5: Enable Cloudflare Proxy (Recommended)

Once you've confirmed the site loads correctly:

```
1. Back in Cloudflare DNS tab
2. Find your CNAME records
3. Click the gray cloud next to each record to turn it ORANGE
4. This enables Cloudflare's CDN, SSL, DDoS protection, and speed optimization
5. Wait 2-3 minutes
6. Test the site again — it should load with HTTPS (padlock in browser)
```

**Result:** Site is live with Cloudflare protection + SSL + CDN.

---

### STEP 6: Force HTTPS (SSL)

```
1. In Cloudflare, go to "SSL/TLS" tab
2. Set SSL/TLS encryption mode to "Full (strict)"
3. Scroll down to "Always Use HTTPS"
4. Toggle it ON
5. This ensures all visitors are redirected to HTTPS automatically
```

---

### STEP 7: Set Up Paul's Admin Access

```
1. Go to: https://paul-williams-insurance.pages.dev/login
2. You'll be redirected to Kimi OAuth login
3. Log in with YOUR credentials first (to test it works)
4. You should be redirected to /admin
5. You should see the dashboard with stats cards and tables

TO GIVE PAUL ACCESS:
1. Paul needs to visit: https://paul-williams-insurance.pages.dev/login
2. He logs in with his own Kimi account
3. After first login, his account is created in the database
4. You (or someone with admin access) need to set his role to "admin" in the database
5. Run this SQL command in the database:
   
   UPDATE users SET role = 'admin' WHERE email = 'paul@hiscurrentemail.com';
```

**Result:** Paul can log in and see his admin dashboard.

---

### STEP 8: Test Everything

```
1. Visit https://paul-williams-insurance.pages.dev/ 
   - Confirm the landing page loads with all sections
   
2. Click "Intake Form" in navigation
   - Visit: https://paul-williams-insurance.pages.dev/intake
   - Walk through all 10 sections
   - Submit a test form
   
3. Visit https://paul-williams-insurance.pages.dev/admin
   - Log in
   - Confirm the test submission appears in the Intake Forms tab
   
4. Go back to the homepage
   - Fill out the quote form
   - Confirm it appears in the Quote Leads tab
```

---

## 3. COMMON ISSUES & SOLUTIONS

| Problem | Solution |
|---------|----------|
| Site shows old content | Clear browser cache (Ctrl+Shift+R) or wait 10 minutes for DNS |
| DNS not working | Check CNAME target is correct, no typos in the URL |
| HTTPS not working | In Cloudflare SSL/TLS tab, set mode to "Full (strict)" |
| Admin page won't load | Make sure you're going to /admin after logging in |
| Intake form submissions not showing | Check browser console for errors, verify tRPC connection |
| Images not loading | Make sure image assets are in the public/ folder and deployed |

---

## 4. HANDOFF CHECKLIST FOR PAUL

When you give Paul access, make sure he knows:

- [ ] His website URL: https://paul-williams-insurance.pages.dev/
- [ ] His login URL: https://paul-williams-insurance.pages.dev/login
- [ ] His admin dashboard: https://paul-williams-insurance.pages.dev/admin
- [ ] How to view new leads (Quote Leads tab)
- [ ] How to view intake submissions (Intake Forms tab)
- [ ] How to update a lead's status (dropdown in the table)
- [ ] How to add internal notes (click a submission, type in notes field)
- [ ] Your contact info for support
- [ ] His monthly service fee and what it covers

---

## 5. SUMMARY OF CHARGES FOR PAUL

| Item | Amount |
|------|--------|
| **One-Time Build Fee** | **$4,000** |
| **Monthly Hosting & Support** (Professional) | **$149/month** |
| **Annual option** (2 months free) | **$1,490/year** |

**What Paul gets for $149/month:**
- Website hosting (always online)
- Security patches and updates
- Monthly database backups
- Phone/email support when he has questions
- Up to 2 content updates per month (text changes, new info, etc.)
- Lead export assistance
- Peace of mind — you handle the technical stuff

---

**Version: June 2026**
**Prepared for: Asim — Paul's tech partner**
