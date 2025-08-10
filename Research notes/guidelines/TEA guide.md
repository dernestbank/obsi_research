



Build a TEA scope














Assessing costs and benefits and time value of money

Cost
	• Cost of equipment
	• Cost of goods and materials
	• Cost of operating the equipment
	• Cost of workers
	• Cost of delivering goods late to customers
	• Cost of lost sales
	• Cost of a strike
	• Cost of rescheduling production to meet a rush job

Explicit, implicit and intangible cost
	• Explicit: “Out-of-pocket” transfer of funds
		• Ex: Payment for an equipment piece
	• Implicit
		• Ex: Depreciation
	• Intangible:
		• Ex: Goodwill: potential for future profits


Cost according to accountants
	• Based on the past
	• Balance sheet
	• Profit-and-loss statement

Direct costs
• Directly attributed to 
products/services
• Purchase of goods/materials 
used in production
• Labor for the production


Direct costs
• Directly attributed to 
products/services
• Purchase of goods/materials 
used in production
• Labor for the production


Cost according to economist
• Based on earning power
	• Opportunity cost
	
Fixed costs
	• Not affected by changes in output

Variable costs
	• Affected by changes in output


Similar to direct and indirect cost, but could be different:
The depreciation of a machine that is used for only one product could be classified as direct cost by accountants, but it is fixed

Opportunity cost
• Cost evaluated based on the best alternative opportunity forgone

• Replacement cost
	• Current cost of goods
	
• Future costs and benefits
	• Decommissioning, disposal
	• Salvage value


---

## Capital Investment (CAPEX)

Initial investment needed for "designing, constructing, installing [and commissioning] a plant and the associated modifications needed to prepare the plant site

Overnight capital cost
• In order to understand how both plant design and project financing impact the overall competitiveness of the technology, their cost effects need to be isolated. 
• This is done by estimating the project capital cost responsive to plant design (no time element), known as Overnight Capital (OC)

![[Pasted image 20250405054715.png]]


### Methods to estimate CapEX

- Short methods: calculate costs from one or few characteristic parameters and often include cost capacity curves or scales of operation factors 
-  Parametric techniques: derive cost from process characteristics and related parameters; cost are based on the number of significant process steps and other characteristic process parameters 
-  Factored methods: apply factors to equipment cost to calculate other direct or indirect cost items. 
-  Unit cost line items: derive costs from rigorous design and offer detailed single equipment cost calculation. 
-  Cost transformation: describes the adoption or transfer of similar plants' CapEx to a projected plant, usually based on capacity or other significant plant parameters


Cost indexes
• Chemical Engineering Plant Cost Index (CEPCI)
• U.S. Bureau of Labor and Statistics
https://www.bls.gov/data/
• Producer Prices Indices (PPI)
• Labor Compensation
• Consumer Price Index (CPI)
• Engineering: Cost Data, Parts and Suppliers
https://guides.libraries.psu.edu/c.php?g=327786&p=3183876

**Learning Curve Effects**
	The first plant of a particular kind is likely to require significantly higher CapEx than subsequent examples. The following two types are therefore distinguished:
	- **First of a kind (FOAK)**: none or only a few similar pioneering plants exist and learning rates are not yet achieved
	- **Nth of a kind (NOAK)**: several plants exist that employ the same or similar technologies and learning rates can be estimated


---


## Techno-economic analysis: profitability, sensitivity and uncertainty analysis


Depreciation methods
	• Straight line
	• Doble declining balance
	• Sum of the years digits

Depreciation methods
• Straight line
• Doble declining balance
• Sum of the years digits



Profitability indicators

Cumulative Cash Flow Diagram for the Evaluation of a New Project
![[Pasted image 20250405060054.png|500]]



Basis of evaluation of profitability
1. #Time
2. #Cash
3. #Interest_rate


| **Static**                                                                                                                                                                                                                                                                                                         | **Dynamic**                                                                                                                                                                                                                                                                                                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| • Consider only one period or an average of multiple periods<br>• Alternative is no investment<br>	• <span style="color:rgb(0, 112, 192)">Absolute or relative profit</span><br>	• <span style="color:rgb(0, 112, 192)">Payback time</span><br>	• <span style="color:rgb(0, 112, 192)">Return on investment</span> | • Include multiple periods<br>• Account for cash flows<br>• Alternative is another investment with similar risk<br>	• <span style="color:rgb(0, 112, 192)">Net present value</span><br>	• <span style="color:rgb(0, 112, 192)">Dynamic payback time</span><br>	• <span style="color:rgb(0, 112, 192)">Dynamic ROI</span><br>	•<span style="color:rgb(0, 112, 192)"> Internal rate of return</span> |

a. Discounted payback period (DPBP)
#Time
the time required after star-up to recover the fixe dcapital investment, FCI_; : with all cash flows discounted back to time zero

Net present value (NPV)
#Cash 

Present value ratio (PVR):
#Cash 
A present value ratio of unity for a project represents a break-even situation

$$PVR= \frac{\text{Present Value of All Positive Cash Flows}}{\text{Present Value of All Negative Cash Flows}}$$

Discounted cash flow rate of return (DCFROR)
#Interest_rate 


understanding the key factors that drives the economic value of our technologies.

![[Pasted image 20250405061214.png|500]]

link economic value to process and market parameters

![[Pasted image 20250405061438.png|500]]

### Sensitivity analysis (SA) | Uncertainty analysis (UA)

- Sensitivity analysis (SA) studies how sensitive the model output is to variations in one or more input variables.
- Uncertainty analysis (UA) allows the practitioner to analyze the uncertainty associated with the model output. 
-  UA deals with the propagation of errors in input data as well as uncertainties in the model itself or the context in which the assessment is conducted.
- UA and SA are complementary, as SA reveals how any uncertainty within the output is constructed, and discloses key input variables that can contribute most to the uncertainty


The purpose of sensitivity analysis is to assess if the model results are robust to these decisions, or small changes lead to large fluctuations in results. 
 to understand how sensitive a plant’s profitability is to changes in the parameters that drive costs and revenues
 plant and market parameters that create the largest impacts or the largest uncertainties on plant profit
To determine where R&D will make a big difference

 Common areas to analyse include:
• Which features are important to collect? If there are unimportant features could these be removed from the model to reduce computation time and the burden of collection?
• How robust is the model to noise in the data?
• How are the results affected when you change parameters in 
your model?


![[Pasted image 20250405062634.png|500]]

![[Pasted image 20250405062739.png|500]]


identifying key variables with Tornado Diagrams
Longer bars indicate greater impact
![[Pasted image 20250405063730.png|400]]


![[Pasted image 20250405064011.png]]

### local vrs global sensitivity

**Local sensitivity**
• Usually modify one factor at a time
• Does not considered any correlations or interactions between different input variables
• Assumes linearity

**Global sensitivity**
Effects on the output of both individual inputs and interactions between the input variables

Uncertainty analysis
#monte_carlo
Uncertainty decreases with increasing maturity levels, as a result of improved data or better understanding of the technology and the conditions under which its research, development, and deployment are conducted.
In the case of low technology maturity, complex uncertainty methods can result in substantial noise.


Three input variables (x1, x2, x3) and their respective probability distributions are transferred to the probability distribution function of the output

![[Pasted image 20250405064506.png|500]]

it brackets the range of possible outcomes and predicts the probability that any given case will occur.
Quantify the risk associated with fluctuation in raw material and product prices and for understanding the implications of uncertainty in Capex and Opex and revenue.


![[Pasted image 20250405064934.png|500]]

![[Pasted image 20250405065129.png|400]]