# Malaysian e-Invoice — Consultant Knowledge Base

**Prepared for:** YYC taxPOD e-Invoice advisory team
**Compiled:** 28 October 2026, from the HASiL source library in this folder
**Status:** Internal working reference, not an HASiL ruling. Before advising, always re-check the latest PDF in the library.

> **How to use this file.** Each rule carries a short citation in square brackets, e.g. **[GL 1.6.10]**. The source register in Section 0 maps each code to its PDF. If a client's transaction date falls before the current version took effect, check the version history in Section 2.5 first.

---

## 0. Source register (latest versions)

| Code | Document | Version / date | File |
|---|---|---|---|
| **GL** | IRBM e-Invoice Guideline | **v4.8, 30 Aug 2026** (replaces v4.7, 7 Jul 2026) | `Guidelines/irbm-e-invoice-guideline (30 August 2026).pdf` |
| **SGL** | IRBM e-Invoice Specific Guideline | **v4.9, 7 Sep 2026** (replaces v4.8, 7 Jul 2026) | `Guidelines/irbm-e-invoice-specific-guideline (7 September 2026).pdf` |
| **GFAQ** | HASiL General FAQ | **4 Sep 2026** | `General FAQ/lhdnm-e-invoice-general-faqs_4sep2026.pdf` |
| **AVI** | Aviation FAQ | 26 Aug 2026 | `Industry Specific FAQ/lhdnm_aviation-faqs (26-8-26).pdf` |
| **CON** | Construction FAQ | 6 Jan 2026 | `Industry Specific FAQ/lhdnm_construction-industry_specific-faqs (6jan2026).pdf` |
| **HC** | Healthcare FAQ | 14 Jun 2024 | `Industry Specific FAQ/lhdnm_healthcare_faqs.pdf` |
| **ECOM** | e-Commerce FAQ | 22 Dec 2023 | `Industry Specific FAQ/lhdnm_industry-specific-faqs_e-commerce_microsite_bi.pdf` |
| **PET** | Petroleum Operations FAQ | 18 Jan 2024 | `Industry Specific FAQ/lhdnm_industry-specific-faqs_petroleum-operations_bi_v2.pdf` |
| **TEL** | Telecommunication FAQ | 22 Dec 2023 | `Industry Specific FAQ/lhdnm_industry-specific-faqs_telecommunication_microsite_bi.pdf` |
| **TOUR** | Tourism FAQ | 14 Jun 2024 | `Industry Specific FAQ/lhdnm_tourism_faqs.pdf` |
| **DON** | Donations or Contributions FAQ | 7 Jul 2025 | `Industry Specific FAQ/specific-faq-donations-or-contributions (7jul2025).pdf` |
| **FIN** | Financial Services, Pawnbroking, Stockbroking, Unit Trust and Money Changing FAQ | **26 Aug 2026** | `Industry Specific FAQ/specific-faq-financial-services-stockbroking-and-unit-trust (26 aug 2026).pdf` |
| **INS** | Insurance and Takaful FAQ | 28 Jan 2025 | `Industry Specific FAQ/specific-faq-insurance-and-takaful (28jan2025).pdf` |
| **PORTAL** | MyInvois Portal FAQ | 9 Mar 2026 | `MyInvois FAQ/myinvois-portal-faqs(9march2026).pdf` |
| **EPOS** | Soalan Lazim MyInvois e-POS (BM) | 9 Jan 2026 | `ePOS/soalan-lazim-myinvois-e-pos (9 jan 2026).pdf` |
| **EPOS-EN** | MyInvois e-POS System FAQ (EN, pilot) | 30 Apr 2025, *superseded on eligibility* | `ePOS/myinvois-e-pos-system-faqs (30 apr 2025).pdf` |

**Not in the library** (cite from the law itself, and verify the wording before quoting): the text of the Income Tax (Issuance of Electronic Invoice) Rules 2024 [P.U.(A) 265/2024], s.82C ITA 1967, the e-Invoice SDK (data catalogue, classification codes, MSIC list, code lists) at https://sdk.myinvois.hasil.gov.my/, and the Service Tax Regulations.

### ⚠ Currency alerts: positions that changed in 2025–2026

1. **There are now 4 phases, not 5.** Since GL v4.6 (7 Dec 2025), "up to RM5 million" is one phase, mandatory from **1 Jan 2026**. The former Phase 5 (up to RM1m, 1 Jul 2026) is gone. **[GL 1.5]**
2. **The exemption threshold is now below RM3 million.** It was below RM500k up to GL v4.5, below RM1m in GL v4.6–v4.7, and became **below RM3m in GL v4.8 (30 Aug 2026)** following the Prime Minister's announcement. It also now carries **anti-avoidance criteria** (non-individual shareholder / holding company / related company or JV with turnover ≥ RM3m). **[GL 1.6.1(e), 1.6.10; GFAQ Q15–20, Q98–104]**
3. **New businesses:** the threshold is now **RM3m**. It was RM500k in v4.4 and RM1m in v4.6–4.7. **[GL 1.5]**
4. **Interim relaxation for the "up to RM5m" phase runs until 31 Dec 2027.** This covers both the 1 Jan 2026 and the 1 Jul 2026 implementation dates. **[SGL 16.1 Table 16.1; GFAQ Q113]**
5. **The e-Invoice Special Voluntary Disclosure Programme (SVDP) runs 7 Jul 2026 – 31 Dec 2027**, using e-Invoice versions "SVDP 1.2" / "SVDP 1.3". **[SGL 17; GFAQ Q123–133]**
6. **No-consolidation list expanded from 1 Jan 2026:** any single transaction **> RM10,000**, electricity service providers, and telco postpaid plans, internet subscriptions and sale of electronic devices. **[SGL 3.7.2 Table 3.6]**
7. **Statutory bodies, statutory authorities, local authorities and international organisations** must e-Invoice goods sold and services performed **from 1 Jul 2025**. **[GL 1.6.1(c)–(d), 1.6.9; GFAQ Q8]**
8. **MyInvois e-POS eligibility has widened.** It was below RM250k in the Apr 2025 pilot, below RM1m (7 Dec 2025), below RM2m (12 Dec 2025), and is now **up to RM5m (9 Jan 2026)**. **[EPOS Q2]**

---

## 1. Legal basis, responsibility and penalties

- The GL and SGL are issued under **s.134A ITA 1967**. **[GL cover; SGL cover]**
- **Income Tax (Issuance of Electronic Invoice) Rules 2024 [P.U.(A) 265/2024]** was gazetted on 30 Sep 2024 and took effect **1 Oct 2024**. For the > RM100m phase, 1 Oct 2024 marks when enforcement and penalties *may begin*. The mandatory implementation dates in GL 1.5 remain unchanged (Phase 1 is still 1 Aug 2024), and the 6-month relaxation for Phase 1 still starts on 1 Aug 2024. **[GFAQ Q11, Q114]**
- **Penalty:** failure to issue an e-Invoice is an offence under **s.120(1)(d) ITA 1967**. It carries a fine of **RM200 – RM20,000**, or imprisonment of up to **6 months**, or both, **for each non-compliance**. **[GFAQ Q41]**
- **Who is responsible:** the issuer remains liable even when it outsources to a service provider or intermediary. For a company, responsibility rests with its **director** (as defined in s.2 ITA). **[GFAQ Q30, Q133]**
- **Accuracy:** the taxpayer must ensure the e-Invoice is complete and accurate and complies with the law, the GL and the SGL. **[GL 2.1]**
- **PDPA:** under **s.82C(11) ITA 1967**, the Personal Data Protection Act 2010 does not apply to personal data processed for e-Invoices issued or transmitted to the DG. **[GFAQ Q144]**
- **Data sharing with RMCD:** e-Invoice data is shared with RMCD under s.138(4)(aa) ITA, s.71(4)(aa) PITA and s.22A(1)(aa) LBATA. **[GL 2.6.2]**
- **Tax deductions / reliefs:** these can still be claimed on existing documentation **until the legislation is amended**. **[GFAQ Q4]**
- **Record keeping:** HASiL stores validated e-Invoices, but taxpayers must still keep sufficient records. **[GL 2.3.7, 2.4.6]** *(The 7-year retention period comes from s.82 ITA 1967 and is not restated in this library.)*
- **Serially numbered receipts:** MSMEs with annual gross takings **> RM150,000** must issue serially numbered receipts (**s.82(1)(b) ITA**) and quote the receipt numbers in their consolidated e-Invoice. MSMEs below that threshold need not issue receipts or consolidated e-Invoices. **[GFAQ Q109]**

---

## 2. Scope: who must comply, and from when

### 2.1 Who
- The regime applies to **all persons in Malaysia** and covers B2B, B2C and B2G. B2G follows the B2B flow. Covered entities include associations, bodies of persons, branches, business trusts, co-operatives, corporations, LLPs, partnerships, property trust funds, property trusts, REITs, representative and regional offices, trust bodies and unit trusts. **[GL 1.3]**
- **No industry is exempt.** Only certain persons and certain income/expense types are exempt. **[GFAQ Q7]**
- **SPVs under s.60I** must implement the regime and hold their own TIN. **[GFAQ Q9]**
- The regime covers **cross-border** transactions, not only domestic ones. **[GFAQ Q5]**
- The obligation sits with the **issuer**: the supplier, or the buyer for self-billed e-Invoices. A buyer cannot compel a supplier to issue an e-Invoice before the supplier's mandatory date, and normal receipts remain valid proof during the transition. **[GL 1.5; GFAQ Q55, Q107]**

### 2.2 Implementation timeline **[GL 1.5 Table 1.1; GFAQ Q11]**

| Phase | Annual turnover / revenue | Mandatory date | Interim relaxation **[SGL 16.1]** |
|---|---|---|---|
| 1 | > RM100m | **1 Aug 2024** (penalties from 1 Oct 2024) | 1 Aug 2024 – 31 Jan 2025 |
| 2 | > RM25m – RM100m | **1 Jan 2025** | 1 Jan 2025 – 30 Jun 2025 |
| 3 | > RM5m – RM25m | **1 Jul 2025** | 1 Jul 2025 – 31 Dec 2025 |
| 4 | Up to RM5m | **1 Jan 2026**, or 1 Jul 2026 "concessionary" date (see 2.4) | **Until 31 Dec 2027** |
| — | **< RM3m and meets GL 1.6.10 criteria** | **Exempt** | n/a |

