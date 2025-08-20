

Daily solar flux as a function of latitude and time


https://kb.solargis.com/docs/pv-energy-yield-simulation
### Evaluate application simulations

Solargis Evaluate web application, specifically the PV energy system simulator, employs our latest and most advanced simulation methods. It supports two types of energy systems, each using a distinct simulation approach:

- **GTI simulator** for theoretical calculation within GTI energy systems
- **PV simulator** for photovoltaic (PV) energy systems.


#### GTI simulator

The GTI simulator is designed as a fast and simple tool for calculating Global Tilt Irradiance (GTI) **without involving electrical simulations**. It focuses exclusively on horizontal and inclined planes of PV module, lacking support for terrain variations, and is limited to simple layouts without bi-facial PV module capabilities.


GTI energy system simulation inputs

Key input data types to the GTI simulator:

- **Solar and Meteorological Time Series**: Essential are GHI and DNI solar radiation inputs.
- **Site Conditions**: This includes location latitude and longitude.
- **PV system configuration**:
    - **Mounting details**: Select from several PV module mountings.
    - **Azimuth**: Orientation of the GTI system to the cardinal points.
    - **Spacing**: Distance between PV modules.


>> GTI energy system simulation processing
The processing consists of an optical simulation only, which includes calculations of the light interaction with surface of a PV module:
> - [Isotropic Sky Model](https://kb.solargis.com/docs/incident-irradiance#solargis-isotropic-sky-model): GTI model assumes uniform distribution of solar radiation in the sky dome.
> - [View Factor](https://kb.solargis.com/docs/incident-irradiance#view-factor): Calculates the proportion of the sky visible from a given point on the panel, which enables quick shading assessment.


GTI energy system simulation outputs

The GTI simulator generates several outputs, including:

- **GTI Theoretical**: Provides GTI inoput to the front side of a PV modul ignoring possible shading.


>> PV energy system simulation inputs
The PV energy system simulator processes the following inputs:
>- **Solar and Meteorological Time Series and TMY data**: Essential for assessing solar radiation and climate conditions.
    
>- **Site Geographical Conditions**: Includes location coordinates, terrain, ground albedo, soiling and snow losses, and horizon.
>- **PV System Configuration**:
    - **PV Configuration from energy system designer**: Details about the photovoltaic system setup, e.g., module or table layout.    
    - **Components**: Specifications of PV modules, inverters, and transformers.    
    - **Electrical Components Layout**: Electrical connections of the components, including losses.    
- **Other Factors**: Considerations such as self-consumption, degradation rates, and system unavailability.




PV energy system simulation outputs

The PV energy system simulator provides the following outputs:

- **GTI Outputs**: We provide Global Tilt Irradiance (GTI) values per time slot, detailing various stages of losses—from theoretical estimates to spectrally corrected values.
    
- **PV Output**: The simulation delivers photovoltaic output data, including total yield and specific yield per time slot, reflecting various stages of losses, including electrical losses due to snow and soiling, up to the grid connection.
    
- **Uncertainty Analysis**: We include an assessment of uncertainty associated with the solar radiation and meteorological parameters, including the one in individual PV simulation steps, helping users understand the reliability of the results.
    
- **Analytical Outputs**: The Evaluate application offers a range of analytical outputs, including graphs and charts that visualize key performance metrics and trends.
    
- **Data Deliverables**: Comprehensive reports and data sets are provided, enabling further analysis and integration into other systems or reports.


![[image.png]]






--- personal prompts

I am developing and modifying a previous model by hysupply on Technoeconomic Analysis of Green hydrogen production. .
The detail on original model can be found at @/about/documentation.md 
 i will customize it for the united state' scenarios based on the USA's RE energy potentials.We will add a streamlit web user interface.We want to predict the cost of hydrogen variable to different geographical locations in the state.
 
I'm adding a UI interface for the model with streamlit.( with nice)
I will add submodules that includes a PEM electrolyser design and options , An energy system design ( wind turbine, solar panel)
 a more dynamic physics informed Renewable energy plant model that changes based on geographical location by latitude and longitude. with also an api calling feature for some system parameters specific to different locations. Solar and Wind traces can be extracted using Renewables Ninja https://www.renewables.ninja/ Requests for data
 I will add a PEM design model with a physic-informed electrochemical model that simulates hydrogen production in the PEM electrolyser.
 
method and details of the model @/About/Manual1.md 
results and calculations pae are shown at @/about/3\ Worksheet.md 

Write an about project and save to @about/project.md following the instructions in @/prompts/01planning.md 



now write out the task needed for this project follow the instructions given in @prompts/02create-prd and save to 

let's start with the streamlit ui first, we will make sure it follows the original excell sheet organization. and work out the backend later.

 restructure pages and inputs.
 For the main TEA module
organize the user input well. read about the proj from @Manual1.md and get the right inputs.
Keep all inputs on one page(inputs page) in groups, some on sidebar, others on main page. 
note that we are converting a work a excel based work to a web based app.

Restructure the results page
restructure the Pages and content. read @'3 Worksheet' for details
with details as shown in The Results sheet Results- should have all visualizations shown at results page with all plots and visualizations as described in S2. Results at @'3 Worksheet'  from Figures 8 to Figures14.
other pages are should follow as described in @'3 Worksheet'
Levelized cost analysis ,
S3. Levelised Cost Analysis
This sheet calculates the capital and operating costs for each component of the model. It presents the annual operational profile for each year up to the lifetime as well as the discounted and non￾discounted cash flows.
S4. Cash Flow Analysis
Sheet S4 contains the detailed cash flows required for calculation of the net profit, return on 
investment and payback period.
Cashflow analysis
S5. Raw Data
To calculate the annual hydrogen production, the tool relies on hourly electricity generation 
profiles in the form of capacity factor traces. 
 The Raw Data sheet currently contains hourly solar and wind traces
S6. Working Data
The Working Data sheet (Figure 18) is where the hourly electrolyser operation and outputs are 
calculated. 

also remeber to mark complete all completed task when they are finished





naa the electrolyser design page should should be electrolcheical desdign driven with parameters such as temperature current density, thickness of membrane and electrolde layers, exchange current densities, limiting current densities, operating pressure, Active cell area etc


now begin process the task in @/tasks/tasks-prd-streamlit-ui.md to write the code following the instructions in @/prompts/04process-task.md

---

Biosteam plus plus
process modeling and simulation gui with biosteam backend( canvas). 
techno-economic analysis 
agentic chat interface copilot
case studies and community examples 
developer mode for direct code editing and debuging

ML features
flowsheet generation
deep research
Agentic MCP
techno-economic analysis results and report generation

Features with some details
Develop a node flow GUI for biosteam. Modern Node Based Flow Editor
Next js
a drag ,drop, connect canvas interface with sidebars and Process instrumentation PID icons for different operational units,. Adopt concepts from Aspen hysis and plus

different applications of biosteam
Access to different opensourced models

A GUI with a sidebar for options and parameters.
Developer mode: The app should have a backend where the user should have access to the codes that connects the UI.

example and template models
---
An example and demonstration feature with already made models drawn form community templates.
Bioindustrial-Park- models from people on different areas.
different applications of biosteam
Access to different opensourced models
https://biosteam.readthedocs.io/en/latest/API/biorefineries/index.html
https://github.com/BioSTEAMDevelopmentGroup/Bioindustrial-Park

AI integration 
	For debuging
	Chat model to build from scratch based on prompt.


PRD for:
1. Node Editor (prd-node-editor.md)
2. Backend Integration (prd-backend.md)
3. AI Features (prd-ai.md)
4. Community Features (prd-community.md)



---

#OpenLCA_Copilot
GUI to translate words to python program that reuns OPENLCA. calls functions with agentic tools protocols. mcp

Tools for web desktop interface.


Open LCA python API
 link to- [[OpenLCA - API]]
Inter-process communiction - IPC

Documentation
link https://greendelta.github.io/openLCA-ApiDoc/


hey i am developing a chat-agent copilot for openLCA softaware. 

Life Cycle Assessment, Large Language Models, Environmental Informatics, openLCA, AI Copilot, Sustainability Decision Support, Agent Systems

MVP 1
Interface framework
**1. PyQt/PySide:**
- **PyQt** and **PySide** are Python bindings for the powerful and feature-rich Qt framework.

Documentation
https://wiki.python.org/moin/PyQt

A lean, five-day sprint plan to get an OpenLCA Copilot MVP up and running using PyQt for the UI, CrewAI for LLM orchestration, and the `olca-ipc` client.

### Project Structure (scaffold)

```pgsql
openlca-copilot/
├── src/
│   ├── ui/
│   │   └── main_window.py          # PyQt application entry
│   ├── agent/
│   │   ├── llm_client.py           # CrewAI wrapper for GPT function calls
│   │   └── intent_router.py        # Maps LLM intents to backend functions
│   ├── olca/
│   │   └── olca_client.py          # olca-ipc wrapper: createProject, runLCA…
│   ├── core/
│   │   └── session_state.py        # Tracks open project, last results
│   └── app.py                      # Boots UI + wires agent + olca
├── tests/                          # Unit tests for each module
├── requirements.txt                # PyQt5, crew-ai, olca-ipc, pytest…
└── README.md                       # Quickstart, future work notes

```
#### Extension Points:

* **Drop-in alternate LLM:** (e.g., local Llama) by swapping `agent/llm_client.py`.
* **Support additional function calls:** by adding stubs in `olca/olca_client.py`.
* **Skin the UI or add dialogs:** just by extending `ui/` components.



---
 429 error fixes
---

Implement Exponential Backoff:
If requests fail with a 429 error, instead of immediately retrying, wait for an increasing amount of time before subsequent retries.

Check Quota Usage:
Review the API usage dashboard or relevant documentation to understand the specific quota limits for your project and API key.

Utilize Caching:
If possible, cache API responses to reduce the need for repeated requests for the same data within a short period.

roocode
gemini-2.0-flash-thinking-ex-01-21
---
Supports images
Does not support computer use
Does not support prompt caching
Context Window: 1,048,576 tokens
Max output: 65,536 tokens
* Free up to 15 requests per minute. After that, billing depends on prompt size
* 

gemini-pro-exp-03-25
---
Context Window: 1,048,576 tokens
Max output: 65,535 tokens
* Free up to 2 requests per minute. 

Supports images
Does not support computer use
Does not support prompt cachin


gemini-2.5-flash-preview-04-17
---
Supports images
Does not support computer use
Does not support prompt caching
Context Window: 1,048,576 tokens
Max output: 65,535 tokens
Input price: $0.15 / 1M tokens
Output price: $0.60 / 1M tokens
* Free up to 15 requests per minute. After that, billing depends on prompt size.


--- cline
plan
deepseek/deepseek-chat-v3-0324:free
DeepSeek V3, a 685B-parameter, mixture-of-experts model, is the latest iteration of the flagship chat model family from the DeepSeek team.
Does not support images
Does not support browser use
Does not support prompt caching
Context Window: 163,840 tokens

t's 671B parameters in size, with 37B active in an inference pass.

Fully open-source model.

**Does not support images\
**Does not support browser use\
**Does not support prompt caching\
Context Window: 163,840 tokens
