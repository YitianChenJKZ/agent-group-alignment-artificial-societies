# Agent Group Alignment

Sources for Artificial Society research blogs on AI agent group alignment,
plus the simulations behind their figures.

## Papers

### Agent Based Modeling for Group Alignment

An agent-based model of a population of fast agents (AI) and slow agents (humans) placed at
random on an n x n grid with a Moore neighbourhood. 

The outcome measure is the C-index: the ratio of slow-origin to fast-origin information at
equilibrium, divided by the ratio of slow to fast agents. 

Three hypotheses are tested against closed-form predictions:

1. Fast agents mainly hear from other fast agents
2. Fast-origin information crowds out slow-origin information
3. Raising P_sf, so fast agents consult slow agents more, restores C = 1 for limited rho.

Files:
- ABM files: agent-based modelling/paper.tex, paper.pdf, references.bib, hypotheses_numerical_simulation.ipynb, figures/
- Principal-agent files: principal-agent problem framework/paper.tex, paper.pdf, group-alignment-numerical-simulation.ipynb, figures/

### AI Agent Group Alignment through the Lens of Principal-Agent Problem Framework

A social norm instillation model where each agent has a hidden latent space norm and a visible output norm. 

Files: Principal-Agent Group Alignment/

## Running the notebooks

Install: pip install -r requirements.txt


## Building the papers

cd "agent-based modelling"
rm -f paper.aux paper.bbl paper.blg paper.log paper.out
pdflatex paper.tex && bibtex paper && pdflatex paper.tex && pdflatex paper.tex

cd "../principal-agent problem framework"
rm -f paper.aux paper.log paper.out
pdflatex paper.tex && pdflatex paper.tex
