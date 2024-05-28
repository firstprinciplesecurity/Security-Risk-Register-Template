# Security Risk Register Template

## 👑 Authors: Talha Tariq and Swathi Joshi 
#### 🗓️ Publish Date: May 28, 2024

### 🔒 Document Classification <Internal>< Ristricted> <Confidential>

### 🏴‍ Overview & Purpose
This document sets the methodology and scoring criteria for information security risks at <organization>. 

### ☠️ Scope
The methodology and security risk scoring criteria provided here are comprehensive and applicable to all security risks at <Organization>. We aim to establish a standardized, uniform way to score and collate security risk information across all lines of business, applications, and infrastructure.

### 🧮 Risk Scoring
This risk scoring rubric provides a structured framework to assess and assign scores to security risks identified at <organization> based on the predefined criteria outlined below.

### Step 1: Likelihood of Threat Event Initiation
How likely is it that an adversary would initiate an adverse event? 

**Guidance:**
Consider existing controls; this should be viewed in the context of all the controls we have in place today.
Consider adversaries <organization> is likely to be targeted by (e.g., hacktivists, nation states, etc.) in the context of the risk being assessed. Use your professional judgment, threat modeling, internal incident-related data, and industry trends to determine whether it’s appropriate to assume the most capable adversary OR average it out across different adversity profiles. 
There will always be uncertainty about when something will happen. If it’s difficult to estimate the likelihood within the next year initially, it can be helpful to ask yourself what the likelihood of it will be over the next 4  years or X years that you see fit. (e.g., over 4 years, it’s almost certain to happen, but in a given year, it’s somewhat likely).

**Examples:**
The likelihood of a GitHub account or access token being compromised
The likelihood of production cloud access compromise
The likelihood of ransomware event.

| Likelihood of Threat Event Initiation | Scoring Criteria | 
| :---: | :---: |
| Critical/ Very High  | \*The threat event is almost certain to occur and/or <br>\* The threat event is easy to initiate, requiring little to no experience to initiate| 
| High  | \*The threat event is highly likely to occur and/or<br>\* The threat event is somewhat difficult to initiate, requiring a less experienced and less capable  adversary (thereby reducing the likelihood)| 
| Medium | \The threat event is somewhat likely to occur and/or <br>\* The threat event is difficult to initiate, requiring an experienced and capable adversary (thereby reducing the likelihood)| 
| Low  | \*An adversary is unlikely to initiate the threat event and/or <br>\* The threat event is very difficult to initiate, requiring an experienced and highly capable adversary (thereby reducing the likelihood)| 

### Step 2: Likelihood of Threat Event Resulting in Adverse Impact
How likely is it that if an adversary initiated the threat event, it would result in an impact to <organization> (e.g., an adversary gained access to a GitHub account or access token, how likely would it be that an adversary executes it, and how bad would be the impact)? 

**Guidance:**
Consider existing controls; this should be viewed in the context of all the controls we have in place today.
Consider adversaries <organization> has and is likely to be targeted by (e.g., hacktivists, nation states, etc.) in the context of the risk being assessed. Use your professional judgment, threat modeling, internal incident-related data, and industry trends to determine whether it’s appropriate to assume the most capable adversary OR average it out across different adversity profiles. 

**Examples:**
The likelihood of a compromised GitHub account or access token being used to impact <organization>
The likelihood of compromised production cloud access being used to impact <organization>

| Likelihood of Threat Event Resulting in Adverse Impact Score | Scoring Criteria | 
| :---: | :---: |
| Critical/ Very High  | If the threat event is initiated, it’s almost certain to result in adverse impact| 
| High  | If the threat event is initiated, it’s highly likely to result in adverse impact| 
| Medium | If the threat event is initiated, it’s somewhat likely to result in adverse impact)| 
| Low  | If the threat event is initiated, it’s unlikely to result in adverse impact| 

