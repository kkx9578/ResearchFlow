# Research Reporting With KAKAMEDLAB ResearchFlow

## Reporting Principle

A clinical LLM study should not place every operational detail in the manuscript body, but the manuscript also should not omit how the results were produced. ResearchFlow separates concise manuscript text from detailed supplementary evidence.

The generated documents are structured drafts. Researchers must verify terminology, numbers, ethical statements, model information, journal requirements, and consistency with the final protocol before submission.

## Module 1: Standardized Batch Generation

### Manuscript Methods Summary

The concise Methods material is intended to retain only information necessary to understand the experiment:

- API-based execution approach
- Model or model set used in the study
- Fixed Prompt and research-material relationship
- Confirmed generation parameters
- Batch, repeated, or multi-model execution design
- Reference to the supplementary methods and run record

### Supplementary Methods

The detailed Methods material can document:

- API channel and model identifiers
- Prompt role, version, fingerprint, and complete original content
- Input and output contract
- Generation settings and repeated-run configuration
- Research-material manifest and content fingerprints
- Run completion, interruption, recovery, and quality-control rules
- Data governance and limitation statements

### Results And Run Evidence

The result appendix can preserve, when returned by the API:

- Research-unit and model association
- Completion status and response identifiers
- Token and provider-reported cost records
- Start time, finish time, and elapsed duration
- Requested and returned model information
- Error or incomplete-state information requiring researcher attention

Generated model text is stored separately from technical evidence so that files intended for expert evaluation do not contain unnecessary run metadata.

## Prompt Roles

In the standard ResearchFlow workflow:

- The researcher-supplied Prompt file is transmitted as the system-level instruction.
- The text, image, or image-text research material is transmitted as the user-level content.

The supplementary materials describe this distinction so readers can understand what was fixed across research units and what changed between inputs.

## Prompt Language

The confirmed research Prompt remains the authoritative original. When an English rendering is needed for an international supplementary appendix, it should be labelled as a translation rather than a replacement for the executed original.

Researchers should verify that translated wording preserves the meaning, constraints, input contract, and output requirements of the original Prompt.

## Module 2: Objective Metrics

### Manuscript Methods Summary

The concise Methods material can state:

- Which metric groups were selected
- Whether analysis used the original Chinese output or an English rendering
- Whether a single translation model and translation procedure were applied
- Which supplementary file contains definitions and item-level values

### Supplementary Methods

The detailed objective-metrics methods can include:

- Metric name and definition
- Applicable language and calculation path
- Software-calculated descriptive measures
- Reference sources for established readability formulas
- Translation pathway used for optional English-language formulas
- Endpoint-efficiency definitions when run records are available

### Results Files

- Word documents provide manuscript-oriented summaries and methodological context.
- Excel workbooks preserve item-level values for checking, filtering, and researcher-directed statistical analysis.

ResearchFlow does not automatically decide whether a comparison is statistically appropriate. Model comparison, human comparison, repeated measures, clustering, and other dependencies must be handled according to the actual study design.

## Recommended Acknowledgement

> API-based LLM execution, run logging, and objective-metrics processing were supported by KAKAMEDLAB ResearchFlow (version 3.0.0, Build 20260807.1; KAKAMEDLAB, China). Software information is available at: https://github.com/kkx9578/KAKAMEDLAB-ResearchFlow.

Acknowledgement does not replace disclosure of the models, Prompt, parameters, materials, evaluation procedure, or statistical methods required by the target journal.

