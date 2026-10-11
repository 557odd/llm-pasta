```

{
  "truth_engine": {
    "metadata": {
      "id": "truth-engine-core",
      "name": "Truth Engine",
      "version": "1.0.0",
      "schema_version": "1.0.0",
      "status": "specification",
      "mode": "evidence_based_claim_evaluation",
      "description": "A modular system for evaluating claims about reality using context, setting, evidence provenance, temporal reasoning, causal graphs, uncertainty calibration, contradiction resolution, and auditable revisions.",
      "design_goals": [
        "Represent reality claims without confusing assertions with observations.",
        "Resolve context and setting before evaluating claim scope.",
        "Maintain evidence provenance and source lineage.",
        "Connect everyday occurrences through traceable causality-symlinks.",
        "Distinguish correlation, temporal order, dependency, and causation.",
        "Detect and preserve contradictions.",
        "Track uncertainty without fabricating precision.",
        "Maintain reproducible, tamper-evident audit history.",
        "Return consistent machine-readable evaluation results."
      ],
      "principles": [
        "A claim is not evidence of itself.",
        "An observation is not necessarily a complete description of reality.",
        "An inference is not a directly observed fact.",
        "Missing evidence does not automatically refute a claim.",
        "Temporal precedence alone does not establish causation.",
        "Correlation alone does not establish causation.",
        "Confidence is not equivalent to truth.",
        "Conflicting evidence must remain traceable.",
        "Conclusions are scoped to their applicable context and setting.",
        "Every material revision must preserve its rationale and lineage."
      ]
    },
    "enums": {
      "claim_status": [
        "unassessed",
        "supported",
        "refuted",
        "partially_supported",
        "conflicted",
        "undetermined",
        "not_applicable"
      ],
      "claim_kind": [
        "descriptive",
        "causal",
        "predictive",
        "normative",
        "definitional",
        "existential",
        "comparative",
        "quantitative"
      ],
      "epistemic_role": [
        "observation",
        "reported_fact",
        "inference",
        "hypothesis",
        "assumption",
        "prediction",
        "decision"
      ],
      "evidence_type": [
        "direct_observation",
        "measurement",
        "primary_document",
        "secondary_source",
        "testimony",
        "derived_data",
        "model_output",
        "experiment",
        "administrative_record",
        "assumption"
      ],
      "evidence_polarity": [
        "supports",
        "refutes",
        "neutral",
        "mixed",
        "unknown"
      ],
      "causal_link_type": [
        "causes",
        "contributes_to",
        "enables",
        "prevents",
        "mediates",
        "moderates",
        "correlates_with",
        "precedes",
        "depends_on",
        "explains",
        "contradicts",
        "feedback_to",
        "unknown"
      ],
      "causal_status": [
        "proposed",
        "temporally_consistent",
        "supported",
        "experimentally_supported",
        "refuted",
        "confounded",
        "undetermined"
      ],
      "uncertainty_type": [
        "epistemic",
        "aleatory",
        "measurement",
        "semantic",
        "temporal",
        "causal",
        "model",
        "sampling",
        "source"
      ],
      "resolution_status": [
        "unresolved",
        "resolved",
        "partially_resolved",
        "not_a_true_conflict"
      ],
      "time_precision": [
        "exact",
        "approximate",
        "date_only",
        "interval",
        "unknown"
      ],
      "setting_type": [
        "physical",
        "social",
        "organizational",
        "technical",
        "legal",
        "digital",
        "abstract",
        "mixed"
      ],
      "audit_action": [
        "create",
        "ingest",
        "normalize",
        "evaluate",
        "revise",
        "link",
        "unlink",
        "resolve",
        "invalidate",
        "review",
        "export"
      ]
    },
    "configuration": {
      "defaults": {
        "verdict": "undetermined",
        "unknown_values": null,
        "allow_unverified_sources": true,
        "require_provenance_for_supported_claim": true,
        "require_explicit_scope": true,
        "require_temporal_validation_for_causal_claims": true,
        "require_alternative_explanations_for_causal_claims": true,
        "allow_probability_without_calibration": false,
        "preserve_conflicting_evidence": true,
        "preserve_original_claim_text": true,
        "automatic_causal_inference": false,
        "automatic_conflict_resolution": false,
        "automatic_overwrite_of_prior_assessments": false
      },
      "evaluation_modes": {
        "strict": {
          "description": "Require traceable evidence and explicit limitations before assigning supported or refuted verdicts.",
          "require_evidence": true,
          "require_provenance": true,
          "unresolved_material_conflict_blocks_definitive_verdict": true
        },
        "exploratory": {
          "description": "Allow provisional hypotheses while labeling their evidential status.",
          "require_evidence": false,
          "require_provenance": false,
          "unresolved_material_conflict_blocks_definitive_verdict": true
        },
        "audit": {
          "description": "Prioritize reproducibility, source lineage, version history, and documented decisions.",
          "require_evidence": true,
          "require_provenance": true,
          "require_evaluation_manifest": true
        }
      },
      "default_mode": "strict",
      "limits": {
        "maximum_graph_depth": 100,
        "maximum_causal_links_per_event": 1000,
        "maximum_evidence_refs_per_claim": 10000,
        "maximum_revision_chain_length": 100000,
        "limits_are_enforcement_targets": true
      }
    },
    "architecture": {
      "layers": [
        {
          "id": "input_layer",
          "components": [
            "input_ingestion",
            "source_registration",
            "event_capture"
          ],
          "purpose": "Accept claims, observations, documents, measurements, and everyday event records."
        },
        {
          "id": "interpretation_layer",
          "components": [
            "reality_model",
            "context_resolver",
            "setting_interpreter",
            "claim_normalizer"
          ],
          "purpose": "Structure statements and establish the scope in which they can be evaluated."
        },
        {
          "id": "evidence_layer",
          "components": [
            "evidence_provenance_graph",
            "temporal_validator"
          ],
          "purpose": "Validate source lineage, evidence relevance, chronology, and temporal applicability."
        },
        {
          "id": "reasoning_layer",
          "components": [
            "truth_evaluator",
            "causality_dependency_engine",
            "contradiction_resolver",
            "uncertainty_calibrator"
          ],
          "purpose": "Evaluate support, refutation, causal hypotheses, conflicts, and unresolved uncertainty."
        },
        {
          "id": "governance_layer",
          "components": [
            "audit_revision_system",
            "structured_output_interface"
          ],
          "purpose": "Preserve decision history and return reproducible, structured results."
        }
      ],
      "components": [
        {
          "id": "reality_model",
          "number": 1,
          "name": "Reality Model",
          "responsibility": "Represent entities, events, states, measurements, and claims about the world.",
          "inputs": [
            "claims",
            "observations",
            "measurements",
            "event_records"
          ],
          "outputs": [
            "reality_entities",
            "reality_states",
            "event_records",
            "observation_records"
          ],
          "operations": [
            "register_entity",
            "record_observation",
            "record_state",
            "record_event",
            "link_observation_to_claim"
          ],
          "invariants": [
            "Assertions and observations remain distinct.",
            "Unobserved does not mean nonexistent.",
            "A reported event must retain its source and epistemic role.",
            "Observed properties must retain measurement limitations."
          ]
        },
        {
          "id": "context_resolver",
          "number": 2,
          "name": "Context Resolver",
          "responsibility": "Identify relevant circumstances, background information, assumptions, and dependencies.",
          "inputs": [
            "normalized_claims",
            "evidence_records",
            "event_records",
            "context_records"
          ],
          "outputs": [
            "resolved_context",
            "context_dependencies",
            "context_gaps"
          ],
          "operations": [
            "resolve_references",
            "identify_assumptions",
            "identify_missing_context",
            "compare_context_versions"
          ],
          "invariants": [
            "Unknown circumstances remain unknown.",
            "Assumptions are never silently promoted to observations.",
            "Context-dependent conclusions identify their applicable conditions."
          ]
        },
        {
          "id": "setting_interpreter",
          "number": 3,
          "name": "Setting Interpreter",
          "responsibility": "Represent the physical, social, organizational, technical, or abstract environment of a claim.",
          "inputs": [
            "normalized_claims",
            "resolved_context",
            "environment_records",
            "applicable_rules"
          ],
          "outputs": [
            "setting_records",
            "setting_constraints",
            "scope_assessments"
          ],
          "operations": [
            "identify_setting",
            "resolve_applicable_rules",
            "validate_rule_time_scope",
            "identify_setting_mismatch"
          ],
          "invariants": [
            "Rules apply only within their defined scope.",
            "Setting changes are represented explicitly.",
            "A rule's existence does not prove that it was followed."
          ]
        },
        {
          "id": "claim_normalizer",
          "number": 4,
          "name": "Claim Normalizer",
          "responsibility": "Transform natural-language statements into structured propositions while preserving the original wording.",
          "inputs": [
            "raw_claims",
            "resolved_context",
            "setting_records"
          ],
          "outputs": [
            "normalized_claims",
            "ambiguity_records",
            "claim_dependencies"
          ],
          "operations": [
            "extract_subject",
            "extract_predicate",
            "extract_object",
            "extract_polarity",
            "extract_quantifiers",
            "extract_time_scope",
            "classify_claim_kind",
            "detect_ambiguity"
          ],
          "invariants": [
            "Original wording is immutable within a claim version.",
            "Ambiguous statements are flagged.",
            "Negation and quantifiers must be preserved.",
            "Causal propositions are distinguished from descriptive propositions."
          ]
        },
        {
          "id": "evidence_provenance_graph",
          "number": 5,
          "name": "Evidence and Provenance Graph",
          "responsibility": "Track evidence sources, lineage, transformations, independence, and claim relationships.",
          "inputs": [
            "evidence_records",
            "source_records",
            "normalized_claims",
            "derived_data"
          ],
          "outputs": [
            "evidence_graph",
            "provenance_paths",
            "source_dependency_records"
          ],
          "operations": [
            "register_source",
            "register_evidence",
            "link_evidence_to_claim",
            "record_transformation",
            "detect_duplicate_sources",
            "trace_source_lineage",
            "verify_content_hash"
          ],
          "invariants": [
            "Every evidence record has a stable identifier.",
            "Derived evidence identifies its parent records.",
            "A valid hash does not independently establish source authenticity.",
            "Source reliability and claim relevance are separate assessments.",
            "Dependent sources are not automatically counted as independent corroboration."
          ]
        },
        {
          "id": "truth_evaluator",
          "number": 6,
          "name": "Truth Evaluator",
          "responsibility": "Evaluate whether the evidence supports, refutes, partially supports, or leaves a claim undetermined.",
          "inputs": [
            "normalized_claims",
            "evidence_graph",
            "resolved_context",
            "setting_records",
            "temporal_assessments",
            "contradiction_records"
          ],
          "outputs": [
            "claim_assessments",
            "evaluation_rationales",
            "missing_evidence_records"
          ],
          "operations": [
            "evaluate_support",
            "evaluate_refutation",
            "evaluate_scope",
            "evaluate_evidence_quality",
            "identify_missing_evidence",
            "assign_provisional_verdict"
          ],
          "invariants": [
            "Verdicts must be supported by recorded reasoning.",
            "Conflicting material evidence is not silently discarded.",
            "Lack of evidence is not automatically evidence of falsity.",
            "A model-generated answer is not independent proof of its own conclusion."
          ]
        },
        {
          "id": "causality_dependency_engine",
          "number": 7,
          "name": "Causality and Dependency Engine",
          "responsibility": "Build and evaluate causal hypotheses and dependencies between daily occurrences and other events.",
          "inputs": [
            "event_records",
            "claim_assessments",
            "evidence_graph",
            "temporal_assessments",
            "context_dependencies"
          ],
          "outputs": [
            "causality_symlinks",
            "dependency_graph",
            "causal_hypotheses",
            "confounding_assessments"
          ],
          "operations": [
            "create_causality_symlink",
            "validate_time_order",
            "propose_mechanism",
            "identify_confounders",
            "identify_alternative_explanations",
            "evaluate_counterfactual_basis",
            "detect_graph_cycles",
            "evaluate_causal_status"
          ],
          "invariants": [
            "Correlation is not causation.",
            "Temporal order alone does not establish causation.",
            "Proposed links remain provisional until sufficiently supported.",
            "Confounders and alternative explanations are recorded.",
            "Feedback loops are distinct from invalid causal cycles.",
            "Causal direction must be explicit."
          ]
        },
        {
          "id": "contradiction_resolver",
          "number": 8,
          "name": "Contradiction Resolver",
          "responsibility": "Identify conflicts between claims, observations, sources, time periods, and settings.",
          "inputs": [
            "normalized_claims",
            "evidence_graph",
            "setting_records",
            "temporal_assessments",
            "claim_assessments"
          ],
          "outputs": [
            "contradiction_records",
            "resolution_candidates",
            "unresolved_conflicts"
          ],
          "operations": [
            "detect_logical_conflict",
            "detect_temporal_conflict",
            "detect_scope_conflict",
            "detect_measurement_conflict",
            "propose_resolution",
            "record_resolution"
          ],
          "invariants": [
            "Claims must be compared within compatible scopes.",
            "Different time periods do not automatically imply contradiction.",
            "Resolution requires a recorded rationale.",
            "Unresolved conflicts remain visible in the final output."
          ]
        },
        {
          "id": "temporal_validator",
          "number": 9,
          "name": "Temporal Validator",
          "responsibility": "Validate timestamps, event order, time intervals, evidence freshness, and rule applicability.",
          "inputs": [
            "event_records",
            "evidence_records",
            "normalized_claims",
            "setting_records"
          ],
          "outputs": [
            "temporal_assessments",
            "temporal_warnings",
            "event_order_constraints"
          ],
          "operations": [
            "normalize_timestamp",
            "preserve_timezone",
            "validate_interval",
            "compare_event_order",
            "validate_evidence_freshness",
            "check_rule_validity_period"
          ],
          "invariants": [
            "Event time is distinct from recording time.",
            "Unknown timestamps remain unknown.",
            "Overlapping intervals may leave event order unresolved.",
            "Temporal consistency does not prove causation."
          ]
        },
        {
          "id": "uncertainty_calibrator",
          "number": 10,
          "name": "Uncertainty Calibrator",
          "responsibility": "Represent epistemic, measurement, temporal, semantic, causal, and model uncertainty.",
          "inputs": [
            "claim_assessments",
            "evidence_graph",
            "causality_symlinks",
            "contradiction_records",
            "temporal_assessments"
          ],
          "outputs": [
            "uncertainty_assessments",
            "calibration_records",
            "sensitivity_assessments"
          ],
          "operations": [
            "classify_uncertainty",
            "identify_uncertainty_sources",
            "calibrate_probability",
            "evaluate_sensitivity",
            "identify_unsupported_precision"
          ],
          "invariants": [
            "Confidence in a verdict is not identical to the probability of the proposition.",
            "Numerical probabilities require a defensible interpretation and method.",
            "Unknown uncertainty is not equivalent to zero uncertainty.",
            "Evidence dependencies must be considered.",
            "Calibration limitations are disclosed."
          ]
        },
        {
          "id": "audit_revision_system",
          "number": 11,
          "name": "Audit and Revision System",
          "responsibility": "Maintain a traceable history of inputs, evaluations, causal links, conflicts, and revisions.",
          "inputs": [
            "engine_operations",
            "claim_assessments",
            "human_reviews",
            "configuration_changes"
          ],
          "outputs": [
            "audit_events",
            "revision_records",
            "evaluation_manifests"
          ],
          "operations": [
            "append_audit_event",
            "version_entity",
            "link_revision",
            "record_reason",
            "verify_hash_chain",
            "reconstruct_evaluation"
          ],
          "invariants": [
            "Prior assessments are retained.",
            "Material changes include a reason.",
            "Audit records reference the relevant entity versions.",
            "Tamper evidence is distinguished from absolute tamper prevention.",
            "Reproduction records include the configuration and source references used."
          ]
        },
        {
          "id": "structured_output_interface",
          "number": 12,
          "name": "Structured Output Interface",
          "responsibility": "Serialize evaluation results into consistent machine-readable responses.",
          "inputs": [
            "claim_assessments",
            "causality_symlinks",
            "contradiction_records",
            "uncertainty_assessments",
            "audit_events"
          ],
          "outputs": [
            "truth_engine_response"
          ],
          "operations": [
            "serialize_result",
            "validate_response_schema",
            "attach_provenance",
            "attach_uncertainty",
            "attach_audit_references"
          ],
          "invariants": [
            "Every result has an explicit verdict.",
            "Every conclusion identifies its applicable scope.",
            "Missing evidence and unresolved contradictions are exposed.",
            "The response distinguishes proposed relationships from verified findings.",
            "A specification is never represented as an executed evaluation."
          ]
        }
      ]
    },
    "data_contracts": {
      "reality_entity": {
        "entity_id": "string",
        "entity_type": "string",
        "label": "string",
        "properties": {},
        "observation_refs": [],
        "created_at": "ISO-8601 string",
        "version": 1
      },
      "reality_state": {
        "state_id": "string",
        "entity_refs": [],
        "properties": {},
        "valid_time": {
          "start": "ISO-8601 string or null",
          "end": "ISO-8601 string or null",
          "precision": "exact|approximate|date_only|interval|unknown"
        },
        "observation_refs": [],
        "limitations": []
      },
      "claim": {
        "claim_id": "string",
        "text": "string",
        "subject": "string or null",
        "predicate": "string or null",
        "object": "any or null",
        "polarity": "positive|negative|unknown",
        "quantifier": "string or null",
        "claim_kind": "descriptive|causal|predictive|normative|definitional|existential|comparative|quantitative",
        "epistemic_role": "observation|reported_fact|inference|hypothesis|assumption|prediction|decision",
        "reality_scope": {},
        "context_ref": "string or null",
        "setting_ref": "string or null",
        "valid_time": {
          "start": "ISO-8601 string or null",
          "end": "ISO-8601 string or null",
          "precision": "exact|approximate|date_only|interval|unknown"
        },
        "source_refs": [],
        "ambiguities": [],
        "created_at": "ISO-8601 string",
        "version": 1,
        "supersedes": "string or null"
      },
      "observation": {
        "observation_id": "string",
        "subject_ref": "string",
        "property": "string",
        "value": "any",
        "unit": "string or null",
        "method": "string or null",
        "observer_ref": "string or null",
        "observed_at": "ISO-8601 string or null",
        "recorded_at": "ISO-8601 string",
        "evidence_refs": [],
        "measurement_uncertainty_ref": "string or null",
        "limitations": []
      },
      "context": {
        "context_id": "string",
        "description": "string",
        "conditions": [],
        "assumptions": [],
        "background_facts": [],
        "unknowns": [],
        "dependency_refs": [],
        "created_at": "ISO-8601 string",
        "version": 1
      },
      "setting": {
        "setting_id": "string",
        "setting_type": "physical|social|organizational|technical|legal|digital|abstract|mixed",
        "description": "string",
        "environment": {},
        "applicable_rules": [],
        "valid_from": "ISO-8601 string or null",
        "valid_until": "ISO-8601 string or null",
        "scope_limitations": [],
        "version": 1
      },
      "source": {
        "source_id": "string",
        "source_type": "person|document|dataset|device|system|website|organization|model|other",
        "name": "string or null",
        "uri": "string or null",
        "author": "string or null",
        "publisher": "string or null",
        "published_at": "ISO-8601 string or null",
        "retrieved_at": "ISO-8601 string or null",
        "identity_verified": false,
        "verification_method": "string or null",
        "limitations": []
      },
      "evidence": {
        "evidence_id": "string",
        "evidence_type": "direct_observation|measurement|primary_document|secondary_source|testimony|derived_data|model_output|experiment|administrative_record|assumption",
        "content": "any",
        "polarity": "supports|refutes|neutral|mixed|unknown",
        "source_ref": "string or null",
        "claim_refs": [],
        "observed_at": "ISO-8601 string or null",
        "recorded_at": "ISO-8601 string or null",
        "acquired_at": "ISO-8601 string or null",
        "valid_time": {
          "start": "ISO-8601 string or null",
          "end": "ISO-8601 string or null",
          "precision": "exact|approximate|date_only|interval|unknown"
        },
        "integrity": {
          "hash_algorithm": "string or null",
          "content_hash": "string or null",
          "verification_status": "verified|unverified|failed|not_available"
        },
        "quality": {
          "relevance": "number from 0 to 1 or null",
          "reliability": "number from 0 to 1 or null",
          "directness": "number from 0 to 1 or null",
          "completeness": "number from 0 to 1 or null",
          "assessment_method": "string or null"
        },
        "derived_from": [],
        "limitations": [],
        "version": 1
      },
      "event": {
        "event_id": "string",
        "description": "string",
        "event_type": "string",
        "participants": [],
        "setting_ref": "string or null",
        "context_ref": "string or null",
        "event_time": {
          "start": "ISO-8601 string or null",
          "end": "ISO-8601 string or null",
          "precision": "exact|approximate|date_only|interval|unknown"
        },
        "recorded_at": "ISO-8601 string",
        "epistemic_role": "observation|reported_fact|inference|hypothesis|assumption|prediction|decision",
        "evidence_refs": [],
        "preconditions": [],
        "outcomes": [],
        "version": 1
      },
      "causality_symlink": {
        "link_id": "string",
        "source_event_id": "string",
        "target_event_id": "string",
        "link_type": "causes|contributes_to|enables|prevents|mediates|moderates|correlates_with|precedes|depends_on|explains|contradicts|feedback_to|unknown",
        "causal_status": "proposed|temporally_consistent|supported|experimentally_supported|refuted|confounded|undetermined",
        "mechanism": "string or null",
        "evidence_refs": [],
        "alternative_explanations": [],
        "confounders": [],
        "counterfactual_basis": "string or null",
        "time_order_verified": false,
        "confidence": null,
        "confidence_method": null,
        "context_ref": "string or null",
        "setting_ref": "string or null",
        "created_at": "ISO-8601 string",
        "reviewed_at": "ISO-8601 string or null",
        "version": 1,
        "supersedes": "string or null"
      },
      "claim_evidence_link": {
        "link_id": "string",
        "claim_id": "string",
        "evidence_id": "string",
        "relationship": "supports|refutes|qualifies|contextualizes|derived_from",
        "rationale": "string",
        "independence_group": "string or null",
        "created_at": "ISO-8601 string"
      },
      "temporal_assessment": {
        "temporal_assessment_id": "string",
        "subject_ref": "string",
        "reference_time": "ISO-8601 string or null",
        "time_order": "before|after|overlapping|simultaneous|unknown",
        "validity": "valid|invalid|uncertain|not_applicable",
        "reason": "string",
        "warnings": [],
        "evaluated_at": "ISO-8601 string"
      },
      "claim_assessment": {
        "assessment_id": "string",
        "claim_id": "string",
        "verdict": "unassessed|supported|refuted|partially_supported|conflicted|undetermined|not_applicable",
        "rationale": "string",
        "supporting_evidence_refs": [],
        "refuting_evidence_refs": [],
        "qualifying_evidence_refs": [],
        "missing_evidence": [],
        "contradiction_refs": [],
        "causality_link_refs": [],
        "uncertainty_ref": "string or null",
        "scope": {
          "reality_ref": "string or null",
          "context_ref": "string or null",
          "setting_ref": "string or null",
          "time_scope": {}
        },
        "evaluated_at": "ISO-8601 string",
        "engine_version": "string",
        "evaluation_mode": "strict|exploratory|audit",
        "version": 1,
        "supersedes": "string or null"
      },
      "contradiction": {
        "contradiction_id": "string",
        "claim_refs": [],
        "evidence_refs": [],
        "conflict_type": "logical|temporal|contextual|measurement|source|scope|unknown",
        "description": "string",
        "resolution_status": "unresolved|resolved|partially_resolved|not_a_true_conflict",
        "resolution_rationale": "string or null",
        "resolution_evidence_refs": [],
        "reviewed_by": "string or null",
        "resolved_at": "ISO-8601 string or null",
        "version": 1
      },
      "uncertainty": {
        "uncertainty_id": "string",
        "claim_id": "string",
        "type": "epistemic|aleatory|measurement|semantic|temporal|causal|model|sampling|source",
        "description": "string",
        "probability": null,
        "interval": {
          "lower": null,
          "upper": null,
          "meaning": null
        },
        "calibration_method": null,
        "calibration_dataset_ref": null,
        "assumptions": [],
        "limitations": [],
        "created_at": "ISO-8601 string"
      },
      "audit_event": {
        "audit_id": "string",
        "timestamp": "ISO-8601 string",
        "actor": "string",
        "action": "create|ingest|normalize|evaluate|revise|link|unlink|resolve|invalidate|review|export",
        "entity_type": "claim|evidence|source|event|causal_link|context|setting|assessment|configuration",
        "entity_id": "string",
        "previous_version": "number or null",
        "new_version": "number or null",
        "reason": "string",
        "input_refs": [],
        "engine_version": "string",
        "configuration_hash": "string or null",
        "previous_event_hash": "string or null",
        "event_hash": "string or null",
        "signature": "string or null"
      }
    },
    "graph_model": {
      "node_types": [
        "entity",
        "state",
        "observation",
        "claim",
        "event",
        "evidence",
        "source",
        "context",
        "setting",
        "assessment",
        "contradiction",
        "uncertainty"
      ],
      "edge_types": [
        "observed_by",
        "supports",
        "refutes",
        "derived_from",
        "occurs_in",
        "depends_on",
        "precedes",
        "causes",
        "contributes_to",
        "enables",
        "prevents",
        "mediates",
        "moderates",
        "correlates_with",
        "contradicts",
        "qualifies",
        "supersedes",
        "revises"
      ],
      "integrity_constraints": [
        "Every edge references existing nodes.",
        "Every causal link references existing source and target events.",
        "Every derived evidence record preserves parent evidence references.",
        "Every assessment references an existing claim version.",
        "Every revision preserves the prior version reference.",
        "A causal edge must declare direction.",
        "A correlation edge must not be silently converted to a causal edge.",
        "A cycle in a causal graph requires explicit feedback-loop or cycle-review metadata.",
        "Graph deletion must not silently erase required audit history."
      ],
      "cycle_policy": {
        "detect_cycles": true,
        "allow_feedback_loops": true,
        "require_feedback_loop_label": true,
        "require_cycle_review": true,
        "interpretation": "A directed cycle may represent a feedback process, a modeling error, or an incorrectly inferred causal relationship."
      }
    },
    "causality_engine": {
      "link_creation_policy": {
        "automatic_creation": "propose_only",
        "required_fields": [
          "source_event_id",
          "target_event_id",
          "link_type",
          "causal_status",
          "evidence_refs",
          "alternative_explanations",
          "time_order_verified"
        ],
        "initial_causal_status": "proposed",
        "missing_time_policy": "preserve_unknown",
        "missing_mechanism_policy": "allow_provisional_hypothesis",
        "missing_evidence_policy": "do_not_promote_to_supported"
      },
      "evaluation_checks": [
        {
          "id": "temporal_precedence",
          "question": "Did the proposed cause occur before the outcome within the available time precision?",
          "failure_action": "mark_temporal_inconsistency_or_undetermined"
        },
        {
          "id": "mechanism",
          "question": "Is there a plausible, testable mechanism connecting the events?",
          "failure_action": "retain_hypothesis_and_record_mechanism_gap"
        },
        {
          "id": "confounding",
          "question": "Could another variable explain both the proposed cause and the outcome?",
          "failure_action": "record_possible_confounders"
        },
        {
          "id": "alternative_explanations",
          "question": "Are other plausible explanations compatible with the evidence?",
          "failure_action": "retain_alternatives"
        },
        {
          "id": "counterfactual",
          "question": "Is there defensible evidence about what would happen if the proposed cause changed?",
          "failure_action": "record_counterfactual_limitations"
        },
        {
          "id": "independent_support",
          "question": "Does the causal claim have evidence beyond repeated copies of the same source?",
          "failure_action": "account_for_source_dependence"
        },
        {
          "id": "causal_direction",
          "question": "Could reverse causation or reciprocal influence explain the relationship?",
          "failure_action": "record_directional_uncertainty"
        }
      ],
      "promotion_policy": {
        "proposed_to_temporally_consistent": "Temporal ordering is compatible with the proposed relationship.",
        "temporally_consistent_to_supported": "Additional relevant evidence supports the causal interpretation and material alternatives have been evaluated.",
        "supported_to_experimentally_supported": "Appropriate experimental evidence supports the relationship within the experiment's scope.",
        "any_status_to_confounded": "Evidence indicates that confounding materially undermines the proposed causal interpretation.",
        "any_status_to_refuted": "Relevant evidence contradicts the proposed causal relationship under the specified conditions.",
        "insufficient_evidence": "Keep the relationship proposed or undetermined."
      },
      "important_limitations": [
        "The status experimentally_supported does not guarantee universal causation.",
        "Counterfactual conclusions depend on assumptions and identification strategy.",
        "A plausible mechanism alone does not prove a causal relationship.",
        "A temporal sequence alone does not prove a causal relationship."
      ]
    },
    "contradiction_engine": {
      "comparison_dimensions": [
        "subject",
        "predicate",
        "object",
        "polarity",
        "quantifier",
        "time_scope",
        "context",
        "setting",
        "measurement_method",
        "source_lineage"
      ],
      "conflict_detection": {
        "logical": "Claims make incompatible assertions about the same proposition and scope.",
        "temporal": "Assertions conflict when evaluated against the same relevant time period.",
        "contextual": "Claims differ because their surrounding conditions differ or are incompletely specified.",
        "measurement": "Measurements differ beyond what their methods or uncertainty can adequately explain.",
        "source": "Sources provide incompatible accounts of the same event or proposition.",
        "scope": "Claims appear incompatible but concern different populations, definitions, or environments."
      },
      "resolution_policy": {
        "automatic_resolution": false,
        "preserve_original_claims": true,
        "preserve_all_material_evidence": true,
        "require_resolution_rationale": true,
        "require_resolution_evidence": true,
        "unresolved_conflict_verdict": "conflicted",
        "non_material_conflict_action": "document_and_continue"
      }
    },
    "temporal_engine": {
      "timestamp_format": "ISO-8601",
      "preserve_timezone": true,
      "store_utc_normalization_when_available": true,
      "distinct_time_fields": [
        "event_time",
        "observed_at",
        "recorded_at",
        "acquired_at",
        "published_at",
        "evaluated_at",
        "valid_from",
        "valid_until"
      ],
      "interval_rules": [
        "Reject an end time earlier than the start time when both refer to the same validated interval.",
        "Do not invent missing timestamps.",
        "Do not impose an event order when the recorded intervals cannot establish one.",
        "Flag incompatible temporal claims for review.",
        "Evaluate source freshness relative to the claim's time scope."
      ],
      "freshness_policy": {
        "enabled": true,
        "default_max_age_seconds": null,
        "max_age_must_be_domain_specific": true,
        "stale_evidence_action": "flag_and_reassess_relevance"
      }
    },
    "uncertainty_engine": {
      "probability_scale": {
        "minimum": 0,
        "maximum": 1,
        "interpretation": "Probability is used only when a proposition and probability model are explicitly defined."
      },
      "default_probability": null,
      "default_confidence": null,
      "calibration_requirements": [
        "Define the proposition being assessed.",
        "Identify the calibration method.",
        "Identify the applicable data or evidence.",
        "Record assumptions and known limitations.",
        "Avoid false precision.",
        "Distinguish probability from evidence quality and verdict status."
      ],
      "uncertainty_categories": {
        "epistemic": "Uncertainty caused by incomplete knowledge or insufficient evidence.",
        "aleatory": "Variability inherent in the modeled process.",
        "measurement": "Uncertainty in measurement instruments, methods, or observations.",
        "semantic": "Ambiguity in wording, definitions, or reference resolution.",
        "temporal": "Uncertainty in event times, durations, or ordering.",
        "causal": "Uncertainty about causal direction, mechanisms, confounding, or counterfactuals.",
        "model": "Uncertainty arising from model assumptions, structure, or limitations.",
        "sampling": "Uncertainty due to incomplete or unrepresentative samples.",
        "source": "Uncertainty about source authenticity, reliability, or provenance."
      },
      "aggregation_policy": {
        "assume_independence": false,
        "allow_unweighted_averaging_of_evidence": false,
        "deduplicate_dependent_sources": true,
        "retain_conflicting_evidence": true,
        "unknown_is_not_zero": true
      }
    },
    "evaluation_pipeline": [
      {
        "step": 1,
        "id": "ingest",
        "action": "Validate incoming payloads and assign stable identifiers.",
        "outputs": ["input_records", "ingestion_audit"]
      },
      {
        "step": 2,
        "id": "register_sources",
        "action": "Register source identities and provenance metadata.",
        "outputs": ["source_records", "provenance_records"]
      },
      {
        "step": 3,
        "id": "normalize_claim",
        "action": "Extract proposition structure and flag ambiguity.",
        "outputs": ["normalized_claims", "ambiguity_records"]
      },
      {
        "step": 4,
        "id": "resolve_reality_context_setting",
        "action": "Establish entities, context, setting, and scope.",
        "outputs": ["reality_records", "context_records", "setting_records"]
      },
      {
        "step": 5,
        "id": "validate_evidence",
        "action": "Evaluate source lineage, relevance, integrity, and dependence.",
        "outputs": ["evidence_graph", "evidence_warnings"]
      },
      {
        "step": 6,
        "id": "validate_time",
        "action": "Check timestamps, temporal scope, and event order.",
        "outputs": ["temporal_assessments", "temporal_warnings"]
      },
      {
        "step": 7,
        "id": "evaluate_claim",
        "action": "Assess supporting evidence, refuting evidence, scope, and missing information.",
        "outputs": ["provisional_assessments"]
      },
      {
        "step": 8,
        "id": "detect_contradictions",
        "action": "Identify logical, temporal, contextual, measurement, source, and scope conflicts.",
        "outputs": ["contradiction_records"]
      },
      {
        "step": 9,
        "id": "construct_causality_symlinks",
        "action": "Create provisional event links and evaluate mechanisms, confounding, and alternatives.",
        "outputs": ["causality_symlinks", "dependency_graph"]
      },
      {
        "step": 10,
        "id": "calibrate_uncertainty",
        "action": "Record uncertainty and calculate probabilities only when justified.",
        "outputs": ["uncertainty_assessments"]
      },
      {
        "step": 11,
        "id": "finalize_assessment",
        "action": "Apply verdict rules and expose unresolved conflicts.",
        "outputs": ["claim_assessments"]
      },
      {
        "step": 12,
        "id": "append_audit",
        "action": "Record the evaluation, references, configuration, and revision relationships.",
        "outputs": ["audit_events", "evaluation_manifest"]
      },
      {
        "step": 13,
        "id": "serialize_response",
        "action": "Validate the final response contract and return the result.",
        "outputs": ["truth_engine_response"]
      }
    ],
    "decision_policy": {
      "supported": {
        "definition": "Relevant evidence supports the proposition within its declared scope.",
        "requirements": [
          "Evidence supports the proposition.",
          "Evidence provenance is available in strict mode.",
          "Material contradictory evidence does not remain unresolved.",
          "The scope and time period are sufficiently clear."
        ]
      },
      "refuted": {
        "definition": "Relevant evidence contradicts the proposition within its declared scope.",
        "requirements": [
          "Evidence is relevant to the exact proposition.",
          "Contradictory evidence is traceable.",
          "The conclusion does not depend solely on missing evidence."
        ]
      },
      "partially_supported": {
        "definition": "Some components of the proposition are supported while others are unsupported or contradicted.",
        "requirements": [
          "The supported portion is identified.",
          "The unsupported or contradicted portion is identified."
        ]
      },
      "conflicted": {
        "definition": "Material supporting and refuting evidence remains unresolved.",
        "requirements": [
          "At least one material conflict is recorded.",
          "The conflict cannot be dismissed as a scope or timing difference."
        ]
      },
      "undetermined": {
        "definition": "Available evidence is insufficient to justify support or refutation.",
        "requirements": [
          "Missing evidence or unresolved uncertainty is documented."
        ]
      },
      "not_applicable": {
        "definition": "The proposition is outside the evaluation scope or cannot meaningfully be evaluated under the configured rules.",
        "requirements": [
          "The reason for non-applicability is recorded."
        ]
      },
      "causal_claim_override": {
        "rule": "A causal claim cannot be marked supported merely because its events are correlated or temporally ordered.",
        "required_checks": [
          "temporal_compatibility",
          "causal_mechanism_or_testable_hypothesis",
          "confounding_assessment",
          "alternative_explanation_assessment",
          "evidence_provenance"
        ]
      },
      "unknown_data_rule": "Missing, ambiguous, or unverified data must not be silently converted into a positive or negative finding."
    },
    "audit_policy": {
      "enabled": true,
      "append_only_log": true,
      "retain_previous_assessments": true,
      "require_revision_reason": true,
      "record_configuration_version": true,
      "record_source_references": true,
      "record_evaluation_timestamp": true,
      "hash_chain": {
        "enabled": true,
        "algorithm": "SHA-256",
        "genesis_hash": null,
        "signing": "optional",
        "note": "Hash-chain verification detects certain changes but does not independently prove the truth or authenticity of recorded content."
      },
      "reproducibility_manifest": {
        "required_fields": [
          "assessment_id",
          "engine_version",
          "configuration_version",
          "evaluation_timestamp",
          "claim_version",
          "evidence_refs",
          "context_ref",
          "setting_ref",
          "evaluation_mode"
        ]
      }
    },
    "security_policy": {
      "external_content_is_untrusted": true,
      "external_content_may_not_override_engine_configuration": true,
      "source_content_and_instructions_are_separate": true,
      "access_control_required_for_sensitive_data": true,
      "data_minimization": true,
      "retention_policy_required": true,
      "secrets_must_not_be_written_to_audit_logs": true,
      "hashes_do_not_replace_authentication": true,
      "human_review_required_for_high_impact_decisions": true
    },
    "validation_rules": [
      {
        "id": "VAL-001",
        "rule": "Every claim has a unique claim_id.",
        "severity": "error"
      },
      {
        "id": "VAL-002",
        "rule": "Every evidence reference resolves to a registered evidence record.",
        "severity": "error"
      },
      {
        "id": "VAL-003",
        "rule": "Every causal link references registered source and target events.",
        "severity": "error"
      },
      {
        "id": "VAL-004",
        "rule": "Every supported assessment in strict mode includes traceable supporting evidence.",
        "severity": "error"
      },
      {
        "id": "VAL-005",
        "rule": "Every unresolved material contradiction is disclosed in the assessment.",
        "severity": "error"
      },
      {
        "id": "VAL-006",
        "rule": "Every revision identifies the prior version or explicitly declares that no prior version exists.",
        "severity": "error"
      },
      {
        "id": "VAL-007",
        "rule": "Probabilities, when present, are numeric values between zero and one and have a defined interpretation.",
        "severity": "error"
      },
      {
        "id": "VAL-008",
        "rule": "Unknown values remain null rather than being replaced with fabricated data.",
        "severity": "error"
      },
      {
        "id": "VAL-009",
        "rule": "Causal links cannot be promoted based only on temporal precedence.",
        "severity": "error"
      },
      {
        "id": "VAL-010",
        "rule": "Timestamp intervals are internally consistent when their boundaries are known.",
        "severity": "error"
      },
      {
        "id": "VAL-011",
        "rule": "Derived evidence records identify their parent evidence when known.",
        "severity": "warning"
      },
      {
        "id": "VAL-012",
        "rule": "Source dependence is evaluated before multiple sources are treated as independent corroboration.",
        "severity": "warning"
      },
      {
        "id": "VAL-013",
        "rule": "Context and setting are represented separately, even when one depends on the other.",
        "severity": "error"
      },
      {
        "id": "VAL-014",
        "rule": "A specification-only operation must not be reported as a completed real-world verification.",
        "severity": "error"
      }
    ],
    "output_contract": {
      "request_id": "string",
      "engine_version": "string",
      "evaluation_status": "completed|partial|failed",
      "claim": {},
      "result": {
        "verdict": "unassessed|supported|refuted|partially_supported|conflicted|undetermined|not_applicable",
        "rationale": "string",
        "scope": {
          "reality_ref": "string or null",
          "context_ref": "string or null",
          "setting_ref": "string or null",
          "time_scope": {}
        },
        "supporting_evidence_refs": [],
        "refuting_evidence_refs": [],
        "missing_evidence": [],
        "contradictions": [],
        "causality_symlinks": [],
        "uncertainty": {},
        "limitations": []
      },
      "audit": {
        "assessment_id": "string",
        "evaluated_at": "ISO-8601 string",
        "configuration_version": "string",
        "source_refs": [],
        "previous_assessment_id": "string or null",
        "revision_reason": "string or null"
      }
    },
    "reference_workflow": {
      "description": "Illustrative daily occurrence workflow. All records below are examples, not verified real-world events.",
      "context": {
        "context_id": "ctx-commute-001",
        "description": "A commute to work using a scheduled bus.",
        "conditions": [
          {
            "condition": "The person intends to catch a specific bus.",
            "status": "assumed"
          }
        ],
        "assumptions": [
          "The planned departure time is accurate."
        ],
        "unknowns": [
          "Actual bus arrival time.",
          "Actual time the person reached the bus stop."
        ],
        "version": 1
      },
      "setting": {
        "setting_id": "setting-commute-001",
        "setting_type": "physical",
        "description": "The route between home, the bus stop, and the workplace.",
        "environment": {
          "transport_mode": "bus"
        },
        "applicable_rules": [
          {
            "rule": "The bus follows a published schedule.",
            "verification_status": "unverified"
          }
        ],
        "valid_from": null,
        "valid_until": null,
        "scope_limitations": [
          "Actual service conditions are not established."
        ],
        "version": 1
      },
      "events": [
        {
          "event_id": "evt-commute-001",
          "description": "The person leaves home later than planned.",
          "event_time": {
            "start": null,
            "end": null,
            "precision": "unknown"
          },
          "epistemic_role": "hypothesis",
          "evidence_refs": []
        },
        {
          "event_id": "evt-commute-002",
          "description": "The person misses the intended bus.",
          "event_time": {
            "start": null,
            "end": null,
            "precision": "unknown"
          },
          "epistemic_role": "reported_fact",
          "evidence_refs": []
        },
        {
          "event_id": "evt-commute-003",
          "description": "The person arrives late at work.",
          "event_time": {
            "start": null,
            "end": null,
            "precision": "unknown"
          },
          "epistemic_role": "reported_fact",
          "evidence_refs": []
        }
      ],
      "causality_symlinks": [
        {
          "link_id": "link-commute-001",
          "source_event_id": "evt-commute-001",
          "target_event_id": "evt-commute-002",
          "link_type": "contributes_to",
          "causal_status": "proposed",
          "mechanism": "A later departure may reduce the time available to reach the bus stop.",
          "evidence_refs": [],
          "alternative_explanations": [
            "The bus arrived earlier than expected.",
            "Travel time to the stop was longer than expected.",
            "The departure time was recorded incorrectly."
          ],
          "confounders": [
            "Unexpected travel conditions."
          ],
          "counterfactual_basis": null,
          "time_order_verified": false,
          "confidence": null,
          "confidence_method": null,
          "context_ref": "ctx-commute-001",
          "setting_ref": "setting-commute-001",
          "created_at": null,
          "reviewed_at": null,
          "version": 1,
          "supersedes": null
        },
        {
          "link_id": "link-commute-002",
          "source_event_id": "evt-commute-002",
          "target_event_id": "evt-commute-003",
          "link_type": "contributes_to",
          "causal_status": "proposed",
          "mechanism": "Missing the intended bus may delay arrival at work.",
          "evidence_refs": [],
          "alternative_explanations": [
            "A later bus was also delayed.",
            "Another transport disruption occurred.",
            "The workplace arrival time was recorded incorrectly."
          ],
          "confounders": [],
          "counterfactual_basis": null,
          "time_order_verified": false,
          "confidence": null,
          "confidence_method": null,
          "context_ref": "ctx-commute-001",
          "setting_ref": "setting-commute-001",
          "created_at": null,
          "reviewed_at": null,
          "version": 1,
          "supersedes": null
        }
      ],
      "expected_assessment": {
        "verdict": "undetermined",
        "rationale": "The proposed chain is plausible, but event times, source evidence, and alternative explanations have not been verified.",
        "supporting_evidence_refs": [],
        "refuting_evidence_refs": [],
        "missing_evidence": [
          "Reliable departure time.",
          "Scheduled and actual bus times.",
          "Verified arrival time at work."
        ],
        "causal_conclusion": "not_established"
      }
    },
    "implementation_acceptance_tests": [
      {
        "test_id": "TEST-001",
        "name": "Separate observation from inference",
        "input_condition": "A user reports that an event occurred but supplies no corroborating evidence.",
        "expected": "Record the report and its source without automatically treating it as independently verified."
      },
      {
        "test_id": "TEST-002",
        "name": "Preserve unknown information",
        "input_condition": "An event has no reliable timestamp.",
        "expected": "Retain an unknown time and avoid inventing event order."
      },
      {
        "test_id": "TEST-003",
        "name": "Reject correlation-only causation",
        "input_condition": "Two events correlate but no causal identification is available.",
        "expected": "Represent correlation without marking causation as established."
      },
      {
        "test_id": "TEST-004",
        "name": "Retain contradictory sources",
        "input_condition": "Two relevant sources provide incompatible accounts.",
        "expected": "Create a contradiction record and preserve both sources."
      },
      {
        "test_id": "TEST-005",
        "name": "Detect dependent evidence",
        "input_condition": "Multiple reports repeat the same original source.",
        "expected": "Record shared provenance and avoid treating every repetition as independent corroboration."
      },
      {
        "test_id": "TEST-006",
        "name": "Preserve revision history",
        "input_condition": "A claim assessment changes after new evidence arrives.",
        "expected": "Create a new assessment version and preserve the prior assessment."
      },
      {
        "test_id": "TEST-007",
        "name": "Separate context and setting",
        "input_condition": "A claim includes situational circumstances and an environmental rule.",
        "expected": "Store contextual conditions separately from the setting and its rules."
      },
      {
        "test_id": "TEST-008",
        "name": "Avoid unsupported probability",
        "input_condition": "Evidence is incomplete and no calibration method is available.",
        "expected": "Return null for the numerical probability and explain the uncertainty."
      },
      {
        "test_id": "TEST-009",
        "name": "Flag invalid causal cycles",
        "input_condition": "A directed causal graph contains a cycle without feedback-loop semantics.",
        "expected": "Flag the cycle for review without silently deleting links."
      },
      {
        "test_id": "TEST-010",
        "name": "Validate output",
        "input_condition": "A final assessment omits required identifiers or contains invalid enum values.",
        "expected": "Reject the response or return a structured validation error."
      }
    ],
    "deployment_requirements": {
      "required_for_production": [
        "JSON Schema validation for input and output contracts.",
        "Persistent storage for claims, evidence, graph edges, and audit events.",
        "Stable identifier generation.",
        "Authentication and authorization.",
        "Append-only audit storage or equivalent revision controls.",
        "Timestamp normalization and timezone-aware comparison.",
        "Graph integrity checks.",
        "Automated acceptance tests.",
        "Error handling and operational monitoring.",
        "Data retention and deletion policies compatible with audit obligations."
      ],
      "optional_extensions": [
        "Graph database backend.",
        "Vector search for semantic retrieval.",
        "Bayesian inference for appropriately specified probabilistic models.",
        "Causal inference methods for suitable observational or experimental data.",
        "Digital signatures for audit records.",
        "Human review and adjudication workflow.",
        "Event streaming for real-time occurrence capture.",
        "External source verification adapters."
      ],
      "implementation_status": {
        "architecture_defined": true,
        "data_contracts_defined": true,
        "decision_policies_defined": true,
        "acceptance_tests_defined": true,
        "runtime_implemented": false,
        "json_schema_compiled": false,
        "persistent_storage_configured": false,
        "external_sources_connected": false,
        "tests_executed": false
      }
    }
  }
}
```
