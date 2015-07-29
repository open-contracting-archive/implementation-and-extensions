# OCDS: Extractive Industries and Land Extension

By [James McKinney](http://opennorth.ca/team/) for the [Open Contracting Partnership](http://www.open-contracting.org/). Originally [available for comment on Google Docs](https://docs.google.com/document/d/1uPXFXTRXXc2zi3vo_arrWm_c_gW6KSPG5aAlD2ri5rw/edit#).

This extension proposal covers requirements within the [extractive industries](http://www.open-contracting.org/extractives) and [land](http://www.open-contracting.org/land) sectors.

This report first documents real, specific [use cases](#heading=h.ywbwky4eev0e), from which it derives [requirements](#heading=h.3lkcorjhisc8); no requirement is without a use case to ground, scope and support it. It then proposes how the Open Contracting Data Standard (OCDS) can fulfill each requirement. A third and final section addresses [out-of-lifecycle requirements](#heading=h.q5knicldsyks), which are not well suited to OCDS.

Use cases are numbered, e.g. "UC1," and requirements are labeled, e.g. “R-Country” for easier reference later. Use cases are not presented in any particular order. You may wish to skip the use cases and jump directly to the [requirements](#heading=h.3lkcorjhisc8).

# Use cases

## UC1: The decision to extract

Publish What You Pay describes this use case as enabling citizens in resource-rich countries "to influence decision-making around the decision to extract, extraction rights and to influence ... the terms and conditions of deals and contracts signed between governments and EI companies" (Publish What You Pay, 201?a).

See the **R-DocumentClassification** requirement in the **[Equitable Origin EO100 Standar**d](#heading=h.jncpqjbnggvg) and **[ResourceContracts.or**g](#heading=h.dkg3i97ynakr) use cases below. In addition to the details in those sections, the documents relating to the decision to extract may deal with issues of:

* consultation process

* free, prior and informed consent

* impact assessments for the economy, alternate livelihoods, food security, health, etc.

* community criteria for "no go" zones

* territorial rights and land claims

* job creation commitments

* resettlement and compensation plans

* community development agreement

* impact and benefit agreement

## UC2: The content of the contract should be accessible to the citizenry

"The content of the contract, lease or concession agreement should be accessible to the citizenry" (Publish What You Pay, 201?b).

Additionally, governments benefit from knowing what contracts companies have agreed to and from comparing contracts from different companies and in different jurisdictions.  Companies benefit from knowing what contracts governments have agreed to and from having evidence of their contract’s existence in case of regime change.

**R-ContractDocument: **Provide a link to the contract document.

Global Witness recommends that "Contracts should provide for the publication of all information required for public monitoring and tracking of mining revenues including estimated and actual production rates" (Global Witness, April 2012). ResourceContracts.org’s Microsoft Excel template, discussed below, includes a field for “Expected production”.

**R-ExpectedProduction:** Provide an estimate of the production.

## UC3: Who are the parties to the contract?

"Corruption and patronage in the contracting and licensing of mining concessions impede efficient tax administration and undermine the popular legitimacy of foreign-owned mining operations" (Besada, 2013). The EITI Standard encourages the disclosure of the beneficial owners of companies, in order to curb corruption and patronage. However, beneficial ownership is not covered by resource contracts, but by legislation creating a new obligation on companies, and it is frequently disclosed through official company registers and not through contracts. Contracting data is necessary, but insufficient, in fulfilling this use case.

**R-Awardee** and **R-Government:** The parties to a contract should be reported.

## UC4: Did a government receive what it is due from a contract?

"The fiscal terms contained within the contracts dictate how much companies will pay. With contract transparency, citizens can assess whether companies are paying what they ought to pay" (Publish What You Pay, 201?b). Some classes of resource revenue, however, are not covered by resource contracts; for example, corporate taxes are covered by tax legislation, and dividends are covered by shareholder agreements. (NOTE:  Along the same lines, the 2012 SEC rules state, "A resource extraction issuer generally need not disclose dividends paid to a government as a common or ordinary shareholder of the issuer as long as the dividend is paid to the government under the same terms as other shareholders" (Securities and Exchange Commission, 2012).) Contracting data is necessary, but insufficient, in fulfilling this use case.

Company-reported payments may not match government-reported receipts (Boas, 2013). Similarly, government-reported receipts may not match receipts reported by accountability institutions (Adam, 2014).

**R-TransactionReconciliation:** In order to identify discrepancies in reporting, companies, governments, and accountability institutions must publish OCDS data, and it must be possible to reconcile which company payments match which government receipts, and which receipts match across reports by governments and accountability institutions. All these entities are unlikely to adopt a common identifier scheme for transactions. An alternate mechanism should allow for transaction reconciliation.

A revenue agency may request that companies make payments in $US dollars, while reporting receipts in the local currency, as in Ghana; however, the companies may only report payments in $US dollars (Boas, 2013). Currency translation may introduce discrepancies between reported payments and receipts.

**R-TransactionCurrency:** In systems in which multiple currencies are in regular use, it should be possible to include transaction amounts in multiple currencies.

Royalty payments are based on the amount of the resource produced and the unit value of the resource at the time of production. The two figures are necessary to reconcile production with payments. Companies may lower royalty payments by using a resource’s hedge price instead of its spot price (Boas, 2013).

**R-TransactionVolume** and **R-TransactionUnit:** In addition to reporting the transaction amount, the volume produced and/or the unit value of the resource should be reported in relevant transactions.

For royalties, some governments apply a flat rate, while others apply a tiered rate (Global Witness, 2014). For example, in the production sharing agreement between the Government of the Republic of Uganda and Tullow Uganda Limited in respect of Exploration Area 1, the royalty on the gross total daily production is 5% for the first 2,500 barrels, 7.5% for the next 2,500 barrels and so on up to a maximum rate of 12.5% (Government of the Republic of Uganda and Tullow Uganda Limited, 2012).

**R-TransactionRate:** For some classes of transactions, in simple cases, it is relevant to declare the rate, in order to ease the reconciliation of production with payments. In complex cases, a standard model may not be achievable, in which case a reference to the contract may be an acceptable alternative.

Although regulations may, for example, establish a quarterly payment frequency for royalties, companies may nonetheless make payments at a different frequency. Since royalty payments are based on production, an unclear periodicity makes it difficult to match royalty against production (Boas, 2013). Periodicity can also indicate the degree to which payments are aggregated over time; for example, the SEC 2012 rules require reporting on an annual basis.

**R-TransactionPeriodicity:** For some classes of transactions, it is relevant to declare the period for which the transaction is made.

## UC5: How did the government manage and use resource revenues?

Most of  this use case’s requirements are better fulfilled by budget and expenditures data than by contracting data. However, some requirements are relevant to contracting.

Legislation may require a government to allocate receipts to, for example, a sovereign development fund instead of its general non-tax revenue account. When new legislation comes into force, receipts may be allocated to an incorrect account (Adam, 2014). Unless a government discloses the accounts to which receipts are allocated, it is impossible for citizens to track revenue payments into the national budget (Global Witness, 2014).

**R-TransactionAccount:** Transactions should identify the account in which the deposit is made.

## UC6: EITI Standard

According to the IETI Standard, "The term license in this context refers to any license, lease, title, permit, or concession by which the government confers on a company(ies) or individual(s) rights to explore or exploit oil, gas and/or mineral resources" (EITI International Secretariat, 2013). Its requirement 3.9 requires the disclosure of:

**R-Awardee:** "License holder(s)."

**R-LocationSpatial:** "Coordinates of the license area."

**R-ApplicationDate:** "Date of application"

**R-AwardDate:** "date of award"

**R-ContractPeriod:** "duration of the license"

**R-Resource:** "In the case of production licenses, the commodity being produced."

Its requirement 3.10 requires the disclosure of:

**R-ProcessDescription:** "a description of the process for transferring or awarding the license"

**R-AwardCriteria:** "the technical and financial criteria used"

**R-Awardee:** "information about the recipient(s) of the license that has been transferred or awarded, including consortium members where applicable"

**R-Exceptions:** "any non-trivial deviations from the applicable legal and regulatory framework governing license transfers and awards"

Furthermore, requirement 3.10 specifies that "Where licenses are awarded through a bidding process during the accounting period covered by the EITI Report, the government is required to disclose":

**R-Candidates:** "the list of applicants"

**R-AwardCriteria:** "the bid criteria"

Its requirement 3.12 specifies that:

**R-ContractDocument:** "Implementing countries are encouraged to publicly disclose any contracts and licenses that provide the terms attached to the exploitation of oil, gas and minerals."

## UC7: Securities and Exchange Commission (SEC) Disclosure of Payments by Resource Extraction Issuers (2012)

Section 1504 of the Dodd-Frank Wall Street Reform and Consumer Protection Act – the Cardin-Lugar Amendment – adds a Section 13(q) to the Securities Exchange Act of 1934, which requires the SEC to issue rules relating to the disclosure of payments by resource extraction issuers to governments.

Under Item 2.01 "Disclosure requirements regarding payments to governments" of Section 2 “Resource Extraction Issuer Disclosure,” the 2012 SEC rules require the disclosure of:

**R-TransactionAmount** and **R-TransactionClassification:** "The type and total amount of such payments made for each project of the resource extraction issuer relating to the commercial development of oil, natural gas, or minerals; The type and total amount of such payments made to each government; The total amounts of the payments, by category listed in (c)(6)(iii)."

**R-TransactionCurrency:** "The currency used to make the payments"

**R-TransactionPeriodicity:** "The financial period in which the payments were made"

**R-BusinessSegment:** "The business segment of the resource extraction issuer that made the payments"

**R-TransactionRecipient** and **R-Country:** "The government that received the payments, and the country in which the government is located"

**R-Project:** "The project of the resource extraction issuer to which the payments relate"

## UC8: EU Accounting and Transparency Directives

The EU disclosure rules form Chapter 10 "Report on payments to governments" of the revised EU Accounting Directive and Article 6 “Report on payments to governments” of the revised EU Transparency Directive.

The EU Accounting Directive requires the disclosure of:

**R-TransactionAmount** and **R-TransactionClassification:** "the total amount of payments made to each government; the total amount per type of payment as specified in points (5)(a) to (g) of Article 41 made to each government; where those payments have been attributed to a specific project, the total amount per type of payment as specified in point (5)(a) to (g) of Article 41, made for each such project and the total amount of payments for each such project." See **[UC13: Classification of transaction**s](#heading=h.yt1f33vpcu8u) for a discussion of payment types, including how the EU Accounting Directive relates to the EITI Standard.

**R-TransactionVolume** and **R-TransactionInKind:** "Where payments in kind are made to a government, they shall be reported in value and, where applicable, in volume. Supporting notes shall be provided to explain how their value has been determined."

## UC9: Equitable Origin EO100 Standard

The EO100 Standard is a certification standard for responsible business practices.

**R-DocumentClassification:** Its provisions describe several documents relating to an extractive industries or land contract:

* 1.6 "Operator shall fully, accurately and freely disclose all social and environmental policies, activities and performance in accordance with recognized sustainability reporting best practices."

* 2.16 "Operator shall identify and publicly report the environmental and social risks and impacts on communities within the project area of influence."

* 4.7 "Operator shall publicly report information related to its activities concerning Indigenous Peoples."

* 5.15 "Operator shall publicly report data related to environmental impacts and mitigation activities."

* 6.5 "Operator shall commission independent Economic, Environmental and Social Impact Assessments for each phase of the project using a recognized international standard to identify impacts and appropriate mitigation measures at each stage of the project life cycle, from exploration through closure."

* 6.6 "Operator shall identify and take steps to avoid and/or mitigate indirect and cumulative impacts, in consultation with relevant stakeholders."

## UC10: ResourceContracts.org

ResourceContracts.org provides a Microsoft Excel template "to assist in annotating contracts for large-scale oil, gas, mining, agriculture and forestry deals" (ResourceContracts.org, 2014). Its fields include:

**R-Country:** "Country"

**R-Awardee:** "Local company name"

**R-OrganizationAddress:** "Company headquarters"

**R-OrganizationWebsite:** "Company website"

**R-DocumentClassification:** "Type of document/right," “Local development agreement,” “Social, environmental and/or human rights impact assessments, as well as related management plans,” “Feasibility studies,” “business plan”

**R-Project:** "Project title"

**R-LocationIdentifier:** "Name and/or number of field, block or deposit"

**R-LocationSpatial:** "Location, longitude and latitude"

**R-LocationClassification:** "Onshore vs Offshore." Note that Brazil classifies locations as “ultra deep water, deepwater, shallow water, onshore” (Morgan, 2014). 

**R-AwardDate:** "Date of issue of title/permit" and “Year of issue of title/permit”

**R-Awardee:** "Name of company executing the document"

**R-Government:** "State agency, national company, ministry executing the document"

**R-ContractDateSigned:** "Date of contract signature" and “Year of contract signature”

**R-ContractPeriod:** "Term"

**R-Resource:** "Type of resources"

**R-TransactionClassification:** "Mining tax / royalty tax," “Production share,” “Service Agreement - Fee to developer / contractor,” “Fixed fee for grant and renewal of license,” “Surface fees,” and “Bonuses”

**R-ContractLanguage:** "Language"

ResourceContracts.org provides a code list for "Type of document/right," including:

* Concession

* Lease

* Production Sharing Agreement

* Service Agreement

* Investment Incentive Agreement

* Memorandum of Understanding

* Forest Management Contract

* Land Concession Agreement

* Land Lease Agreement

* Land Sale Agreement

* Timber Sale Contract

**R-DocumentClassification:** A code list should ease the discovery of relevant documents.

## UC11: Revenue Development Foundation Online Data Repository

The [Revenue Development Foundation Online Data Repository for Sierra Leone](http://sierraleone.revenuesystems.org) publishes metadata for each contract and license: 

* **R-ApplicationTitle** and **R-ContractTitle:** "Code"

* **R-ApplicationDate:** "Date Of Application"

* **R-Government:** "Issuing Office"

* **R-Applicant **or **R-Awardee:** "Company"

* **R-ApplicationItem** and **R-ContractType:** "License Type"

* **R-ApplicationStatus** and **R-ContractStatus:** "Status"

* **R-ContractPeriod:** "Date Approved"

* **R-ContractPeriod:** "Date Expired"

* **R-LocationSize:** "Area"

* **R-LocationName:** "Locations"

* **R-Resource:** "Resources"

* **R-LocationSpatial:** "GIS"

**R-ApplicationTransaction:** Within its "Payments" tables, it publishes:

* **R-TransactionDate:** "Date"

* **R-TransactionClassification:** "Type"

* **R-TransactionReconciliation:** "Receipt"

* **R-TransactionAmount:** "Amount"

**R-ApplicationItem** and **R-ContractType: **The possible values of "License Type" are:

* Reconnaissance

* Excl. Prospecting-Precious

* Excl. Prospecting-NonPrecious

* Exploration

* Exploration-Precious

* Exploration-NonPrecious

* Small Scale

* Large Scale

**R-ApplicationStatus** and **R-ContractStatus: **The possible values of "Status" are:

* "Canceled"

* "Active License"

* "Approval"

* "Registration"

* "Validation"

* "Payment"

* "Suspended"

* "Expired"

* "Under Review"

* "Archived"

**R-TransactionClassification: **The possible values of payment type include:

* Application Fee

* Primary Licence fee

* Annual Licence fee

## UC12: OpenOil

The [OpenOil](http://repository.openoil.net/wiki/Main_Page) repository collects oil contracts and concessions data and publishes metadata for each contract:

**R-Country:** "Jurisdiction"

**R-LocationName:** "Contract Area"

**R-ContractTitle:** "Title"

**R-Awardee:** "Contractor(s)"

**R-ContractDateSigned:** "Signed"

**R-ContractDocument:** "Original Contract Source"

**R-Publisher:** "Disclosure Mode"

**R-ContractLanguage:** "Language"

## UC13: Classification of transactions

Requirements 4.1(b) and (c) of the EITI Standard describes revenue streams, including:

* The host government’s production entitlement (such as profit oil)

* National state-owned enterprise production entitlement

* Profits taxes

* Royalties

* Dividends

* Bonuses, such as signature, discovery and production bonuses

* Licence fees, rental fees, entry fees and other considerations for licences and/or concessions

* Sale of the state’s share of production or other revenues collected in-kind

The payment types in the 2012 SEC rules and EU Accounting Directive are based on those of the EITI Standard, and they also include "**payments for** **infrastructure improvements**." The 2012 SEC rules explain that “a resource extraction issuer must disclose payments […] that it has made […]  for infrastructure improvements if it has incurred those payments, whether by contract or otherwise, to further the commercial development of oil, natural gas, or minerals. [...] If an issuer is obligated to build a road rather than paying the host country government to build the road, the issuer would be required to disclose the cost of building the road as a payment to the government.” The EITI Standard discusses “infrastructure provisions and barter arrangements” in its requirement 4.1(d).

The 2012 SEC rules do not require companies "to disclose social or community payments, such as payments to build a hospital or school, because it is not clear that these types of payments are part of the commonly recognized revenue stream." The EITI Standard discusses "**social expenditures**" in its requirement 4.1(e).

The 2012 SEC rules do not require companies "to disclose payments made for transporting oil, natural gas, or minerals for a purpose other than export." Payments for purposes of export may include export taxes or related duties, as in Guinea, Liberia and Sierra Leone EITI reports. The EITI Standard discusses **transportation** in its requirement 4.1(f). South Sudan’s Petroleum Act, 2012 includes **customs duties**.

The production sharing agreement between the Government of the Republic of Uganda and Tullow Uganda Limited in respect of Exploration Area 1 contains a **second royalty** based on the project’s cumulative production, which Global Witness describes as a "fairly unusual revenue provision in an oil contract" (Global Witness, 2014).

The Petroleum Revenue Management Act 2011 (Act 815) of Ghana additional includes "**capital gains tax** derived from the sale of ownership of exploration, development and production rights," which is a type of profits tax.

The Ghana Extractive Industry Transparency Initiative also includes "**property rate**," which are taxes or levies on improvements to land (e.g. buildings).

**R-TransactionClassification:** As evidenced above, several use cases relating to payment disclosures require the classification of transactions.

## UC14: Status of license or contract

Global Witness describes cases in which mining operations may be suspended (Global Witness, November 2012) or in which licenses may be renewed (Global Witness, 2014).

**R-ContractStatus:** The contract status property should allow for suspensions and renewals.

## UC15: Natural Resource Governance Institute project registry

The anticipated registry will make available, in a machine-readable format, project-level information from EITI reports and other sources.

**R-Source:** "report_id: Report id from eg. EITI or the like" and "source_uri: Link to the source of the data"

**R-TransactionPeriodicity:** "year: The year of the filing"

**R-Country:** "country: Country name" and "country_id: Following ISO 3166 Alpha-2, which is a two letter code."

**R-Resource:** "commodity_type: The extraction method / commodity type should be assigned based on the International Standard Industrial Classification of All Economic Activities (ISIC), Rev.4."

**R-Project:** "project_name: Name of the project as it appears in report" and "project_id: Project ID as assigned by the national or local government" and "project_uri: The project uri will consist of [ISO-3166] - [projectID] as published on resourceprojects.org/Project-Uri"

**R-Awardee:** "company_name: The name of the company as registered at the national company register"

**R-OrganizationIdentifier:** "company_id: The company number as issued by the Companies House. In the case that a company has obtained a Legal Entity Identifier (LEI), this should be submitted."

**R-ContractTitle:** "license_name: The name of the license related to the project"

**R-ContractID:** "license_id: The ID of the license related to the project"

**R-TransactionRecipient:** "government: The government entity receiving the project payment"

**R-OrganizationIdentifier:** "organisation_identifier: The Organisation Identifier as issued by the IATI Technical Secretariat"

**R-TransactionVolume:** "production_volume: The production amount"

**R-TransactionUnit:** "commodity_unit: The unit indicated how the commodity is measures (eg. barrels). Values can for example include: Bbls, m3, Mt, Kg, or Oz"

**R-TransactionClassification:** "payment_type: See the proposed list for payment types"

**R-TransactionCurrency:** "currency: Following ISO 4217"

**R-TransactionReconciliation: **"payment_received_by_government: Payment as reported by the government recipient" and "payment_by_company: Payment as reported by the company" 

**R-LocationSpatial: **"project_area: geojson or XML"

Note that this use case recommends using Legal Entity Identifiers (LEI) for the identifier or additionalIdentifiers properties of the Organization class.

## UC16: South Sudan Petroleum Act, 2012

Under Section 17 Reconnaissance Licenses of Chapter VII Reconnaissance:

* **R-InitiationType**, **R-LocationName** and **R-EligiblityCriteria:** "the Ministry may [...] announce an open, transparent, non-discriminatory and competitive public tender to grant a reconnaissance licence for a defined geographical area to a person with the requisite technical competence, sufficient experience, history of compliance and ethical conduct, financial capacity and any other requirements stipulated by the Ministry to adequately fulfil the requirements of the licence."

* **R-ContractPeriod:** "A reconnaissance licence shall be granted for a period not exceeding one year, unless otherwise stipulated by the Ministry."

Under Section 18 Tendering Procedure and Qualification Requirements of Chapter VIII Exploration and Production Sharing Agreements:

* **R-InitiationType:** "Petroleum agreements shall be entered into following an open, transparent, non-discriminatory and competitive tender process conducted in accordance with applicable law governing public procurement."

* **R-LocationName** and **R-AwardCriteria:** "The call for tenders shall define the relevant contract area and clearly state the applicable award criteria."

* **R-EligiblityCriteria:** "Petroleum agreements may only be entered into with a company or group of companies with the requisite technical competence, sufficient experience, history of compliance and ethical conduct and financial capacity to adequately fulfil all obligations of the petroleum agreements, applicable law and any other requirements stipulated by the Ministry."

Under Section 19 Petroleum Agreement:

* **R-InitiationType:** "The Ministry shall negotiate a petroleum agreement [...]."

* **R-LocationName:** "The area covered by a petroleum agreement shall be specified in the agreement and may comprise one or more blocks or parts of blocks."

Under Section 21 Operator:

* **R-EligiblityCriteria:** "The operator shall be a person having the requisite technical competence, sufficient experience, history of compliance and ethical conduct and financial capacity and any other requirements stipulated by the Ministry to adequately fulfil the duties of operator." 

Under Section 26 Exploration Period of Chapter IX Exploration and Relinquishment:

* **R-ContractPeriod:** "Petroleum agreements shall provide for an exploration period not exceeding six years from the effective date of the agreement."

Under Section 31 Plan for Development and Operation of Chapter X Development and Production:

* **R-DocumentClassification:** "If a declaration of commerciality is made, the contractor shall submit to the Ministry a plan for development and operation of the discovery for approval."

Under Section 37 Licence to Install and Operate Transportation Systems of Chapter XI Transporation, Treatment and Storage:

* **R-EligiblityCriteria:** "The Ministry shall grant a licence on the basis of an evaluation of the application, including the environmental and social impact assessment, and the technical competence, experience, history of compliance and ethical conduct and financial capacity of the applicant and the contractor, as well as safety related aspects."

Under Section 39 Decommissioning Plan of Chapter XII Cessation of Petroleum Activities:

* **R-DocumentClassification:** "A licensee or a contractor who owns or operates a petroleum facility shall submit a decommissioning plan for the facilities, including wells, to the Ministry before the applicable licence or petroleum agreement expires or is terminated or before use of the facility ceases permanently."

Under Section 41 Decommissioning Fund:

* **R-TransactionAccount:** "The licensee and the contractor shall establish a decommissioning fund immediately after the approval of a plan for development and operation or the granting of a licence for transportation systems, as prescribed in the regulations. The decommissioning fund shall be sufficient to cover the full costs of decommissioning."

Under Section 52 Health and Safety Management Plan of Chapter XIV Health, Safety and Protection of the Environment:

* **R-DocumentClassification:** "Prior to the commencement of petroleum activities, a licensee or a contractor shall prepare a health and safety management plan adequate for the systematic implementation of health and safety requirements pertaining to the petroleum activities to be conducted, the facilities to be used and the site."

Under Section 59 Strategic Environmental Assessment, Environmental and Social Impact Assessments, which several other sections reference:

* **R-DocumentClassification:** "The Ministry, in consultation with the ministry responsible for the environment, shall initiate and coordinate a strategic environmental assessment prior to the opening of a new area pursuant to Section 15 of this Act." “The Ministry shall, in consultation with the ministry responsible for the environment, coordinate an environmental and social impact assessment that shall be initiated and undertaken by the licensee or contractor and linked to the strategic environmental assessment [...].” “The licensee or contractor shall, concurrently with the environmental and social impact assessment, conduct a comprehensive environmental baseline study that provides for an understanding of the existing environment in the contract area [...].”

Under Section 60 Environmental Management Plan:

* **R-DocumentClassification:** "Prior to the commencement of petroleum activities, a licensee or a contractor shall prepare an environmental management plan for the systematic implementation of the environmental requirements for the petroleum activities." “An environmental audit shall, when necessary, be performed on the environmental management plan by the ministry responsible for the environment or an expert on its behalf, at the expense of the licensee or contractor.” “Annual reports should be made to the Ministry and the ministry responsible for the environment on implementation of the environmental management plan.”

Under Section 63 Procurement of Goods and Services of Chapter XV Procurement of Goods and Services and Local Content:

* **R-InitiationType:** "Subject to the provisions in this Chapter, procurement of goods and services that exceed a prescribed threshold value shall follow open, transparent, non- discriminatory and competitive tendering procedures as prescribed in the regulations."

Under Section 65 Local Employment and Training:

* **R-DocumentClassification:** "A licensee or contractor carrying out petroleum activities shall, in consultation with the Ministry, prepare and implement plans and programmes to train South Sudanese nationals in job classifications and in all aspects of petroleum activities, including plans and programmes for post-graduate training and scholarships."

Under Section 67 Local Content Plans and Reports:

* **R-DocumentClassification:** "A licensee or contractor shall prepare and implement annual local content plans that are adequate for the systematic implementation of the requirements set out in Sections 64 to 66 of this Act and the regulations." “The licensee or contractor shall submit and publish an annual report describing the initiatives regarding local content taken in the preceding year and their results.”

Under Section 79 Ministerial disclosure and publication of Chapter XVII Data and Information, Record-Keeping, Reporting and Public Access to Information:

* **R-AwardRationale:** "The Minister shall make available to the public, both on the Ministry website and by any other appropriate means to inform interested persons: [...] justification of award of petroleum agreements [...]" 

Under Section 82 Community Development Plan and Fund of Chapter XVIII Miscellaneous Provisions:

* **R-DocumentClassification:** "The Ministry shall provide a community development plan, after consultation with local communities in the contract area."

* **R-TransactionAccount:** "A licensee or contractor shall establish a fund called the Community Development Fund to finance the plan."

## UC17: 2013 Brazil oil block bidding round

**R-EligiblityCriteria:** A 2013 Brazil bidding round had different eligibility criteria depending on the location and complexity of the oil block (Morgan, 2014). Criteria "included minimum net asset requirements for bidders based on block depth, and bidder qualification was scored on prior operational experience with each depth, as well as the amount invested in exploration activities and production volumes over the previous five years" (Morgan, 2014).

**R-AwardCriteria:** "The bids of eligible companies were scored based on the cash bonus offered, the exploration work program and its value, and the local content commitment (a percentage of the exploration and development and production phase that will use national services and equipment)" (Morgan, 2014).

## UC18: IMF Template for Government Revenues from Natural Resources

The main contribution of the IMF Template to this document is the thorough analysis of transaction types and mapping to the Government Finance Statistics Manual (GFSM) 2001.

**R-Resource:** See Table 1: Proposed Natural Resource Products from the Central Product Classification (Class Level), which is a subset of the United Nations’ [Central Product Classification (CPC) Ver.2](http://unstats.un.org/unsd/cr/registry/cpc-2.asp).

**R-BusinessSegment:** See Table 2: Industries Engaged in Natural Resource Activity from the ISIC Rev 4.

**R-TransactionClassification:** See Table 3. Template—Government Revenues from Natural Resources and Appendix I: *GFSM 2001* Classification of Revenue.

Under Appendix II: Report Form for Government Revenues from Natural Resources:

* **R-Country:** "Country Name"

* **R-TransactionCurrency:** "Currency"

* **R-Government:** "Level of Government"

* **R-Resource:** "Specify natural resources from which revenues are received"

* **R-TransactionInKind:** "If any revenues are received in kind please provide information separately for the corresponding category."

Appendix III provides informative examples of the implementation of the template.

# Requirements

The requirements below follow from the use cases above. Stakeholders should be consulted to confirm and validate any proposed additions or changes to the Open Contracting Data Standard. A preliminary list of stakeholders is included in Appendix 2.

OCDS is used to describe unique contracting processes. The first step towards publishing open contracting data is to identify contracting processes. OCDS currently focuses on procurement contracts, where each tender identifies a unique contracting process. In the extractive industries and land sectors, on the other hand, a confidential negotiation process may produce a contract, i.e. no public information is available before the publication of the contract. In such cases, each contract should identify a unique contracting process.

The requirements below may require renaming properties, notably Release.buyer and Award.suppliers. To minimize the effort required by implementers to update to the next release, a proposal is to deprecate the old terms in the next major release (2.0), and remove the old terms in the following major release (3.0). Data implementing 2.0 may use either the old terms or the new terms. Data implementing 3.0 must use the new terms. This proposal can be formalized as a deprecation policy.

The changes to OCDS discussed below are summarized in a [spreadsheet](https://docs.google.com/a/opennorth.ca/spreadsheets/d/1nniKoHvLdpctJq19l8-VYxg7rL4baQjdf-8ZMqT1_kQ/edit#gid=0).

## Release

### R-Project

The EITI Standard provides no definition or guidance for the term "project."

The EU Accounting Directive defines a project as "the operational activities that are governed by a single contract, license, lease, concession or similar legal agreements and form the basis for payment liabilities with a government. None the less, if multiple such agreements are substantially interconnected, this shall be considered a project."

The 2012 SEC rules provide similar guidance: "The contract defines the relationship and payment flows between the resource extraction issuer and the government, and therefore, we believe it generally provides a basis for determining the payments, and required payment disclosure, that would be associated with a particular ‘project.’"

An anticipated project registry by the Natural Resource Governance Institute (NRGI) uses the EU definition, and also includes anything that is reported as being a project by an EITI report. NRGI’s Anders Pedersen clarifies that a project may include multiple contracts, licenses, leases or concessions; may involve multiple companies; may produce multiple resources (e.g. silver and gold from the same mine); and may pay multiple government entities (e.g. local and national governments).

Given the lack of a precise definition of "project," it is expected that stakeholders will sometimes disagree as to whether two contracting processes belongs to the same project. This ambiguity, however, is not a reason to omit project identification from OCDS, as it is useful even if unreliable.

OCDS currently identifies a project with the Budget.project property, which is defined as "the name of the project that through which this contracting process is funded," and through the Budget.projectID property, which is defined as “an external identifier for the project that this contracting process forms part of, or is funded via.” “Project” takes on a different, specific, useful meaning within the context of a budget; therefore, the existing properties should be maintained and should not be re-used to fulfill this requirement.

Instead, a new Release.project property can be added to fulfill this requirement; different contracting processes within the same project would publish the same value for this property, so that these contracting processes may be linked by their common project. The property’s definition should result from further consultation with stakeholders and may be based on the EU and SEC definitions; it may be necessary for the definition to be imprecise, given the lack of convergence on a precise definition in the extractive industries and land sectors. A project identification scheme should be developed, similar to the organization identification scheme.

### R-Government

The existing Release.buyer property fulfills this requirement. However, the name of the property is more appropriate to a procurement contract than, for example, an exploration license, where the company that is paying a fee to acquire exploration rights is more likely to be considered the "buyer." See also **[R-Awarde**e](#heading=h.zdztyfw1v3wz). In a public-private partnership (which is not the subject of this extension), the terms “buyer” and “supplier” are similarly inappropriate.

If OCDS is intended to apply to contracts between any two parties, and if those parties are in direct negotiation, then it is unclear what terms will consistently distinguish one from the other. The International Aid Transparency Initiative uses provider-org and receiver-org; the Construction Sector Transparency Initiative uses "project owner," “procuring entity,” “contract administration entity,” and “contract firm”; the Extractive Industries Transparency Initiative uses “government’ and “company.” None of these options would work for all use cases.

If OCDS is intended to apply to only contracts with a government party, an option is to rename buyer to governmentEntity or similar.

The definition of this property will change accordingly.

### R-Country

A new Release.country property can be added to fulfill this requirement, whose value is a two-letter, uppercase [ISO 3166-1 alpha-2 country code](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2). Its definition may be "the country in which the government is located" if buyer is renamed to governmentEntity.

### R-Publisher

The existing RecordPackage.publisher and ReleasePackage.publisher properties fulfill this requirement.

## Planning

### R-ExpectedProduction

A new Planning.estimatedProduction property can be added to fulfill this requirement, whose value would be similar to Item, with at a minimum the quantity and unit properties in common. Further consultation with stakeholders is necessary to determine whether the property should be defined as total production over the contract period or as an average annual production rate.

## Initiation

### R-InitiationType

At present, OCDS only implements one initiation process: tender. The extractive industries and land sectors use many other processes, which, once modeled, would share some properties with OCDS’ current Tender type. The options are:

1. To make Tender more generic to accommodate more processes into one type.

2. To create new initiation types, re-using property names from the Tender type.

The second option is preferred for several reasons. First, some processes will have properties that are not shared with others; if a single type were implemented – containing all possible properties – it may lead to incoherent data, e.g. a process with both a classification of "direct negotiation" and a value for its tenderers property. Using multiple types prevents incoherent data and makes automatic validation easier. Second, using multiple types maintains the specification’s flexibility, by allowing different types to diverge over time if such divergence better fulfills requirements, reflects reality and/or eases adoption.

Initiation processes may be competitive or non-competitive. A tender process is a specific type of competitive process. Competitive processes are often public, while non-competitive processes are often confidential. Future work on OCDS can take as a starting point two generic classes: CompetitiveProcess and NonCompetitiveProcess. All new initiation types should be added as possible values for Release.initiationType. Both initiation types should have the following properties in common with Tender:

* id

* title

* description

* status

* items

* See this section’s other requirements regarding other properties.

Additional properties from Tender may be added as the use cases are developed further. Regarding the inclusion of items in NonCompetitiveProcess, the resource and the type of title (exploration license, production sharing agreement, etc.) is often known, even if the process is otherwise confidential.

### R-ProcessDescription

Re-use of the description property within Tender fulfills this requirement. Its definition may be changed to "a description of the process." The description should reference any model production sharing agreements used.

### R-Exceptions

The EITI Standard requires the disclosure of "any non-trivial deviations from the applicable legal and regulatory framework governing license transfers and awards" (EITI International Secretariat, 2013). A new Release.initiationTypeRationale property can be added to fulfill this requirement, mirroring procurementMethodRationale. Its definition may be “an explanation for the choice of initiation type, including an explanation for any non-trivial deviations from applicable legal or regulatory frameworks.”

### R-AwardCriteria

Re-use of the awardCriteria and awardCriteriaDetails properties within Tender fulfills this requirement. Its definition may be changed to "the criteria used to award candidates."

### R-EligiblityCriteria

Re-use of the eligibilityCriteria property within Tender fulfills this requirement. Its definition may be changed to "the eligibility, qualification or pre-qualification criteria for award candidates."

### R-Candidates

Re-use of the numberOfTenderers and tenderers properties within Tender fulfills this requirement. The properties should be renamed to numberOfCandidates and candidates in new initiation types. OCDS may consider renaming Tender.tenderers and Tender.numberOfTenderers for consistency; however, tenderers and numberofTenderers are clearer for procurement and maintain status quo. The definition of candidates may be "all entities who are candidates for awards," and the definition of numberOfCandidates may be “the number of entities who are candidates for awards.”

## Application

OCDS has already identified use cases for including information about bids or applications in a procurement process. In the extractive industries and land sectors, applications may be competitive or non-competitive. For the below requirements, a new applications property should be added to each initiation type, whose definition may be "submissions in consideration for an award." Its value should be an array of a new Application class, whose definition may be “a submission in consideration for an award.” Its initial properties are described below. In procurement, a “bid” is a type of application.

### R-ApplicationTitle

A new Application.title property can be added to fulfill this requirement. Its definition may be "the application’s title."

### R-ApplicationDate

A new Application.date property can be added to fulfill this requirement, whose value is a date. Its definition may be "the date on which the application was received."

### R-ApplicationStatus

A new Application.status property can be added to fulfill this requirement. Its definition may be "the application’s status." The Revenue Development Foundation should be consulted to clarify the definitions of the statuses in its Online Data Repository (see use case above) and to clarify which statuses relate to applications versus contracts.

### R-Applicant

A new Application.applicants property can be added to fulfill this requirement, whose value is an array of Organization. Its definition may be "the entity submitting the application or on whose behalf the application is submitted."

### R-ApplicationItem

Re-use of the items property within the initiation type of the Application fulfills this requirement.

### R-ApplicationTransaction

A new Application.transactions property can be added to fulfill this requirement, whose value is an array of Transaction. Its definition may be "transactions made against the application."

## Award

### R-Awardee

Re-use of the suppliers property within Award fulfills this requirement. The property should be renamed in new initiation types, possibly to awardees. OCDS may consider renaming Award.suppliers for consistency. Its definition may be changed to "the entities receiving the award."

### R-AwardDate

The existing Award.date property fulfills this requirement.

### R-AwardRationale

A new Award.rationale property can be added to fulfill this requirement. Its definition may be "a justification of the award to the awardee(s)."

## Contract

### R-ContractID

The existing Contract.id property fulfills this requirement.

### R-ContractTitle

The existing Contract.title property fulfills this requirement.

### R-ContractDateSigned

The existing Contract.dateSigned property fulfills this requirement.

### R-ContractPeriod

The existing Contract.period property fulfills this requirement.

### R-ContractLanguage

The existing Document.language property fulfills this requirement.

### R-ContractStatus

The existing Contract.status property fulfills this requirement. "suspended" should be added as a possible value. Further consultation with stakeholders is necessary to determine whether to add “renewed” as a possible value or to re-use the existing “active” possible value and to model renewals in another way. The Revenue Development Foundation should be consulted to clarify the definitions of the statuses in its Online Data Repository (see use case above) and to clarify which statuses relate to applications versus contracts.

### R-ContractDocument

The existing Contract.documents property fulfills this requirement.

### R-ContractType

The existing Document.documentType property fulfills this requirement. The documentType codelist should be expanded to include, for example:

* Production License

* Reconnaissance License (Revenue Development Foundation)

* Prospecting License (Revenue Development Foundation)

* Exploration License (Revenue Development Foundation)

* Concession (ResourceContracts.org, 2014)

* Lease (ResourceContracts.org, 2014)

* Production Sharing Agreement (ResourceContracts.org, 2014)

* Service Agreement (ResourceContracts.org, 2014)

* Investment Incentive Agreement (ResourceContracts.org, 2014)

* Memorandum of Understanding (ResourceContracts.org, 2014)

* Forest Management Contract (ResourceContracts.org, 2014)

* Land Concession Agreement (ResourceContracts.org, 2014)

* Land Lease Agreement (ResourceContracts.org, 2014)

* Land Sale Agreement (ResourceContracts.org, 2014)

* Timber Sale Contract (ResourceContracts.org, 2014)

It’s possible that Document.documentType is the only published property for a Document.

Further consultation with stakeholders is necessary to complete the codelist.

### R-Source

The existing Contract.documents property fulfills this requirement, as it can serialize the titles, links, etc. of sources.

## Item

### R-Resource (Commodity)

The existing Item.classification property fulfills this requirement. In terms of scheme, the International Monetary Fund recommends using the Central Product Classification (CPC) Ver.2, which includes, for example, code "1101" for “Coal, not agglomerated.” Using a common scheme avoids inconsistent terminology like “timber,” “lumber” and “wood.”

The Natural Resource Governance Institute recommends using the International Standard Industrial Classification of All Economic Activities (ISIC), Rev.4, which includes, for example, code "0610" for “Extraction of crude petroleum”; however, ISIC is better suited to the classification of organizations, as in **R-BusinessSegment**.

## Location

OCDS already anticipates the addition of a Location extension (see [GitHub issue 26](https://github.com/open-contracting/standard/issues/26)). For the below requirements, a new Item.locations property should be added, whose definition may be "geographic areas to which the item is related." Its value should be an array of a new Location class, whose definition may be “a geographic area.” Its initial properties are described below.

### R-LocationName

A new Location.name property can be added to fulfill this requirement. Its definition may be, "the location’s name."

### R-LocationSpatial

A new Location.geo property can be added to fulfill this requirement. Its definition may be, "the location’s geo coordinates." Its value should result from further consultation with stakeholders; options include [GeoJSON](http://geojson.org/) (IETF [draft](https://datatracker.ietf.org/doc/draft-butler-geojson/)), a string of [KML](https://developers.google.com/kml/documentation/?csw=1) or [GML](http://www.opengeospatial.org/standards/gml) (Open Geospatial Consortium), [GeoCoordinates](http://schema.org/GeoCoordinates) or [GeoShape](http://schema.org/GeoShape) classes (Schema.org), a link to a file such as a [shapefile](http://en.wikipedia.org/wiki/Shapefile), or a link to a feature in OpenStreetMap (see [it in use for oil blocks](http://osm.moabi.org/way/12307/#map=8/-4.018/18.441&layers=B), by Mikel Maron and Leo Botrill at Moabi DRC).

### R-LocationIdentifier

A new Location.identifier property can be added to fulfill this requirement, whose value is an Identifier. Its definition may be "the location’s primary identifier."

### R-LocationSize

A new Location.size property can be added to fulfill this requirement, whose value is a number, whose unit is km2. Its definition may be "the location’s surface area in km2."

### R-LocationClassification

A new Location.classification property can be added to fulfill this requirement, whose value is a Classification. Its definition may be "the location’s primary classification." Further consultation with stakeholders is necessary to complete a codelist; Brazil has the codes “ultra deep water, deepwater, shallow water, onshore.”

## Organization

### R-OrganizationAddress

The existing Organization.address property fulfills this requirement.

### R-OrganizationWebsite

The existing Organization.contactPoint.url property fulfills this requirement.

### R-OrganizationIdentifier

The existing Organization.identifier property fulfills this requirement.

### R-BusinessSegment

A new Organization.classification property can be added to fulfill this requirement, whose value is a Classification. Its definition may be "the organization’s primary classification." Possible codelists include the International Standard of Industrial Classification of All Economic Activities (ISIC), Standard Industrial Classification (SIC), Global Industry Classification Standard (GICS) and North American Industry Classification System (NAICS). The International Monetary Fund recommends ISIC (International Monetary Fund, 2014).

## Document

### R-DocumentClassification

The existing Document.documentType property fulfills this requirement. The documentType codelist already has codes for:

* feasibilityStudy: feasibility study (ResourceContracts.org, 2014)

* landImpact: land and settlement impact assessment (CoST)

* environmentalImpact: environmental impact (ResourceContracts.org, 2014; Petroleum Act, 2012)

* riskProvisions: mitigation plan/strategy (Global Witness, 2014)

The codelist should be expanded to include:

* local development agreement (ResourceContracts.org, 2014)

* business plan (ResourceContracts.org, 2014)

* development plan (Global Witness, 2014; Petroleum Act, 2012)

* strategic environmental assessment (Petroleum Act, 2012)

* environmental baseline study (Petroleum Act, 2012)

* economic impact assessment (EO100 Standard)

* social impact assessment (ResourceContracts.org, 2014)

* cultural impact assessment (Global Witness, November 2012)

* human rights impact assessment (ResourceContracts.org, 2014)

* environmental management plan (ResourceContracts.org, 2014; Petroleum Act, 2012)

* social management plan (ResourceContracts.org, 2014)

* human rights management plan (ResourceContracts.org, 2014)

* health and safety management plan (Petroleum Act, 2012)

* community development plan (Petroleum Act, 2012)

* local content plan (Petroleum Act, 2012)

* employment plan (Petroleum Act, 2012)

* decommissioning plan (Global Witness, 2014; Petroleum Act, 2012)

* environmental management plan annual report (Petroleum Act, 2012)

* local content annual report (Petroleum Act, 2012)

* environmental audit (Petroleum Act, 2012)

* dispute resolution mechanism (Global Witness, 2014)

* inspection report, including health, safety, environmental and financial inspections (Global Witness, 2014)

Further consultation with stakeholders is necessary to complete the codelist.

## Transaction

OCDS implements transactions at Contract.implementation.transactions.

Neither OCDS nor IATI, on which OCDS’ transactions are modeled, require transactions to be disaggregated; therefore, a transaction may represent an aggregated amount.

### R-TransactionAccount

A new Transaction.receiverAccount property can be added to fulfill this requirement. Its definition may be "the account in which the amount is deposited, for example, a stabilisation fund, if applicable.“

### R-TransactionAmount

The existing Transaction.amount property fulfills this requirement.

### R-TransactionDate

The existing Transaction.date property fulfills this requirement. This requirement is not to be confused with **R-TransactionPeriodicity** below.

### R-TransactionClassification

A new Transaction.classification property can be added to fulfill this requirement, whose value is a Classification. Its definition may be "the transaction’s primary type (e.g. royalty)."

See especially **[UC13: Classification of transaction**s](#heading=h.yt1f33vpcu8u) and **[UC18: IMF Template for Government Revenues from Natural Resource**s](#heading=h.764brxl3mana). The International Monetary Fund recommends Government Finance Statistics Manual (GFSM) 2001.

### R-TransactionCurrency

The existing Value.currency property fulfills this requirement if a single currency is reported. If two currencies are reported, a new Transaction.amountUSD property can be added to fulfill this requirement, whose value is a number. Its definition may be "the value of the transaction in US dollars." If this property is used, the currency property of the Transaction.amount should be the local currency.

All use cases above for multiple currencies involve the US dollar and a local currency. If there are doubts that the US dollar will maintain its special status in the world economy, a new Transaction.foreignAmount property can be added to fulfill this requirement, whose value is an Value. Its definition may be "the value of the transaction in a foreign currency."  If this property is used, the currency property of the Transaction.amount should be the local currency.

### R-TransactionPeriodicity

A new Transaction.period property can be added to fulfill this requirement, whose value is a Period. Its definition may be "the financial period for which the transaction is made."

### R-TransactionRate

A new Transaction.rate property can be added to fulfill this requirement, whose value is a number representing a percentage. Its definition may be "the applicable rate used to calculate the transaction’s amount, for example, the royalty rate."

### R-TransactionRecipient

The existing Transaction.receiverOrganization property fulfills this requirement.

### R-TransactionReconciliation

This document proposes no solution for transaction reconciliation. Additional stakeholder engagement is necessary to design solutions to this hard problem. The **Revenue Development Foundation Online Data Repository** use case uses receipt numbers to reconcile payments with receipts. Further research should determine whether this is a common practice.

### R-TransactionInKind

A new Transaction.inKind property can be added to fulfill this requirement, whose value is a boolean. Its definition may be "whether the transaction was made in-kind."

### R-TransactionVolume

A new Transaction.quantity property can be added to fulfill this requirement, whose value is a number, not an integer, to allow, for example, fractions of ounces of gold. Its definition may be "the volume or quantity of goods transacted, if the transaction is made in-kind or if its amount is based on a quantity or volume (e.g. barrels of oil)." OCDS may consider changing the value of Item.quantity from an integer to a number for consistency. See the next requirement about the name and value of the unit of measure.

### R-TransactionUnit

A new Transaction.unit property can be added to fulfill this requirement, whose value is an object with the same properties as Item.unit. Its definition may be "the unit in which the goods are transacted, if the transaction is made in-kind or if its amount is based on a unit value (e.g. spot price)."

# Out-of-lifecycle requirements

OCDS is deliberately designed to make it easy to disclose information at specific points in the lifecycle of a contracting process:

* A process is planned.

* A process is initiated, for example, with a tender, which may be amended.

* An award is made, which may be amended.

* A contract is signed, which may be amended.

* Transactions are made against the contract.

* Progress is made on contract milestones.

Information relating to a contracting process that falls outside its lifecycle is more challenging for a publisher to add and update, as it does not line up with any event directly relating to the contract. In other words, there is no event to trigger the publisher to update the data. Specific examples follow.

## Beneficial ownership

Use cases from the EITI Standard, civil society (Global Witness, November 2012), and others highlight the importance of disclosing the beneficial ownership of the companies that are party to contracts. However, changes in beneficial ownership occur unrelated to any contract; in other words, such changes occur outside the lifecycle of any contract. It is therefore recommended for beneficial ownership information to be linked from, but not modeled in, OCDS. A new property can be added to the Organization class to link to this information.

## Production share

The Natural Resource Governance Institute use case requires the disclosure of the share an entity holds in a project. For example, the Government of Ghana’s interest in the Jubilee Field was 13.75% at the time of the contract’s signature. However, in this project as in others, interests can be changed as a result of a two-step process of unitization and redetermination. In the case of the Jubilee Field, this process is provided for in the Jubilee Field Unitization and Unit Operating Agreement (Adam, 2014). Under the terms of the agreement, interests are automatically revised on redetermination; the contract is not renegotiated, i.e. the change of interest occurs outside the lifecycle of the contract. It is therefore recommended for information about interests to be linked from, but not modeled in, OCDS. A new property can be added to the Contract class to link to this information.

# Bibliography

Allen & Overy. [Guide to Extractive Industries Documents – Mining](https://www.documentcloud.org/documents/563542-guide-to-contract-terminology-mining.html)*. *World Bank Institute Governance for Extractive Industries Programme, January 2013.

Adam, Mohammed Amin. [Public Interest Report No. 2: Three Years of Petroleum Revenue Management in Ghana – Transparency without Accountability](http://www.aceplive.com/wp-content/uploads/2014/08/ACEP-Report-PRMA-Final.pdf). Africa Centre for Energy Policy, July 2014.

Besada, Hany and Philip Martin. *[Mining Codes in Africa: Emergence of a "Fourth" Generation*?](http://www.nsi-ins.ca/wp-content/uploads/2013/04/Mining-Codes-in-Africa-Emergence-of-a-%E2%80%9CFourth%E2%80%9D-Generation-Hany-Besada1.pdf) The North-South Institute, March 2013.

Boas & Associates. [Final Report on the Aggregation/Reconciliation of Mining Sector Payments and Receipts: 2010-2011](https://www.google.ca/url?sa=t&rct=j&q=&esrc=s&source=web&cd=2&cad=rja&uact=8&ved=0CDEQFjAB&url=https%3A%2F%2Feiti.org%2Ffiles%2FGhana-2010-2011-EITI-Report_0.pdf&ei=2xN4VK-dEMPnsASy24DQDg&usg=AFQjCNETl_uCWlTUq5XKNP7YVfvKWiXB_A&bvm=bv.80642063,d.cWc). Ghana Extractive Industries Transparency Initiative (GHEITI), February 2013.

[The EITI Standard](https://eiti.org/files/English_EITI%20STANDARD_11July_0.pdf). EITI International Secretariat, 11 July 2013.

[Directive 2013/34/EU of the European Parliament and of the Council of 26 June 201*3](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32013L0050&from=EN). Official Journal of the European Union, 29 June 2013.

[Directive 2013/50/EU of the European Parliament and of the Council of 22 October 2013](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32013L0050&from=EN). Official Journal of the European Union, 6 November 2013.

[Getting to Gold: How Afghanistan’s first mining contracts can support transparency and accountability in the sector](http://www.globalwitness.org/sites/default/files/library/Getting%20to%20Gold_1.pdf). Global Witness, April 2012.

[Copper Bottomed? Bolstering the Aynak contract: Afghanistan’s first major mining deal](http://www.globalwitness.org/sites/default/files/library/Copper%20Bottomed.pdf). Global Witness, November 2012.

[A Good Deal Better? Uganda's Secret Oil Contracts Explained](http://www.globalwitness.org/ugandaoilcontracts/files/Report_A_good_deal_better_low_res.pdf). Global Witness, September 2014.

[Template to Collect Data on Government Revenues from Natural Resources](http://www.imf.org/external/pubs/ft/gfs/manual/pdf/templatedata.pdf). International Monetary Fund, 24 January 2014.

[The Petroleum Act, 2012](http://www.mpmisouthsudan.org/docs/Petroleum%20Act,%202012%20-%20Signed%20-%20July%206.pdf). National Legislative Assembly of South Sudan, 2012.

[Data format for project level data store - guidanc*e](https://docs.google.com/document/d/1wvhG0m4-E7soLZykTTmg68Q6FEnegD5AhXBVhZi87TM/edit#). Natural Resource Governance Institute, 2014.

[Publish Why You Pay and How You Extract](http://www.publishwhatyoupay.org/about/publish-why-you-pay-and-how-you-extract). Publish What You Pay, 201?a.

[Contract Transparency](http://www.publishwhatyoupay.org/about/advocacy/contract-transparency). Publish What You Pay, 201?b.

Morgan, Jana. [Position Statement on Section 1504 of the Dodd-Frank Wall Street Reform and Consumer Protection Act](http://www.sec.gov/comments/df-title-xv/resource-extraction-issuers/resourceextractionissuers-28.pdf). Publish What You Pay, 2014.

[Guidance Note for Annotating Commercial Agriculture and Forestry Contracts Using the WBI-RWI-VCC Template](http://www.revenuewatch.org/sites/default/files/resourcecontracts/CCSI_NRGI_WBG_Guidance_Note_Annotating_Commercial_Ag_Forests_draft_022014.1.pdf). ResourceContracts.org, February 2014.

[Disclosure of Payments by Resource Extraction Issuers](http://www.sec.gov/rules/final/2012/34-67717.pdf). Securities and Exchange Commission, 13 November 2012.

[Production Sharing Agreement for Petroleum Exploration Development and Production in the Republic of Uganda by and between the Government of the Republic of Uganda and Tullow Uganda Limited in respect of Exploration Area 1](http://www.globalwitness.org/ugandaoilcontracts/files/PSA_EA1A.pdf). Government of the Republic of Uganda and Tullow Uganda Limited, February 2012.

# Appendix 1: Glossary

**Accountability institution:** An independent entity established by legislation to monitor and evaluate the government’s compliance with relevant legislation in the management and use of resource revenues.

**Surface rent:** "An amount payable for use of land, based on a flat rate per unit of measurement" (Allen & Overy, 2013). Also known as **Ground rent**.

# Appendix 2: Stakeholders

An incomplete list of stakeholders with whom future consultations may be held follows:

* [Columbia Center on Sustainable Investment](http://ccsi.columbia.edu/)

* [Extractive Industries Transparency Initiative](https://eiti.org/) (EITI)

    * [EITI Albania](http://www.albeiti.org/)

    * [EITI Azerbaijan](http://www.eiti.az/)

    * [EITI Cameroon](http://www.eiticameroon.org/)

    * [ITIE Congo](http://www.itie-congo.org/)

    * [ITIE Guinée](http://www.itie-guinee.org/)

    * [ITIE Mauritanie](http://itie-mr.org/)

    * [ITIE République Démocratique du Congo](http://www.itierdc.com/)

    * [GHEITI](http://www.gheiti.gov.gh/) (Ghana)

    * [LEITI](http://www.leiti.org.lr/) (Liberia)

    * [NEITI](http://neiti.org.ng/) (Nigeria)

    * [PH-EITI](http://data.gov.ph/eiti/) (Philippines)

    * [SLEITI](http://www.sleiti.gov.sl/) (Sierra Leone)

* [GOXI](http://goxi.org/)

* [Global Witness](http://new.globalwitness.org/)

* [Natural Resource Governance Institute](http://www.resourcegovernance.org/)

* [Oakland Institute](http://www.oaklandinstitute.org/)

* [OpenOil](http://openoil.net/)

* [Publish What You Pay](http://www.publishwhatyoupay.org/)

* [Revenue Development Foundation](http://revenuedevelopment.org/)

* [Transparency International](http://www.transparency.org/)

* [Africa Centre for Energy Policy](http://acepghana.com/) (Ghana)

* [Civic Society Coalition on Oil and Gas](http://www.csco.ug/) (Uganda)

* [LICADHO](http://www.licadho-cambodia.org/) (Cambodia)

* [Policy Forum](http://www.policyforum-tz.org/) (Tanzania)

See OpenOil’s [Exploring Oil Data: A Reporter’s Handbook](http://openoil.net/exploring-oil-data/) for additional stakeholders.

# Index

[[TOC]]