### Step 3: Overall Likelihood
The overall likelihood is a function of the likelihood of the threat event being initiated and the likelihood of the level of the impact once initiated. Using the scores from above, use the table below to calculate the overall likelihood.
| Likelihood of Threat Event Initiation |--- Likelihood of Threat Event Resulting in Adverse Impact----| 
| :---: | :---: |

| Likelihood of Threat Event Initiation | Low| Medium| High| Very High|
| :---: | :---: | :---: |:---: | :---: |
| Critical/ Very High  | Medium  |  High|  Very High/Critical|  Very High/Critical| 
| High  | Medium| High  |  High|  Very High/Critical| 
| Medium | Low| Medium| High| High|
| Low  | Low| Low| Medium| Medium|

### Step 4: Level of Impact and Monetary Loss Value of Threat Event Initiation
If an adversary initiated the threat event (e.g., used GitHub admin privileges), what would the impact be to <organization>? 

**Guidance:**
Consider existing controls; this should be viewed in the context of all the controls we have in place today.
Consider adversaries <organization> has and is likely to be targeted by (e.g., hacktivists, nation states, etc) in the context of the assessed risk. Use your professional judgment, threat modeling, internal incident-related data, and industry trends to determine whether it’s appropriate to assume the most capable adversary OR average it out across different adversity profiles. 
For situations where we can't neatly categorize the impact into a granular category, use the General column in the scoring table as an open-ended option where the impact can be clearly articulated otherwise.

| Impact Score|-------------------------------------------Impact Areas-----------------------------------------------------------| 
| :---: | :---------------------------------------------------: |

| Impact Score | General| Customers| Legal and Regulatory| Reputation & Image| Business Continuity & Productivity | Financial
| :---: | :---: | :---: |:---: | :---: | :---: | :---: |
| Critical/ Very High  | The threat event could be expected to have multiple severe or catastrophic adverse effects on <organization>  |  Significant impact directly affecting a substantial number of customers |\* Public regulatory action <be>\*Litigation against <organization><br>\* Criminal investigations and charges<be>\* Major data breach with legal implications |  Negative press in major publications or  widespread coverage| At least X employees impacted | More than $X
| High  | The threat event could be expected to have a severe or catastrophic adverse effect on <organization| Noticeable direct and indirect impact on several customers  |\*Significant regulatory fines<br>\* Regulatory investigations<br>\* Contract breaches with significant consequence<br> \* Major data breaches| Negative press in media | Between X and Y, employees  impacted| $X to $Y| 
| Medium | The threat event could be expected to have a serious adverse effect on <organization>| Moderate indirect impact on a few customers |\* Warning and/or moderate regulatory fines <br>\*Contract breaches with moderate consequence <br>\* Moderate data breaches| Limited coverage in media| Between X and Y, employees are impacted| $X to $Y|
| Low  | The threat event could be expected to have a limited adverse effect on <organization>|  No customers are directly or indirectly impacted|\* Minor violation of company policy<br>\* Minor contract disputes <br>\*Minor compliance discrepancies| Limited coverage in media| Fewer than X employees are impacted| Less than $Y

### Step 5: Overall Risk Score

#### 💎 Inherent Risk (Risk given controls today)
After risks have been assigned a likelihood and impact score, use the table below to determine the likelihood and impact risk score to get an overall risk score. Use this score as the Risk Score in Jira/Spreadsheet/confluence or any other relevant tool. 

| Overall Likelihood |---------------------- Overall Impact-----------------------| 
| :---: | :---: |

| Overall Likelihood | Low| Medium| High| Very High/Critical|
| :---: | :---: | :---: |:---: | :---: |
| Critical/ Very High  | Medium  |  High|  Very High/Critical|  Very High/Critical| 
| High  | Medium| High  |  High|  Very High/Critical| 
| Medium | Low| Medium| High| High|
| Low  | Low| Low| Medium| Medium|

#### 𝌬 Residual Risk (Risk after new controls are put in place)
After creating a remediation plan, we want to know the new level of risk after new controls are implemented. This is the risk that remains after remediation. Repeat steps 1-5 to calculate residual risk and consider the new controls.