**How turnover is determined [GL 1.5]:**
1. With audited financial statements: turnover/revenue in the statement of comprehensive income for **FY2022**.
2. Without audited financial statements: revenue in the **YA2022** tax return.
3. If the FY2022 accounting year end changed, **pro-rate to 12 months**. *Example: 18 months' revenue of RM60m → RM40m → Phase 2, 1 Jan 2025.*
- Once a phase is fixed, **later turnover changes do not move it**. **[GL 1.5]** Once a taxpayer becomes mandated, it **cannot fall back into the exemption**. **[GFAQ Q104]**
- **Voluntary early adoption** is allowed. **[GL 1.5; GFAQ Q112]**
- Invoices issued **before** a taxpayer's date need **not** be converted. **[GL 1.5]**
- **Sole proprietors:** aggregate **all** sole proprietorships registered under the same individual. *Example: three businesses totalling RM3.11m → mandatory.* **[GFAQ Q102]**

### 2.3 New businesses **[GL 1.5; GFAQ Q13–14]**
- **Commenced 2023–2025, with turnover ≥ RM3m in YA2023/2024/2025:** mandatory from **1 Jul 2026**.
- **Commenced 2023–2025, < RM3m throughout and meets the exemption criteria:** exempt. If turnover later reaches ≥ RM3m (YA2026 onwards), the taxpayer must implement from **1 January of the second year after that YA**.
- **Commenced 2023–2025, < RM3m but fails the criteria** (e.g. subsidiary of a group already on e-Invoice): **1 Jul 2026**.
- **Commencing 2026 onwards and failing the criteria:** **1 Jul 2026 or commencement date, whichever is later**. *Example: subsidiary incorporated 1 Sep 2026 → 1 Sep 2026.*
- **Commencing 2026 onwards and meeting the criteria:** implement from 1 January of the **second year** after the YA in which turnover reaches RM3m. *Example: YA2026 revenue RM3.12m → 1 Jan 2028.* Below RM3m → exempt.

### 2.4 The RM3m exemption **[GL 1.6.1(e), 1.6.10; GFAQ Part 3]**
- **Below RM3m annual turnover/revenue → exempt** from issuing e-Invoices, consolidated e-Invoices and **self-billed** e-Invoices. **[GFAQ Q98, Q105]**
- This applies to **all categories** of taxpayer (individuals, partnerships, companies, co-operatives, etc.).
- **The exemption does NOT apply** if the taxpayer:
  - (a) has **non-individual shareholder(s)** (or equivalent) with turnover ≥ RM3m; or
  - (b) is a **subsidiary of a holding company** with turnover ≥ RM3m; or
  - (c) has a **related company** (as defined in s.2 Promotion of Investments Act 1986) or a **JV** with turnover ≥ RM3m.
- **Related-company tests [GFAQ Q103]:**
  - A common **corporate** shareholder holding **≥ 20%** → related. Below 20% is still related if that shareholder has **control** over operations.
  - A common **individual** shareholder → **not** related, even if that person is also a common director.
  - A common director with **no shareholding** → **not** related.
- **YA2022 below RM3m but criteria not met** → **1 Jul 2026** concessionary implementation date. **[GFAQ Q12(b), Q99 example]**
- **YA2022 below RM3m, turnover later ≥ RM3m in YA2023–2025** → **1 Jul 2026**. If ≥ RM3m only in YA2026 or later → 1 January of the second year after that YA. **[GFAQ Q12(a)]**
- **Effect of the threshold increase (RM1m → RM3m) for taxpayers already caught [GFAQ Q15–20]:**
  - Eligible taxpayers may **stop issuing immediately**, with **no application** to HASiL needed.
  - **No penalties** apply for non-issuance since their earlier date.
  - They **need not join the SVDP** for omitted e-Invoices.
  - Voluntary continuation is encouraged.
- **Important:** buyers dealing with exempt suppliers use the supplier's receipts or existing documents as proof of expense. **[GL 1.6.2]**

### 2.5 Threshold / timeline history (what changed, when)

| GL version | Date | Phases | Exemption | New-business threshold |
|---|---|---|---|---|
| v4.4 / v4.5 | 5 Jun 2025 / 7 Jul 2025 | 5 (Phase 4: > RM1m–5m, 1 Jan 2026; Phase 5: up to RM1m, 1 Jul 2026) | < RM500k | RM500k |
| v4.6 / v4.7 | 7 Dec 2025 / 7 Jul 2026 | 4 (up to RM5m, 1 Jan 2026) | < RM1m | RM1m |
| **v4.8** | **30 Aug 2026** | 4 | **< RM3m + 1.6.10 criteria** | **RM3m** |

The SGL relaxation period for "> RM1m – RM5m" was 1 Jan 2026 – 30 Jun 2026, and for "up to RM1m" 1 Jul 2026 – 31 Dec 2026 (SGL 7 Jul 2025, v4.3). It is now **until 31 Dec 2027** for the whole "up to RM5m" tier (SGL from 20 Apr 2026, v4.7 onward).

### 2.6 Persons exempt from issuing (including self-billed) **[GL 1.6.1]**
- (a) **Foreign diplomatic office.** Suppliers to them may replace buyer details per SGL Table 3.5 and must keep supporting documents. **[GL 1.6.4; SGL 3.7.4–3.7.5]**
- (b) **Individual not conducting business.**
- (c) **Statutory body / statutory authority / local authority**, for:
  - (i) collection of payments, fees, charges, statutory levies, summonses, compounds and penalties under written law; and
  - (ii) goods sold and services performed **before 1 Jul 2025**.
- (d) **International organisations** (GL Appendix 3 list: UN agencies, World Bank Group, ADB, IsDB, ICRC, AFC, BWF, etc.), for goods and services **before 1 Jul 2025**.
- (e) **Taxpayers below RM3m** (subject to 1.6.10).
- Suppliers **to** these persons must still issue e-Invoices. **[GL 1.6.3]** The exemption does not extend to **entities owned by** these persons. **[GL 1.6.5]**

### 2.7 Income / expense types where no e-Invoice is required (including self-billed) **[GL 1.6.7]**
- (a) Employment income.
- (b) Pension.
- (c) Alimony.
- (d) Dividends in specific circumstances (see Section 14).
- (e) Zakat.
- (f) Contract value for buying or selling **securities / derivatives traded on an exchange** (Malaysia or elsewhere).
- (g) Disposal of **unlisted shares**, *except* where the disposer is a company, LLP, trust body or co-operative society.
- (h) Donations or contributions received, as specified in DON Part A Q1 (see Section 20.10).

---

## 3. Document types and when an e-Invoice is needed

**When:** an e-Invoice is needed as **proof of income** (sales) and **proof of expense** (purchases, returns, discounts, and self-billed cases such as purchases from foreign suppliers). **[GL 1.4]** It covers **all types of income and expense** apart from the listed exclusions. **[GFAQ Q56]**

| Type | Purpose | Self-billed variant |
|---|---|---|
| **Invoice** | Records a sale/transaction (including self-billed to document an expense) | Self-Billed Invoice |
| **Credit Note** | Reduces the original value (errors, discounts, returns) **without** return of money | Self-Billed Credit Note |
| **Debit Note** | Adds charges to the original | Self-Billed Debit Note |
| **Refund Note** | Confirms **return of money** to the buyer | Self-Billed Refund Note |

**[GL 1.4, Glossary; PORTAL Q34]**
- *Example:* 8 faulty chairs at RM10 each are returned and refunded → **Refund Note** of RM80. **[GL 1.4 Example 1]**
- **Refunds that do not need a Refund Note:** money paid wrongly, overpayments, and return of security deposits. **[GFAQ Q54]**
- An e-Invoice is a **structured XML / JSON file**, not a PDF or JPG. The PDF is only a *visual representation*. **[GFAQ Q1–2]**
- Malaysia uses the **Continuous Transaction Control (CTC)** model. **[GFAQ Q3]**

---

## 4. Workflow: MyInvois Portal and API

### 4.1 Transmission mechanisms **[GL 2.2 Table 2.1; GFAQ Q3, Q134, Q137–140]**
- **MyInvois Portal** (free, accessed via MyTax): individual form entry, or **batch upload** using a pre-defined Excel template. The portal signs documents itself, so **no digital certificate is needed**. **[PORTAL Q15]**
- **API:** direct ERP integration, **Peppol** service providers, or non-Peppol technology providers. API submissions need a **digital certificate** (.cer / .pfx), and the hashed signature goes in the request. A service provider may sign with its own certificate. **[GL 2.4.1.1; GL App 1 field 23]**
- **MyInvois Mobile App** and **MyInvois e-POS** (see Section 22).
- Mechanisms may be **combined**, provided there is **no duplication**. Reconcile to make sure. **[GFAQ Q3, Q134]**
- Technology providers need no registration or certification "at this juncture". **[GFAQ Q138–139]**
- The SDK was published on 9 Feb 2024. **[GFAQ Q136]**
- **Formats:** XML or JSON following **UBL 2.1**. **[GL 2.4]**

### 4.2 Step-by-step **[GL 2.3 / 2.4]**
1. **Pre-submission:** retrieve and verify TINs via MyTax, or register through **e-Daftar**. **[GL 2.3.1]** Individuals use a TIN with the **"IG"** prefix. **[GFAQ Q32]**
2. **Create and submit** when the sale concludes (including CN/DN/RN). The e-Invoice date/time must be the **current** date/time. **[GL App 1 field 22]**
3. **Validation** happens in near real time (usually **< 2 seconds**). HASiL returns the **IRBM Unique Identifier Number (UUID)**, the validation date/time and the validation link. If validation fails, an error message comes back; fix it and resubmit. **[GL 2.3.3, 2.4.3; GFAQ Q42]** The supplier's own invoice number stays as a separate field. **[GFAQ Q44]**
4. **Notification:** supplier and buyer are notified by e-mail. **[GL 2.3.4]**
5. **Sharing:** the supplier must share the validated e-Invoice with the buyer. **Concession (until further notice):** the supplier may share **either** the validated e-Invoice **or** a visual representation, which must carry the **QR code**. Any visual format may be used. **[GL 2.3.5, 2.4.4; GFAQ Q45–46]**
6. **Rejection / cancellation: the 72-hour window** (see 4.3).
7. **Storage** in the HASiL database. **[GL 2.3.7]**
8. **Reporting:** retrieve as XML/JSON, metadata, grid or PDF (Portal), or as XML/JSON and metadata (API). **[GL 2.3.8, 2.4.7]**

