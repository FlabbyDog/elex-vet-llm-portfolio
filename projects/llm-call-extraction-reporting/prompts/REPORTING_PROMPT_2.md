Instructions for Creating a Root Cause Analysis Report

Overview
This guide provides instructions for creating a Root Cause Analysis report for staff performance evaluation. Follow these guidelines to generate a thorough analysis that identifies underlying causes of performance patterns rather than just describing symptoms.

The final report should not exceed 3000 words.

Before You Begin
1. The response should not exceed 3000 words
2. Check the database for Overall Staff Performance data for the specific staff member
3. Review the Comprehensive Analysis report if available, as this will provide context for deeper analysis
4. Ensure you have access to call metrics, performance scores, and transcript highlights
5. Based your analysis on current and available data. Do not invent your own data. 
6. Consider the number of days against the metrics. 

CODE LIBRARY:

Combined Call Direction and Categories:
- INBOUND-CLIENT: Incoming call from a client
- INBOUND-STAFF: Incoming call from another staff member
- INBOUND-SERVICEPROV: Incoming call from a service provider
- OUTBOUND-CLIENT: Staff calling a client
- OUTBOUND-STAFF: Staff calling another staff member
- OUTBOUND-SERVICEPROV: Staff calling a service provider

Call Outcome:
- ANS&STO: Call was answered and conversation occurred
- NO_ANS&VM-MSGLEFT: No answer and the staff member left a message
- NO_ANS&VM-NOMSG: No answer and the staff member did NOT leave a message

Preparation Coding System:

PREP: Preparation 
  .HX: General history reviewed
  .RECENT: Recent visits mentioned
  .CHRONIC: Ongoing conditions discussed
  .PREVT: Preventive treatments referenced
  .OVERDUE: Overdue services mentioned
  .MEDHX: Medication history discussed
  .LAB: Lab results referenced
  .IMG: Imaging results mentioned
  .DIET: Dietary information discussed
  .BEHAV: Behavioral notes referenced
  .CURVISIT: Current visit details mentioned


Preparation Score Guide (1-10):
- 1-3: Little to no evidence of preparation, missing crucial information
- 4-6: Basic preparation, but overlooking important details or history
- 7-8: Good preparation, covering most relevant information
- 9: Thorough preparation, demonstrating comprehensive knowledge of patient history
- 10: Exceptional preparation, anticipating potential issues and questions

Service Categories and Subcategories:

SURG: Surgical Procedures
  .DENT: Dental
  .DESEX: Desexing
  .ORTH: Orthopedic
  .SOFT: Soft Tissue
  .EYE: Ophthalmic
  .ONCO: Oncological
  .NEUR: Neurological
  .THOR: Thoracic
  .ABDO: Abdominal
  .RECON: Reconstructive
  .MINI: Minimally Invasive

MED: Medical Care
  .PREV: Preventative
  .ACUTE: Acute Care
  .CHRON: Chronic Care
  .VACC: Vaccinations
  .PARA: Parasite Control
  .DERM: Dermatological Care
  .CARD: Cardiac Care
  .RESP: Respiratory Care
  .GAST: Gastrointestinal Care
  .NEUR: Neurological Care
  .ENDO: Endocrine Care
  .OPHT: Ophthalmological Care
  .DENT: Dental Care
  .GERI: Geriatric Care
  .PAIN: Pain Management

DIAG: Diagnostics
  .LAB: Laboratory Tests
  .IMG: Imaging
  .ENDO: Endoscopy
  .ULTR: Ultrasound
  .XRAY: X-Ray
  .CT: CT Scan
  .MRI: MRI
  .BIOP: Biopsy
  .CULT: Culture and Sensitivity
  .CYTL: Cytology

WELL: Wellness
  .NUTR: Nutrition
  .WEIGHT: Weight Management
  .BEHAV: Behavioral
  .GROOM: Grooming
  .DENT: Dental Hygiene
  .EXER: Exercise Planning
  .ENVR: Environmental Enrichment
  .PREVT: Preventative Care Planning
  .REPRO: Reproductive Health
  .GERI: Geriatric Wellness

PROD: Products
  .MED: Medications
  .SUPP: Supplements
  .FOOD: Prescription Diets and Food
  .EQUIP: Equipment
  .HYGI: Hygiene Products
  .DENT: Dental Products
  .PARA: Parasite Control Products
  .BEHAV: Behavioral Aids
  .MOBI: Mobility Aids
  .NUTR: Nutritional Supplements

CONS: Consultations
  .VET: Veterinary Consults
  .PROGCHK: Progress Recheck
  .RESCHK: Resolution Recheck
  .LTPLAN: Long Term Plan Development
  .DENTCHK: Dental Assessment
  .WTCHK: Weight Assessment
  .PREVPLN: Preventatives Plan
  .BANDAGE: Bandage change


Recommendation Clarity and Relevance Scores (1-10):
- 1-3: Inappropriate or missing critical recommendations
- 4-6: Basic recommendations made, but lacking in detail or personalization
- 7-8: Appropriate recommendations with good explanations
- 9: Comprehensive recommendations tailored to specific patient needs
- 10: Exceptional, proactive recommendations considering both immediate and long-term health

Missed Opportunity Categories:

 .CONS: Consultation
 .WELL: Wellness Care
 .PREV: Preventive Care
 .DIAG: Diagnostic Tests
 .TREAT: Treatments
 .PROD: Products
 .SERV: Services
 .FIN: Financial Options
 .EDU: Educational Information


Timeframe Format:

IMM: Immediate (within 48 hours)
     D: _ days
FUT:
     D: _ days
     W: _ weeks
     1W: 1 week
     1M: 1 month
     3M: 3 months
     6M: 6 months
     1Y: 1 year


Impact Assessment:
- HEALTH: Impact on pet health (HIGH, MED, LOW)
- REV: Impact on practice revenue (HIGH, MED, LOW)

Booking Status:
- BOOK.OFFERED.YES: Staff attempted to schedule an appointment
- BOOK.OFFERED.NO: No attempt made to schedule an appointment

Booking Clarity (if BOOK.OFFERED.YES):

.EXIST-CLEARDAY&TIME: Both specific day of week AND exact time explicitly stated
.EXIST-NOTCLEAR: Either specific day or exact time not explicitly stated
.NEWBOOK: New booking confirmed with both clear day/date and time

Reason (if BOOK.OFFERED.NO):

.STAFF.NODIS: Staff did not discuss or attempt to make a booking
.CLIENT: Client-related reasons:
  .IMM: Client cannot make an immediate appointment
  .FUT: Client prefers to book at a later date
  .COST: Client expresses concerns about cost
  .TIME: Client has general time constraints
  .FAM: Client needs to discuss with family members
  .INS: Client needs to check insurance coverage
  .MOREOP: Client wants to explore more options

Booking Effectiveness Score (1-10):
- 1-3: Failed to attempt booking or made significant errors
- 4-6: Attempted booking but with notable difficulties or missed opportunities
- 7-8: Successfully booked appointments with minor room for improvement
- 9: Efficient booking process with clear communication of details
- 10: Exceptional booking process, overcoming obstacles and maximizing opportunities

Reminder Categories:

IMM: Immediate reminders (within 48 hours)
FUT: Future reminders (beyond 48 hours)


Reminder Format:
Target Date: When the action should occur (DD/MM/YYYY)
Reminder Date: When to send the reminder (typically a few days to 2 weeks before target date)
Action: Clear statement of required action

Reminder Priority:
- HIGH: Critical for patient health or time-sensitive
- MED: Important but not immediately critical
- LOW: Beneficial but can be delayed if necessary

Reminder Responsibility:
- RCPT: Receptionist
- NUR: Nurse
- DR: Veterinarian
- ANY: Any staff member

Reminder Assessment Score (1-10):
- 1-3: Poor (Many missed reminders, unclear actions, or inappropriate timing)
- 4-6: Average (Most necessary reminders set, some clarity or timing issues)
- 7-8: Good (Comprehensive reminders with clear actions and appropriate timing)
- 9-10: Excellent (All necessary reminders set with exceptional clarity, timing, and actionable details)

Financial Discussion Categories:
 .PRICE: Discussion of specific prices or costs for services
 .ESTIM: Providing estimates or price ranges for services
 .PAYM: Payment methods or options (credit/debit, cash, VetPay, ZipPay, Afterpay)
 .PLAN: Discussion of payment plans or financing options
 .INSUR: Pet insurance discussions or GapOnly® claims
 .CONC: Client expressing financial concerns
 .DISC: Discussions about discounts or promotions
 .VALU: Explanations of value or cost-benefit of treatments
 .COMP: Comparison of costs between options or services

Staff Approach:
 .CLEAR: Price information provided clearly and comprehensively
 .VAGUE: Price information provided was unclear or incomplete
 .AVOID: Staff avoided or deflected financial discussions
 .PROAC: Staff proactively addressed financial matters
 .REACT: Staff only discussed finances in reaction to client queries
 .RANGE: Staff provided price ranges rather than exact figures
 .BUNDL: Staff discussed service bundles or packages for better value

Price Disclosure Categories:
 .EXACT: Specific dollar amount given
 .RANGE: Price range provided
 .CATEG: Category indicated (LOW/MED/HIGH)
 .NOMEN: No price mentioned for recommended service
 .REFER: Referred to another staff member for pricing
 .DEFER: Postponed price discussion until future contact

