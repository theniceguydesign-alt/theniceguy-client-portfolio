# Intake Form Replacement — Completion Report

## Summary

The generic 6-step intake form was completely replaced with a precise digital replica of Paul's two Acrisure Personal Lines Placement Intake Forms. Every section, field, and label from the original PDFs is now represented in the digital form.

---

## Source Forms Replaced

### Form 1: Placement Intake Form (Fillable) — Internal
- 4 pages, 6 sections (Acrisure NAI PL)
- Internal submission info, client info, homeowners/property (with sub-sections 3D-3K), automobile (4A-4E), umbrella, watercraft

### Form 2: Personal Lines Placement Intake Form — eff. 06-15-26
- 10 pages, 10 sections (Acrisure Placement Underwriting Intake)
- Routing & Client, Billing & Notes, Property Underwriting, Liability/Scheduled/UW Triggers, Auto Drivers, Auto Vehicles, Auto Coverage, Boat/Watercraft, Motorcycle/ATV/RV, Scheduled Jewelry + Umbrella + Attestation

---

## New Digital Form — 10 Sections (matches Form 2 exactly)

### Section 1: Routing & Client
| Field | Type | Notes |
|-------|------|-------|
| Lines Included | Multi-checkbox | Homeowners, Auto, Umbrella, Boat/Watercraft, Motorcycle/ATV, RV/Motorhome, Scheduled Property, Renters |
| Primary Named Insured(s) | Text | Required |
| DOB(s) | Text | |
| Email | Email | Required |
| Phone | Tel | Required |
| Primary Address | Text | |
| Risk State | Select | FL, GA, AL, SC, Other |
| Risk Address (if different) | Text | |
| Occupation(s) | Text | |
| Prior Address (if moved in last 5 years) | Text | |
| Group Discount | Text | |

### Section 2: Billing and Notes
| Field | Type | Notes |
|-------|------|-------|
| Mortgagee Clause | Text | Lender name & address |
| Loan Number | Text | |
| Escrow Bill? | Select | Yes/No — conditional payment method field |
| Payment Method / Pay Plan | Text | Conditional on "No Escrow" |
| Lienholder/Billing Info | Text | Vehicle # and lienholder |
| Placement Notes | Textarea | |
| Additional Notes / UW Concerns | Textarea | |
| Home Losses (Past 5 Years) | Textarea | |
| Auto Losses (Past 5 Years) | Textarea | |

### Section 3: Property (Underwriting)
**Property Basics:** Prior Carrier, Exp. Date, Tenure, Property Type, Families, Year Purchased, Year Built, Stories, Sq Ft, Miles to Fire Dept, Hydrant Feet, Exterior Construction

**Roof:** Roof Material, Roof Type, Roof Update Year, conditional "Other" description

**Basement & Garage:** Basement Type, Garage Type, Finished Percentage, Garage Stalls, Detached Structure over 1,000 sq ft

**Update Years:** Electrical, Plumbing, Heating, Cooling, Water Heater, Generator/Solar

**Bathroom and Kitchen:** Bathroom Count and Type, Kitchen Grade, Bedroom Count, Flooring type/percentage, Deck/Porch

### Section 4: Liability, Scheduled Items & UW Triggers
**Liability Triggers:** Pool/Sauna/Hot Tub, Trampoline, Animals (with conditional breed/bite history for dogs), Wood Burning Stove/Fireplace, Land Size

**Security/Water:** Central Burglary/Fire Alarm, Whole Home Generator, Auto Water Shut Off Valve, Jewelry Scheduled Needed (conditional valuable articles fields)

**Valuable Articles (conditional):** Total Scheduled Value, Appraisals Status

### Section 5: Automobile — Drivers
**Auto Overview:** Prior Carrier, Expiration, Tenure, Good Student Discount checkbox, Student Away at School

**Drivers 1-4 (repeatable blocks):** Full Name, DOB, DL State, DL Number, Marital Status, Good Student, Accidents/Tickets/Violations

### Section 6: Automobile — Vehicles
**Vehicles 1-4 (repeatable blocks):** Year, Make, Model, VIN, Title, Usage, Garaging ZIP, Lienholder

**Vehicle Notes** textarea

### Section 7: Automobile — Coverage Requested
**Coverage by Vehicle (1-3):** Comprehensive Deductible, Collision Deductible, Deductible Type (Glass, Towing, Rental), Additional Coverages (OEM, Special Equip)

**Liability Limits:** Bodily Injury, Un/Underinsured, PIP Limit, Medical Payments

### Section 8: Boat / Watercraft
**Watercraft 1-3:** Year, Make, Model, Hull #, Approx Value, Length

Storage Location, Motor/Trailer/HP/Top Speed Notes, Special Equipment

### Section 9: Motorcycle / ATV & RV
**Motorcycle/ATV 1-3:** Year, Make, Model, VIN

**Camper/Motorhome:** Year, Make, Model, VIN, Length, Towed or Driven, Number of Slide Outs

### Section 10: Scheduled Jewelry / Valuable Articles Detail + Umbrella + Attestation
**Scheduled Items 1-6 (conditional on jewelry scheduled):** Description, Value, Appraisal Date

**Umbrella:** Eligible select, Desired Limit (1M-5M)

**Attestation:** "I confirm the above information is complete and accurate" + Completed By (Name) + Date

---

## Files Modified

| File | Action |
|------|--------|
| `src/pages/IntakeForm.tsx` | **Complete rewrite** — replaced generic 6-step form with exact replica of Acrisure 10-section form |

---

## Key Improvements Over Previous Version

1. **Exact field matching** — Every field from both PDFs is now present
2. **Proper section numbering** — Sections 1-10 match the Acrisure form exactly
3. **Section labels in nav** — "Client", "Billing & Notes", "Property", "Liability & Items", "Auto Drivers", "Auto Vehicles", "Auto Coverage", "Watercraft", "Motorcycle/ATV/RV", "Scheduled Items"
4. **Conditional fields** — Escrow payment method, animal details, jewelry scheduling, umbrella all show/hide based on selections
5. **Repeatable blocks** — Multiple drivers (4), vehicles (4), watercraft (3), motorcycles (3), scheduled items (6)
6. **Attestation** — Legal confirmation with signature name and date on final step
7. **Acrisure branding** — "Personal Lines Placement Intake Form" header

---

## Deployment

- **Version ID:** `30462dc`
- **Status:** Successfully deployed
- **Route:** `/intake`