### 4.3 The 72-hour rule **[GL 2.3.6, 2.4.5, 2.5.2; GFAQ Q47–53]**
- **Buyer rejection:** within **72 hours of validation**, the buyer may *request rejection*, stating a reason (e.g. wrong SST number, BRN). The supplier is notified and **may cancel** within the same 72 hours.
- **Supplier cancellation:** within **72 hours**, with a justification. The buyer is notified. A cancelled e-Invoice is void; reissue if needed.
- **After 72 hours there is no cancellation.** Adjust instead with a **CN / DN / RN**.
- The 72-hour window is a **convenience**. A CN/DN/RN may be used even inside the window. **[GL 2.3.6; GFAQ Q50]**
- Validated e-Invoices **cannot be edited**. **[GFAQ Q47]**
- **No time limit** applies to issuing CN/DN/RN; follow company policy. **[GFAQ Q52]**
- **One CN/DN/RN may adjust several originals**, listing every UUID in "Original e-Invoice Reference Number". Consolidated e-Invoices can be adjusted too. For pre-implementation invoices with no UUID, enter **"NA"**. **[GFAQ Q53; PORTAL Q16]**
- **Consolidated e-Invoices, and e-Invoices to foreign buyers, cannot be rejected by the buyer.** Fix errors by CN/DN/RN. **[SGL 3.6.10, 10.5.3]**

### 4.4 Validation statuses and rules **[GL 2.5]**
- **Statuses:** Submitted → **Valid** / **Invalid** / **Cancelled**.
- **Validators:** Structure (immediate), Core fields (immediate), Signature (background), Taxpayer (background), Referenced documents for CN/DN/RN (background), Code (immediate and background), Duplicate document (background).
- **Submission limits:** **5MB per submission, 100 e-Invoices per submission, 300KB per e-Invoice.** There is no limit on line count. **[SGL 3.6.4; GFAQ Q135]**
- **Portal batch upload limits:** ≤ 100 documents and ≤ 25MB per Excel file; at most 1,000 drafts per taxpayer at a time. **[PORTAL Q25–26]**
- **System downtime:** availability target is 99.97%. Suppliers have **72 hours after the system is restored** to submit, and API systems should implement retry. **[GFAQ Q143]** Where downtime is documented, the DG assesses case by case and will not act if the justification is valid. **[GL 2.5.4]**
- **Time zone:** API and batch upload stamps are in **UTC**; the Portal shows **MYT (UTC+8)**. **[PORTAL Q29]**

---

## 5. The 55 data fields **[GL 2.4, Appendix 1]**

The 55 fields fall into 8 categories: Address, Business Details, Contact Number, Invoice Details, Parties, Party Details, Payment Info, Products/Services. **Bold** = mandatory, (A) = mandatory where applicable, (O) = optional.

| # | Field | Note |
|---|---|---|
| 1 | **Supplier's Name** | |
| 2 | **Buyer's Name** | |
| 3 | **Supplier's TIN** | |
| 4 | **Supplier's Reg./ID/Passport No.** | BRN (new 12-digit SSM number); MyKad/MyTentera; passport/MyPR/MyKAS |
| 5 | Supplier's SST Reg. No. (A) | Mandatory for SST registrants |
| 6 | Supplier's Tourism Tax Reg. No. (A) | Hotel operators, online travel operators |
| 7 | Supplier's e-mail (O) | |
| 8 | **Supplier's MSIC code** | 5-digit |
| 9 | **Supplier's Business Activity Description** | |
| 10 | **Buyer's TIN** | |
| 11 | **Buyer's Reg./ID/Passport No.** | |
| 12 | Buyer's SST Reg. No. (A) | |
| 13 | Buyer's e-mail (O) | |
| 14–15 | **Supplier's / Buyer's Address** | |
| 16–17 | **Supplier's / Buyer's Contact No.** | |
| 18 | **e-Invoice Version** | e.g. 1.0, 1.1; SVDP 1.2 / 1.3 for SVDP |
| 19 | **e-Invoice Type** | Invoice / CN / DN / RN / self-billed variants |
| 20 | **e-Invoice Code/Number** | Supplier's internal number |
| 21 | Original e-Invoice Ref. No. (A) | UUID of the original, for CN/DN/RN |
| 22 | **e-Invoice Date and Time** | Must be current |
| 23 | **Issuer's Digital Signature** | |
| 24 | **Invoice Currency Code** | |
| 25 | Currency Exchange Rate (A) | |
| 26 | Frequency of Billing (O) | |
| 27 | Billing Period (O) | |
| 28 | **Classification** | 3-digit code from the IRBM catalogue |
| 29 | **Description of Product/Service** | |
| 30 | **Unit Price** | |
| 31 | **Tax Type** | Line and invoice level |
| 32 | Tax Rate (A) | |
| 33 | **Tax Amount** | |
| 34 | Details of Tax Exemption (A) | e.g. buyer's sales tax exemption cert. no.; **C3 approval number required** **[GFAQ Q29]** |
| 35 | Amount Exempted from Tax (A) | |
| 36 | **Subtotal** | Line level |
| 37 | **Total Excluding Tax** | |
| 38 | **Total Including Tax** | |
| 39 | Total Net Amount (O) | Recommended for batch upload **[PORTAL Q30]** |
| 40 | **Total Payable Amount** | |
| 41 | Rounding Amount (O) | |
| 42 | Total Taxable Amount per Tax Type (O) | |
| 43–48 | Quantity, Measurement, Discount Rate/Amount, Fee/Charge Rate/Amount (O) | |
| 49–55 | Payment Mode, Supplier Bank A/C, Payment Terms, Prepayment Amount/Date/Ref., Bill Ref. No. (O) | |

**BRN:** enter the **new 12-digit SSM BRN**. BRN validation has been **temporarily disabled since 19 Jul 2024**. Non-SSM bodies enter their relevant registration number. **[GFAQ Q36–37]** Unregistered bodies (e.g. religious bodies) use the **stamp certificate number** of their governing document, not the adjudication number. **[DON A Q9]**

**Annexure [GL Appendix 2]:**
- *Mandatory (import/export of goods):* Customs Form No. 1, 9 etc. reference number.
- *Optional:*
  - Shipping recipient's name, address, TIN and registration/ID number.
  - Incoterms.
  - Product tariff (HS) code.
  - FTA information and certified exporter authorisation number (export only).
  - Customs Form No. 2 reference number.
  - Country of origin.
  - Details of other charges.

---

## 6. General TINs and placeholder conventions

### 6.1 General TINs **[SGL Appendix 1; GFAQ Q33–35]**

| General TIN | Use |
|---|---|
| **EI00000000010** (General Public) | (i) Malaysian individual who gives only a MyKad/MyTentera number; (ii) non-Malaysian individual who gives only a MyPR/MyKAS number; (iii) **buyer's TIN in a consolidated e-Invoice**; (iv) **supplier's TIN in a consolidated self-billed e-Invoice** |
| **EI00000000020** (Foreign Buyer / Foreign Shipping Recipient) | Non-Malaysian individual buyer with passport only; **export** where the foreign buyer's TIN is unavailable; foreign shipping recipient |
| **EI00000000030** (Foreign Supplier) | **Self-billed** only: non-Malaysian individual supplier with passport only; **import** where the foreign supplier's TIN is unavailable |
| **EI00000000040** (Government Buyer) | Buyer is Government, state government/authority, government authority, local authority, statutory authority/body, or an exempt institution without a TIN. Enter BRN as **"NA"** **[GFAQ Q34]** |

- It is the taxpayer's responsibility to check whether the foreign party actually **has** a TIN. Do not default to a general TIN. **[GFAQ Q35]**
- **Portal error ERR205:** "EI00000000010" with ID type "NA" is allowed **only for consolidated** e-Invoices, which must also use classification **"004 – Consolidated e-Invoice"**. **[PORTAL Q41]**
- **ERR206** (NRIC/Army number mismatch): the buyer's identity is not on HASiL's records. Verify it, or e-mail the details to myinvois@hasil.gov.my. **[PORTAL Q40]**

### 6.2 Individual buyer / supplier concession **[SGL 3.5.4–3.5.7, 8.7–8.8, Tables 3.1–3.3, 8.2; App 4]**
- **Malaysian individuals (MyKad/MyTentera) and MyPR/MyKAS holders** may give: (i) TIN only, (ii) ID number only, or (iii) both.
  - **TIN only** → enter the TIN, with ID field **"000000000000"**.
  - **ID only** → enter TIN **"EI00000000010"**, with the ID number.
- **Other non-Malaysian individuals** give: (i) TIN only, or (ii) TIN plus passport. If there is no TIN, use the general TIN with the passport number:
  - **EI00000000020** as buyer;
  - **EI00000000030** as supplier (self-billed).
- **Individual buyers** must give their full name (as per MyKad/passport), **residential address** and contact number. SST number is entered as **"NA"** if not registered. *Example: Mr Soo gives his MyKad number but no TIN, and still receives a valid e-Invoice.* **[SGL 3.5 Example 1]**

### 6.3 "NA" and "00000" conventions
- Use **"NA"** wherever a detail is not applicable, not available or not provided by a foreign party (BRN, SST number, address fields in consolidated e-Invoices).
- For the supplier's **MSIC** in self-billed e-Invoices, enter **"00000"** if unknown. **[SGL Tables 8.3, 9.1, 10.1, 10.2]**

---

## 7. Transactions with buyers and the consolidated e-Invoice

### 7.1 Buyer wants an e-Invoice **[SGL 3.5]**
1. The supplier asks whether an e-Invoice is required.
2. The buyer provides its details (SGL Table 3.1).
3. The supplier completes the remaining fields and submits.
4. The validated e-Invoice becomes the buyer's proof of expense.

Buyers who want an e-Invoice **must** give the supplier their details. **[GFAQ Q31]**

### 7.2 Buyer does not want one: consolidated e-Invoice **[SGL 3.6]**
- The supplier issues a **normal receipt**, which is not submitted to HASiL.
- The supplier then submits **one consolidated e-Invoice per month**, **within 7 calendar days after month-end**. **[SGL 3.6.2]**
- Consolidation is allowed for **B2B, B2C and B2G** where no e-Invoice was requested, except the Table 3.6 activities. **[GFAQ Q39]**
- **Buyer details:**
  - Name **"General Public"**.
  - TIN **EI00000000010**.
  - Registration number, address, contact and SST all **"NA"**.
  - Classification **004**.
  **[SGL Table 3.5 / App 2; PORTAL Q41]**
- **"Description" field methods** (one or a combination):
  - (a) each receipt as a line;
  - (b) continuous receipt-number chains as lines, with a new line whenever the chain breaks;
  - (c) per branch or location using (a) or (b).
  **Receipt reference numbers must be included** (relaxed during the interim period, see Section 17). **[SGL 3.6.3]**
