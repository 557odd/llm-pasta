```

OBJECTIVE
  Construct a framework for evaluating claims against evidence while preserving
  distinctions among reality, context, and setting.

CORE PRINCIPLE
  A claim cannot be evaluated reliably without identifying:
    1. WHAT is being claimed                 -> REALITY
    2. UNDER WHAT information and conditions -> CONTEXT
    3. WITHIN WHICH environment or rule set  -> SETTING

  TRUTH ENGINE = Reality Model
              + Context Resolver
              + Setting Interpreter
              + Evidence Evaluator
              + Temporal Validator
              + Contradiction Resolver
              + Uncertainty Calibrator
              + Verifiable Output


===============================================================================
LAYER 00 :: FOUNDATION
===============================================================================

  00.1  PURPOSE
        Determine what can reasonably be asserted, what supports it, under
        which conditions it holds, and what remains unknown.

  00.2  FUNDAMENTAL DISTINCTIONS
        FACT             = A proposition supported by adequate evidence.
        CLAIM            = A proposition asserted as true or false.
        EVIDENCE         = Information relevant to evaluating a claim.
        OBSERVATION      = Recorded or perceived information about an event.
        INFERENCE        = A conclusion derived from evidence and assumptions.
        ASSUMPTION       = A premise accepted provisionally.
        MODEL            = A representation of some aspect of reality.
        CONTEXT          = Information needed to interpret a claim.
        SETTING          = The environment, scenario, or rule framework.
        TRUTH STATUS     = The engine's current assessment of a proposition.
        UNCERTAINTY      = The degree to which available information is
                           insufficient to establish a conclusion.

  00.3  FOUNDATIONAL RULES
        R-001  Separate observations from interpretations.
        R-002  Separate evidence from conclusions.
        R-003  Preserve source provenance.
        R-004  Preserve temporal and situational qualifications.
        R-005  Distinguish unknown from false.
        R-006  Distinguish disagreement from contradiction.
        R-007  Do not convert plausibility into certainty.
        R-008  Revise conclusions when material new evidence arrives.
        R-009  Distinguish real-world truth from model-internal truth.
        R-010  Never claim verification that was not performed.


===============================================================================
LAYER 01 :: REALITY ENGINE
===============================================================================

  FUNCTION
    Represent the world, its entities, events, states, relationships, and
    observable properties without confusing the representation with reality.

  1.1 ONTOLOGY
      |
      +-- Entities
      |     +-- People
      |     +-- Organizations
      |     +-- Objects
      |     +-- Systems
      |     +-- Concepts
      |     +-- Locations
      |
      +-- Events
      |     +-- Actions
      |     +-- State transitions
      |     +-- Occurrences
      |     +-- Interactions
      |
      +-- Properties
      |     +-- Identity
      |     +-- Quantity
      |     +-- Quality
      |     +-- State
      |     +-- Capability
      |     +-- Measurable attributes
      |
      +-- Relationships
      |     +-- Part-of
      |     +-- Member-of
      |     +-- Located-at
      |     +-- Depends-on
      |     +-- Causes
      |     +-- Correlates-with
      |
      +-- Constraints
            +-- Physical
            +-- Logical
            +-- Mathematical
            +-- Biological
            +-- Institutional
            +-- Domain-specific

  1.2 OBSERVATION MODEL
      Input:
        - Sensor measurements
        - Documents
        - Records
        - Test results
        - Direct observations
        - Witness reports
        - Instrumented system outputs

      Process:
        - Validate measurement units.
        - Determine observation time.
        - Identify the observer and method.
        - Check measurement uncertainty.
        - Detect missing or corrupted values.
        - Separate raw observations from interpreted meaning.

      Output:
        OBSERVATION_RECORD

  1.3 WORLD-STATE MODEL
      Represent:
        ENTITY -> PROPERTY -> VALUE -> VALID_TIME
        EVENT  -> PARTICIPANT -> TIME -> LOCATION
        STATE  -> PRECONDITION -> TRANSITION -> POSTCONDITION
        CLAIM  -> SUPPORTING_EVIDENCE -> EVALUATION

      Important:
        A stored record represents what a source reported.
        It does not automatically establish that the reported event occurred.

  1.4 TEMPORAL REALITY
      |
      +-- Past state
      +-- Present state
      +-- Projected future state
      +-- Historical reconstruction
      +-- Time-dependent properties
      +-- Conflicting timestamps
      +-- Unknown temporal boundaries

      Temporal rules:
        - Record when an event occurred.
        - Record when the information was collected.
        - Record when the information became available.
        - Expire or revalidate time-sensitive claims.
        - Never equate publication date with event date.

  1.5 CAUSALITY AND DEPENDENCY
      |
      +-- Temporal precedence
      +-- Mechanism evidence
      +-- Intervention evidence
      +-- Confounding variables
      +-- Alternative explanations
      +-- Correlation-versus-causation checks
      +-- Counterfactual analysis

      Rule:
        A causal claim requires stronger justification than the observation
        that two events occurred together or in sequence.

  1.6 REALITY LIMITS
      |
      +-- Directly observable
      +-- Indirectly measurable
      +-- Inferable from evidence
      +-- Model-dependent
      +-- Currently unobservable
      +-- Unknown
      +-- Not well-defined

      Output:
        REALITY_MODEL + OBSERVATION_SET + LIMITATIONS


===============================================================================
LAYER 02 :: CONTEXT ENGINE
===============================================================================

  FUNCTION
    Resolve the conditions and background information necessary to interpret
    a proposition without altering the underlying evidence.

  2.1 CONTEXT DIMENSIONS
      |
      +-- Linguistic Context
      |     +-- Definitions
      |     +-- Syntax
      |     +-- Ambiguous references
      |     +-- Implicit premises
      |     +-- Meaning in surrounding text
      |
      +-- Historical Context
      |     +-- Period
      |     +-- Preceding events
      |     +-- Relevant historical conditions
      |     +-- Changes over time
      |
      +-- Social Context
      |     +-- Roles
      |     +-- Relationships
      |     +-- Norms
      |     +-- Institutional practices
      |
      +-- Technical Context
      |     +-- Domain terminology
      |     +-- Specifications
      |     +-- Units and conventions
      |     +-- Version dependencies
      |
      +-- Evidentiary Context
      |     +-- Source provenance
      |     +-- Source independence
      |     +-- Corroboration
      |     +-- Missing information
      |     +-- Evidence quality
      |
      +-- Temporal Context
      |     +-- Relevant date
      |     +-- Validity interval
      |     +-- Information freshness
      |     +-- Historical versus current meaning
      |
      +-- Intent Context
            +-- User's objective
            +-- Question type
            +-- Requested level of precision
            +-- Required decision
            +-- Intended audience

  2.2 CONTEXT RESOLUTION PIPELINE
      |
      +-- Step A: Parse the claim.
      +-- Step B: Resolve entities and references.
      +-- Step C: Identify domain and terminology.
      +-- Step D: Retrieve relevant background evidence.
      +-- Step E: Identify assumptions and omissions.
      +-- Step F: Detect conflicting interpretations.
      +-- Step G: Evaluate alternative readings.
      +-- Step H: Return the minimal sufficient context.

  2.3 CONTEXT INTEGRITY
      Rules:
        - Do not invent missing background information.
        - Label inferred context separately from supplied context.
        - Preserve original source meaning.
        - Avoid selective context that reverses a source's meaning.
        - Distinguish an explanation from evidence.
        - Retain meaningful disagreement among sources.
        - Avoid treating popularity as proof.

  2.4 CONTEXT DEPENDENCY TYPES
      |
      +-- REQUIRED
      |     The claim cannot be interpreted correctly without it.
      |
      +-- SUPPORTING
      |     It increases or decreases evidentiary strength.
      |
      +-- QUALIFYING
      |     It restricts the situations in which the claim applies.
      |
      +-- IRRELEVANT
      |     It contributes no material information to the evaluation.
      |
      +-- UNKNOWN
            Its relevance or value has not been established.

  2.5 CONTEXT OUTPUT
      CONTEXT_FRAME {
        domain
        definitions
        referenced_entities
        temporal_scope
        source_provenance
        known_assumptions
        missing_information
        alternative_interpretations
        confidence_limitations
      }


===============================================================================
LAYER 03 :: SETTING ENGINE
===============================================================================

  FUNCTION
    Determine the environment, scenario, operating conditions, and rule system
    within which a proposition is asserted or evaluated.

  DISTINCTION
    CONTEXT = Information that helps explain or interpret a claim.
    SETTING = The environment or scenario in which the claim is evaluated.

  3.1 SETTING TAXONOMY
      |
      +-- Physical Setting
      |     +-- Location
      |     +-- Environmental conditions
      |     +-- Available resources
      |     +-- Physical constraints
      |
      +-- Temporal Setting
      |     +-- Date and time
      |     +-- Duration
      |     +-- Sequence of events
      |     +-- Historical period
      |
      +-- Operational Setting
      |     +-- Runtime environment
      |     +-- Infrastructure
      |     +-- Configuration
      |     +-- Permissions
      |     +-- Active dependencies
      |
      +-- Institutional Setting
      |     +-- Jurisdiction
      |     +-- Organization
      |     +-- Policy regime
      |     +-- Applicable procedures
      |
      +-- Social Setting
      |     +-- Participants
      |     +-- Roles
      |     +-- Audience
      |     +-- Interaction norms
      |
      +-- Simulation Setting
      |     +-- Simulated entities
      |     +-- Initial conditions
      |     +-- Simulation rules
      |     +-- Random variables
      |     +-- Model boundaries
      |
      +-- Fictional Setting
      |     +-- Canonical facts
      |     +-- Narrative rules
      |     +-- Established world state
      |     +-- Author-defined exceptions
      |
      +-- Counterfactual Setting
      |     +-- Hypothetical intervention
      |     +-- Changed premise
      |     +-- Preserved conditions
      |     +-- Assumed causal structure
      |
      +-- Decision Setting
            +-- Available choices
            +-- Objective function
            +-- Risk tolerance
            +-- Applicable constraints
            +-- Cost of error

  3.2 SETTING CONTRACT
      Every evaluated scenario should identify:

        setting_id
        setting_type
        environment
        applicable_rules
        initial_conditions
        active_configuration
        constraints
        participant_roles
        temporal_scope
        model_or_world_boundary
        known_exceptions

  3.3 SETTING VALIDATION
      Check:
        - Is the setting explicitly specified?
        - Is it inferred, assumed, or directly observed?
        - Are the applicable rules known?
        - Are there incompatible rule systems?
        - Has the setting changed since the claim was made?
        - Does the claim cross a system boundary?
        - Is the claim being mistakenly transferred between settings?

  3.4 SETTING BOUNDARIES
      Example:
        A statement can be true in a simulation but false in the physical world.
        A policy can apply in one jurisdiction but not another.
        A software capability can exist in one version but not another.
        A fictional statement can be canonical in one continuity but not another.

      OUTPUT:
        SETTING_FRAME + RULES + BOUNDARIES + VALIDITY CONDITIONS


===============================================================================
LAYER 04 :: CLAIM NORMALIZATION ENGINE
===============================================================================

  FUNCTION
    Convert natural-language assertions into explicit, testable propositions.

  4.1 CLAIM COMPONENTS
      |
      +-- Subject
      +-- Predicate
      +-- Object or value
      +-- Quantifier
      +-- Polarity
      +-- Time interval
      +-- Location or scope
      +-- Conditions
      +-- Modality
      +-- Source attribution

  4.2 CLAIM TYPES
      |
      +-- Descriptive      : What is or was the case?
      +-- Historical       : What happened?
      +-- Quantitative     : How much or how many?
      +-- Causal           : What caused what?
      +-- Predictive       : What may happen?
      +-- Normative        : What should happen?
      +-- Legal            : What rule applies?
      +-- Definitional     : What does a term mean?
      +-- Comparative      : Which is greater or different?
      +-- Existential      : Does something exist?
      +-- Modal            : Is something possible or necessary?
      +-- Model-relative   : What holds under a specified model?

  4.3 NORMALIZATION RULES
      - Preserve the original semantic intent.
      - Expand ambiguous pronouns and references when supported.
      - Separate compound claims into individually testable propositions.
      - Identify hidden premises.
      - Preserve qualifiers such as "all," "some," "usually," and "possibly."
      - Keep normative conclusions distinct from descriptive findings.

  4.4 EXAMPLE
      Input:
        "The system is secure."

      Normalized claims:
        C1: The system satisfies specified security requirements.
        C2: The system passed specified tests.
        C3: No vulnerabilities are known within a defined assessment scope.
        C4: The system is secure under the stated threat model.

      Evaluation:
        These claims are not equivalent.
        Passing tests does not establish the absence of all vulnerabilities.


===============================================================================
LAYER 05 :: EVIDENCE AND PROVENANCE ENGINE
===============================================================================

  FUNCTION
    Evaluate whether available information adequately supports each claim.

  5.1 EVIDENCE CLASSES
      |
      +-- Direct measurement
      +-- Reproducible experiment
      +-- Primary-source record
      +-- Independent corroboration
      +-- Expert interpretation
      +-- Secondary reporting
      +-- Testimony
      +-- Statistical inference
      +-- Mathematical proof
      +-- Computational result
      +-- Model output
      +-- Unverified assertion

  5.2 SOURCE PROVENANCE
      Record:
        source_id
        source_type
        author_or_origin
        creation_time
        publication_time
        retrieval_time
        method_of_collection
        transformation_history
        cited_dependencies
        integrity_checks
        known_limitations

  5.3 EVIDENCE QUALITY DIMENSIONS
      |
      +-- Relevance
      +-- Authenticity
      +-- Accuracy
      +-- Independence
      +-- Reproducibility
      +-- Completeness
      +-- Timeliness
      +-- Methodological rigor
      +-- Susceptibility to bias
      +-- Applicability to the claim

  5.4 CORROBORATION
      Determine whether evidence sources are genuinely independent.

      Multiple publications repeating one unsupported assertion do not
      necessarily constitute multiple independent confirmations.

  5.5 EVIDENCE GRAPH
      Claim C
        |
        +-- Supported by --> Evidence E1
        |
        +-- Supported by --> Evidence E2
        |
        +-- Challenged by --> Evidence E3
        |
        +-- Depends on --> Assumption A1
        |
        +-- Limited by --> Condition K1

      Preserve:
        - The path from evidence to conclusion.
        - The assumptions needed for each inference.
        - Any evidence that materially opposes the conclusion.


===============================================================================
LAYER 06 :: TRUTH EVALUATION ENGINE
===============================================================================

  FUNCTION
    Produce calibrated judgments based on claim type, relevant rules, evidence,
    assumptions, and the limits of available knowledge.

  6.1 EVALUATION METHODS
      |
      +-- Deductive
      |     Validity of reasoning from premises.
      |
      +-- Inductive
      |     Strength of generalization from observations.
      |
      +-- Statistical
      |     Appropriate estimation and uncertainty analysis.
      |
      +-- Empirical
      |     Measurement, observation, testing, replication.
      |
      +-- Causal
      |     Mechanism, temporal evidence, confounding, intervention.
      |
      +-- Formal
      |     Proof under explicit axioms and definitions.
      |
      +-- Documentary
      |     Source authenticity, corroboration, and provenance.
      |
      +-- Model-based
            Consistency with assumptions, model structure, and validation.

  6.2 EVALUATION SEQUENCE
      1. Identify the proposition.
      2. Determine its claim type.
      3. Resolve relevant context.
      4. establish the setting and applicable rules.
      5. Retrieve evidence and provenance.
      6. Check definitions and logical consistency.
      7. Assess evidence quality.
      8. Search for counterevidence.
      9. Test competing explanations.
      10. Evaluate assumptions and dependencies.
      11. Assign a calibrated truth status.
      12. Record remaining uncertainty.
      13. Produce an auditable explanation.

  6.3 TRUTH STATUS ENUMERATION
      |
      +-- VERIFIED
      |     Strong, appropriate evidence supports the claim within a defined
      |     scope; "verified" must never imply universal certainty.
      |
      +-- SUPPORTED
      |     Available evidence favors the claim.
      |
      +-- PLAUSIBLE
      |     The claim is compatible with current knowledge but lacks sufficient
      |     direct evidence for stronger classification.
      |
      +-- DISPUTED
      |     Material evidence or credible interpretations conflict.
      |
      +-- INCONCLUSIVE
      |     Available evidence does not adequately resolve the claim.
      |
      +-- UNVERIFIED
      |     The claim has not been adequately checked.
      |
      +-- CONTRADICTED
      |     Reliable evidence conflicts with the claim under matching
      |     definitions, time, scope, and setting.
      |
      +-- FALSIFIED_WITHIN_SCOPE
      |     A defined test or counterexample disproves a suitably bounded claim.
      |
      +-- NOT_WELL_DEFINED
      |     The proposition is too ambiguous or incoherent to evaluate reliably.
      |
      +-- NOT_APPLICABLE
            The evaluation does not apply to the specified subject or setting.

  6.4 IMPORTANT SEMANTIC RULES
      - "Unknown" does not mean "false."
      - "Not found" does not necessarily mean "does not exist."
      - "Supported" does not mean "proven beyond all doubt."
      - "Contradicted" must refer to the same proposition and scope.
      - "Verified" must specify what was checked and by which method.
      - Predictive truth must account for the forecast horizon and uncertainty.
      - Moral or normative claims require explicit values and standards.
      - Mathematical proof establishes a conclusion relative to its premises,
        definitions, and formal system.

  6.5 CALIBRATION
      Confidence must reflect:
        - Evidence strength.
        - Evidence independence.
        - Claim complexity.
        - Measurement uncertainty.
        - Model limitations.
        - Competing explanations.
        - Missing information.
        - Stability over time.

      Do not convert a qualitative evidence assessment into a numerical
      probability unless the probability has a defensible interpretation.


===============================================================================
LAYER 07 :: CONTRADICTION AND CONFLICT RESOLUTION
===============================================================================

  FUNCTION
    Distinguish genuine incompatibility from apparent disagreement caused by
    differences in definitions, time, context, or setting.

  7.1 CONFLICT TYPES
      |
      +-- Logical Conflict
      +-- Factual Conflict
      +-- Temporal Conflict
      +-- Definition Conflict
      +-- Scope Conflict
      +-- Measurement Conflict
      +-- Source Conflict
      +-- Model Conflict
      +-- Jurisdiction Conflict
      +-- Perspective Conflict

  7.2 RESOLUTION ORDER
      |
      +-- A. Compare exact propositions.
      +-- B. Normalize terminology and definitions.
      +-- C. Align temporal boundaries.
      +-- D. Align units and measurement methods.
      +-- E. Align contextual assumptions.
      +-- F. Align settings and applicable rules.
      +-- G. Verify source provenance.
      +-- H. Compare evidence quality.
      +-- I. Identify whether the conflict remains genuine.
      +-- J. Preserve unresolved disagreements.

  7.3 CONFLICT POLICY
      Never:
        - Automatically prefer the newest statement without checking authority.
        - Automatically prefer an official source without examining its evidence.
        - Average mutually incompatible claims merely to produce consensus.
        - Suppress minority evidence when it is materially relevant.
        - manufacture a resolution when the available evidence is insufficient.

      Output:
        CONFLICT_REPORT {
          claim_a
          claim_b
          conflict_type
          shared_assumptions
          differing_assumptions
          evidence_comparison
          resolution_status
          remaining_uncertainty
        }


===============================================================================
LAYER 08 :: TEMPORAL TRUTH AND CHANGE MANAGEMENT
===============================================================================

  FUNCTION
    Track how claims, evidence, settings, and conclusions change over time.

  8.1 TEMPORAL RECORD
      claim_id
      claim_valid_from
      claim_valid_until
      evidence_observed_at
      source_published_at
      evaluated_at
      last_verified_at
      next_review_condition

  8.2 CHANGE TYPES
      |
      +-- New evidence
      +-- Corrected evidence
      +-- Changed definition
      +-- Changed law or policy
      +-- Changed software version
      +-- Changed environmental conditions
      +-- Superseded source
      +-- Previously unknown contradiction

  8.3 REVALIDATION TRIGGERS
      - A key source is corrected or withdrawn.
      - The validity period expires.
      - A relevant setting changes.
      - A dependency receives a new version.
      - A material contradiction appears.
      - A new observation invalidates a prior assumption.

  8.4 VERSIONING POLICY
      Store prior conclusions rather than silently overwriting them.

      Every material revision should identify:
        OLD CONCLUSION
        NEW EVIDENCE
        CHANGED ASSUMPTIONS
        NEW CONCLUSION
        REASON FOR CHANGE
        REVISION TIMESTAMP


===============================================================================
LAYER 09 :: REALITY-CONTEXT-SETTING FUSION
===============================================================================

  PURPOSE
    Integrate the three primary layers into one evaluable representation.

                         +-----------------------+
                         |      USER CLAIM       |
                         +-----------+-----------+
                                     |
                         +-----------v-----------+
                         |   CLAIM NORMALIZER    |
                         +-----------+-----------+
                                     |
                +--------------------+--------------------+
                |                    |                    |
       +--------v--------+  +--------v--------+  +--------v--------+
       | REALITY ENGINE  |  | CONTEXT ENGINE |  | SETTING ENGINE  |
       |                 |  |                |  |                 |
       | Entities        |  | Meaning        |  | Environment     |
       | Events          |  | Provenance     |  | Rules           |
       | Observations    |  | Assumptions    |  | Constraints     |
       | States          |  | Time and scope |  | Boundaries      |
       +--------+--------+  +--------+-------+  +--------+--------+
                |                    |                    |
                +--------------------+--------------------+
                                     |
                         +-----------v-----------+
                         | EVIDENCE GRAPH        |
                         | AND DEPENDENCY MODEL  |
                         +-----------+-----------+
                                     |
                         +-----------v-----------+
                         | TRUTH EVALUATOR       |
                         +-----------+-----------+
                                     |
                +--------------------+--------------------+
                |                    |                    |
       +--------v--------+  +--------v--------+  +--------v--------+
       | CONFLICT CHECK  |  | TIME VALIDATOR  |  | CALIBRATOR      |
       +--------+--------+  +--------+--------+  +--------+--------+
                |                    |                    |
                +--------------------+--------------------+
                                     |
                         +-----------v-----------+
                         | AUDITABLE RESULT      |
                         | STATUS + EVIDENCE     |
                         | SCOPE + UNCERTAINTY   |
                         +-----------------------+


===============================================================================
LAYER 10 :: OUTPUT CONTRACT
===============================================================================

  Every evaluated claim should produce a structured result.

  TRUTH_RESULT {
    result_id

    claim {
      original_text
      normalized_proposition
      claim_type
      subject
      predicate
      scope
    }

    reality {
      relevant_entities
      observed_states
      relevant_events
      known_constraints
      observation_limitations
    }

    context {
      definitions
      relevant_background
      assumptions
      source_provenance
      missing_information
      alternative_interpretations
    }

    setting {
      setting_type
      environment
      applicable_rules
      temporal_scope
      boundaries
    }

    evidence {
      supporting_evidence[]
      contradicting_evidence[]
      evidence_quality
      source_independence
      dependency_graph
    }

    evaluation {
      truth_status
      rationale
      confidence_assessment
      counterarguments[]
      unresolved_questions[]
      conditions_of_validity[]
    }

    audit {
      evaluation_timestamp
      method_used
      sources_checked[]
      checks_performed[]
      limitations[]
      revision_history
    }
  }


===============================================================================
LAYER 11 :: SYSTEM INTEGRITY AND GUARDRAILS
===============================================================================

  11.1 EPISTEMIC GUARDRAILS
       - No fabricated evidence.
       - No fabricated source citations.
       - No unsupported certainty.
       - No conflation of opinion, inference, and observation.
       - No implicit conversion of an assumption into a fact.
       - No silent substitution of definitions.
       - No hidden changes to claim scope.

  11.2 DATA INTEGRITY
       - Preserve source identifiers.
       - Record transformations.
       - Detect duplicate evidence.
       - Identify circular support.
       - Version claims and evaluations.
       - Separate untrusted inputs from executable instructions.
       - Maintain access controls for sensitive information.

  11.3 ADVERSARIAL CHECKS
       - Could the claim be false despite the available evidence?
       - Is a key source dependent on another source?
       - Does the evidence support the exact proposition or only a weaker one?
       - Has contradictory evidence been omitted?
       - Does the conclusion depend on a disputed assumption?
       - Is a model being mistaken for the world?
       - Has evidence been transferred incorrectly between settings?
       - Would a plausible alternative explanation fit the observations?

  11.4 FAILURE STATES
       INSUFFICIENT_EVIDENCE
       AMBIGUOUS_CLAIM
       CONFLICTING_SOURCES
       UNKNOWN_SETTING
       STALE_INFORMATION
       INVALID_INFERENCE
       UNRESOLVED_DEPENDENCY
       SOURCE_INTEGRITY_FAILURE
       MODEL_OUT_OF_SCOPE

       On failure:
         RETURN THE LIMITATION
         IDENTIFY THE MISSING REQUIREMENT
         PRESERVE VALID FINDINGS
         AVOID INVENTING A DEFINITIVE ANSWER


===============================================================================
LAYER 12 :: RECOMMENDED IMPLEMENTATION MODULES
===============================================================================

  CORE
    truth_engine/
      __init__
      claim_parser
      claim_normalizer
      truth_evaluator
      confidence_calibrator
      result_schema

  ONTOLOGY
    reality/
      entity_registry
      event_model
      world_state
      observation_store
      causal_graph
      temporal_model

  INTERPRETATION
    context/
      semantic_resolver
      domain_classifier
      provenance_resolver
      assumption_registry
      ambiguity_detector
      context_builder

  ENVIRONMENTS
    setting/
      environment_registry
      rule_registry
      configuration_resolver
      scenario_manager
      boundary_validator
      counterfactual_engine

  EVIDENCE
    evidence/
      evidence_ingestion
      source_registry
      integrity_validator
      corroboration_engine
      evidence_graph
      retrieval_adapter

  VALIDATION
    validation/
      logical_consistency
      statistical_validation
      empirical_validation
      temporal_validation
      conflict_resolution
      adversarial_review

  GOVERNANCE
    governance/
      audit_log
      policy_engine
      access_control
      privacy_controls
      provenance_tracking
      change_management

  INTERFACES
    interfaces/
      api
      cli
      reporting
      human_review
      monitoring


===============================================================================
LAYER 13 :: MINIMUM VIABLE TRUTH ENGINE
===============================================================================

  PHASE 1 -- CLAIM PROCESSING
    [ ] Parse a claim into a testable proposition.
    [ ] Identify ambiguous terms.
    [ ] Identify claim type and scope.

  PHASE 2 -- TRIAD MODEL
    [ ] Build the reality representation.
    [ ] Resolve contextual dependencies.
    [ ] Identify setting and applicable rules.

  PHASE 3 -- EVIDENCE
    [ ] Retrieve source evidence.
    [ ] Track source provenance.
    [ ] Record supporting and contradicting evidence.
    [ ] Separate assumptions from observations.

  PHASE 4 -- EVALUATION
    [ ] Check logical consistency.
    [ ] Evaluate the evidence.
    [ ] Detect contradictions.
    [ ] Calibrate uncertainty.
    [ ] Assign a scoped truth status.

  PHASE 5 -- AUDIT AND REVISION
    [ ] Return a traceable explanation.
    [ ] Preserve limitations.
    [ ] Record evaluation time.
    [ ] Enable re-evaluation when inputs change.


===============================================================================
FINAL ARCHITECTURAL DEFINITION
===============================================================================

  REALITY
    What exists, occurred, or can be observed or inferred.

  CONTEXT
    What gives a proposition its relevant meaning, provenance, scope,
    background, and interpretive conditions.

  SETTING
    Where, when, and under which environmental conditions, rules, or scenario
    the proposition is evaluated.

  EVIDENCE
    What supports, challenges, qualifies, or fails to address the proposition.

  TRUTH ENGINE
    The process that integrates these inputs to produce a scoped, evidence-based,
    uncertainty-aware, revisable assessment.

  CONCEPTUAL FORMULA

    TRUTH_ASSESSMENT =
        EVALUATE(
            CLAIM,
            REALITY_MODEL,
            CONTEXT_FRAME,
            SETTING_FRAME,
            EVIDENCE_GRAPH,
            TEMPORAL_SCOPE,
            EVALUATION_RULES
        )

  CRITICAL LIMITATION

    The engine does not create truth or guarantee access to objective reality.
    It creates an auditable process for determining which claims are justified
    by the available evidence, under explicitly stated conditions.

===============================================================================
END :: TRUTH ENGINE OUTLINE
===============================================================================
