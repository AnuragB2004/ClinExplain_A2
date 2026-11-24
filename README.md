# ClinExplain
README prose word count: 393 (excluding this line, headings, code blocks and setup commands).

## Project status
ClinExplain is an academic interaction prototype for exploring how explanation design may affect reliance on clinical AI recommendations. It contains three fabricated patient vignettes, a simulated recommendation, a static feature-attribution view, interactive what-if controls within a counterfactual-style verification view, clinician accept/reject/override controls, and a session decision log.

Implemented: case selection, interface states, explanation-mode switching, decision capture, and CSV export.
Simulated: recommendation labels, confidence values, feature contributions, and the deliberately incorrect recommendation in Case B.
Not implemented: a trained or clinically validated prediction model, real patient records, SHAP computation, a validated counterfactual algorithm, recruitment of clinicians, or a formal user study.

## Technology
- Python and Streamlit: interactive web interface and state.
- Pandas: session decision log and CSV export.
- Matplotlib: illustrative feature-contribution chart.
- No external AI model or API is called.

## Run locally
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
streamlit run app/streamlit_app.py
```

## Inspect the prototype
Choose a synthetic case in the sidebar. Switch between the two explanation modalities. Record an accept, reject, or override decision. Open the session decision log and optionally export it as CSV. Case B deliberately pairs a lower-concern AI recommendation with a higher-concern scenario reference to create a controlled automation-bias walkthrough. All values are invented for demonstration and are not medical thresholds.

## Development record
- Initial scope: translated the A1 research question into a small interface that makes the two explanation conditions and user decision visible.
- Scope decision: used a deterministic simulation rather than claiming to have trained a clinical model. This keeps the prototype inspectable and avoids presenting fabricated outputs as clinical evidence.
- Interaction decision: added an explicit override path to preserve human agency and capture reliance behaviour.
- Scenario decision: included one deliberately misleading recommendation so a reviewer can inspect the intended failure case.
- Testing completed: installed dependencies (Streamlit 1.67); ran the app; exercised all three cases in both explanation modes with no errors; recorded Accept, Reject and Override decisions; verified CSV export (example in `docs/screenshots/example_decision_log.csv`); captured screenshots in `docs/screenshots/`.

## AI assistance
GitHub Copilot in VS Code assisted with drafting the application structure, interface text, README, architecture description and report. Suggestions were checked against the application source and captured interface states. Literature claims and repository details still require author verification; AI-generated suggestions are not evidence of clinical validity.

## Repository and accompanying files
Project report: [ClinExplain_A2_Project_Report.docx](ClinExplain_A2_Project_Report.docx). The `docs/` folder contains the architecture diagram, storyboard and screenshots. The submitted ZIP may contain the same project files if required by the submission portal. No API keys are required.