- Receipts may be split across several consolidated e-Invoices to stay within the size limits. **[SGL 3.6.4]**
- **Notification goes to the supplier only.** There is no buyer rejection, and the consolidated e-Invoice **need not be shared**: it is the supplier's proof of income. **[SGL 3.6.10; GFAQ Q121]**
- **Late requests:** a buyer who later wants an e-Invoice must ask **within the month of the transaction**. After that the supplier may refuse. *Examples: a meal on 21 Jul, requested 28 Jul → must be issued; a purchase on 30 Sep, requested 1 Oct → may be refused.* **[SGL 3.6.8, Examples 4–5]**
- **Self-billed e-Invoices cannot be consolidated**, except for: (a) individuals not conducting business; (b) interest paid to the public at large; (c) insurance claims, compensation or benefits paid to individuals not in business or to government bodies; (d) self-billed circumstances involving the taxpayer's **overseas branches or offices**. These follow the same timing: monthly, within 7 days. **[SGL 3.6.5–3.6.7, Table 3.4]**
  - In a consolidated self-billed e-Invoice the supplier is "General Public", TIN EI00000000010, MSIC "00000", other fields "NA".
- **MSMEs:** consolidated e-Invoicing is allowed except for Table 3.6 items. **[GFAQ Q108]**
- **Issuance options for suppliers:** retailer web portal or app, POS integration (about 60 seconds of interaction), MyInvois Mobile App, or a post-transaction self-serve portal. Any other method is acceptable. **[SGL 3.8]**
- **Timing generally:** there is **no fixed deadline** for normal e-Invoices; follow current invoicing practice. The fixed deadlines apply only to consolidated e-Invoices, self-billed imports, and foreign income. **[GFAQ Q38]**
- Drafts and proforma documents can be saved in the Portal. **[GFAQ Q40]**

### 7.3 Where consolidation is NOT allowed: e-Invoice for each transaction **[SGL 3.7.2 Table 3.6]**

| # | Industry / activity | No consolidation for |
|---|---|---|
| 1 | Automotive | Sale of **any motor vehicle** (including trailers) |
| 2 | Aviation | **Flight tickets**; **private charter** |
| 3 | Luxury goods and jewellery | *On hold.* Consolidation is allowed until details are released |
| 4 | Construction | **Construction contractor** undertaking a construction contract (Income Tax (Construction Contracts) Regulations 2007) |
| 5 | Licensed betting and gaming | **Pay-outs to winners.** Casino and gaming-machine pay-outs are **exempt until further notice** |
| 6 | Agents / dealers / distributors | Payments to them (s.83A(4) ITA definition) |
| 7 | **All industries** | **Any single transaction > RM10,000**, from **1 Jan 2026** |
| 8 | Electricity service provider | Distribution, supply or sale of electricity, from **1 Jan 2026** |
| 9 | Telecommunication | **Postpaid plans, internet subscriptions, sale of electronic devices**, from **1 Jan 2026** |

- For these activities the supplier must **collect the buyer's details**. The individual-ID concession in 6.2 still applies. **[SGL 3.7.1, 3.7.3]**
- Even bodies not approved for tax exemption must give their details to suppliers in these activities (e.g. motor vehicles, construction). **[DON A Q7]**
- **During the interim relaxation period** all of these **may** be consolidated (see Section 17).

---

## 8. Periodic statements and bills **[SGL 4]**

- **Industries:** digital/e-payment, banking and finance, healthcare, insurance, stockbroking, telecommunications, and others. **[SGL 4.1]**
- **Format:** submit the e-Invoice as XML/JSON and present it to the buyer as the usual **statement or bill**. Amounts owed **and** payments/credits (e.g. rebates) may appear in the **same** e-Invoice, limited to the supplier's own income and expense. **[SGL 4.2.2–4.2.4]**
- **Frequency:** submit at the existing statement frequency (monthly, quarterly, annual, etc.). **[SGL 4.2.5]**
  - *Example:* a telco's RM10 monthly loyalty rebate goes in the bill e-Invoice. **[SGL Example 6]**
- **e-Invoice Code/Number** = statement reference. **[SGL Table 4.1]**
- **Buyer does not want one:** issue the normal statement, aggregate, and submit a **consolidated e-Invoice within 7 calendar days after the end of the billing month**. **[SGL 4.3]**
- **Regulated industries** (FIs, payment systems, brokers, UTMC/UTF) need **not** disclose statement reference numbers in the consolidated "Description" field, but **must** enter a relevant description. **[SGL 4.3.7; FIN A Q2, B Q4, C Q9]**

---

## 9. Disbursement vs reimbursement **[SGL 5; GFAQ Q59]**

**Definitions:**
- **Reimbursement:** out-of-pocket costs incurred by the **payee** (e.g. airfare, travel, accommodation, phone, photocopying) and recovered from the payer.
- **Disbursement:** costs incurred by the **payer**, paid to a third party by the payee **on the payer's behalf**.

**Scenario 1: Supplier 1 invoices the buyer directly.**
- Supplier 2 (the intermediary) pays on the buyer's behalf.
- Supplier 2 **excludes** that amount from its own e-Invoice, issues **no separate** e-Invoice for it, and passes on the **payment proof**.
- *Example:* the florist e-Invoices Perniagaan Adibah directly; the event planner pays the RM4,000 on its behalf and bills only its service fee.

**Scenario 2: Supplier 1 invoices Supplier 2.**
- Supplier 2 recharges the buyer in its own e-Invoice, showing the **service fee and the disbursement/reimbursement as separate lines**.
- *Example:* a hotel e-Invoices the event planner, who recharges the RM30,000 hall rental as a separate line.

