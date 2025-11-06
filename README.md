# Football-Transfer-Window-Optimization


**Objective:** Build a data-driven transfer strategy to improve Manchester United’s squad quality while respecting real-world constraints like budget, player fit, injuries, and club philosophy.

This project turns football recruitment into an optimization problem using mathematical modeling, scraped player data, and scenario simulations. Think of it as a sandbox where analytics meets sporting decisions.

---

## 📂 Project Overview

Football clubs don’t just buy “good players.” They operate under:

* Fixed transfer and wage budgets
* Squad size and positional requirements
* Tactical system and coaching philosophy
* Injury risk and scenario uncertainty
* Player fit, wages, resale value, and age profiles

This repo builds optimization models to simulate transfer windows that maximize squad strength under realistic constraints.


## Key Goals

* Boost squad *overall rating* and *balance*
* Respect the transfer + wage budget split
* Prioritize players who fit club/manager style
* Handle uncertainty (random budgets, injuries)
* Optimize mid-season transfers when injuries hit

---

## Methods

| Module                  | Description                                                |
| ------------------------| ---------------------------------------------------------- |
| Base MIP Model          | Maximize squad improvement given budget + positional needs |
| Stochastic Model        | Budget uncertainty + dynamic player selection              |
| Manager Playstyle Model | Filters and weights based on tactics & positions           |
| Injury Response Model   | Second-period optimization to replace injured players      |

**Solver:** CPLEX
**Approach:** Mixed-Integer Programming + scenario planning
**Data Source:** Scraped from `https://sofifa.com/players`

---

## Data

The player dataset includes:

* Overall rating
* Position
* Age
* Wage + transfer value
* Attributes relevant to playstyle
* Injury risk assumptions

Scraped from **SoFIFA** and pre-processed for optimization.

---

## Results Snapshot

* Efficient squad improvement given spending caps
* Balanced positional coverage
* Injury replacements with minimal quality loss
* Demonstrated trade-offs between star signings vs squad depth

> The model consistently favors balanced squads, efficient contracts, and young high-growth players—mirroring modern data-driven clubs.

---

## Tech Stack

| Component     | Tools                         |
| ------------- | ----------------------------- |
| Language      | Python                        |
| Optimization  | CPLEX                         |
| Modeling      | MIP, scenario simulation      |
| Data          | Pandas, custom scraper        |
| Visualization | Matplotlib / Notebook outputs |

---

## How to Run

```bash
git clone <repo-url>
cd football-transfer-optimization
pip install -r requirements.txt
jupyter notebook FTWO_Project.ipynb
```

You'll need **CPLEX** installed & licensed (free academic license available).

---

## Future Improvements

* Integrate advanced injury forecasting
* Market inflation + multi-season planning
* Transfer negotiation simulation
* Deep learning for player potential predictions
* UI to play "Director of Football Mode"

---

## Contributions

Ideas, issues, and PRs welcome.

---

## Author

Built with passion for football, data science, and optimization modeling.
