



G. A. Buchner, A. W. Zimmermann, A. E. Hohgräve, and R. Schomäcker, “Techno-economic Assessment Framework for the Chemical Industry—Based on Technology Readiness Levels,” _Ind. Eng. Chem. Res._, vol. 57, no. 25, pp. 8502–8517, Jun. 2018, doi: [10.1021/acs.iecr.8b01248](https://doi.org/10.1021/acs.iecr.8b01248).

@buchnerTechnoeconomicAssessmentFramework2018



![[image.png]]




![[Learning/TEA/attachments/image-1.png]]



![[Learning/TEA/attachments/image-2.png]]



![[Learning/TEA/attachments/image-3.png]]



### **TEA Framework**

**1. Purpose and Structure**  
Buchner et al. define **Techno-Economic Assessment (TEA)** as a structured approach to evaluate the economic viability of technologies through measurable indicators such as profitability. The TEA structure mirrors the ISO 14040 LCA phases:

1. **Goal & Scope Definition**
2. **Inventory (Cost & Market Parameters)**
3. **Impact Assessment (Profitability Analysis)**
4. **Interpretation**


### ✅ **Key Concepts**

#### 🔷 Technology Readiness Levels (TRLs) Adapted for Chemical Industry

- TRL 1–4: Applied research
- TRL 5–7: Process development and pilot testing
- TRL 8–9: Deployment in industrial settings
    
> A unique TRL table is provided to relate tangible work outputs to estimation techniques.

#### 🔷 Cost Estimation Aligned with TRLs

- **CapEx Estimation Methods** evolve with TRL progression:
    
    - **TRL 3–4**: Short methods, global factor methods
    - **TRL 5–6**: Functional unit counting methods
    - **TRL 6–7**: Component-factored, simulation-based methods
        
- **OpEx Estimation** starts from TRL 2 onward using:
    
    - Stoichiometry, reaction enthalpy
    - Experimental mass/energy flows (TRL 3–6)
    - Full simulations (TRL 6–9)
        

**Scheme 2 and Scheme 3** illustrate detailed structures of **COGS** and **CapEx**, respectively.

---

### ✅ **Supporting Table (S1) Usage**

Table S1 in the supplementary file gives **estimation factors** for:
- **Indirect OpEx (e.g., utilities, maintenance, admin)**
- **General expenses (e.g., R&D, M&S, IP licensing)**
    
These factors are provided as:
- **Ranges** (e.g., 0.01–0.02 of ISBL or sales price)
- **Type-based applications** (e.g., per labor or investment cost)


----


---

### 1. A six-step TEA cycle anchored to TRLs

Buchner’s framework [1] folds the familiar ISO-14040 life-cycle logic into six TEA steps:

1.  **Rate maturity (TRL 1-9)**—establish how much reliable technical data exist.
2.  **Set goal, scope & scenario**—state the investment question, system boundaries, time/locale, and align with any companion LCA so inventories can be shared.
3.  **Cost estimation**—translate technical data into cost items.
4.  **Market analysis**—translate market intelligence into revenue items.
5.  **Profitability analysis**—combine 3 & 4 in suitable economic indicators.
6.  **Interpretation & decision support**—judge, recommend, iterate.

The six steps run in a loop; each new development sprint feeds better data into the next pass [1].

---

### 2. The TRL lens—what “counts” as evidence in chemicals?

A chemical-industry-specific TRL table (TRL 1 idea → TRL 9 full-scale production) ties tangible work products: bench tests, pilot-plant runs, demonstration plants, audited start-ups; to the level of data reliability [1].

**Why this matters:** every cost- or revenue-estimation technique demands a minimum evidence level; forcing detail too early can lock in poor design choices.

---

### 3. Cost architecture you will document

The framework insists on writing costs in a standard tree before any maths are done [1]:

* **COGS** → **COGM** + general expenses.
* **COGM** → **CapEx** + **OpEx**.
* **CapEx** breaks into fixed-capital investment (inside vs. outside battery limits, direct vs. indirect items), working capital, start-up, contingency [1].
* **OpEx** splits into direct (materials; energy & utilities) and indirect (labour, maintenance, IP royalties, etc.) [1].
* **General-expense** factors (administration, marketing, long-term R&D, etc.) are usually applied after COGM is known.

The supporting information supplies factor ranges for every indirect OpEx and general-expense line item—ideal when your own data are still sparse [S1].

---

### 4. Picking the right cost-estimation method for each TRL

Buchner arranges the classical methods along the TRL ruler so you never ask for data that do not yet exist:

| TRL window        | Typical evidence                               | Recommended CapEx method (examples)              | Typical error band   |
| :---------------- | :--------------------------------------------- | :----------------------------------------------- | :------------------- |
| 3 (concept validated) | simplified flows, stoichiometry                | Short rules (e.g., Kiddoo, Tolson-Sommerfeld)    | –50 % / +100 %       |
| 4                 | block flow, bench data                         | Global-factor methods (Burgert, Cran)            | –30 % / +50 %        |
| 5                 | preliminary simulation, equipment list         | Functional-unit counting (Bridgwater IV, Hill)   | –20 % / +30 %        |
| 6                 | detailed simulation, vendor quotes             | Component-factored methods (Guthrie, Happel-Jordan) | –15 % / +20 %        |
| 7 (demo)          | pilot economics, tendered equipment            | Same as TRL 6 only with tender prices or EPC bids | –10 % / +15 %        |

(Criteria and error widths from Table 2 in the article [1]).

**Transformation tools**—index escalation, location factors, the “six-tenths” scaling rule—can adjust any estimate to the required time, place, or capacity [1].

---

### 5. Operational-cost recipes along TRLs

* **Materials:** stoichiometry (TRL 2), measured yields (TRL 3-6), flowsheet simulation (TRL 5-9).
* **Energy & utilities:** reaction enthalpy proxies (TRL 2), simple heat-balance correlations (TRL 3-4), rigorous utilities simulation thereafter.
* **Indirect OpEx:** factorised to CapEx or direct labour until detailed site rules are known (≤ TRL 6) [1].

Table S1 provides the factor library to support this staged approach [S1].

---

### 6. Profitability indicators that evolve with maturity

* **TRL 1-4:** static ratios (cost per kg, gross margin, simple ROI) suffice while time profiles are still speculative.
* **TRL 5-9:** introduce time and risk—NPV, IRR, pay-back, scenario Monte Carlo—once cash-flow schedules are defensible [1].

---

### 7. How to replicate the framework in your own analyses

1.  Create a living TEA workbook whose first sheet is the TRL log. At each gate you record new evidence and raise the TRL.
2.  Lock the cost tree structure early (Section 3 above). Every new datum must map to one of those boxes; if it does not, decide whether it is immaterial or your scope needs widening.
3.  Choose estimation methods from the TRL menu (Section 4); note the method’s nominal error band in the workbook.
4.  Pull indirect-cost factors from Table S1 until you replace them with site-specific quotes.
5.  Mirror your LCA inventory—mass and energy streams—so both assessments update together [1].
6.  Run the profitability sheet appropriate to your TRL (static vs. cash-flow). Track assumptions in a dedicated “scenario” tab so decision-makers can test sensitivities.
7.  Close every loop with an interpretation memo that (i) states the current TRL, (ii) highlights the dominant cost driver and data gap, and (iii) recommends the next experimental or commercial milestone.

Following this disciplined cycle turns the framework into a repeatable, auditable decision engine—exactly what Buchner and co-authors intended [1].

---


---

**References:**

[1] Buchner et al. (Please provide the full citation for Buchner et al. from your source for accurate referencing.)
[S1] Supporting Information for Buchner et al. (Please provide the full citation for the supporting information for accurate referencing.)


### Next step

If you share the specifics of your own technology and its present TRL, I can populate the workbook skeleton with the correct estimation formulas, factor look-ups, and a starter profitability dashboard tailored to your case.




# TEA cycle into a maintainable Python package and exposed as a callable “toolbox” for AI agents.



Below is a road‑map you can follow to transform the Buchner et al. TEA cycle into a maintainable Python package and expose it as a callable “toolbox” for AI agents. The sequence is deliberately modular so you can iterate and extend without breaking older studies.

---

## 1  • Define the core domain objects first

|Object|Why it matters|Suggested implementation|
|---|---|---|
|**`TRLRecord`**|Single source of truth for maturity evidence & gate history|`@dataclass(strict=True)` with fields `level:int`, `evidence:dict`, `date:datetime`|
|**`CostTree`**|Enforces the Buchner cost hierarchy (CapEx → OpEx → COGM → COGS)|Use [**pydantic**] models so values validate/serialize automatically; nest sub‑objects `Capex`, `Opex`, etc.|
|**`Scenario`**|Bundles technical setup + economic assumptions for one run|Typed mapping of: flow data ↔ utility data ↔ factor library ↔ financial settings|
|**`ResultBundle`**|Harmonised output (cost sheet, KPIs, audits) readable by humans & machines|`attrs` or `pydantic` model that stores Pandas DataFrames plus metadata hash|

These objects become the lingua‑franca between every internal module **and** any external agent.

---

## 2  • Lay out the package skeleton

```graphql
tea_mod/
│
├─ core/               # Domain objects + shared utilities
│   ├─ trl.py
│   ├─ cost_tree.py
│   ├─ factors.py      # Table S1 numerics in JSON / YAML
│   └─ scenario.py
│
├─ estimators/         # Algorithms mapped to TRL windows
│   ├─ capex_shortcut.py
│   ├─ capex_factor.py
│   ├─ capex_detailed.py
│   ├─ opex_direct.py
│   └─ opex_indirect.py
│
├─ analytics/          # Profitability & sensitivity tools
│   ├─ cashflow.py
│   ├─ kpi.py
│   └─ monte_carlo.py
│
├─ io/                 # Parsers & writers (Excel, YAML, JSON‑LD)
│   ├─ load.py
│   └─ dump.py
│
├─ agents/             # Thin wrappers so LLM agents can “think with” TEA
│   ├─ schema.py       # JSON‑Schema for function calling
│   └─ toolkits.py     # LangChain / LlamaIndex Tool objects
│
└─ __init__.py
```

_Keep the **estimators/** folder pluggable:_ every estimator class should implement a common interface (`estimate(trl_record, scenario) -> CostTree`) so future methods (e.g., vendor‑quote pulls) drop in cleanly.

---

## 3  • Embed the Buchner TRL logic as strategy pattern

```python
class CapexEstimator(Protocol):
    def estimate(self, trl: TRLRecord, scenario: Scenario) -> CostTree: ...

class ShortcutEstimator(CapexEstimator):     # TRL ≤3
    ...
class FactorEstimator(CapexEstimator):       # TRL 3–5
    ...
class DetailedEstimator(CapexEstimator):     # TRL ≥5
    ...
```

Then supply a dispatcher:

```python
def select_capex_estimator(trl_level: int) -> CapexEstimator:
    if trl_level <= 3:   return ShortcutEstimator()
    if trl_level <= 5:   return FactorEstimator()
    return DetailedEstimator()
```

The same pattern applies to OpEx and profitability routines.

---

## 4  • Store the factor library centrally

Convert _Supporting Information_ tables (e.g., indirect‑cost factors, scaling exponents) to a structured JSON or YAML file under **core/factors.py**. Load them once at import time and cache.

```python
from importlib.resources import files
FACTOR_DB = yaml.safe_load(files("tea_mod").joinpath("data/factors.yaml").read_text())
```

---

## 5  • Expose agent‑ready functions

### 5.1  Create a JSON schema for each callable

```python
# agents/schema.py
from pydantic import BaseModel, Field

class TEACall(BaseModel):
    trl_level: int = Field(..., ge=1, le=9, description="Current TRL number")
    scenario_file: str = Field(..., description="Path or URL to YAML scenario")
```

### 5.2  Register as LangChain Tool (example)

```python
# agents/toolkits.py
from langchain.tools import BaseTool
from .schema import TEACall
from ..runner import run_tea   # orchestrates the 6‑step cycle

class TEATool(BaseTool):
    name = "tea_mod_run"
    description = "Run a techno‑economic assessment and return KPIs"
    args_schema = TEACall

    def _run(self, trl_level: int, scenario_file: str):
        return run_tea(trl_level, scenario_file).dict()
```

An LLM‑based agent can now reason about next steps (“Raise TRL? Change feed price?”) and call `tea_mod_run()` when needed.

---

## 6  • Automate reproducibility & tests

- **Versioning** – embed semantic versioning (`__version__`) and persist the factor‑library hash inside every `ResultBundle`.
    
- **CI** – use GitHub Actions to run pytest on a matrix of sample scenarios.
    
- **Notebooks / docs** – a `docs/` folder with Jupyter‑Book or Sphinx ties the code back to the Buchner paper sections (cross‑linked).
    

---

## 7  • Road‑map milestones

|Milestone|Deliverable|Tools|
|---|---|---|
|**M0** (week 1)|Package scaffold & domain classes stubbed|Poetry or Hatch|
|**M1** (week 3)|CapEx & OpEx estimators functional through TRL 5|Pandas, NumPy|
|**M2** (week 5)|Cash‑flow analytics + YAML scenario loader|SciPy, StatsModels|
|**M3** (week 7)|LangChain tool wrappers, unit‑tested|LangChain|
|**M4** (week 9)|Example chat‑agent notebook demonstrating automated TEA loop|Jupyter, OpenAI|

_After M2 you can already test the package on legacy Excel TEA studies by converting them to YAML scenarios._

---



Below is an integrated design outline that layers a **REST-style API** and a lightweight **graphical user interface (GUI)** on top of the modular package we sketched earlier. Nothing in the core logic changes—we simply expose it through two thin “skins,” both of which speak the same Pydantic data models, so your agent system, a human on the GUI, or a program calling the API all receive identical, version-controlled results.

---

## 1 • Keep the core pure

The folder **`tea_mod/`** remains _framework-only_: no web imports, no GUI code.  
Everything a front-end needs—`Scenario`, `TRLRecord`, `ResultBundle`—is serialisable as JSON via `pydantic.BaseModel.json()`.

---

## 2 • REST API layer (`tea_api`)

### 2.1 Structure

```
tea_api/
│
├─ main.py            # FastAPI app factory
├─ routers/
│   ├─ run.py         # /run   – synchronous TEA execution
│   ├─ jobs.py        # /jobs  – async + background queue (Celery/RQ)
│   └─ meta.py        # /meta  – versions, factor hashes, health
└─ requirements.txt   # fastapi, uvicorn[standard], python-multipart
```

_Each router imports **tea_mod** and never re-implements business logic._

### 2.2 Minimal “/run” endpoint

```python
@router.post("/run", response_model=ResultBundle)
def run_tea(call: TEACall):
    scenario = Scenario.parse_file(call.scenario_file)
    bundle   = tea_mod.runner.run_tea(call.trl_level, scenario)
    return bundle   # FastAPI auto-serialises the Pydantic model
```

_Authentication tip:_ add a `X-API-Key` header dependency or OAuth2 password flow if the service will leave localhost.

---

## 3 • GUI layer (`tea_gui`)

### 3.1 Why Streamlit?

- requires no front-end build chain (good for rapid science demos)
- treats Pydantic models as first-class citizens
- can call the **same FastAPI** via `requests` _or_ import `tea_mod` directly in “desktop” mode
    

### 3.2 Layout concept

```
tea_gui/
│
├─ Home ❱ sidebar
│     • choose scenario YAML / upload
│     • slider → TRL 1-9
│     • toggle → “Use remote API” vs “Local run”
│
├─ Main pane
│     • expandable sections:
│         – Cost breakdown tree  (st.dataframe)
│         – Cash-flow plot       (matplotlib image)
│         – Uncertainty bars     (st.altair_chart)
│     • download button → ResultBundle.json
└─ streamlit_app.py
```

A `settings.toml` file can store the base-URL of the API so the same UI works in both local-desktop and server-client deployments.

---

## 4 • Binding the AI agent to both layers

- **Direct call (offline notebook / LangChain Tool):** keep using the `TEATool` wrapper that imports `tea_mod`.
- **Remote call (LLM accessible from anywhere):** replace the `.run()` method with an HTTPS POST to `/run`. Because the request/response bodies are identical `TEACall` and `ResultBundle` JSON, you can switch by a single config flag.
    

---

## 5 • Updated package map & build flow

```
repo-root/
│
├─ tea_mod/          # core engine – pure python, no web deps
├─ tea_api/          # FastAPI service – optional extra
├─ tea_gui/          # Streamlit app – optional extra
├─ pyproject.toml    # defines extra sets:  pip install tea_mod[api] / [gui]
└─ docs/
```

`pyproject.toml` excerpt:

```toml
[project.optional-dependencies]
api = ["fastapi>=0.111", "uvicorn[standard]"]
gui = ["streamlit>=1.34"]
```

---

## 6 • Milestone additions

| New milestone | Target week | Deliverable                                                                                                                   |
| ------------- | ----------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **M5**        | 11          | FastAPI `/run` + `/meta`, Dockerfile (`FROM python:3.12-slim`)                                                                |
| **M6**        | 13          | Streamlit GUI with live cost-tree and cash-flow plots; CI workflow deploying both API and GUI images to GH Container Registry |

---

## 7 • Next sprint suggestions

1. **Decide deployment topology.**  
    _Single container_ (Gunicorn + Uvicorn + Streamlit on different ports) is simplest for demo; _separate services_ scale better.
2. **Introduce async job queue** if full TEA runs might last minutes.  
    FastAPI endpoint stores `Scenario` in Redis, returns job-id; GUI polls until finished.
3. **Add user session & file vault** (S3 or MinIO) so scenarios and result bundles persist beyond one run.
    

---

### Want a live scaffold?

I can generate the project structure—with FastAPI stubs, Streamlit placeholder pages, and continuous-integration YAML—in a canvas for you to pull directly into GitHub. Let me know and I’ll drop the fully runnable skeleton.












-----
✅ **Next Step: Framework for Replication**

Now that the core framework and data sources are fully assimilated, we can proceed to:

> 📌 **Draft a replicable Python-based TEA Framework** based on TRL-specific method selection, cost structure definitions, and appropriate factorized calculations.

This will include:

- A structured cost model from TRL 3 to TRL 7
- Modular estimation functions (CapEx, OpEx)
- Factor database integration (Table S1)
- Output: Profitability metrics (NPV, IRR, payback) per TRL stage