**Intercompany "paid on behalf" with no sale between the parties:**
- No e-Invoice is needed (e.g. a parent pays a subsidiary's supplier and the subsidiary repays).
- If the parent **charges a fee** for this, it must e-Invoice the fee. **[SGL Example 9]**

---

## 10. Employees: perquisites, benefits and expenses incurred for the employer

**10.1 Perquisites and benefits [SGL 6]** (e.g. utility bills, parking, car maintenance, club/gym membership, professional subscriptions, allowances)
- Employees should ask the supplier to issue the e-Invoice in the **employer's** name **where possible**.
- **Concession:**
  - (a) An e-Invoice in the **employee's** name, or existing supporting documents, is accepted as the employer's proof of expense.
  - (b) For benefits paid to **foreign suppliers**, **no self-billed e-Invoice** is needed by employer or employee; foreign receipts are accepted.
- The concession applies **only if the benefit is clearly stated in the employer's policy**.

**10.2 Expenses incurred on the employer's behalf [SGL 7]** (accommodation, toll, mileage, parking, telecommunications, overseas expenses)
- The same concession applies: an e-Invoice in the employee's name or existing documents is accepted.
- **Overseas expenses need no self-billed e-Invoice.**
- Applies only if the employer can **prove the employee acted on its behalf**.

**Related points:**
- **Director fees:** under a contract **for service** the director e-Invoices the company. Under a contract **of service** the fees are employment income and **exempt**. **[GFAQ Q58]**
- Locum doctors and nurses follow the same split. **[HC Q5]**

---

## 11. Self-billed e-Invoice **[SGL 8; App 3]**

The **buyer** issues the self-billed e-Invoice **only** in these circumstances. **[SGL 8.3]** Self-billing is **not allowed** outside SGL 8.3, e.g. just because the supplier did not issue an e-Invoice, or because of poor connectivity. **[GFAQ Q26–28]**

| # | Circumstance | Supplier | Buyer (issuer) |
|---|---|---|---|
| (a) | Payments to **agents, dealers, distributors** | Agent / dealer / distributor | Payer |
| (b) | Goods/services from **foreign suppliers** | Foreign seller | Malaysian purchaser |
| (c) | **Profit distribution** (e.g. dividends), where not exempt | Recipient | Distributor |
| (d) | **e-Commerce** | Merchant / service provider (driver, rider) | Platform |
| (e) | Pay-outs to **betting and gaming winners** (casino and gaming machines exempt) | Winner | Licensed operator |
| (f) | **Individuals not conducting business**, only if no other self-billed head applies | Individual | Person transacting |
| (g) | **Interest payments**, with exceptions below | Interest recipient | Payer |
| (h) | **Insurance claims, compensation and benefits** | Policyholder / beneficiary | Insurer |
| (i) | **Capital reduction, share/capital/unit redemption, share buyback, return of capital, liquidation proceeds** | Investor | Investee |

**Interest exceptions, where the supplier issues a normal e-Invoice instead [SGL 8.3(g)]:**
- (i) Businesses such as FIs charging interest to the **public at large**.
- (ii) Interest paid by an **employee to the employer** (staff loans).
- (iii) Interest paid by a **foreign payor** to a Malaysian taxpayer.
- (iv) Interest paid to a **Malaysian related company that provides centralised treasury services** (to be implemented by 1 Jul 2025 at the latest).
- (v) **Late-payment interest or charges** imposed by Malaysian taxpayers.

**Examples [SGL 8, Examples 11–20]:**
- An employee sells his gaming console to a company → the company self-bills.
- Vacant land rented from a teacher, or an office owned by three individual landlords (not in business) → the tenant self-bills, with **separate self-billed e-Invoices for each co-owner** in their agreed proportions.
- A tea-time snack bought from a roadside stall not yet mandated → **no self-billing allowed**; use the handwritten receipt.
- Mortgage interest paid to a bank → the **bank** issues the e-Invoice (exception (i)).
- Interest on a loan from a holding company that is **not** a treasury centre → the **borrower self-bills**. If the lender **is** a Malaysian treasury centre → the lender issues.
- Interest paid to the estate administrator of a deceased moneylender → the payer self-bills.

**Timing for (i) capital transactions [SGL 8.3 fn 3]:**
- Written agreement, no government approval needed → **date of agreement**.
- Approval needed → **date of approval**, or the date the **last condition** is met.
- No written agreement → **date of completion**.

**Mechanics:**
- Once a self-billed e-Invoice is issued, the other party issues **no** e-Invoice. **[SGL 8.4]**
- The buyer **must share** the validated self-billed e-Invoice with the supplier. The concession allows either the e-Invoice or its visual representation, with QR code. **[SGL 8.5]**
- **Exception:** foreign suppliers need **not** be sent the self-billed e-Invoice. **[SGL 10.4.6]**
- **Accrual or paid basis** is acceptable, applied consistently, for agents and for interest. **[GFAQ Q65, Q70]**
- **Fields:** supplier TIN (foreign: EI00000000030); MSIC "00000" if unknown; e-Invoice Code = supplier's invoice or receipt number. **[SGL Table 8.3]**

---

## 12. Agents, dealers and distributors **[SGL 9; GFAQ Q65–69]**

- **Seller → purchaser:** a normal e-Invoice, or receipts plus a monthly consolidated e-Invoice.
- **Seller → agent:** a **self-billed e-Invoice** for commissions and incentives, **monetary or otherwise** (s.83A ITA). It cannot be consolidated (Table 3.6). Malaysian agents **must** provide their TIN and BRN.
  - *Example:* a car agent's 20% commission → the company self-bills. **[SGL 9.4; Example 21]**
- This applies **even to corporate agents** that currently invoice the company: they **stop** issuing, and the payer self-bills. **[GFAQ Q66]**
- **Frequency:** periodic agent statements may be used (bi-weekly, monthly). **Non-monetary incentives** (trips, gifts) may be transmitted **annually**, when the CP58 data is ready, if not available earlier. **[GFAQ Q67–68]**
- **Net basis** (gross less clawbacks) is allowed if the reversal lines are shown. If a clawback exceeds the commission → issue a **self-billed credit note**, even when nothing is paid. **[GFAQ Q69 Scenarios 1–2]**
- **Rental charged to an agent** and set off against commission → the company issues a **separate normal e-Invoice** for the rental. **[GFAQ Q69 Scenario 3]**

---

## 13. Cross-border transactions **[SGL 10, 13; GFAQ Q76–97]**

A **foreign supplier** is any supplier outside or not established in Malaysia, including a non-Malaysian individual. **[SGL 10.2]**

### 13.1 Imports (foreign seller → Malaysian purchaser): self-billed **[SGL 10.4]**

**Deadlines:**
- **Goods:** issue by the **end of the second month after the month of customs clearance**. **[SGL 10.4.8; GFAQ Q80]**
- **Services:** issue by the **end of the month after the month of (1) payment or (2) receipt of the foreign invoice, whichever is earlier**, following the imported taxable service rules. **[SGL 10.4.9; GFAQ Q89]**
- **e-PAM, LCL shipments and drop shipments not physically imported:** issue when the foreign invoice is **recorded in the accounts**. **[GFAQ Q91]**

**Content:**
- Include **service tax on imported taxable services** where applicable. **[SGL 10.4.7]**
- **Exclude** import duty and sales tax charged by RMCD. **[GFAQ Q77]**
- Value = **actual transaction value per the foreign invoice**. Incoterm extras go under "Details of other charges". **[GFAQ Q79]**
- Supplier TIN = **EI00000000030** if none is available. Missing details = **"NA"**. **[SGL Table 10.1]**

**Process:**
- Only the purchaser is notified; there is **no obligation to share** with the foreign seller. **[SGL 10.4.5–10.4.6]**
- **No consolidation** of foreign-supplier self-billed e-Invoices, even from the same supplier, except via the overseas-branch exception (SGL 3.6.5). **[GFAQ Q76]**
- **Foreign e-commerce platforms:** a Malaysian buyer **must self-bill**. **[GFAQ Q81]**
- **Currency:** the purchaser may use its **internal exchange rate** for import self-billing. **[SGL 13.4]**

**Multiple shipments under one invoice [GFAQ Q82]:**
- **(a) Invoice issued by the first clearance:** **one** self-billed e-Invoice based on the invoice, quoting the K1 reference. No more are needed for later shipments.
- **(b) Invoice issued after the first clearance:** a self-billed e-Invoice **per shipment**, at the declared value, until the invoice arrives; then a **final** one by the next clearance.
- **(c) Invoice issued after the final shipment:** one per shipment, plus a final adjustment if the totals differ. The final one is due by the end of the second month after the month of the foreign invoice.

**Customs form reference (Annexure):**
- **Required:** goods from a **bonded warehouse or Free Zone** delivered into the PCA (K1/K9) **[GFAQ Q83]**; goods delivered by a foreign supplier's Malaysian supplier from a bonded warehouse or FZ → K9 **[GFAQ Q88]**; **DDP** purchases (obtain the reference from the supplier or forwarder) **[GFAQ Q95]**.
- **Optional:** bonded-warehouse and drop-ship resale chains (K8 discretionary) **[GFAQ Q84–87]**; exports (K2) **[GFAQ Q90]**.
- **Excluded:** e-PAM low-value goods **[GFAQ Q92]**; LCL shipments **[GFAQ Q93]**; drop shipments not imported **[GFAQ Q94]**; movements between Peninsular Malaysia, Labuan, Sabah and Sarawak **[GFAQ Q97]**.
- **Several references:** separate them with commas (e.g. B18B12345670, B18B12345671). **[GFAQ Q96; PORTAL Q17]**
- **Clearance or invoice before the mandatory date:** no self-billed e-Invoice is needed. **[GFAQ Q117, Q119]**

### 13.2 Exports (Malaysian seller → foreign purchaser) **[SGL 10.5]**
- Issue a normal e-Invoice under current practice. **[GFAQ Q90]**
- **Buyer TIN:** use **EI00000000020** if there is none. For a MyPR/MyKAS individual, use EI00000000010.
- Only the seller is notified. A copy may be shared; **no rejection is possible**, so correct errors by CN/DN/RN.
- K2 reference: optional.

### 13.3 Currency **[SGL 13; GFAQ Q25]**
- Any currency may be used.
- Show an RM exchange rate only where conversion to RM is legally required.
- **Rate hierarchy:** (1) RMCD or IRBM legal/tax rules; otherwise (2) internal policy.

---

## 14. Profit distribution and foreign income

### 14.1 Domestic dividends **[SGL 11.1]**
- **Exempt from self-billing:**
  - taxpayers **not entitled to deduct tax under s.108 ITA**; and
  - companies **listed on Bursa Malaysia**.
  Shareholders also issue nothing. Existing dividend vouchers and warrants continue.
- **All other distributors** (e.g. other trusts and unit trusts; see FIN C Q4 for UTF/IUTA) must issue a **self-billed e-Invoice** to each recipient when the profit is paid or credited.
  - e-Invoice Code = dividend voucher number. **[SGL Table 11.1]**
- Insurers' **bonuses** and **surplus or investment profit distributions** to participants → self-billed under SGL 11. **[INS E Q4]**

### 14.2 Foreign dividends and foreign income **[SGL 11.2, 12]**
- The **Malaysian recipient issues the e-Invoice to itself as Supplier**, with the foreign payor as Buyer, as **proof of income**.
- **Deadline:** **end of the month after the month of receipt**. **[SGL 12.4; GFAQ Q38]**
- **Payor TIN:** EI00000000020 (or EI00000000010 for MyPR/MyKAS individuals). **[SGL Table 12.1]**
- Interest paid by a **foreign** FI → the account holder issues the e-Invoice. **[FIN B Q10]**

---

## 15. e-Commerce **[SGL 14; ECOM]**

| Flow | Issuer | Document |
|---|---|---|
| Platform ↔ purchaser | **Platform** (as supplier) | e-Invoice on request, or a receipt plus a monthly **consolidated** e-Invoice (except Table 3.6 items). The merchant issues **nothing** to the purchaser. |
| Platform → merchant / service provider (sales proceeds) | **Platform**, self-billed | **Self-billed** e-Invoice for **all** platform transactions, at the existing statement frequency (daily/weekly/monthly). **No consolidation.** Foreign merchants: EI00000000030 |
| Platform → merchant (platform fees and commissions) | **Platform** | Normal e-Invoice; foreign merchants: EI00000000020 |

**[SGL 14.4–14.6; ECOM Q1–5]**
- This is for tax compliance only and **does not change the commercial nature or liability** of the transaction. **[SGL 14.4.2, 14.5.2]**
- **Classification:** use the e-commerce classification code. **[ECOM Q1]**
- **Proforma** invoices are allowed before goods are received; submit only the final one. **[ECOM Q6]**
- **Returns refunded by the platform** → the platform issues a **refund note**. **[ECOM Q7]**
- **Do not combine** e-commerce and physical-store transactions in one consolidated e-Invoice. **[ECOM Q8]**
- **MSMEs below RM3m selling on a local platform** must still give their details to the platform. They issue nothing for platform sales, but must e-Invoice **physical-store** sales if they are in scope. **[GFAQ Q106, Q110]**

---

## 16. Specific transaction treatments (quick reference)

| Situation | Treatment | Source |
|---|---|---|
| **Deposits** | Refundable → no e-Invoice. Non-refundable → e-Invoice | GFAQ Q57; HC Q10; TOUR Q3; FIN A Q12 |
| **Intercompany charges** | e-Invoice **required** | GFAQ Q60 |
| **Inter-department / inter-division** (same entity) | Not required (optional) | GFAQ Q61; INS E Q1 (interfund) |
| **Individual landlord** | Conducting business → landlord e-Invoices. Not in business → **tenant self-bills** (if the tenant is a business) | GFAQ Q62; TEL Q3 |
| **Utilities billed in the landlord's name** | Include them in the landlord's e-Invoice, or in the tenant's self-billed e-Invoice | GFAQ Q63 |
| **Consignment** | The consignor e-Invoices when the consignee **sells or consumes** the goods | GFAQ Q64 |
| **Vouchers / gift cards** (monetary and non-monetary) | Free or refundable → no e-Invoice on issue. **Non-refundable sold → e-Invoice on sale** | GFAQ Q71 |
| Expired vouchers | Free or non-refundable → none. **Refundable expired → e-Invoice on expiry** | GFAQ Q72 |
| Redemption, refundable voucher | e-Invoice at redemption; "Total Excluding Tax" = full sale value (voucher may go in "prepayment") | GFAQ Q73 |
| Redemption, non-refundable voucher | e-Invoice for the amount **not** covered by the voucher; show the voucher as a separate line | GFAQ Q74 |
| Purchase-with-purchase voucher (free) | No e-Invoice for the voucher | GFAQ Q75 |
| **Return of money to buyers** | **Refund note**, except wrong payments, overpayments and security deposit refunds | GFAQ Q54; INS B Q5 |
| **C3 sales tax exemption** | Enter the C3 details in "Details of Tax Exemption" | GFAQ Q29 |
| **Accounting / audit adjustments** (MTM, FX gains, amortisation) | No e-Invoice | FIN A Q16 |
| **Loan principal** | No e-Invoice; **interest** does need one | FIN A Q6; FIN E Q1 |
| **Free services to staff** | Nil-value e-Invoice only if that is current practice | HC Q11 |
| **Nil-income transactions** | Not required; a "Nil" e-Invoice is optional | FIN C Q7; AVI Q5 |

---

## 17. Interim relaxation period **[SGL 16; GFAQ Q113–122]**

The Government agreed on **26 Jul 2024** to a relaxation period per phase (see the table in Section 2.2). The "up to RM5m" tier now runs **until 31 Dec 2027**.

**During the relaxation period taxpayers may:**
- (a) Issue **consolidated e-Invoices for all transactions**, including Table 3.6 activities.
- (b) Issue **consolidated self-billed e-Invoices for all self-billed circumstances**.
- (c) Enter **any description** in "Description of Product or Service". Receipt numbers are not required. **[GFAQ Q122]**
- (d) **Decline individual e-Invoice requests**, provided (a) or (b) is followed.

**Protections and obligations:**
- **No prosecution under s.120 ITA** during the relaxation period, **provided** (a) and (b) are followed. **[SGL 16.3]**
- The relaxation is **optional**. Ready taxpayers may issue individual e-Invoices. **[GFAQ Q115]**
- Consolidated e-Invoices are still due **monthly, within 7 days**, not once at the end of the period. **[GFAQ Q116]**

**Phase 1 timing examples:**
- Goods cleared in Aug 2024 → individual self-billed e-Invoice by 31 Oct 2024, or consolidated by 7 Nov 2024.
- Services in Aug 2024 → individual by 30 Sep 2024, or consolidated by 7 Oct 2024.

**[GFAQ Q118, Q120]**

---

## 18. e-Invoice Special Voluntary Disclosure Programme (SVDP) **[SGL 17; GFAQ Q123–133]**

**Window:** **7 Jul 2026 – 31 Dec 2027**. There is **no registration or application**; just submit within the window.

**Who it covers:**
- e-Invoices that were not submitted or were missed after the mandatory date.
- e-Invoices that were submitted with errors.
- Taxpayers who submitted nothing at all.
- Taxpayers **under, or notified of, an e-Invoice compliance review**.

**Benefit:** **no compliance review, penalty or prosecution** on disclosed e-Invoices, **unless**:
- the disclosure itself is non-compliant; or
- it involves **fraud, wilful default or negligence**.

**Rules:**
- Use e-Invoice version **"SVDP 1.2"** (without digital signature) or **"SVDP 1.3"** (with signature), **only** for SVDP submissions.
- **Consolidated e-Invoices are submitted per month**, never as one lump sum. *Example: Jan–Apr 2026 → four consolidated e-Invoices.*
- **Transactions > RM10,000 need individual e-Invoices** even under the SVDP. *Example: a RM12k item in Feb 2026.*
- **Post-relaxation periods must follow full rules.** *Example: Phase 1, Jan–Mar 2026 self-billed → individual self-billed e-Invoices*, apart from the 3.6.5 consolidation exceptions.

**How to correct errors** (e.g. an incomplete buyer address, or the wrong classification code such as "022 Others" instead of "026 books/publications"):
- Issue a **credit note** to reverse the original.
- Then issue a **new correct e-Invoice**.

**Other points:**
- Within the 72-hour window you may simply cancel and reissue, or use the SVDP. **[GFAQ Q126–128]**
- Pre-7 Jul 2026 voluntary corrections remain recognised and need not be redone. **[GFAQ Q125]**
- Multiple disclosures are allowed. **[GFAQ Q129]**
- Errors in SVDP submissions → fix them with CN/DN/RN. **[GFAQ Q130]**
- Omissions from consolidated e-Invoices in the relaxation period → either (a) a CN plus a new full consolidated e-Invoice, or (b) a separate consolidated e-Invoice for the omitted items. **[GFAQ Q131]**
- **Each group entity discloses separately.** **[GFAQ Q132]**
- Vendor-caused errors are still the taxpayer's responsibility, but the taxpayer may still use the SVDP. **[GFAQ Q133]**
- Taxpayers below RM3m who meet the exemption criteria **need not participate**. **[GFAQ Q19]**

---

## 19. MSME notes **[GFAQ Part 3]**

- **Below RM3m and meeting the criteria → exempt.** See Section 2.4 for the full rules.
- **Large enterprises cannot compel MSMEs** to issue before their mandatory date. **[GFAQ Q107]**
- **Receipts:** MSMEs with gross takings **> RM150k** must issue serially numbered receipts (s.82(1)(b)), and those receipt numbers feed the consolidated e-Invoice. Below RM150k → no receipts and no consolidated e-Invoice. **[GFAQ Q109]**
- **Free tools:** MyInvois Portal, the MyInvois Mobile App and MyInvois e-POS. **[GFAQ Q111, Q140]**

---

## 20. Industry digests

### 20.1 Construction (CON, 6 Jan 2026)
- **Contractors** (per the Construction Contracts Regulations 2007) must e-Invoice charges to **sub-contractors, including penalties**. **[Q1]**
- **Progress claims:** issue the e-Invoice on the claim. Where **certification of work done** is required, issue it when the **certificate** is obtained. **[Q2]**
- **Materials bought on the owner's behalf** and billed in the progress claim → current billing continues, but the contractor's invoices must be e-Invoices. **[Q3]**
- **Sale of construction materials to related companies** → an e-Invoice on request, otherwise receipts plus a consolidated e-Invoice. *Note:* the contractor activity itself is a no-consolidation item (Table 3.6). **[Q4]**

### 20.2 Aviation (AVI, 26 Aug 2026)
- **Flight tickets and private charters:**
  - Local airlines: an e-Invoice for **all** sales, regardless of point of sale.
  - Foreign airlines: where the **IATA point of sale is Malaysia**.
  - **No consolidation.** **[Q1]**
- **Buyer details:** the **purchaser** (not the passenger). For group bookings, either the purchaser for all tickets or each passenger. **[Q2]**
- **Concession for buyers who do not want an e-Invoice:**
  - Malaysian buyers → **actual details**.
  - **Non-Malaysian** buyers → name "General Public", TIN **EI00000000020**, BRN "NA", and **the airline's own** address, contact and SST details where the buyer's are unavailable. **[Q3]**
- **Excess baggage at the counter** → an e-Invoice on request, otherwise receipt plus consolidated. **[Q4]**
- **Fare changes:** price up → invoice or DN for the difference. Price down → CN or RN. No change → nothing (a nil e-Invoice is optional). **[Q5]**
- **Ancillaries:**
  - **Flight-related** (seats, baggage), sold with the ticket → one combined or separate e-Invoices. Sold separately → the ticket e-Invoice is mandatory; the ancillary gets one on request.
  - **Non-flight** (insurance, hotel, car rental) → the airline issues if it is the **principal**; if it acts as **agent**, the service provider issues. **[Q6]**

### 20.3 Tourism (TOUR, 14 Jun 2024)
- **Travel agent as principal** → the agent e-Invoices the consumer (ticket mandatory, no consolidation), and the airline e-Invoices the agent.
- **Travel agent as agent** → the **airline** e-Invoices the consumer and **self-bills the agent's commission**. **[Q1]**
- **Buyer details:** as for aviation. **[Q2]**
- **Package deposits:** refundable → nothing. Non-refundable → an e-Invoice for the deposit, then a separate one for the balance. **[Q3]**
- **Tour guides:** local guides e-Invoice the agency; for **foreign** guides, the agency **self-bills**. **[Q4]**
- **Packages including flights → no consolidation.** Packages without flights → consolidation is allowed. **[Q5]**

### 20.4 Healthcare (HC, 14 Jun 2024)
- **Buyer = the patient**; for **minors (< 18)**, the parent or guardian. This holds whoever pays (TPA, MCO, insurer, employer, guardian). **[Q1]**
- Consolidation is allowed for self-paying patients who do not want an e-Invoice. **[Q2]**
- **Proforma bills to insurers for the FGL** are fine. Issue the e-Invoice on **final billing / discharge**, or consolidate within 7 days of month-end. **[Q3]**
- **Independent consultants:**
  - Co-provision → separate e-Invoices from the hospital and from the consultant.
  - Outsourcing → the hospital issues one e-Invoice to the patient, and the consultant (or the company representing them) e-Invoices the hospital. **[Q4]**
- **Locums:** contract **for** service → the locum (or agency) e-Invoices. Contract **of** service → employment income, exempt. **[Q5]**
- **Referrals between hospitals:** each billing hospital e-Invoices the patient. If Hospital C bills for Hospital D's services, D e-Invoices C. **[Q6]**
- **Rentals and management fees** charged to consultants or tenants → e-Invoice per the billing cycle. **[Q7]**
- Use the **Detailed Bill**, not the summary bill. **[Q8]**
- **Phase determination:** consultants and the hospital each follow **their own** threshold. **[Q9]**
- **Admission deposits:** refundable → none. **[Q10]**
- **Staff medical:** a nil e-Invoice only if that is current practice. **[Q11]**

### 20.5 Telecommunications (TEL, 22 Dec 2023)
- **Adjustments** to a prior bill may go in the next cycle's bill or a CN/DN/RN. **[Q1]**
- **Prepaid plans sold to agents or traders** → current billing continues. **[Q2]**
- **Rented premises:** a business landlord e-Invoices; an individual landlord not in business → the telco **self-bills**. **[Q3]**
- **Add-on services** (e.g. streaming) billed through the telco:
  - a **local** vendor e-Invoices the customer;
  - for a **foreign** vendor, the customer self-bills;
  - the telco e-Invoices its own platform fee or commission. **[Q4]**
- *Note:* from 1 Jan 2026, postpaid plans, internet subscriptions and electronic device sales **cannot be consolidated** (Table 3.6).

### 20.6 Petroleum operations (PET, 18 Jan 2024)
- **Crude sales:** supplier TIN = the **contractor's ITA TIN**, with the petroleum-operations classification code. **[Q1]**
- **Buyer TIN for costs:**
  - **joint costs** → the PSC operator's TIN;
  - **sole costs** → the contractor's TIN.
  **Recharges of joint costs are exempt until further notice.** **[Q2]**
- **Contiguous blocks:** same principles. **[Q3]**
- **Inter-ledger transactions** (back charges) between a PSC and its operator → **exempt until further notice**. **[Q4]**
- **Sales via an agent:** contractor → agent → buyer, with e-Invoices at each step. **[Q5]**
- **Upstream Gas Sales Agreement:** the operator may issue on the contractor's behalf using the **contractor's details**. **[Q6]**
- **Supplementary payments:** current practice; true-ups by DN/CN. **[Q7]**
- **Cash calls and JIB** are settlement mechanisms → **no e-Invoice**. **[Q8]**

### 20.7 Insurance and Takaful (INS, 28 Jan 2025)
- **Consolidation** is allowed for policyholders who do not want an e-Invoice. **Annual premium statements** may be used; submit within 7 days after the end of the issuance month. *Example:* the first statement covering Jan–Dec 2024 may be sent in Feb/Mar 2025 without excluding Jan–Jul 2024. **[A Q1–3]**
- **Ad-hoc requests:** follow the statement cycle. **[A Q4]**
- **Buyer = policyholder**, even for products not eligible for relief. **[A Q5]**
- **Premium breakdown with classification codes:** 014 education/medical, 015 takaful/life, 022 others, 024 PRS/deferred annuity. **[B Q1]**
- **Joint policy** → the principal policyholder (separate e-Invoice on request). **[B Q2]**
- **Collections on behalf** (e.g. stamp duty): include them only if the third party e-Invoices the insurer; they are not the insurer's income, so use the appropriate code. **[B Q3]**
- **Intermediaries:**
  - **Master policy** with the intermediary → the insurer e-Invoices the intermediary, which e-Invoices end customers. If it does not, the insurer issues directly.
  - **Individual policy** → the insurer e-Invoices the end customer. **[B Q4]**
- **Policy termination refunds** → refund note (standard exceptions apply). **[B Q5]**
- **Minors** → parent or guardian. **[B Q6]**
- **Group policies** → master policyholder; separate e-Invoices per entity on request. **[B Q7]**
- **Employer-collected premiums** → the e-Invoice goes to the **employee policyholder**. **[B Q8]**
- **Cash before cover** → existing process. **[B Q9]**
- **Reinsurance:** a local reinsurer e-Invoices the cedant; for a **foreign** reinsurer the cedant **self-bills**. Net-basis statements are allowed. **[B Q10]**
- **Claims, compensation and benefits** → **self-billed by the insurer** to the policyholder or beneficiary, regardless of who is paid (hospital, workshop). **Consolidation is allowed for individuals not in business.** **[C Q1]**
- **Scrap and wreck disposal:**
  - insurer-owned → the insurer e-Invoices the workshop;
  - business policyholder → the policyholder e-Invoices;
  - individual or foreign policyholder → the **workshop self-bills**. **[C Q2]**
- **Knock-for-knock:** the at-fault party's insurer self-bills its own policyholder. Driver A's insurer cancels (within 72 hours) or issues a **self-billed CN**. **[C Q3]**
- **Agent exam or registration fees** paid on the agent's behalf → follow the disbursement logic. **[D Q1]**
- **Interfund charges** → not required. **[E Q1]**
- **Endorsements** of pre-implementation policies → original reference "NA". **[E Q2]**
- **Policy loan / APL / late interest** → an e-Invoice is needed; statements may be used. **[E Q3]**
- **Bonuses and surplus distributions** → self-billed under SGL 11. **[E Q4]**
- **MMIP:**
  - MMIP e-Invoices the policyholder;
  - statements to insurers on a net basis;
  - MMIP **self-bills** the insurer's agency commission. **[E Q5]**

### 20.8 Financial services (FIN, 26 Aug 2026)

**A. Banks and financial institutions**
- **Customer consent** is needed for individual e-Invoices (FSA/IFSA secrecy). **[A Q1]**
- **Consolidated e-Invoices:** a relevant description is required; statement numbers are not needed. **[A Q2]**
- **Resident banks:** e-Invoice activities **in and outside Malaysia**, including overseas branches. **[A Q3]**
- **Interest paid to depositors:** the FI issues the e-Invoice (statement format); the customer issues nothing. **[A Q4]**
- **Walk-in customers:** consolidation is allowed except for Table 3.6 items. **[A Q5]**
- **Loans:** interest → e-Invoice; principal → none. **[A Q6]**
- **Interbank interest:** the lender e-Invoices. **[A Q7]**
- **Non-refundable treasury premiums or fees:** e-Invoice. **[A Q8]**
- **Joint, omnibus, custodial, trust, estate and escrow accounts:** issue to the principal holder (others on request). **[A Q9]**
- **Card networks:** **foreign** processors (Visa, Mastercard, etc.) → the FI **self-bills**. **Local** processors (e.g. PayNet) → they e-Invoice the FI, and statements may be used. **[A Q10]**
- **Inward remittance:** the FI self-bills the foreign correspondent's fee, then e-Invoices any recharge to the local recipient. **[A Q11]**
- **Foreclosure auction upfront payments:** non-refundable → e-Invoice. **[A Q12]**
- **Card rewards:**
  - **cashback** → in the statement e-Invoice;
  - **free points** and redemptions → none;
  - **extra charges** on redemption → e-Invoice. **[A Q13–14]**
- **Adjustments** may go in the next month's statement e-Invoice. **[A Q15]**
- **Accounting adjustments** (gains, MTM, FX, amortisation) → none. **[A Q16]**
- **Interest rate swaps:** the dealer or intermediary issues an e-Invoice or self-billed e-Invoice. **[A Q17]**

**B. Securities and derivatives broking**
- **Exchange-traded securities and derivatives contract values** → exempt (GL 1.6.7(f); the FAQ cites "1.6.8"). **[B Q1]**
- **Unquoted securities or derivatives**, on issue or transfer → the **issuer or transferor** e-Invoices. Timing: agreement / approval / last condition / completion. **[B Q2]**
- **Contract notes or monthly statements** may serve as the visual representation. **[B Q3]**
- **Secrecy:** no statement number needed in consolidated e-Invoices. **[B Q4]**
- **Brokerage, clearing and other fees** → e-Invoice on request, otherwise receipts plus consolidated. **[B Q5]**
- **Stamp duty and other collections on behalf** → include them only if the third party bills the broker. **[B Q6]**
- **BMDep CDS fees** → BMDep e-Invoices. **[B Q7]** **ADAs** e-Invoice their rebates. **[B Q8]**
- **Nominee foreign dividends:** the **client** e-Invoices the foreign dividend; the nominee e-Invoices its fees. **[B Q9]**
- **Trust-money interest:**
  - the local FI e-Invoices the account holder;
  - the broker **self-bills the full interest** to clients and separately e-Invoices its handling fee. **[B Q10]**
- **Bursa listing-fee rebate** → refund note. **[B Q11]**
- **Remisier commission** → self-billed (SGL 9). **[B Q12]**
- **CDS fees recharged** by nominees → e-Invoice. **[B Q13]**
- **SC levy:** follow the current flow; Bursa includes the collection on behalf. **[B Q14]**

**C. Unit trusts**
- **Subscription:** the UTF e-Invoices the investor. **Redemption:** the **UTF self-bills** the investor. Statement frequency is allowed. **[C Q1–2]**
- **Sales charges:** UTMC → IUTA → investors, each e-Invoicing the next. **[C Q3]**
- **Dividends:** UTF → IUTA, then IUTA → investors, both **self-billed**. **[C Q4]**
- **Management fees:** UTMC e-Invoices the UTF; the UTF e-Invoices investors for their apportioned share. Rebates go by CN/RN quoting the original UUID. **[C Q5]**
- **Fund of funds:** the local UTMC self-bills the foreign manager's fee and issues a **self-billed CN/RN** for foreign rebates. **[C Q6]**
- **No sales charge** → no e-Invoice (a nil one is optional). **[C Q7]**
- **PRS PPA fee** → the UTMC e-Invoices end investors. **[C Q8]**
- **Secrecy:** relevant description, no statement numbers. **[C Q9]**

**D. Money changers**
- **Sale of foreign currency** to an individual → a **positive** e-Invoice. **Purchase** from an individual → a **negative-valued** e-Invoice. Both may share one e-Invoice.
- **No request** → receipts plus consolidated.
- **Charges** go as a separate line. **[D Q1–2]**
- **Between changers:** the seller e-Invoices. **[D Q3]**
- **Buying from a foreign supplier** → self-billed. **[D Q4]**

**E. Pawnbroking**
- **Loan principal** → none. **Ticket charges and interest** on redemption or renewal → e-Invoice, or receipt plus consolidated. **[E Q1]**
- **Unredeemed pledge** (loan ≤ RM200) transferring to the pawnbroker → the pawnbroker **self-bills**. **[E Q2]**
- **Auction:**
  - if the pawnbroker buys → it self-bills the purchase and e-Invoices the interest and charges;
  - if a third-party bidder buys → the **bidder self-bills**. **[E Q3]**
- **Auction surplus**, whether held, returned or surrendered to the AGD → none. **[E Q4–5]**
- **Resale of pledged items** → e-Invoice, or receipt plus consolidated. **[E Q6]**
- **Year-end accrued interest** → none. **[E Q7]**

### 20.9 e-Commerce
See Section 15.

### 20.10 Donations or contributions (DON, 7 Jul 2025)

**When an e-Invoice is needed [A Q1–2]**
- Donations received need an individual or consolidated e-Invoice, **except**:
  - (a) **Religious institutions** set up exclusively for worship or the advancement of religion. This exception is **lost** if they are an **approved IOF** (s.44(6), 44(6B), 44(11B), 44(11C), 44(11D)) or run a **s.34(6)(h)** approved project.
  - (b) Any person receiving donations that are **not tax-exempt** under the ITA.
- **Monetary donations by any payment method:**
  - on request → individual e-Invoice;
  - otherwise → a **consolidated e-Invoice within 7 days after month-end**, listing receipt numbers.

**What needs no e-Invoice [A Q3–5]**
- **Donations in kind** → no e-Invoice.
- **Donors to unapproved charities** do not self-bill.
- **Places of worship:** none for donations, but **sales of goods or services do need e-Invoices**.

**Obligations that still apply [A Q6–7]**
- **Unapproved bodies** must still self-bill imports and foreign services under SGL 8.3.
- They must also give their details for Table 3.6 purchases.

**Registration and systems [A Q8–11]**
- **BRN:**
  - registered bodies use their ROS, SSM, BHEUU or other registration number;
  - unregistered bodies use the **stamp certificate number** of the governing document.
- **Branches** may use the head office TIN and BRN, or register their own.
- **Existing systems** or the MyInvois Portal may be used.

**Approved IOFs [B Q1–3]**
- If the donor asks, issue an **individual e-Invoice**. It **replaces the pre-printed official receipt**, with no prior approval needed.
- Otherwise, issue the pre-printed receipt **plus** a monthly consolidated e-Invoice.
- Other non-e-Invoice e-receipts need **separate HASiL approval**.

---

## 21. MyInvois Portal operations (PORTAL, 9 Mar 2026)

**Access**
- Access is via **MyTax** (https://mytax.hasil.gov.my/).
- **Sandbox:** https://preprod-mytax.hasil.gov.my/. Roles must be applied for separately for each environment. **[Q2]**

**Roles [Q3–4]**
- **Business Owner** (sole proprietor).
- **Company Director / Organisation Administrator.** The previous holder must terminate the role first.
- **Estate Administrator.**
- **Representatives** appointed in MyTax.
- Use **Switch Taxpayer** to reach the business profile.

**Representative types [Q5–14]**
- Types are **User**, **ERP** and **Intermediary**.
- Permissions: submit, cancel, reject, manage representatives/ERPs/intermediaries, edit visual templates.
- **Unlimited ERPs** may be registered. Client ID and secret can be regenerated.
- Intermediaries must be **businesses, not individuals**. They **cannot be deleted**; end them by setting the "Representation To" date.
- If the director changes, **all representatives must be reappointed**.
- **Logo:** PNG, 400×400 px, 10–250KB.

**Documents [Q15–21]**
- **No digital certificate** is needed on the Portal.
- One CN/DN/RN can carry **multiple UUIDs**. Customs references are separated by commas.
- **Search Recent:** 10-day window within the last 31 days. **Search All:** 31-day window within the past 2 years.
- **Export:** 100 documents.
- **Print** is available only for Portal-submitted documents, not API ones.

**Batch upload [Q22–33]**
- Excel template; may be renamed.
- Limits: ≤ 100 documents and ≤ 25MB per file; ≤ 1,000 drafts.
- **Mandatory worksheets:** Documents, DocumentLineItems, LineItemsTaxes, DocumentTotalTax.
- Fill **TotalNetAmount** to avoid "Document Not Available".
- Delete formatted empty rows.
- **UTC** timestamps apply.
- "Copy as Draft" works only for Portal and Mobile App documents.

**Visual templates [Q34–35]**
- Customisable for **all 8 document types**: logo, header, footer, and supplier/buyer/billing/payment/shipping/import-export details.

**Notifications [Q36–37]**
- Sent to the e-mails set in the **Taxpayer Profile** (separate several with ";", 250 characters maximum).
- Whitelist **@myinvois.hasil.gov.my** and **@hasil.gov.my**.

**Errors [Q38–42]**
- **"You have been blocked"** → report through the feedback form.
- **"Taxpayer not found"** for an intermediary → exact name, TIN or BRN mismatch.
- **ERR206** → buyer ID not in HASiL records.
- **ERR205** → general TIN with "NA" is allowed only for consolidated e-Invoices (code 004).
- **"ArrayItem Not Valid #/Invoice[0]"** → zero-based index of the faulty invoice; validation stops at the first error.

---

## 22. MyInvois e-POS (EPOS, 9 Jan 2026)

**What it is:** a **free** POS from HASiL for micro and small businesses. It handles sales recording, inventory, reports, receipts and e-Invoices, and has an **offline mode** that syncs automatically. **[Q1, Q6, Q10–11, Q35]**

**Eligibility (current) [Q2]:**
- (i) The owner or director is a **Malaysian citizen**.
- (ii) The business operates in Malaysia.
- (iii) Annual revenue **up to RM5m**.

| Version | Eligibility threshold |
|---|---|
| 30 Apr 2025 (pilot) | < RM250k |
| 7 Dec 2025 | < RM1m |
| 12 Dec 2025 | < RM2m |
| 9 Jan 2026 | up to RM5m |

**Who cannot use it:** tax agents, service providers and intermediaries. It is for businesses dealing **directly with customers at the premises**. Businesses with an existing POS may use it if they are eligible. **[Q4–5]**

**Features and costs:**
- Needs internet and a device. Printers and scanners are optional; hardware costs are borne by the business. **[Q7–9]**
- **No payment-gateway integration.** **[Q14]**
- Scans the **customer's Taxpayer QR code**, generated from the MyInvois Portal. **[Q15]**
- No transaction limit; runs 24 hours. **[Q16]**
- It may be combined with the Portal, provided there is **no duplication**. **[Q12]**

**Registration:**
- Register **in person at a main HASiL office** (not satellite or UTC offices). Approval takes about **3 working days**. **[Q17–20]**
- Documents needed: name, IC, TIN, e-mail, business registration certificate (if any). **[Q19]**
- Owners without a BRN need a TIN in their own name. **[Q22]**
- **One e-mail per business.** Only **one** sole proprietorship per owner may register. **[Q26]**
- **Over RM5m** → no longer eligible. HASiL will notify the business and give it time to move to a commercial POS. Later revenue changes do not alter the eligibility status that has been set. **[Q28]**
- **Client ID and Client Secret expire.** Regenerate them in the MyInvois Portal and update them in e-POS; otherwise sales still record but e-Invoices are not transmitted. **[Q29–31]**

**Roles and audit:** Supervisor, POS Cashier, Accountant, Auditor; an **audit log** is kept. **[Q32–33]**

**Help:**
- e-POS helpdesk **03-8680 3767**, Mon–Fri 9am–6pm.
- Live chat and feedback form; microsite https://www.hasil.gov.my/myinvoisepos. **[Q38–39]**

---

## 23. Tax incentives for e-Invoice adoption **[GFAQ Q24]**

| Incentive | Law | Detail | Period |
|---|---|---|---|
| Deduction for ESG-related spending, including **consultation fees for developing customised e-Invoice software** by MSMEs | P.U.(A) 193/2025 | Up to **RM50,000 per YA** | YA2024–YA2027 |
| **ACA** on ICT equipment and software for e-Invoice | P.U.(A) 162/2026 | Claim period cut from 3 to **2 years** (IA 20%, AA 40%) | YA2024–YA2027 |
| ACA on **customised software development cost** | P.U.(A) 163/2026 | As above | YA2024–YA2027 |
| ACA on the above, further cut to **1 year** | *Gazette order pending* | 2 years → 1 year | YA2026–YA2027 |

---

## 24. Systems, security and data **[GL 3.0; SGL 15; GFAQ Q144–147]**

- **ISO/IEC 27001:2022** (ISMS) and **ISO 22301:2019** (BCMS).
- Encryption, authentication, access control, firewalls and logging.
- Compliance with the **LHDNM Cyber Security Policy** and the government cloud-computing security circular.
- **PDPA disapplied:** s.82C(11) ITA.

---

## 25. Contacts **[GFAQ Q23]**

| Channel | Detail |
|---|---|
| General e-Invoice queries | **myinvois@hasil.gov.my** |
| SDK / technical feedback | https://feedback.myinvois.hasil.gov.my |
| e-Invois HASiL Help Desk | **03-8682 8000**, 24 hours, Mon–Sun |
| Live chat | https://www.hasil.gov.my/en/e-invoice/contact-us |
| SDK microsite | https://sdk.myinvois.hasil.gov.my |
| Peppol (MDEC) | clic@mdec.com.my, https://mdec.my/ |
| e-POS helpdesk | 03-8680 3767 |
| Engagement sessions | via the relevant HASiL state office **[GFAQ Q22]** |

---

## 26. Consultant triage checklist (use on every client question)

1. **Is the issuer in scope on the transaction date?**
   - Find the phase from FY2022/YA2022 turnover (pro-rate if needed).
   - Check new-business rules.
   - Check the **< RM3m exemption** and the **1.6.10 group tests**.
   - Check for exempt persons (GL 1.6.1).
2. **Is the income or expense excluded?** (GL 1.6.7: employment, pension, alimony, zakat, listed securities, certain dividends and share disposals, certain donations.)
3. **Who issues?** The supplier normally. The **buyer (self-billed)** only for the SGL 8.3 list, which **cannot be extended**.
4. **Which document?** Invoice / CN / DN / RN, or a self-billed variant. Return of money → RN, except wrong payments, overpayments and deposits.
5. **Can it be consolidated?**
   - Has the buyer requested one?
   - Is it a **Table 3.6** activity (motor vehicle, flight tickets, construction contractor, betting pay-outs, agent payments, **> RM10k**, electricity, telco postpaid and internet)?
   - Is it a self-billed exception under SGL 3.6.5?
   - Is the taxpayer still in its **relaxation period** (for the up-to-RM5m tier, until 31 Dec 2027)?
6. **Buyer and supplier identifiers:**
   - TIN, or the individual ID concession.
   - General TINs: 010 (public / ID-only), 020 (foreign buyer), 030 (foreign supplier, self-billed), 040 (government).
   - Otherwise "NA" or "00000".
7. **Timing:**
   - Normal → current practice.
   - Consolidated → **within 7 days after month-end**.
   - Imported goods → **end of the 2nd month after clearance**.
   - Imported services → **end of the month after the earlier of payment or invoice**.
   - Foreign income → **end of the month after receipt**.
   - Capital transactions → agreement / approval / completion.
8. **Corrections:**
   - Within **72 hours** → cancel (supplier) or request rejection (buyer).
   - After that → CN/DN/RN quoting the original UUID(s).
   - Historic non-compliance → **SVDP (until 31 Dec 2027)**: SVDP 1.2/1.3, per month, > RM10k individually.
9. **Industry overlay:** check the relevant industry FAQ in Section 20.
10. **Next actions for the client:**
    - Set up MyTax/MyInvois roles.
    - Choose a mechanism (Portal / API / Peppol / e-POS).
    - Map the 55 fields and classification codes (SDK).
    - Set up the month-end consolidation routine.
    - Set up the self-billed calendar.
    - Store UUIDs against ledger entries.
    - Keep records for 7 years (s.82 ITA).
11. **Escalate to HASiL** for novel structures or contentious classifications: myinvois@hasil.gov.my or the feedback form. **Never invent a paragraph or Q&A reference.**

---

## 27. Known gaps and caveats in this library

- The **text of P.U.(A) 265/2024 and s.82C ITA** is not in the library. Positions on them are drawn from the GFAQ only.
- **Classification codes, MSIC codes, tax-type codes and API specifications** live in the **SDK**, not here. Codes quoted above (004, 014, 015, 022, 024, 026) appear in the FAQs.
- **Luxury goods and jewellery** no-consolidation details are still "to be released". **[SGL Table 3.6]**
- The **FIN FAQ B Q1** cites "GL 1.6.8" for the exchange-traded securities exemption; in GL v4.8 that exemption sits at **1.6.7(f)**.
- **Older industry FAQs** (Telco and e-Commerce, Dec 2023; Petroleum, Jan 2024; Healthcare and Tourism, Jun 2024) predate later SGL changes such as the Table 3.6 additions and the RM10k rule. Read them **together with** the current SGL.
- **The library is newer than some internal briefings:**
  - the threshold is **RM3m**, not RM500k;
  - there are **4 phases**, not 5;
  - e-POS eligibility is **up to RM5m**, not RM750k.
  Always cite from the latest PDFs listed in Section 0.

*End of knowledge base.*
