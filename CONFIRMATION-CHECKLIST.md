# Information to Confirm Before Launch

The Evercrest website does not display any detail that hasn't been verified. Each item below appears on the site as a dashed "… to be confirmed" label, or is left out entirely, until the practice confirms it.

Once an item is confirmed, enter it in the file listed and the site updates everywhere it is used. Most items go in `src/config/site.ts`.

## 1. Location and contact

| Confirm | Where it appears | Set in |
| --- | --- | --- |
| [ ] Street address (and suite or unit, if any) | Contact page, footer, search data | `siteConfig.location.streetAddress`, `addressLine2` |
| [ ] City | Contact page, footer, search data, page titles | `siteConfig.location.city` |
| [ ] ZIP code | Contact page, footer, search data | `siteConfig.location.postalCode` |
| [ ] Map embed link (once the address is confirmed) | Contact page | `siteConfig.location.mapEmbedUrl` |
| [ ] Directions link (e.g. Google Maps) | Contact page, footer | `siteConfig.location.mapLink` |
| [ ] Telephone number | Contact page, footer, appointment banner, policies | `siteConfig.contact.phone`, `phoneHref` |
| [ ] Email address | Contact page, footer, Privacy Policy, Accessibility page | `siteConfig.contact.email` |
| [ ] Fax number (optional) | Not shown yet | `siteConfig.contact.fax` |

## 2. Office hours

| Confirm | Set in |
| --- | --- |
| [ ] Hours for each day, Monday to Sunday (including "Closed" days) | `siteConfig.officeHours` |
| [ ] Holiday closures or other notes (optional) | `siteConfig.officeHoursNote` |

## 3. Dentist

| Confirm | Set in |
| --- | --- |
| [ ] Full name | `siteConfig.dentist.name` |
| [ ] Degree (DDS or DMD) | `siteConfig.dentist.degree` |
| [ ] Title or role (e.g. "General Dentist") | `siteConfig.dentist.title` |
| [ ] Biography | `siteConfig.dentist.biography` |
| [ ] Education | `siteConfig.dentist.education` |
| [ ] License(s) | `siteConfig.dentist.licensure` |
| [ ] Professional memberships | `siteConfig.dentist.professionalMemberships` |
| [ ] Portrait photo | `siteConfig.dentist.photo` (put the file in `public/images/`) |

## 4. Services

The site lists eight **proposed** services. Confirm which ones the practice offers, and whether any are missing.

- [ ] Preventive Dentistry
- [ ] Dental Examinations and Cleanings
- [ ] Restorative Dentistry
- [ ] Cosmetic Dentistry
- [ ] Tooth-Colored Fillings
- [ ] Crowns and Bridges
- [ ] Gum Health
- [ ] Oral Health Education
- [ ] Any additional services to add

Edit in `src/config/services.ts`. Ask the dentist to review the service descriptions for clinical accuracy.

## 5. Insurance, payment, and policies

| Confirm | Set in |
| --- | --- |
| [ ] Accepted / in-network insurance plans | `siteConfig.insurance.acceptedPlans` |
| [ ] Accepted payment methods | `siteConfig.insurance.paymentMethods` |
| [ ] Financing or payment plans, if offered | `siteConfig.insurance.financingNote` |
| [ ] Cancellation and rescheduling policy | `siteConfig.policies.cancellation` |
| [ ] Late arrival policy | `siteConfig.policies.lateArrival` |

## 6. Online appointment requests and forms (Dentrix Ascend)

| Confirm | Set in |
| --- | --- |
| [ ] Where appointment requests should be delivered: a webhook, or an email address through Resend | Environment variables (see `.env.example`) |
| [ ] That the delivery service is suitable for patient information (for example, it will sign a HIPAA Business Associate Agreement) | Practice / compliance review |
| [ ] Dentrix Ascend online scheduling link, if the practice uses it | `siteConfig.practiceManagement.onlineSchedulingUrl` |
| [ ] Dentrix Ascend online patient forms link, if the practice uses it | `siteConfig.practiceManagement.patientFormsUrl` |

Until delivery is set up, the appointment form says online requests are coming soon, and it sends nothing.

## 7. Photography

- [ ] Review each photo in `src/config/images.ts`: check that it loads, suits the page, and that its alt text describes it accurately
- [ ] Preferably, replace them with the practice's own photos (reception, treatment rooms, team)
- [ ] Get written permission from any staff or patients who appear in practice photos

## 8. Legal and compliance

- [ ] Privacy Policy: legal review, plus an effective date (`src/app/privacy-policy/page.tsx`)
- [ ] Notice of Privacy Practices: available from the practice (the Privacy Policy refers to it)
- [ ] Accessibility statement: approval of its wording (`src/app/accessibility/page.tsx`)
- [ ] Copyright start year, if wanted (`siteConfig.copyrightStartYear`)

## 9. Website and listings

| Confirm | Set in |
| --- | --- |
| [ ] Website domain (e.g. `https://www.example.com`) | `siteConfig.url` |
| [ ] Social media accounts, if any | `siteConfig.social` |
| [ ] Google Business Profile and other listings, once the address is confirmed | Outside the website |
