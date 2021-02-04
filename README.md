# Learning From Agentic Action: Modelling Causal Inference from Intention

This github repository contains the source code and data analysis for the CogSci submission titled, "Learning From Agentic Action: Modelling Causal Inference from Intention".

## Source Code for Inference Models

The inference models were implemented in WebPPL. Our findings can be replicated by running the source code on [webppl.org](http://webppl.org).

### Intentional Agent Model

Source code can be found in "intentional-model.webppl".

### Unintentional Agent Model

Source code can be found in "unintentional-model.webppl".

### Two-agent-independent Model

This is a mixture model of the intentional agent model and unintentional agent model. The intentional agent component can be replicated from the file, "two-agent-model(intentional).webppl (It takes a different set of observations compared to the "Intentional Agent Model" described above).  The unintentional agent component is identical to the "Unintentional Agent Model" described above.

We computed the posterior for this model by taking a weighted sum of both model components' predictions. The mixture parameter was chosen by optimizing for RMSE. This analysis can be found in the "primary-analysis.html" file. 

### Mixed-Intentional Model

This is a mixture model of the intentional agent model and unintentional agent model, similar to the Two-agent model. The intentional agent component is identical to the "Intentional Agent Model" described above. The unintentional agent component is identical to the "Unintentional Agent Model" described above.

We computed the posterior for this model by taking a weighted sum of both model components' predictions. The mixture parameter was chosen by optimizing for RMSE. This analysis can be found in the "primary-analysis.html" file. 

### Two-agent-coop Model

This is a mixture model of the "Two-agent-independent Model" described above and another two agent model which assumes that both agents are cooperative. This second model assumes the two agents have joint beliefs which explain their combined actions. Upon making these assumptions, the second model's predictions are equivalent to that of the "Intentional Agent Model" described above.

We computed the posterior for this model by taking a weighted sum of both model components' predictions. The mixture parameter was chosen by optimizing for RMSE. This analysis can be found in the "primary-analysis.html" file.

## Analsis Results and Code

In the "primary-analysis.html" file, we document our results and analysis code. This includes results for the statistical tests ran in the paper, including the main analyses, manipulation checks, and KSD difference tests. It also contains the analysis for our grid searches to find the optimal mixture parameters for the "Mixed-Intentional Model" and the "Two-agent-coop Model". 
