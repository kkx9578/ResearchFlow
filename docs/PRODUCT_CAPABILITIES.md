# KAKAMEDLAB ResearchFlow Product Capabilities

## Product Scope

KAKAMEDLAB ResearchFlow is a proprietary visual workflow application for clinical large-language-model research. It standardizes user-visible experiment configuration, batch execution, run provenance, publication-oriented artifacts, and objective text metrics.

This document describes product behavior visible to authorized users. It does not disclose source code, internal architecture, server infrastructure, authorization mechanisms, or implementation algorithms.

## 1. Research Task Modes

| Mode | Research material | Output |
|---|---|---|
| Text processing | Word or supported text material | Word text |
| Image interpretation | One or more images associated with a research unit | Word text |
| Image-text integration | Images plus accompanying text for the same research unit | Word text |

The current product generation workflow focuses on text output. Image or video generation is not represented as a supported ResearchFlow output mode in this release.

## 2. Model And Experiment Configuration

- Load the current model catalogue through the configured API channel.
- Search and select one or more models without software-imposed primary or secondary ranking.
- Run selected models under the same Prompt, materials, and confirmed generation settings.
- Configure supported parameters such as temperature, Top P, Top K, seed, and maximum output tokens when required by the study.
- Omit optional parameters when the researcher does not intend to control them.
- Set repeated generation counts for studies that require multiple outputs under the same condition.
- Record requested and returned model identifiers for later review.

Model capability and parameter support can vary by provider and model. Researchers remain responsible for confirming that selected models are appropriate for the protocol.

## 3. Prompt And Research Materials

- Use a researcher-supplied Prompt file rather than an automatically invented research objective.
- Record the confirmed Prompt content and SHA-256 fingerprint.
- Treat the uploaded Prompt as the system-level instruction and each research material as the user-level content supplied to the model.
- Record material identifiers and content fingerprints for traceability.
- Remember the most recently used directory to reduce repetitive file navigation.
- Require the researcher to confirm that all materials have been de-identified and meet applicable governance requirements.

## 4. Execution And Recovery

- Run a real preflight item before opening full-batch execution.
- Check API access, selected models, materials, Prompt, parameters, and run-record completeness.
- Display task progress, completed items, explicit failures, unknown states, and remaining work.
- Preserve completed work when an authorized user stops or closes a task.
- Resume an interrupted task or start a clean task from the current configuration.
- Reprocess incomplete items under the same confirmed configuration when appropriate.
- Separate generated research outputs from technical run records.

Recovery features reduce avoidable repetition. They do not guarantee that every third-party model or provider request will succeed.

## 5. Multi-Model Output Organization

ResearchFlow creates a task directory identified by run time and organizes generated results by model. This supports:

- Clear attribution of each result to its requested model
- Multiple outputs for the same research material
- Separation of model results from run metadata
- Review of model-specific folders without manual renaming
- Consistent downstream ingestion by the objective-metrics module

## 6. Research Provenance

Depending on the response returned by the provider, ResearchFlow can record:

- Requested and returned model identifiers
- Confirmed generation parameters
- Prompt and material fingerprints
- Response identifiers and completion status
- Input, output, reasoning, and total Token information
- Provider-reported cost information
- Start time, finish time, and elapsed duration
- Interruption, completion, and recovery state

API keys are not written into research outputs or publication-oriented artifacts.

## 7. Publication-Oriented Artifacts

The batch-generation workflow can prepare:

- A concise Methods paragraph for the manuscript body
- A more detailed supplementary Methods document
- Prompt documentation with role, version, original content, and fingerprint
- A run and result appendix containing the evidence needed to review the execution
- Model outputs organized for subsequent evaluation

These files are research-writing drafts and evidence records. They require researcher review and adaptation to the target journal.

## 8. Objective Metrics

The objective-metrics module reads a completed ResearchFlow task and can calculate selected groups of measures:

- Basic Chinese text description and structural measures
- Advanced Chinese linguistic features available in the local analysis runtime
- English readability formulas for English text or consistently translated text
- API endpoint latency and text-output efficiency measures when source records are available

It can generate Word methodology and result materials together with an Excel workbook containing structured item-level values.

## 9. Product Boundaries

ResearchFlow does not:

- Design the research question or eligibility criteria
- Decide which model is scientifically preferable
- Replace expert ratings or clinical validation
- Select the correct statistical method for every study
- Guarantee provider availability, publication, or reviewer acceptance
- Replace ethics review, data governance, or professional medical judgment

## Release Identity

- Product: KAKAMEDLAB ResearchFlow
- Version: 3.0.0
- Build: 20260807.1
- Platform: Windows
- Distribution: Proprietary