Financial Effectiveness Score (1-10):
1-3: Poor (Avoided financial discussions, provided unclear information, or showed insensitivity to client's budget concerns)
4-6: Average (Basic financial information provided, some attempt to address concerns)
7-8: Good (Clear financial discussions, good sensitivity to budget, and offered some payment solutions)
9-10: Excellent (Proactive, clear, and sensitive financial discussions with effective solutions and value communication)

STANDARD SERVICE PRICING REFERENCE

CONSULTATIONS
- Standard Consultation: $130
- Emergency/Urgent Care Consultation: $150
- Vaccination Package (includes consultation + vaccination): $130
- Recheck/Follow-up Consultation: $80-110
- Extended/Complex Consultation: $150-180
- Consultation Lameness - $300, consultation included, Includes: NSAIDs, Rest and Blood Panel
- Microchipping: $60-80

PREVENTATIVE CARE
- Basic Vaccination (C3): $90-110 (excluding consultation)
- Complete Vaccination (C5): $110-130 (excluding consultation)

Annual Heartworm Injection:
- Small (0-10kg): $125-170
- Medium (10.1-25kg): $215-300
- Large (25.1-40kg): $325-430
- Extra Large (40.1-60kg): $470-605

- Worming Treatments (based on weight): $15-65
- Flea/Tick Treatments (monthly): $25-85

Bravecto Quantum Injection (Admin fee included in price range)
- Small (0-10kg): $125-$170
- Medium (10.1-25kg): $215-$300
- Large (25.1-40kg): $325-$430
- Extra Large (40.1-60kg): $470-$605

DIAGNOSTICS
- Comprehensive Blood Profile (Unwell Patient): $375
- Wellness Blood Profile: $335
- Pre-Anaesthetic Blood Profile (<7yr): $280
- Urinalysis: $145
- Abdominal Ultrasound: $700
- Radiology Under General Anesthesia: $680
- Radiology with Sedation: $700

SURGICAL PROCEDURES
- Dental (Cleaning):
- Small (<15kg): $800-1,000
- Medium (15-30kg): $900-1,200
- Large (>30kg): $1,000-1,400

Dental COHAT (Cleaning) Consultation and anesthesia included
- Small (<15kg): $800 (Grade 1) to $1,000 (Grade 4)
- Medium (15-30kg): $900 (Grade 1) to $1,200 (Grade 4)
- Large (>30kg): $1,000 (Grade 1) to $1,400 (Grade 4)
- Dental Extractions (>6 teeth): $1,600-3,000

Canine Spay:
- 0-10kg: $630
- 10-15kg: $640
- 15-25kg: $725
- 25-35kg: $780
- 35-45kg: $800
- 45kg: $840

Feline Spay: $530

Canine Castration:
- 0-10kg: $570
- 10-15kg: $585
- 15-25kg: $650
- 25-35kg: $680
- 35-45kg: $715
- 45kg: $735

Feline Castration: $370
Celiotomy: $3,300

SPECIALIZED CONSULTATIONS
- Acute Diarrhea (Conservative): $800
- Acute Vomiting (Conservative): $1,150
- Acute Vomiting and Diarrhea (Conservative): $1,250
- Acute Diarrhea and Vomiting (Comprehensive): $2,450
- Severe Gastro: $2,400
- Consultation with Urinalysis & Full Bloods: $595
- Comprehensive Urinary Assessment: $1,100
- Consultation Lameness (with NSAIDs & Blood Panel): $300
- Eye Examination and Medications: $400
- Skin Consultation: $700
- Ear Consultation: $250
- Sedated Ear Examination: $700

MEDICATIONS (AVERAGE COSTS)
- Standard Medications (includes dispensing fee): $35-90
- Specialized Medications: $90-180
- Long-term/Chronic Medication (monthly): $50-120
- Prescription Script Fee: $15-25

If not mentioned, estimate based on breed:
- Small Dogs (<15kg): Chihuahua, Dachshund, Jack Russell, Pug, Shih Tzu, Yorkshire Terrier, Maltese, Pomeranian
- Medium Dogs (15-30kg): Border Collie, Cocker Spaniel, Bull Terrier, Staffordshire Terrier, Beagle,  Australian Cattle Dog
- Large Dogs (>30kg): German Shepherd, Labrador, Golden Retriever, Rottweiler, Boxer, Doberman
- Cats: Average 4-5kg (unless specified as exceptionally large or small)

PAYMENT OPTIONS REFERENCE:

DIRECT PAYMENT
- Credit/Debit cards
- Cash
- EFTPOS

PAYMENT PLANS
- VetPay: Spread payment over 3-8 months
- ZipPay: Interest-free payment plans
- Afterpay: Split into 4 equal payments

INSURANCE
- GapOnly®: Direct insurance claim processing
- Standard Pet Insurance: Client pays, then claims back

COST-BENEFIT REFERENCE FOR COMMON PROCEDURES
PREVENTATIVE PROCEDURES
Annual Vaccinations:
Cost: $130
Benefit: Prevents diseases that could cost $500-2,500+ to treat

Annual Dental Cleaning:
Cost: $800-1,400
Benefit: Prevents advanced dental disease requiring extractions ($1,600-3,000)

Parasite Control:
Cost: $125-605 annually
Benefit: Prevents parasitic diseases requiring $500-3,000 in treatment

DIAGNOSTIC INVESTMENTS
Blood Work:
Cost: $280-375
Benefit: Early detection of conditions that become more expensive to treat when advanced

Imaging:
Cost: $680-700
Benefit: Precise diagnosis avoiding trial treatments that may cost $300-800 without addressing underlying issue

Objection Categories:
COST: Price-related objections
TIME: Time or scheduling-related objections
NEED: Objections about necessity of product/service
RISK: Concerns about risks or side effects
ALT: Preference for alternative treatments/products
TRUST: Lack of trust or confidence in recommendation
OTHER: Any objections that don't fit above categories

Staff Response:
HANDLED: Staff addressed objection effectively
PARTIAL: Staff attempted to address objection but was not fully effective
UNHANDLED: Staff did not address objection
ESCALATED: Staff escalated objection to supervisor or veterinarian

Objection Handling Techniques:
LISTEN: Active listening to fully understand objection
EMPATHY: Showing understanding of client's concern
EDUCATE: Providing additional information to address objection
REFRAME: Presenting recommendation from different perspective
VALUE: Emphasizing value or benefits of recommendation
ALTERNATIVE: Offering alternative options or solutions
PROBING: Asking questions to uncover root of objection

Objection Handling Effectiveness Score (1-10):
- 1-3: Poor (Objections ignored or poorly handled, leading to negative outcomes)
- 4-6: Average (Basic attempt to address objections, with mixed results)
- 7-8: Good (Most objections handled effectively, leading to positive outcomes)
- 9-10: Excellent (All objections handled with skill, leading to positive outcomes and enhanced client relations)

Next Steps Clarity Levels:
CLEAR: Clearly stated and confirmed
PART: Partially clear, some details missing
UNCL: Unclear or not explicitly stated

Responsibility:
CLIN: Clinic responsibility
CLIENT: Client responsibility
BOTH: Shared responsibility

Next Steps Clarity Score (1-10):
- 1-3: Poor (Next steps unclear or not discussed)
- 4-6: Average (Some next steps mentioned but lack detail or confirmation)
- 7-8: Good (Most next steps clearly communicated with responsibilities assigned)
- 9-10: Excellent (All next steps explicitly stated, confirmed, and understood by all parties)

Client Engagement Score (1-10):
- 1-3: Poor (Client unresponsive or disinterested)
- 4-6: Average (Client responsive but not actively engaged)
- 7-8: Good (Client actively participates and shows interest)
- 9-10: Excellent (Client highly engaged, asking questions and showing strong interest)

Education Topics:
PREV: Preventive care
DIAG: Diagnostic procedures
TREAT: Treatment options
MED: Medication information
NUTR: Nutrition and diet
BEHAV: Behavioral issues
HOME: Home care instructions

Quality Aspects:
CLEAR: Clarity of explanation
COMP: Comprehensiveness of information
LEVEL: Appropriateness for client's level of understanding
VERI: Verification of client's comprehension

Rating:
HIGH: Excellent
MOD: Moderate
LOW: Poor


Education Effectiveness Score (1-10):
- 1-3: Poor (Minimal or unclear educational content)
- 4-6: Average (Basic information provided, some clarity issues)
- 7-8: Good (Clear and comprehensive education on most topics)
- 9-10: Excellent (Exceptional education, tailored to client, with verified comprehension)


 CONSOLIDATED MISSED OPPORTUNITIES


Categories:
CARE: Missed care recommendations
BOOK: Missed booking opportunities
EDUC: Missed educational opportunities
REVE: Missed revenue opportunities
COMM: Missed communication opportunities
PROC: Missed procedural opportunities

Impact Assessment:
HEALTH: Impact on pet health (HIGH, MED, LOW)
SAT: Impact on client satisfaction (HIGH, MED, LOW)
REV: Impact on practice revenue (HIGH, MED, LOW)


Priority:
Rank from 1 (highest) to 5 (lowest) based on overall impact and urgency


FOLLOW-UP ACTIONS

Action Categories:
CALL: Follow-up phone call needed
BOOK: Appointment needs to be scheduled
REM: Reminder needs to be set
EDUC: Educational materials need to be sent
QUOTE: Quote or estimate needs to be provided
PROC: Procedural change or implementation required
TRAIN: Staff training or coaching needed


Timeframe Format:
D: Number of days
W: Number of weeks
M: Number of months


Responsibility:

RECEP: Receptionist
TECH: Veterinary Technician
VET: Veterinarian
MGR: Practice Manager


Action Priority:
Rank from 1 (highest) to 5 (lowest) based on urgency and impact

UPDATED REMINDERS

Updated Reminder Categories:

NEW: Newly created reminder
MOD: Modified existing reminder
CAN: Cancelled reminder


Reminder Types:

CALL: Follow-up call
BOOK: Appointment booking
CHECK: Health check or recheck
REFILL: Medication refill
TEST: Diagnostic test
ADMIN: Administrative task


Updated Reminders Assessment Score (1-10):
- 1-3: Poor (Many missed or inappropriate reminders)
- 4-6: Average (Most necessary reminders set, some timing or assignment issues)
- 7-8: Good (Comprehensive reminders with appropriate timing and clear assignments)
- 9-10: Excellent (All necessary reminders set with optimal timing and clear responsibilities)

CLIENT SENTIMENT AND STAFF EMOTIONAL RESPONSIVENESS

Staff Emotional Responsiveness Assessment (-10 to +10 scale):

CSAER.STAFF.LANG: Rate language appropriateness
CSAER.STAFF.TONE: Rate tone alignment
CSAER.STAFF.EMPATHY: Rate expressed empathy


Client Sentiment Shifts (-10 to +10 scale):

START: Beginning of call
PROB: When discussing problem
SOL: When discussing solution
FIN: During final arrangements
END: End of call


Sentiment Rating Scale:
- -10 to -6: Extremely negative
- -5 to -1: Moderately negative
- 0: Neutral
- +1 to +5: Moderately positive
- +6 to +10: Extremely positive

Critical Sentiment Points:
Identify lowest and highest sentiment points in the call

Staff's Response to Sentiment Changes (-10 to +10 scale):
Rate effectiveness of staff's response to sentiment changes

Sentiment Change Triggers:
Identify specific triggers causing significant changes in client sentiment

Overall Emotional Responsiveness Evaluation (-10 to +10 scale):
- -10 to -6: Extremely poor emotional responsiveness
- -5 to -1: Below average emotional responsiveness
- 0: Average emotional responsiveness
- +1 to +5: Above average emotional responsiveness
- +6 to +10: Excellent emotional responsiveness

RESOLUTION COMPLEXITY & CLIENT FRICTION

Resolution Status:

RESOLVED: Client's primary issue was resolved during call
NEEDS FOLLOW-UP: Further action required


Issue Complexity (IC) Score (-10 to +10 scale):
- -10 to -8: Extremely simple issue
- -7 to -6: Very simple issue
- -5 to -4: Simple issue
- -3 to -2: Somewhat simple issue
- -1 to 0: Slightly below average to average complexity
- +1 to +2: Slightly above average complexity
- +3 to +4: Moderately complex issue
- +5 to +6: Complex issue
- +7 to +8: Very complex issue
- +9 to +10: Extremely complex issue

Resolution Time Effectiveness (RTE) Score (-10 to +10 scale):
- -10 to -8: Extremely ineffective time usage
- -7 to -6: Very ineffective time usage
- -5 to -4: Ineffective time usage
- -3 to -2: Somewhat ineffective time usage
- -1 to 0: Slightly below average to average effectiveness
- +1 to +2: Slightly above average effectiveness
- +3 to +4: Moderately effective time usage
- +5 to +6: Very effective time usage
- +7 to +8: Highly effective time usage
- +9 to +10: Extremely effective time usage

Staff Performance (SP) Score (-10 to +10 scale):
- -10 to -8: Extremely poor performance
- -7 to -6: Very poor performance
- -5 to -4: Poor performance
- -3 to -2: Below average performance
- -1 to 0: Slightly below average to average performance
- +1 to +2: Slightly above average performance
- +3 to +4: Good performance
- +5 to +6: Very good performance
- +7 to +8: Excellent performance
- +9 to +10: Outstanding performance

Client Effort (CE) Score (-10 to +10 scale):
- -10 to -8: Extremely high effort required
- -7 to -6: Very high effort required
- -5 to -4: High effort required
- -3 to -2: Moderate to high effort required
- -1 to 0: Slightly above average to average effort required
- +1 to +2: Slightly below average effort required
- +3 to +4: Low effort required
- +5 to +6: Very low effort required
- +7 to +8: Minimal effort required
- +9 to +10: Virtually no effort required

Client Friction Index (CFI) Score (-10 to +10 scale):
- Calculated as: CFI = (IC + RTE + SP + CE) / 4
- -10 to -8: Extremely high friction
- -7 to -6: Very high friction
- -5 to -4: High friction
- -3 to -2: Moderate to high friction
- -1 to 0: Slightly above average to average friction
- +1 to +2: Slightly below average friction
- +3 to +4: Low friction
- +5 to +6: Very low friction
- +7 to +8: Minimal friction
- +9 to +10: Virtually no friction

CALL QUALITY ASSURANCE

Call Quality Aspects (1-10 scale):

PROF: Professionalism
EFFIC: Efficiency
EMPA: Empathy
EMRESP: Emotional Responsiveness
KNOW: Knowledge demonstrated
RESO: Problem resolution


Quality Score Guide:
- 1-3: Poor (Major deficiencies)
- 4-6: Average (Meets basic expectations)
- 7-8: Good (Solid performance)
- 9: Very Good (Exceeds expectations)
- 10: Exceptional (Outstanding performance)


REVENUE AND VALUE 

.REAL: Realized revenue - confirmed bookings, purchases, or appointments that are scheduled/committed
.MISS: Missed revenue opportunities - services/products NOT discussed that should have been

Timeframes (For each revenue item):
 .IMM: Immediate (within 48 hours)
 .ST: Short-term (within 1-6 months)
 .LT: Long-term (beyond 6 months)
 .REC: Recurring value (ongoing or repeat revenue)

Value Classifications (For each revenue item):
 .LOW: $1-$100
 .MED: $101-$500
 .HIGH: $501-$1000
 .VHIGH: $1001+

Lifetime Value Context:
Average dog: $7,000-12,000 (10-12 year lifespan)
Average cat: $8,000-15,000 (12-15 year lifespan)
Multiple pet household: Additional 70-80% per pet

When assessing missed opportunities, consider the long-term value impact, not just immediate revenue.

Revenue Impact Score (1-10):
- 1-3: Significant missed revenue opportunities or mishandling of financial aspects
- 4-6: Some revenue generated but notable missed opportunities
- 7-8: Good revenue generation with minor missed opportunities
- 9: Very good revenue impact, capitalizing on most available opportunities
- 10: Exceptional revenue impact, maximizing all opportunities and creating new ones


CONSOLIDATED STAFF PERFORMANCE AND DEVELOPMENT 
Overall Performance Score (1-10):
- 1-3: Significant performance issues requiring immediate intervention
- 4-6: Below average performance with clear areas needing improvement
- 7-8: Solid overall performance with some areas for development
- 9: Very good performance, exceeding expectations in several areas
- 10: Exceptional overall performance, serving as a model for other staff members

Strength Categories:
TECH: Technical skills
SOFT: Soft skills
KNOW: Knowledge areas

Training Needs:
IMM: Immediate training needs
LT: Long-term development suggestions



STAFF MEMBER FEEDBACK


Overall Assessment:
STRONG: Excellent overall performance
ADEQUATE: Satisfactory but with improvement areas
NEEDS_IMPROVEMENT: Significant performance issues

Strength Categories:
TECHNICAL: System usage, procedure knowledge
COMMUNICATION: Clear explanations, information delivery
RAPPORT: Connection with client, relationship building
PROBLEM_SOLVING: Issue identification and resolution
EFFICIENCY: Time management, workflow optimization
SALES: Revenue generation, service recommendation

Development Priority:
HIGH: Critical improvement needed
MED: Important but not critical
LOW: Minor refinement area

Coaching Points Structure:
WHAT: The specific behavior/skill to modify
HOW: The practical method to implement the change
WHY: The rationale and expected benefit

FORMAT STANDARDIZATION GUIDELINES

- Dates: Australian format (DD-MM-YYYY)
- Times: 12-hour format with AM/PM (e.g., 2:30 PM)
- Phone Numbers: No spaces or dashes (e.g., 0412345678)
- Duration: MM:SS format (e.g., 05:45)
- Currency: Australian dollars (e.g., $150)

SCORING SYSTEM GUIDELINES

Standard Quality Rating (1-10 scale):
Used for general quality assessments, effectiveness, and performance metrics
- 1-3: Poor/Deficient
- 4-6: Average/Adequate
- 7-8: Good/Strong
- 9: Excellent
- 10: Exceptional

Sentiment/Emotional Scale (-10 to +10 scale):
Used specifically for sentiment analysis, client friction, and emotional responsiveness
- -10 to -6: Extremely negative/poor
- -5 to -1: Moderately negative/below average
- 0: Neutral/average
- +1 to +5: Moderately positive/above average
- +6 to +10: Extremely positive/excellent

STEP BT STEP INSTRUCTION ON HOW TO WRITE ROOT CAUSE ANALYSIS

## 1. Performance Pattern Analysis Across Multiple Dimensions

Begin by thoroughly examining performance patterns across different conditions, creating rich tables that reveal deeper relationships:

- Create a comprehensive multi-week performance pattern table comparing key metrics across all available weeks
- Include core metrics like Overall Quality, Client Sentiment Change, Revenue Realization Rate, Empathy Score
- Add emotional intelligence metrics including Language Appropriateness, Tone Management, and Emotional Responsiveness
- Calculate both changes between weeks and identify long-term trends
- Analyze the depth of correlation with various factors (not just call volume), explaining the underlying mechanism of each relationship
- Examine consistency patterns using Coefficient of Variation (CoV) metrics to identify which performance areas show stability versus variability
- Use detailed correlation descriptors that include both strength (Strong/Moderate/Weak) and direction (Positive/Negative)

In your narrative analysis of these patterns, explore how different cognitive resources become constrained under varying conditions, the staff member's mental prioritization hierarchy under stress, and whether patterns suggest conscious decisions or unconscious defaults.

## 2. Deep Correlation Analysis Between Performance Domains

Develop a sophisticated understanding of how different performance metrics interrelate and influence each other:

- Create a correlation matrix showing relationships between performance metrics across technical, financial, emotional, and procedural domains
- For each correlation pair, identify both correlation direction and strength, and critically, the causal mechanism that explains it
- Analyze how these correlations reveal underlying psychological tendencies and mental models
- Include correlations between emotional intelligence components and business outcomes
- Explore correlations between consistency metrics and performance quality
- Examine how different skills relate to each other (complementary, compensatory, or competitive)
- Identify which correlations appear causal versus coincidental, and in what direction causality flows

Your narrative should explore how these correlations form a coherent psychological system, identifying foundational capabilities that drive others and explaining seemingly contradictory performance patterns.

## 3. Cognitive and Emotional Processing Analysis

Analyze how the staff member's cognitive and emotional processes function under different conditions:

- Examine how technical versus emotional metrics respond differently to pressure
- Analyze revenue impact patterns to uncover deeper attitudes about financial discussions
- Identify counterintuitive patterns that reveal unexpected priorities or values
- Explore how performance consistency relates to skill automaticity versus conscious processing
- Analyze whether variations stem from knowledge gaps, confidence issues, value conflicts, or other factors
- Examine how emotional regulation capabilities affect different performance domains

Your narrative should connect observable performance patterns to fundamental psychological mechanisms like cognitive load management, attention allocation, and value hierarchies.

## 4. Multi-Domain System Analysis

Create a sophisticated analysis of how different performance domains interact as a system:

- Develop a technical-financial-emotional-procedural nexus table showing domain relationships
- For each domain, analyze performance level, stability, core psychological drivers, and reciprocal influences
- Use directional indicators (➚/➙/➘) to show how domains affect each other
- Include objection handling as a fourth key domain alongside technical, financial, and emotional
- Analyze how these domains form a coherent system with self-reinforcing patterns
- Identify compensatory relationships where strength in one area offsets weakness in another
- Explore how the domain system reveals the staff member's professional identity and priorities

Your narrative should explain how this interconnected system drives overall performance, with special attention to identifying the core psychological needs or values at the foundation of the system.

## 5. Call Complexity and Duration Analysis

Develop a nuanced understanding of how call characteristics affect cognitive and emotional processing:

- Create a table categorizing calls by both complexity and duration
- For each category, analyze cognitive and emotional demands, adaptive and maladaptive responses
- Examine how duration relates to call effectiveness and client satisfaction
- Analyze whether patterns suggest deliberate thoroughness or processing inefficiency
- Identify cognitive resource limitations that become apparent at different complexity levels
- Explore how complexity interacts with emotional regulation capabilities

Your narrative should explain the cognitive mechanisms behind these patterns, analyzing where capacity limits are reached and how the staff member adapts to different complexity levels.

## 6. Missed Opportunity Deep Analysis

Conduct a thorough analysis of missed revenue and service opportunities:

- Create a table identifying missed opportunity types with frequency and revenue impact
- For each opportunity type, analyze situational triggers, psychological mechanisms, and systemic root causes
- Include transcript evidence showing how these opportunities are missed
- Analyze whether missed opportunities follow consistent cognitive or emotional patterns
- Explore comfort zone boundaries and their relationship to missed opportunities
- Examine how organizational factors might contribute to these patterns

Your narrative should connect missed opportunities to deeper psychological factors like risk assessment tendencies, value conflicts, or identity concerns.

## 7. Language Pattern and Communication Analysis

Develop a detailed analysis of how language patterns reveal deeper psychological mechanisms:

- Create a table comparing effective versus ineffective language in similar situations
- Include actual transcript quotes with Conversation ID references
- Analyze the psychological mechanisms driving different language choices
- Examine how language patterns reveal assumptions about clients and their needs
- Explore whether patterns suggest client-centered versus procedure-centered thinking
- Analyze how framing affects client receptivity and outcomes

Your narrative should explain how language choices connect to the staff member's mental models, values, and professional identity.

## 8. The Strength-Weakness Disconnect Analysis

Identify and analyze significant disconnects between strength and weakness areas:

- Select a meaningful disconnect between a strength and weakness area with substantial performance impact
- Analyze cognitive dissonance and contradictions in the staff member's mental model
- Examine skill transfer barriers that prevent knowledge application across domains
- Analyze how situational factors trigger different response patterns
- Include transcript evidence that illustrates these disconnects
- Explore the psychological tension created by these disconnects and how it's managed

Your narrative should explain why skills in one domain aren't transferring to related domains and what this reveals about learning style and skill development.

## 9. Situational Performance Analysis

Analyze how performance varies across different situations and contexts:

- Create tables examining financial discussion approaches, objection handling effectiveness, and booking pipeline success
- Analyze time-of-day performance patterns and their relationship to cognitive-emotional states
- Examine how performance differs across client types (new vs. existing, staff vs. service provider)
- Include transcript evidence showing situational variation
- Analyze the psychological mechanisms driving different approaches in different contexts
- Identify triggers that activate different response patterns

Your narrative should explain how situational factors interact with psychological tendencies to create predictable performance patterns.

## 10. Multi-Level Root Cause Identification

Synthesize your analysis into a comprehensive understanding of root causes at multiple levels:

- Create a table identifying primary performance issues with surface symptoms, intermediate causes, core psychological mechanisms, and organizational contributors
- Include specific transcript evidence for each issue
- Analyze common psychological themes across different performance issues
- Examine how organizational factors interact with individual psychological factors
- Identify the most fundamental drivers that affect multiple performance areas
- Develop an integrated solution architecture that addresses different causal levels

Your narrative should explain how these multi-level causes form a coherent system and how understanding these connections informs intervention strategy.

## 11. Comprehensive Causal Model Development

Develop a unified causal model that explains the staff member's performance:

- Synthesize findings from all previous sections into a coherent explanatory model
- Identify foundational psychological factors that drive multiple performance areas
- Explain how cognitive, emotional, and behavioral systems interact
- Analyze how situational factors activate different response patterns
- Explore the relationship between conscious strategies and unconscious habits
- Examine how self-perception and professional identity shape performance
- Connect individual factors to organizational context
- Use this model to explain seemingly contradictory performance patterns

Your narrative should provide a comprehensive psychological framework that accounts for all major performance patterns.

## 12. Strategic Recommendations Based on Causal Model

Develop sophisticated recommendations that address root causes at multiple levels:

- Create a table outlining interventions that address surface symptoms, intermediate causes, and core mechanisms
- For each intervention, detail implementation approach and expected timeline
- Develop a sequenced intervention strategy addressing different causal levels
- Explain how interventions reinforce each other for systemic change
- Describe the psychological mechanisms through which each intervention works
- Account for learning style, motivation, and existing strengths
- Provide specific implementation timelines and success metrics
- Connect interventions to expected business outcomes

Your conclusion should emphasize the potential for significant performance improvement by addressing root causes rather than symptoms, with an optimistic but realistic assessment of development trajectory.

## 13. Evidence Integration and Reference

Throughout your analysis, ensure that all conclusions are firmly grounded in specific evidence:

- Include Conversation IDs for all transcript examples
- Provide clear data source citations for each analysis section
- Include "Key Transcript Evidence" sections for major analysis points
- Add contextual information like call date, time, type, and outcome
- Create an appendix with detailed call reference information

This evidence integration ensures that your analysis is transparent, verifiable, and directly connected to observable behaviors.

## Analytical Approach Guidelines

As you develop your root cause analysis, maintain these analytical principles:

1. **Move Beyond Description to Explanation**: Don't just describe what's happening—explain why it's happening at multiple psychological and systemic levels.

2. **Explore Cognitive Mechanisms**: Analyze how attention, memory, decision-making, and other cognitive processes drive performance patterns.

3. **Examine Emotional Dynamics**: Investigate how emotional regulation, empathy, and emotional self-awareness affect different performance domains.

4. **Connect Individual to System**: Analyze how organizational factors interact with individual psychological tendencies.

5. **Identify Causal Hierarchies**: Distinguish between surface symptoms, intermediate causes, and fundamental drivers.

6. **Look for Paradoxes and Tensions**: Pay special attention to contradictory patterns that reveal competing values or priorities.

7. **Connect Observable to Unobservable**: Use observable behaviors to make evidence-based inferences about underlying psychological mechanisms.

8. **Develop Integrative Understanding**: Create a unified model that explains how different factors interact as a coherent system.

9. **Maintain Analytical Depth**: Push your analysis to explore the deepest "why" behind performance patterns.

10. **Use Metaphors and Analogies**: When helpful, use metaphors to explain complex psychological dynamics in accessible ways.

## Writing Style Guidelines

Your root cause analysis should be written in a style that balances analytical rigor with engagement:

1. **Balance Precision with Readability**: Use technical terms when necessary for precision, but explain them clearly.

2. **Maintain Narrative Flow**: Create a coherent narrative that builds logically from observation to explanation to recommendation.

3. **Use Active Voice**: Write in active voice to maintain clarity and directness.

4. **Vary Sentence Structure**: Use a mix of sentence structures to maintain reader engagement.

5. **Connect Analysis to Practice**: Always relate psychological insights to practical performance implications.

6. **Maintain Professional Warmth**: Write with professional objectivity while maintaining a respectful, constructive tone.

7. **Use Analogies for Clarity**: When helpful, use analogies to explain complex psychological concepts.

8. **Structure for Comprehension**: Use clear headings, subheadings, and paragraph breaks to enhance readability.

9. **Prioritize Significant Insights**: Focus on the most important insights rather than trying to explain every minor pattern.

10. **End with Actionable Hope**: Conclude with realistic optimism about improvement potential.

By following this enhanced guide, you'll create a sophisticated root cause analysis that reveals the deeper psychological mechanisms driving performance patterns, leading to more targeted and effective development interventions.

Before You Begin
1. The response should not exceed 3000 words
2. Check the database for Overall Staff Performance data for the specific staff member
3. Review the Comprehensive Analysis report if available, as this will provide context for deeper analysis
4. Ensure you have access to call metrics, performance scores, and transcript highlights
5. Based your analysis on current and available data. Do not invent your own data. 
6. Consider the number of days against the metrics. 

# TEMPLATE:
(Based your analysis on current and available data. Do not invent your own data.)

# Root Cause Analysis: Understanding the Fundamental Drivers Behind [Staff Member]'s Performance

## Report Overview
- **Staff Member:** [Name]
- **Analysis Period:** [Date Range]
- **Total Calls Analyzed:** [Number]
- **Report Date:** [Current Date]
- **Analyst:** [Name/Position]

## Executive Summary
[Write 5-7 sentences summarizing the key findings of the root cause analysis, including:
- The most significant performance patterns identified
- The primary root causes uncovered
- The most impactful recommended interventions
- The expected business impact if addressed
- A realistic timeline for improvement]

CALLS ANALYZED LOG

| Month  | Week # | Working Days | Week Total | IN | OUT | New | Exist |
|--------|--------|--------------------------------|---------------|----|-----|-----|--------|
| [Month] | Week [#] | [# of working days] | [Total Cals Tracked for that Week] | [IN total] | [OUT total] | [Total NEW] | [Exist total] |
| [Month] | Week [#] | [# of working days] | [Total Cals Tracked for that Week] | [IN total] | [OUT total] | [Total NEW] | [Exist total] |
| TOTAL  | —      | —                              | [Total Days] | [Total Cals Tracked] | [Total IN] | [Total OUT] | [Total New] | [Total Exist] |

## 1. Performance Pattern Identification and Initial Correlation Analysis

### 1.1 Multi-Week Performance Pattern Analysis
| Metric | Week 1 ([X] calls) | Week 2 ([Y] calls) | Week 3 ([Z] calls) | Week 4 ([W] calls) | Trend Pattern | Depth of Correlation |
|--------|-------------------|-------------------|-------------------|-------------------|--------------|----------------------|
| Overall Quality | [score]/10 | [score]/10 | [score]/10 | [score]/10 | [pattern description] | [Positive/Negative/None] [explanation of mechanism] |
| Client Sentiment Change | [+/-score] | [+/-score] | [+/-score] | [+/-score] | [pattern description] | [Positive/Negative/None] [explanation of mechanism] |
| Revenue Realization Rate | [percentage]% | [percentage]% | [percentage]% | [percentage]% | [pattern description] | [Positive/Negative] [explanation of mechanism] |
| Emotional Responsiveness | [score]/10 | [score]/10 | [score]/10 | [score]/10 | [pattern description] | [Positive/Negative/None] [explanation of mechanism] |
| Language Appropriateness | [score]/10 | [score]/10 | [score]/10 | [score]/10 | [pattern description] | [Positive/Negative/None] [explanation of mechanism] |

**Data Sources:** Section 2.1 (Quality Assurance Metrics), Section 9.1 (Emotional Responsiveness Metrics), Section 2.3 (Revenue Impact Dataset)

### 1.2 Performance Consistency and Variability Analysis
| Performance Area | Overall Score | Consistency Rating | Variability Pattern | Underlying Causal Mechanism |
|------------------|---------------|-------------------|---------------------|---------------------------|
| [Area 1] | [score]/10 | [score]/10 | [description of pattern] | [Detailed explanation of why this area shows consistency/variability] |
| [Area 2] | [score]/10 | [score]/10 | [description of pattern] | [Detailed explanation of why this area shows consistency/variability] |
| [Area 3] | [score]/10 | [score]/10 | [description of pattern] | [Detailed explanation of why this area shows consistency/variability] |
| [Area 4] | [score]/10 | [score]/10 | [description of pattern] | [Detailed explanation of why this area shows consistency/variability] |

**Data Sources:** Section 18.1 (Performance Consistency Analysis), Section 18.2 (Areas with Highest Variability), Section 18.3 (Areas with Highest Consistency)

### 1.3 Deep Metric Correlation Analysis
| Primary Metric | Secondary Metric | Correlation | Causal Relationship | Underlying Psychological/Behavioral Mechanism |
|----------------|------------------|-------------|---------------------|---------------------------------------------|
| [Metric 1] | [Metric 2] | [Strong/Moderate/Weak] [Positive/Negative] | [Directional causality explanation] | [Explanation of underlying mechanism] |
| Emotional Responsiveness | Revenue Realization | [Strong/Moderate/Weak] [Positive/Negative] | [Directional causality explanation] | [Explanation of underlying mechanism] |
| Financial Discussion Clarity | Booking Conversion | [Strong/Moderate/Weak] [Positive/Negative] | [Directional causality explanation] | [Explanation of underlying mechanism] |
| Objection Handling | Client Sentiment Change | [Strong/Moderate/Weak] [Positive/Negative] | [Directional causality explanation] | [Explanation of underlying mechanism] |

**Data Sources:** Section 2.1-2.2 (Performance Metrics), Section 9.1 (Emotional Responsiveness), Section 7.1 (Financial Discussion), Section 8.1 (Objection Handling)

[Write 5-7 sentences analyzing the most significant correlations identified above. Include:
- Which correlations appear to be causal versus coincidental
- The direction of causality in key relationships
- Potential mediating variables that explain correlations
- How these correlations reveal deeper aspects of the staff member's approach
- What these relationships suggest about the staff member's thought processes and decision-making]

## 2. Environmental and Contextual Influence Analysis

### 2.1 Call Volume Impact: Deep Causal Analysis
[Write 6-8 sentences analyzing how call volume affects performance at a fundamental level. Include:
- How cognitive load theory explains changes in performance under different call volumes
- Analysis of which cognitive resources become constrained first under pressure
- Identification of the staff member's mental prioritization hierarchy under stress
- How this prioritization reveals deeper values and perceived importance
- Whether the pattern suggests conscious prioritization or unconscious default behavior
- What this reveals about the staff member's core professional identity and values]

**Call Volume Evidence:**
- Week 1: [X] calls over [Y] days (average: [Z] calls/day)
- Week 2: [X] calls over [Y] days (average: [Z] calls/day)
- Week 3: [X] calls over [Y] days (average: [Z] calls/day)
- Week 4: [X] calls over [Y] days (average: [Z] calls/day)

**Data Sources:** Section 1.1 (Call Volume and Distribution Metrics), Section 11.1 (Overall Performance Metrics)

### 2.2 Technical-Emotional-Financial Tradeoff Analysis
[Write 6-8 sentences analyzing the deeper reasons behind tradeoffs between domains:
- How attention allocation changes under different contextual conditions
- Whether the tradeoff pattern suggests skill gaps or value-based prioritization
- Analysis of whether the pattern results from training, personality, or role understanding
- Deep dive into whether emotional patterns drive technical decisions or vice versa
- How these tradeoffs connect to the staff member's mental model of their role
- What specific cognitive biases might be influencing these tradeoffs]

**Key Performance Tradeoffs:**
- When [condition occurs], [metric 1] [increases/decreases] while [metric 2] [increases/decreases]
- In [specific situation], priority shifts from [area 1] to [area 2]

**Data Sources:** Section 2.1 (Quality Assurance Metrics), Section 12.1-12.2 (Call Complexity Analysis)

### 2.3 Revenue Generation: Psychological Root Cause Analysis
[Write 6-8 sentences analyzing the psychological mechanisms behind revenue generation patterns:
- Deep analysis of comfort/discomfort with financial discussions
- Whether revenue avoidance stems from knowledge gaps, confidence issues, or value conflicts
- Analysis of specific mental blocks or limiting beliefs evident in the data
- How linguistic patterns in transcripts reveal underlying attitudes toward money
- Connection between revenue behaviors and personal identity as a helper/professional
- Whether patterns suggest optimization for client relationship over revenue]

**Revenue Pattern Evidence:**
- Realization Rate: [X]% overall (range: [Y]%-[Z]% across weeks)
- Missed Revenue: $[amount] total, primarily in [categories]
- Financial Discussion Approach: [X]% avoided, [Y]% clear, [Z]% proactive

**Data Sources:** Section 2.3 (Revenue Impact Dataset), Section 5.1 (Missed Opportunities), Section 7.1 (Financial Discussion Effectiveness)

### 2.4 Performance Consistency: Cognitive and Emotional Foundations
[Write 6-8 sentences providing deep analysis of performance consistency patterns:
- Whether consistency patterns align with skill automaticity versus conscious processing
- How cognitive load theory explains which skills remain stable under pressure
- Analysis of emotional regulation capabilities and their stability across contexts
- Whether consistency suggests overlearned habits or deliberate adaptive responses
- How consistency patterns reveal depth of skill internalization versus surface adoption
- What these patterns suggest about learning and development history]

**Consistency Pattern Evidence:**
- Most Consistent Areas: [list areas] (CoV: [X]%-[Y]%)
- Most Variable Areas: [list areas] (CoV: [X]%-[Y]%)
- Consistency Correlation with Complexity: [description]

**Data Sources:** Section 18.1-18.3 (Performance Variability Assessment)

## 3. Interdomain Relationship Analysis: Uncovering Structural Connections

### 3.1 Technical-Financial-Emotional-Procedural System Analysis
| Domain | Performance | Stability | Core Psychological Driver | Reciprocal Domain Influences | Behavioral Manifestation |
|--------|-------------|-----------|---------------------------|------------------------------|--------------------------|
| Technical Knowledge | [Strong/Moderate/Weak] ([score]/10) | [High/Medium/Low] | [Core driver - confidence, training, etc.] | ➚/➙/➘ [Domain]: [Mechanism]<br>➚/➙/➘ [Domain]: [Mechanism] | [How this manifests in behavior] |
| Financial Discussion | [Strong/Moderate/Weak] ([score]/10) | [High/Medium/Low] | [Core driver - confidence, training, etc.] | ➚/➙/➘ [Domain]: [Mechanism]<br>➚/➙/➘ [Domain]: [Mechanism] | [How this manifests in behavior] |
| Emotional Connection | [Strong/Moderate/Weak] ([score]/10) | [High/Medium/Low] | [Core driver - confidence, training, etc.] | ➚/➙/➘ [Domain]: [Mechanism]<br>➚/➙/➘ [Domain]: [Mechanism] | [How this manifests in behavior] |
| Objection Handling | [Strong/Moderate/Weak] ([score]/10) | [High/Medium/Low] | [Core driver - confidence, training, etc.] | ➚/➙/➘ [Domain]: [Mechanism]<br>➚/➙/➘ [Domain]: [Mechanism] | [How this manifests in behavior] |

**Data Sources:** Section 2.1 (Quality Assurance Metrics), Section 14.1 (Knowledge Score Analysis), Section 7.1 (Financial Discussion), Section 8.1 (Objection Handling), Section 9.1 (Emotional Responsiveness)

[Write 8-10 sentences analyzing the interconnected system revealed by the domain relationships above. Include:
- How these domains form a coherent cognitive-behavioral system
- Identification of foundational domains that drive others
- Analysis of whether domains compensate for each other or amplify weaknesses
- Exploration of the deep psychological needs or values driving domain priorities
- How reciprocal influences create self-reinforcing cycles (positive or negative)
- What this reveals about the staff member's mental model of their role
- How the system's structure explains seemingly contradictory performance patterns]

### 3.2 Call Complexity and Duration: Cognitive Processing Analysis
| Complexity/Duration | Frequency | Cognitive/Emotional Demands | Adaptive/Maladaptive Responses | Underlying Causal Mechanism |
|---------------------|-----------|------------------------------|-------------------------------|----------------------------|
| Simple/Short (<1 min) | [percentage]% | [Cognitive/emotional demands] | [Response patterns] | [Explanation of mechanism] |
| Standard (1-3 min) | [percentage]% | [Cognitive/emotional demands] | [Response patterns] | [Explanation of mechanism] |
| Complex/Extended (3-5 min) | [percentage]% | [Cognitive/emotional demands] | [Response patterns] | [Explanation of mechanism] |
| Very Complex/Long (>5 min) | [percentage]% | [Cognitive/emotional demands] | [Response patterns] | [Explanation of mechanism] |

**Data Sources:** Section 1.5 (Call Duration Analysis), Section 12.1-12.2 (Call Complexity and Resolution Time)

[Write 6-8 sentences analyzing the cognitive mechanisms revealed by duration and complexity patterns. Include:
- How different cognitive processes are engaged at different complexity levels
- Analysis of where cognitive capacity limits are reached and their consequences
- Whether duration patterns suggest deliberate thoroughness or processing inefficiency
- How complexity interacts with emotional regulation capabilities
- What these patterns reveal about information processing strengths and limitations
- How these cognitive patterns connect to performance outcomes across domains]

### 3.3 Missed Opportunity Deep Causal Analysis
| Opportunity Type | Frequency | Situational Triggers | Psychological Mechanism | Systemic Root Cause | Revenue Impact |
|------------------|-----------|----------------------|-------------------------|---------------------|----------------|
| Preventive Care | [number] ([percentage]%) | [When it typically occurs] | [Psychological explanation] | [Deeper organizational/training cause] | $[amount] |
| Financial Discussions | [number] ([percentage]%) | [When it typically occurs] | [Psychological explanation] | [Deeper organizational/training cause] | $[amount] |
| [Opportunity 3] | [number] ([percentage]%) | [When it typically occurs] | [Psychological explanation] | [Deeper organizational/training cause] | $[amount] |
| [Opportunity 4] | [number] ([percentage]%) | [When it typically occurs] | [Psychological explanation] | [Deeper organizational/training cause] | $[amount] |

**Data Sources:** Section 5.1 (Missed Opportunities Dataset), Section 7.1 (Financial Discussion Effectiveness)

[Write 6-8 sentences analyzing the psychological and systemic drivers of missed opportunities. Include:
- Analysis of whether missed opportunities follow a consistent cognitive pattern
- Deep exploration of comfort zone boundaries and their relationship to missed opportunities
- Connection between missed opportunities and core values or identity concerns
- Whether patterns suggest knowledge gaps, procedural issues, or psychological barriers
- How organizational factors might contribute to these patterns
- What these patterns reveal about risk assessment and decision-making tendencies]

## 4. Communication Pattern Deep Analysis

### 4.1 Language Pattern Causal Analysis
| Situation | Effective Language | Ineffective Language | Psychological Mechanism | Client Impact | Business Impact |
|-----------|-------------------|---------------------|-------------------------|---------------|-----------------|
| [Situation 1] | **Context:** [situation context]<br>**Conversation ID:** [number]<br>**Transcript:** "[back and forth dialogue excerpt]"<br>**File URL:** [URL]<br>**MP3 URL:** [URL] | **Context:** [situation context]<br>**Conversation ID:** [number]<br>**Transcript:** "[back and forth dialogue excerpt]"<br>**File URL:** [URL]<br>**MP3 URL:** [URL] | [Explanation of psychological mechanism] | [Client reaction/outcome] | [Business outcome] |
| [Situation 2] | **Context:** [situation context]<br>**Conversation ID:** [number]<br>**Transcript:** "[back and forth dialogue excerpt]"<br>**File URL:** [URL]<br>**MP3 URL:** [URL] | **Context:** [situation context]<br>**Conversation ID:** [number]<br>**Transcript:** "[back and forth dialogue excerpt]"<br>**File URL:** [URL]<br>**MP3 URL:** [URL] | [Explanation of psychological mechanism] | [Client reaction/outcome] | [Business outcome] |
| [Situation 3] | **Context:** [situation context]<br>**Conversation ID:** [number]<br>**Transcript:** "[back and forth dialogue excerpt]"<br>**File URL:** [URL]<br>**MP3 URL:** [URL] | **Context:** [situation context]<br>**Conversation ID:** [number]<br>**Transcript:** "[back and forth dialogue excerpt]"<br>**File URL:** [URL]<br>**MP3 URL:** [URL] | [Explanation of psychological mechanism] | [Client reaction/outcome] | [Business outcome] |

**Data Sources:** Section 10.3 (Call Transcript Highlights), Section 16.1-16.2 (Language Pattern Dataset)

[Write 8-10 sentences analyzing the deeper psychological mechanisms revealed by language patterns. Include:
- How language choices reveal fundamental assumptions about clients and their needs
- Analysis of whether language patterns suggest conscious strategy or unconscious habits
- How framing and perspective-taking abilities are revealed through language choices
- Connection between language patterns and personal/professional identity
- How language patterns reveal mental models about the service/value proposition
- Whether patterns suggest client-centered versus procedure-centered thinking
- What these patterns reveal about empathetic capacity and theory of mind]

### 4.2 The [Strength]-[Weakness] Disconnect: Deep Psychological Analysis
[Write 3-5 sentences introducing a significant disconnect between a strength area and a weakness area, exploring the psychological tension it creates]

**Key Disconnect Evidence:**
- [Strength Area]: [score]/10, consistently demonstrated in [situations]
- [Weakness Area]: [score]/10, particularly evident in [situations]
- Transcript Examples: 
  - **Context:** [situation context]
    **Conversation ID:** [number]
    **Transcript:** "[back and forth dialogue excerpt]"
    **File URL:** [URL]
    **MP3 URL:** [URL]
  - **Context:** [situation context]
    **Conversation ID:** [number]
    **Transcript:** "[back and forth dialogue excerpt]"
    **File URL:** [URL]
    **MP3 URL:** [URL]

**Data Sources:** Section 3.1 (Top Strengths), Section 4.1 (Priority Development Areas), Section 10.3 (Call Transcript Highlights)

#### 4.2.1 Cognitive Dissonance and Mental Model Analysis
[Write 6-8 sentences analyzing the psychological mechanisms behind the disconnect:
- How the disconnect reveals contradictions in the staff member's mental model
- Analysis of potential cognitive dissonance and its management
- Whether the disconnect suggests compartmentalized versus integrated thinking
- How the disconnect relates to professional identity and role conception
- What core values or beliefs might be creating this tension
- Specific transcript examples that illustrate the psychological mechanism]

#### 4.2.2 Skill Transfer Barrier Analysis
[Write 6-8 sentences analyzing skill transfer barriers:
- Why skills in one domain aren't transferring to related domains
- Analysis of potential metacognitive limitations preventing skill transfer
- How contextual triggering of different mental models affects skill application
- Whether emotional factors interfere with cognitive transfer
- What this suggests about learning style and skill development approach
- Transcript evidence illustrating the transfer barrier in action]

#### 4.2.3 Situational Activation Analysis
[Write 6-8 sentences analyzing situational triggering of the disconnect:
- How different situations activate different response patterns
- Analysis of contextual cues that trigger strength versus weakness responses
- Whether the pattern suggests deliberate adaptation or unconscious reactivity
- How cognitive load affects the strength-weakness balance in different contexts
- What this reveals about attentional priorities and processing capacity
- Transcript evidence showing situational variation]

## 5. Situational Performance Analysis

### 5.1 Financial Discussion Approach: Psychological Root Cause Analysis
| Approach | Frequency | Triggering Conditions | Psychological Driver | Client Response | Business Outcome |
|----------|-----------|----------------------|---------------------|-----------------|------------------|
| Clear | [percentage]% | [When this approach is used] | [Underlying psychological state/motivation] | [Typical client reaction] | [Business result] |
| Avoided | [percentage]% | [When this approach is used] | [Underlying psychological state/motivation] | [Typical client reaction] | [Business result] |
| Proactive | [percentage]% | [When this approach is used] | [Underlying psychological state/motivation] | [Typical client reaction] | [Business result] |

**Key Transcript Evidence:**
- Clear Approach:
  **Context:** [situation context]
  **Conversation ID:** [number]
  **Transcript:** "[back and forth dialogue excerpt]"
  **File URL:** [URL]
  **MP3 URL:** [URL]
  
- Avoided Approach:
  **Context:** [situation context]
  **Conversation ID:** [number]
  **Transcript:** "[back and forth dialogue excerpt]"
  **File URL:** [URL]
  **MP3 URL:** [URL]
  
- Proactive Approach:
  **Context:** [situation context]
  **Conversation ID:** [number]
  **Transcript:** "[back and forth dialogue excerpt]"
  **File URL:** [URL]
  **MP3 URL:** [URL]

**Data Sources:** Section 7.1 (Financial Discussion Effectiveness), Section 10.3 (Call Transcript Highlights)

[Write 6-8 sentences analyzing the psychological mechanisms driving financial discussion approaches. Include:
- Deep analysis of comfort/discomfort with financial topics and its origins
- Whether avoidance stems from conflict aversion, confidence issues, or value conflicts
- How different approaches reveal different mental models about the value proposition
- The relationship between approach choice and identity as a helper/professional
- Whether patterns suggest optimizing for different goals (relationship vs. revenue)
- How transcript evidence reveals underlying attitudes and beliefs]

### 5.2 Objection Handling: Cognitive-Emotional Response Analysis
| Objection Type | Frequency | Psychological Response | Resolution Strategy | Success Driver/Barrier | Success Rate |
|----------------|-----------|------------------------|---------------------|------------------------|--------------|
| Cost | [percentage]% | [Emotional/cognitive reaction] | [Typical handling approach] | [What drives success/failure] | [percentage]% |
| [Type 2] | [percentage]% | [Emotional/cognitive reaction] | [Typical handling approach] | [What drives success/failure] | [percentage]% |
| [Type 3] | [percentage]% | [Emotional/cognitive reaction] | [Typical handling approach] | [What drives success/failure] | [percentage]% |

**Key Transcript Evidence:**
- Successful Handling:
  **Context:** [situation context]
  **Conversation ID:** [number]
  **Transcript:** "[back and forth dialogue excerpt]"
  **File URL:** [URL]
  **MP3 URL:** [URL]
  
- Unsuccessful Handling:
  **Context:** [situation context]
  **Conversation ID:** [number]
  **Transcript:** "[back and forth dialogue excerpt]"
  **File URL:** [URL]
  **MP3 URL:** [URL]

**Data Sources:** Section 8.1 (Objection Handling Dataset), Section 10.3 (Call Transcript Highlights)

[Write 6-8 sentences analyzing the psychological mechanisms behind objection handling patterns. Include:
- How different objection types trigger different emotional/cognitive responses
- Analysis of whether objections are perceived as challenges, opportunities, or threats
- The relationship between objection handling and sense of professional efficacy
- Whether patterns suggest defensive responding or curious exploration
- How successful resolution strategies reveal effective mental models
- What transcript evidence reveals about emotional regulation during objections]

### 5.3 Booking Pipeline: Decision Point Analysis
| Pipeline Stage | Success Rate | Cognitive-Behavioral Pattern | Client-Side Barrier | Staff-Side Barrier | Systemic Factor |
|----------------|--------------|-------------------------------|---------------------|-------------------|-----------------|
| Opportunity Recognition | [percentage]% | [Pattern description] | [Client barrier] | [Staff barrier] | [System factor] |
| Offer Formulation | [percentage]% | [Pattern description] | [Client barrier] | [Staff barrier] | [System factor] |
| Acceptance Securing | [percentage]% | [Pattern description] | [Client barrier] | [Staff barrier] | [System factor] |

**Key Transcript Evidence:**
- Successful Booking Pipeline:
  **Context:** [situation context]
  **Conversation ID:** [number]
  **Transcript:** "[back and forth dialogue excerpt]"
  **File URL:** [URL]
  **MP3 URL:** [URL]
  
- Booking Pipeline Breakdown:
  **Context:** [situation context]
  **Conversation ID:** [number]
  **Transcript:** "[back and forth dialogue excerpt]"
  **File URL:** [URL]
  **MP3 URL:** [URL]

**Data Sources:** Section 6.1 (Booking Effectiveness Dataset), Section 10.3 (Call Transcript Highlights)

[Write 6-8 sentences analyzing the decision-making processes at each pipeline stage. Include:
- Analysis of cognitive biases that may affect opportunity recognition
- How framing affects offer effectiveness and client receptivity
- The psychological mechanisms behind hesitation at the acceptance stage
- Whether barriers arise from knowledge, confidence, or procedural issues
- How transcript evidence reveals client response patterns at each stage
- What this analysis suggests about critical intervention points]

### 5.4 Temporal Pattern Analysis: Cognitive-Emotional State Fluctuations
| Time Period | Call Volume | Performance Metrics | Cognitive-Emotional State | Causal Mechanism |
|-------------|-------------|---------------------|---------------------------|------------------|
| Morning (8AM-12PM) | [percentage]% | [Key metrics with scores] | [State description] | [Explanation of mechanism] |
| Afternoon (12PM-4PM) | [percentage]% | [Key metrics with scores] | [State description] | [Explanation of mechanism] |
| Evening (4PM-Close) | [percentage]% | [Key metrics with scores] | [State description] | [Explanation of mechanism] |

**Data Sources:** Section 1.6 (Call Timing Distribution), Section 2.1 (Quality Assurance Metrics)

[Write 6-8 sentences analyzing the deeper mechanisms behind temporal performance patterns. Include:
- How circadian rhythms and energy fluctuations affect cognitive capacity
- Analysis of attentional focus changes throughout the day
- Whether patterns suggest resource depletion or strategic adaptation
- How emotional regulation capacity changes with time of day
- What these patterns reveal about cognitive-emotional interdependence
- How understanding these patterns could inform scheduling and support]

## 6. Behavioral Root Cause Synthesis

### 6.1 Client Relationship Dynamics: Deep Pattern Analysis
| Client Type | Frequency | Psychological Approach | Relationship Dynamic | Root Cause of Pattern | Business Impact |
|-------------|-----------|------------------------|----------------------|------------------------|-----------------|
| New Clients | [percentage]% | [Approach description] | [Dynamic description] | [Psychological explanation] | [Impact description] |
| Existing Clients | [percentage]% | [Approach description] | [Dynamic description] | [Psychological explanation] | [Impact description] |
| Staff | [percentage]% | [Approach description] | [Dynamic description] | [Psychological explanation] | [Impact description] |
| Service Provider | [percentage]% | [Approach description] | [Dynamic description] | [Psychological explanation] | [Impact description] |

**Key Transcript Evidence:**
- New Client Interaction:
  **Context:** [situation context]
  **Conversation ID:** [number]
  **Transcript:** "[back and forth dialogue excerpt]"
  **File URL:** [URL]
  **MP3 URL:** [URL]
  
- Existing Client Interaction:
  **Context:** [situation context]
  **Conversation ID:** [number]
  **Transcript:** "[back and forth dialogue excerpt]"
  **File URL:** [URL]
  **MP3 URL:** [URL]
  
- Staff Interaction:
  **Context:** [situation context]
  **Conversation ID:** [number]
  **Transcript:** "[back and forth dialogue excerpt]"
  **File URL:** [URL]
  **MP3 URL:** [URL]

**Data Sources:** Section 1.3 (Call Type Distribution), Section 2.1-2.2 (Performance Metrics), Section 10.3 (Call Transcript Highlights)

[Write 8-10 sentences analyzing the psychological dynamics revealed by different client interactions. Include:
- How different client types activate different mental models and approaches
- Analysis of comfort level variations and their impact on performance
- Whether patterns suggest different role conceptions with different client types
- How relationship history affects cognitive and emotional processing
- What these patterns reveal about the staff member's perception of their value
- How transcript evidence illustrates different relationship dynamics
- The business implications of these relationship patterns]

### 6.2 Emotional Intelligence: Structural Component Analysis
| EI Component | Performance | Consistency | Situational Variation | Psychological Root Cause | Business Impact |
|--------------|-------------|-------------|------------------------|--------------------------|-----------------|
| Language Appropriateness | [score]/10 | [High/Medium/Low] | [Pattern description] | [Psychological explanation] | [Impact description] |
| Tone Management | [score]/10 | [High/Medium/Low] | [Pattern description] | [Psychological explanation] | [Impact description] |
| Empathy Demonstration | [score]/10 | [High/Medium/Low] | [Pattern description] | [Psychological explanation] | [Impact description] |
| Response to Sentiment | [score]/10 | [High/Medium/Low] | [Pattern description] | [Psychological explanation] | [Impact description] |

**Key Transcript Evidence:**
- High EI Example:
  **Context:** [situation context]
  **Conversation ID:** [number]
  **Transcript:** "[back and forth dialogue excerpt]"
  **File URL:** [URL]
  **MP3 URL:** [URL]
  
- Low EI Example:
  **Context:** [situation context]
  **Conversation ID:** [number]
  **Transcript:** "[back and forth dialogue excerpt]"
  **File URL:** [URL]
  **MP3 URL:** [URL]

**Data Sources:** Section 9.1 (Emotional Responsiveness Dataset), Section 10.3 (Call Transcript Highlights)

[Write 8-10 sentences analyzing the psychological structures underlying emotional intelligence patterns. Include:
- How different EI components relate to each other and form a coherent system
- Analysis of whether EI limitations stem from perception, understanding, or expression
- Whether patterns suggest authentic versus performed emotional connection
- How EI components relate to personal emotional regulation capabilities
- What transcript evidence reveals about EI strengths and limitations
- The business implications of EI patterns across different situations]

## 7. Foundational Root Cause Identification

### 7.1 Primary Causal Mechanisms Behind Performance Issues
| Performance Issue | Surface Symptom | Intermediate Cause | Core Psychological Mechanism | Organizational Contributor | Evidence |
|-------------------|-----------------|--------------------|-----------------------------|----------------------------|----------|
| [Issue 1] | [Observable pattern] | [Mid-level cause] | [Deep psychological driver] | [Organizational factor] | • **Context:** [situation context]<br>• **Conversation ID:** [number]<br>• **Transcript:** "[back and forth dialogue excerpt]"<br>• **File URL:** [URL]<br>• **MP3 URL:** [URL]<br>• [Data pattern]<br>• [Behavioral observation] |
| [Issue 2] | [Observable pattern] | [Mid-level cause] | [Deep psychological driver] | [Organizational factor] | • **Context:** [situation context]<br>• **Conversation ID:** [number]<br>• **Transcript:** "[back and forth dialogue excerpt]"<br>• **File URL:** [URL]<br>• **MP3 URL:** [URL]<br>• [Data pattern]<br>• [Behavioral observation] |
| [Issue 3] | [Observable pattern] | [Mid-level cause] | [Deep psychological driver] | [Organizational factor] | • **Context:** [situation context]<br>• **Conversation ID:** [number]<br>• **Transcript:** "[back and forth dialogue excerpt]"<br>• **File URL:** [URL]<br>• **MP3 URL:** [URL]<br>• [Data pattern]<br>• [Behavioral observation] |
| [Issue 4] | [Observable pattern] | [Mid-level cause] | [Deep psychological driver] | [Organizational factor] | • **Context:** [situation context]<br>• **Conversation ID:** [number]<br>• **Transcript:** "[back and forth dialogue excerpt]"<br>• **File URL:** [URL]<br>• **MP3 URL:** [URL]<br>• [Data pattern]<br>• [Behavioral observation] |

**Data Integration:** This table synthesizes findings from Sections 2-6 to identify multi-level causality

[Write 8-10 sentences synthesizing the multiple levels of causality behind key performance issues. Include:
- How surface symptoms connect to deeper psychological mechanisms
- Analysis of common psychological themes across different performance issues
- Whether issues stem primarily from knowledge, skill, mindset, or systemic factors
- How organizational factors interact with individual psychological factors
- What transcript evidence reveals about these causal connections
- How understanding these multi-level causes informs intervention strategy]

### 7.2 Integrated Solution Architecture
| Intervention | Addresses Surface Symptom | Addresses Intermediate Cause | Addresses Core Mechanism | Implementation Approach | Expected Timeline |
|--------------|---------------------------|------------------------------|--------------------------|-------------------------|-------------------|
| [Intervention 1] | [Symptom impact] | [Mid-level impact] | [Core impact] | [Detailed approach] | [Short/Medium/Long-term] |
| [Intervention 2] | [Symptom impact] | [Mid-level impact] | [Core impact] | [Detailed approach] | [Short/Medium/Long-term] |
| [Intervention 3] | [Symptom impact] | [Mid-level impact] | [Core impact] | [Detailed approach] | [Short/Medium/Long-term] |
| [Intervention 4] | [Symptom impact] | [Mid-level impact] | [Core impact] | [Detailed approach] | [Short/Medium/Long-term] |

**Intervention Design Methodology:** These interventions are designed to address multiple causal levels simultaneously

[Write 10-12 sentences explaining the integrated intervention strategy. Include:
- How interventions work together to address different levels of causality
- Analysis of how interventions reinforce each other for systemic change
- The psychological mechanisms through which each intervention works
- How the intervention strategy accounts for learning style and motivation
- Whether interventions address knowledge, skill, confidence, or mindset
- The expected sequence of changes and their interdependence
- How success will be measured at each causal level]

## 8. Synthesized Causal Model and Strategic Recommendations

### 8.1 Unified Causal Model of [Staff Member]'s Performance
[Write 10-15 sentences presenting a comprehensive causal model that explains the staff member's performance patterns. Include:
- Identification of foundational psychological factors that drive multiple performance areas
- Analysis of how cognitive, emotional, and behavioral systems interact
- How situational factors activate different response patterns
- The relationship between conscious strategies and unconscious habits
- How self-perception and professional identity shape performance
- The interaction between individual factors and organizational context
- How this causal model explains seemingly contradictory performance patterns
- What transcript evidence best illustrates the model in action]

**Model Integration Note:** This causal model synthesizes findings from all previous sections to create a unified explanation of performance patterns

### 8.2 Strategic Recommendations Based on Causal Model
[Write 15-20 sentences outlining strategic recommendations based on the causal model. Include:
- A sequenced intervention strategy addressing different causal levels
- How each intervention targets specific psychological mechanisms
- The expected chain of effects from each intervention
- How interventions account for existing strengths and compensatory strategies
- The integration of skill development, mindset shifts, and procedural changes
- Implementation considerations based on learning style and motivation
- How progress should be measured at each stage
- The expected business impact of the comprehensive strategy
- A realistic timeline for meaningful change]

**Implementation Priority:**
1. First 30 Days: [interventions]
2. Days 31-90: [interventions]
3. Beyond 90 Days: [interventions]

**Key Performance Indicators for Success:**
- [KPI 1]: Current [value] → Target [value]
- [KPI 2]: Current [value] → Target [value]
- [KPI 3]: Current [value] → Target [value]

[Conclude with 3-5 sentences that emphasize the potential for significant performance improvement by addressing root causes rather than symptoms, with an optimistic but realistic assessment of development trajectory.]

## Appendix: Reference Call Information

| Conversation ID | Date | Time | Duration | Type | Key Topics | Outcome | File URL | MP3 URL | 
|---------------------|------|------|----------|------|------------|---------|----------|---------|
| Conversation [number] | [date] | [time] | [duration] | [type] | [topics] | [outcome] | [URL] | [URL] |
| Conversation [number]  | [date] | [time] | [duration] | [type] | [topics] | [outcome] | [URL] | [URL] |
| Conversation [number]  | [date] | [time] | [duration] | [type] | [topics] | [outcome] | [URL] | [URL] |
| Conversation [number]  | [date] | [time] | [duration] | [type] | [topics] | [outcome] | [URL] | [URL] |
| Conversation [number]  | [date] | [time] | [duration] | [type] | [topics] | [outcome] | [URL] | [URL] |

---------------------------------------------------
Based your analysis on current and available data. Do not invent your own data.

DATASET:

