# OSN Website and App Policies

Customized versions of the General Legal templates for Operational & Strategic Networks Inc. (OSN). They cover osnplatform.com, sabre.osnplatform.com, SABRE, and OSN's digital JAWS wargame.

| Document | Publish at | Based on |
|----------|-----------|----------|
| [Terms of Use](terms-of-use.md) | osnplatform.com/terms | [templates/terms-of-use](../templates/terms-of-use/) + OSN's Terms of Service draft |
| [Privacy Policy](privacy-policy.md) | osnplatform.com/privacy | [templates/privacy-policy-us](../templates/privacy-policy-us/) + OSN's Privacy Policy draft |
| [Cookie Notice](cookie-notice.md) | osnplatform.com/cookies | [templates/cookie-notice](../templates/cookie-notice/) |
| [Subprocessors](subprocessors.md) | osnplatform.com/subprocessors | OSN Legal & Compliance doc, item 8 |
| [Accessibility Statement](accessibility.md) | osnplatform.com/accessibility | OSN Legal & Compliance doc, item 9 |

These are drafts. Have counsel review them before publishing. Highlighted text (`<mark>` tags) still needs a decision or a fact.

## Facts used

| Fact | Value | Source |
|------|-------|--------|
| Legal name | Operational & Strategic Networks Inc. | DE Certificate of Incorporation |
| Entity | Delaware corporation, incorporated April 8, 2026 | DE Certificate of Incorporation |
| Notice address | 119 Berkeley Pl., Brooklyn, NY 11217 | Company Info; incorporator address; OSN Legal & Compliance drafts |
| Contact | leo@osnplatform.com | Founder instruction; one-pagers |
| Governing law | Delaware; courts in New Castle County | OSN Terms draft; SABRE Pilot Agreement |
| Arbitration | AAA, individual only, video hearings, 30-day opt-out, not for government users | OSN Terms draft |
| Liability cap | Greater of $100 or fees paid in the prior 12 months | OSN Terms draft |
| Minimum age | 13; under 18 only through an Organization with any required consent | OSN Terms and Privacy drafts |
| Hosting | AWS us-east-2 (Ohio): EC2, Postgres and Redis on EBS, S3 backups, CloudFront for map tiles | SABRE AWS Production Stack |
| Network | Cloudflare DNS, CDN, and Tunnel; Cloudflare terminates TLS | SABRE AWS Production Stack |
| Sign-in | Secure JWT cookie; CloudFront signed cookies for `.osnplatform.com` minted at login | SABRE AWS Production Stack |
| AI | External LLM API called from the `llm-worker` service; provider not documented | SABRE AWS Production Stack |
| Map data | Esri World Imagery, OpenFreeMap, OpenStreetMap, Copernicus DEM, Sentinel-2 land cover | SABRE Architecture doc |
| Uploads | Custom maps (GeoTIFF, Shapefile, GeoJSON, images) and `.sabre` scenario packages | SABRE Architecture doc; Package Encryption doc |
| Contact form | Name, email, topic (JAWS inquiry, JAWS application, press, SABRE waitlist, other), message | osnplatform.com/contact |
| Data promises | No sale, no ads, model training with Organization opt-out, nothing that identifies a unit, location, capability, or readiness level, no CUI | OSN drafts; Pilot Agreement; customer one-pager |
| JAWS | Rules and doctrine originated by the University of Michigan's cadet-led Joint Advanced Wargame Staff; OSN built the digital platform | Research Deployment draft; customer one-pager |

## Decisions the founders need to make

These are real conflicts between OSN's own documents. The policies will be wrong until they are settled.

1. **Which address is OSN's headquarters?** Three are in use. Brooklyn is on the certificate of incorporation and in these policies. Chesterfield, MI is listed as the headquarters on the Michigan foreign qualification. osnplatform.com says Ann Arbor, MI. If Brooklyn is the principal office, ask counsel whether OSN must register to do business in New York. Michigan requires an amended filing within 30 days of a change to that form's information.
2. **What can OSN do with de-identified data?** Four documents say four different things:
    - OSN Terms draft: only to operate and improve the Service.
    - These policies: improve the Service, train models, publish aggregate research, share with research partners, never sell.
    - Research Deployment draft: may share with research bodies; may not sell for commercial purposes.
    - SABRE Pilot Agreement: may "commercially exploit" it for any lawful purpose.

    Pick one rule. Then fix the Pilot Agreement or the policies to match.
3. **How strong is the anonymization promise?** The customer one-pager says player data is anonymized before any use beyond live session analytics. These policies say names are removed "where practical" before model training. Marketing that promises more than the policy is an FTC risk. Make them match. A flag sits in the Privacy Policy.
4. **Model-training opt-out.** The policies promise Organizations can opt out of model training. The Pilot Agreement has no opt-out. Add a checkbox to Schedule 1, or drop the promise.
5. **Deletion timing.** The policies promise deletion within 90 days after a subscription ends. The Pilot Agreement deletes within 60 days, only on written request. Both work only if OSN can actually do it. Pick a schedule you can meet.
6. **Who owns training data?** The Pilot Agreement and these Terms say the customer owns it. The Research Deployment draft says OSN owns it. The draft also names "Operational & Strategic Networks, LLC," which no longer exists. Update it before reuse.
7. **Minimum age.** Your drafts use 13. SABRE's users are college cadets and officers. If no one under 17 will use it, a higher floor lowers your obligations.

## Still to fill in

1. Effective date (all five documents)
2. AI model provider: name, location, and confirmation its terms bar training on OSN data
3. Contact form processor and any payment processor (Subprocessors page)
4. Analytics provider for the Cookie Notice, or delete that row
5. Whether EBS volumes and S3 backups are encrypted at rest. The Privacy Policy only claims it once you confirm.
6. Which map layers load directly from Esri or OpenFreeMap in the browser
7. Backup purge period; confirm the 90-day and 12-month periods are achievable
8. Accessibility reply time

## Items for counsel

1. **Export controls.** Whether any SABRE content falls under ITAR or EAR, and whether foreign nationals may use it.
2. **Arbitration.** Enforceability of AAA arbitration and the class waiver, including for users under 18.
3. **Automated decisions.** Whether the profiling statement fits how Organizations use SABRE scores.
4. **Map licenses.** Esri World Imagery has its own terms of use, which may limit commercial use without an Esri account. OpenStreetMap's license requires visible attribution in the map. Confirm Google Maps is fully removed, since Google's terms bar mixing its maps with others.
5. **IP ownership.** The Terms say OSN owns SABRE. Confirm the chain of title: founder and contributor invention assignments, the v1 rules built with volunteer cadets, any claim from the University of Michigan through Build & Launch or Fuel funding, and any invention agreement from a founder's outside employer.
6. **JAWS.** Written permission to use the JAWS name and rules.
7. **Trademark.** Sabre Corporation holds SABRE marks for software. Clear the name before building the brand further.
8. **New York SHIELD Act.** As a New York business, OSN needs a written security program that matches the Privacy Policy.

## Changes from OSN's Drive drafts

- Kept the substance of the OSN Privacy Policy and Terms of Service drafts in the OSN Legal & Compliance doc, including AAA arbitration. One exception: the de-identified data rule is broader than your draft to match the Pilot and Research agreements. See decision 2.
- Rebuilt them on the attorney-drafted General Legal templates for fuller coverage: informal dispute step, batch claims, state privacy notices, and the CCPA disclosure table.
- Added what the company's real setup requires: JAWS attribution, third-party map data, uploads and shared scenarios, AI credits, map access cookies, subprocessors, and accessibility.

## Publishing checklist

- [ ] Settle the decisions above and fill every highlighted field
- [ ] Counsel review
- [ ] Post all five pages and link them in the osnplatform.com footer. The footer has no policy links today.
- [ ] Add Terms and Privacy links and a clickwrap checkbox to the SABRE sign-in screen. It has neither today. Log who accepted which version and when.
- [ ] Add a Privacy Policy link next to the contact form
- [ ] Show OpenStreetMap and Esri attribution on the SABRE map
- [ ] Keep old versions on file and email users before material changes take effect
