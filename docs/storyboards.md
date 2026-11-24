# Storyboard captions

## Storyboard 1 — Inspecting a recommendation
1. The user selects Case A from the sidebar.
2. The system displays the synthetic patient vignette and a simulated lower-concern recommendation.
3. The user selects Static feature attribution and inspects the illustrative contribution chart.
4. The user records a decision. The system adds it to the session log.

## Storyboard 2 — Comparing explanation modalities
1. The user keeps the same case selected.
2. The user switches from Static feature attribution to Interactive counterfactual.
3. The system replaces the bar chart with a what-if explanation and verification prompts.
4. The user compares the two displays before recording a decision.

## Storyboard 3 — Detecting a deliberately incorrect recommendation
1. The user selects Case B, the deliberately misleading scenario.
2. The system displays a lower-concern recommendation despite the vignette's higher-concern reference label.
3. In counterfactual mode, the system explicitly prompts inspection of the patient information.
4. The user can reject the recommendation or request further review, then record the reason.
