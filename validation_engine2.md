
OBJECTIVE
  Adapt the Truth Engine from general truth evaluation into a practical system
  for understanding ordinary daily occurrences, identifying plausible causes,
  connecting related events, and updating conclusions as new evidence arrives.

CORE IDEA
  Every occurrence becomes a traceable event.
  Every proposed cause becomes a testable relationship.
  Every relationship becomes a typed CAUSALITY_SYMLINK.
  Every conclusion remains bounded by evidence, context, and setting.

  EVENT -> OBSERVATION -> CONTEXT -> CANDIDATE CAUSE
        -> CAUSALITY_SYMLINK -> EVIDENCE CHECK
        -> UPDATED UNDERSTANDING

PRIMARY RULE
  An event occurring before another event does not, by itself, establish
  causation. The engine must distinguish observed sequence, correlation,
  plausible mechanism, supported causation, and unresolved explanation.


===============================================================================
01 :: DAILY OCCURRENCE MODEL
===============================================================================

  Treat ordinary life as a stream of observable events and reported experiences.

  EVENT CATEGORIES
    1. Physical events
        Movement, weather, objects, transportation, equipment, surroundings.

    2. Personal actions
        Decisions, routines, tasks, habits, omissions, interventions.

    3. Social events
        Conversations, requests, responses, agreements, disagreements.

    4. Environmental events
        Noise, temperature, traffic, lighting, interruptions, resource changes.

    5. Cognitive events
        Expectations, interpretations, recollections, plans, decisions.

    6. Operational events
        Deadlines, errors, notifications, service interruptions, system changes.

    7. Outcomes
        Delays, completed tasks, missed opportunities, unexpected results.

    8. Unknown or disputed events
        Occurrences reported by others, ambiguous observations, incomplete
        records, or events whose details have not been independently checked.

  DAILY EVENT RECORD
    event_id
    event_time
    recorded_time
    event_description
    event_type
    observer_or_source
    directly_observed_facts[]
    reported_information[]
    interpretation[]
    immediate_outcome
    environmental_conditions[]
    context_id
    setting_id
    evidence_refs[]
    unresolved_details[]

  INTEGRITY RULE
    Store what happened separately from what someone believes it means.

  EXAMPLE
    OBSERVATION:
      "The meeting started 15 minutes late."

    INTERPRETATION:
      "The organizer does not respect my time."

    CAUSAL HYPOTHESIS:
      "The meeting started late because the preceding meeting ran over."

    These are three different records, not three interchangeable facts.


===============================================================================
02 :: THE CAUSALITY-SYMLINK MODEL
===============================================================================

  DEFINITION
    A CAUSALITY_SYMLINK is a persistent, typed reference connecting two or more
    event records through an explicitly evaluated causal hypothesis.

    It behaves like a symbolic link in the knowledge graph:
      - It references existing event records.
      - It preserves source and evidence provenance.
      - It records the proposed mechanism.
      - It exposes assumptions and alternatives.
      - It can be strengthened, weakened, invalidated, or superseded.
      - It never makes the causal claim true merely by existing.

  BASIC STRUCTURE

    [EVENT A: Possible Cause]
             |
             | CAUSALITY_SYMLINK
             | type = CAUSED
             | evidence = E1, E2
             | mechanism = M1
             | alternatives = A1, A2
             | status = PLAUSIBLE
             v
    [EVENT B: Observed Outcome]

  LINK TYPES
    CAUSED_BY
      Evidence supports a causal contribution from one event to another.

    CONTRIBUTED_TO
      An event was one contributing factor among several.

    ENABLED
      An event made another event possible but was not necessarily sufficient.

    PREVENTED
      An action or condition helped avert an outcome.

    TRIGGERED
      An event initiated a process or transition.

    MEDIATED_BY
      An effect appears to operate through an intermediate event.

    MODERATED_BY
      A condition changes the strength or direction of a proposed effect.

    CORRELATED_WITH
      Events vary together, but causality has not been established.

    PRECEDED
      One event happened earlier than another; no causal claim is implied.

    CONFLICTS_WITH
      Two observations or claims are inconsistent under the same conditions.

    EXPLAINS_PARTIALLY
      A proposed cause accounts for some, but not all, of an outcome.

    UNKNOWN_RELATION
      A relationship is suspected but has not been classified adequately.

  LINK SCHEMA

    causality_symlink {
      link_id
      source_event_ids[]
      target_event_ids[]
      relation_type

      proposed_mechanism
      necessary_conditions[]
      contributing_conditions[]
      assumptions[]
      supporting_evidence_refs[]
      opposing_evidence_refs[]
      alternative_explanations[]

      causal_status
      confidence_basis
      scope_conditions[]
      valid_time_interval
      reviewer_or_method
      created_at
      last_evaluated_at
      revision_history[]
    }

  GRAPH RULE
    A symlink can connect an event to an earlier event, a recurring condition,
    an intermediate mechanism, or a group of contributing causes.

    Multi-cause representation:

      [Cause A] ----\
      [Cause B] -----+--> [Intermediate Event] --> [Outcome]
      [Condition C] -/

    Do not force a single-cause explanation when multiple contributors are
    plausible or when evidence cannot distinguish among them.


===============================================================================
03 :: EVERYDAY CAUSALITY PIPELINE
===============================================================================

  INPUT
    A daily occurrence, observation, report, or question.

      |
      v

  STEP 1 :: CAPTURE
    Record the occurrence without inserting a causal explanation.

      |
      v

  STEP 2 :: NORMALIZE
    Identify who or what was involved, what changed, and when.

      |
      v

  STEP 3 :: GROUND IN CONTEXT
    Establish relevant history, expectations, surrounding events, and
    information sources.

      |
      v

  STEP 4 :: DEFINE SETTING
    Specify the environment, constraints, applicable rules, and time window.

      |
      v

  STEP 5 :: GENERATE CANDIDATE CAUSES
    Identify plausible causes and contributing conditions.
    Label them as hypotheses, not findings.

      |
      v

  STEP 6 :: CREATE CAUSALITY-SYMLINKS
    Connect the relevant event records using typed relationships.

      |
      v

  STEP 7 :: TEST EACH LINK
    Check time ordering, mechanism, evidence, alternatives, and confounders.

      |
      v

  STEP 8 :: UPDATE THE GRAPH
    Promote, weaken, reject, or leave each relationship unresolved.

      |
      v

  STEP 9 :: REPORT
    State what is observed, what is supported, what remains uncertain,
    and what additional observation could change the assessment.

  CONTINUOUS LOOP
    New occurrence -> new event node -> new or revised symlink -> re-evaluation.


===============================================================================
04 :: CAUSALITY VALIDATION RULES
===============================================================================

  Each candidate link is evaluated against the following checks.

  C1. TEMPORAL ORDER
      Did the proposed cause precede the effect, or otherwise operate through
      a known causal process?

  C2. MECHANISM
      Is there a plausible, domain-appropriate explanation of how the cause
      could produce the observed effect?

  C3. EVIDENCE
      What observations, records, experiments, or reliable reports support
      the proposed relationship?

  C4. ALTERNATIVES
      Could another event or condition explain the same outcome?

  C5. CONFOUNDERS
      Could a third factor influence both the proposed cause and the outcome?

  C6. BASELINE
      Does the outcome occur when the proposed cause is absent?

  C7. REPEATABILITY
      Does the relationship recur under comparable conditions?

  C8. INTERVENTION
      Does deliberately changing the proposed cause change the outcome?
      Apply only when appropriate, ethical, safe, and feasible.

  C9. SCOPE
      Under which conditions does the relationship hold, and where might
      it fail?

  C10. REVISION
       What new evidence would weaken, strengthen, or overturn the link?

  IMPORTANT
    Repeated observation can strengthen a hypothesis, but recurring events
    can still share hidden causes. Intervention evidence also requires care:
    an apparent change after an action may result from another simultaneous
    change rather than from the action itself.
```

```
===============================================================================
05 :: CAUSAL STATUS MACHINE
===============================================================================

  LINK STATUS ENUMERATION

    OBSERVED_SEQUENCE
      The source event preceded the target event.

    HYPOTHESIZED
      A possible causal relationship has been proposed.

    PLAUSIBLE
      A reasonable mechanism exists, but direct supporting evidence is limited.

    PARTIALLY_SUPPORTED
      Some evidence supports the relationship, but important gaps remain.

    SUPPORTED
      Multiple relevant observations or credible evidence support the
      relationship within the specified conditions.

    STRONGLY_SUPPORTED
      Converging evidence, appropriate methods, and alternatives analysis
      provide strong support for the bounded causal claim.

    INTERVENTION_SUPPORTED
      Appropriate intervention evidence supports a causal interpretation.

    DISPUTED
      Credible evidence supports materially different explanations.

    UNRESOLVED
      Available evidence is insufficient to determine the relationship.

    REJECTED
      Evidence contradicts the proposed relationship under the tested
      conditions or demonstrates that its assumptions were invalid.

    EXPIRED
      The relationship may no longer apply because the underlying conditions
      or setting have materially changed.

  PROMOTION RULE
    Move a link to a stronger status only when new evidence justifies doing so.

  DEMOTION RULE
    Reduce the status when evidence weakens, assumptions fail, or new
    information provides a better explanation.

  NO AUTOMATIC CERTAINTY
    The status describes the support available for a causal claim.
    It is not a guarantee that the system has discovered the ultimate cause.


===============================================================================
06 :: REAL-WORLD EXAMPLE A -- MISSED BUS
===============================================================================

  DAILY OCCURRENCE
    The bus departed before the person reached the stop.

  EVENT NODES

    E001: Person left home at 08:05.
    E002: Bus departed at 08:10.
    E003: Person arrived at the stop at 08:12.
    E004: Person missed the bus.

  OBSERVED RELATIONSHIPS

    E001 --PRECEDED--> E003
    E002 --PRECEDED--> E003
    E003 --CONTRIBUTED_TO--> E004

  CANDIDATE CAUSALITY-SYMLINKS

    CS001:
      source = E003
      target = E004
      relation = CONTRIBUTED_TO
      status = SUPPORTED

      Basis:
        Arrival occurred after the bus departed, assuming the identified
        bus was the intended service and the timestamps are reliable.

    CS002:
      source = E001
      target = E004
      relation = CONTRIBUTED_TO
      status = PLAUSIBLE

      Basis:
        Leaving earlier may have prevented the missed bus, but travel time,
        the schedule, and other possible delays need to be checked.

    CS003:
      source = BUS_SCHEDULE
      target = E004
      relation = UNKNOWN_RELATION
      status = UNRESOLVED

      Basis:
        The timetable may have differed from expectations. Actual departure
        information is needed before attributing fault to the schedule.

  ADDITIONAL CHECKS
    - Was the bus early, on time, or delayed?
    - Was the correct stop used?
    - Did traffic or a route change affect arrival?
    - Was the departure timestamp reliable?

  RESULT
    The immediate timing mismatch is established by the example's records.
    The deeper explanation for why the person arrived late requires further
    evidence.

  CAUSALITY-SYMLINK:
    Earlier departure time
      -> potentially earlier arrival
      -> potentially successful boarding

  COUNTERFACTUAL TEST
    "Would arriving at the stop before the actual departure have prevented
    this specific missed bus?"

  A positive answer is likely under ordinary boarding conditions, but
  confirmation still depends on the actual event details.


===============================================================================
07 :: REAL-WORLD EXAMPLE B -- UNANSWERED MESSAGE
===============================================================================

  DAILY OCCURRENCE
    A person sends a message and receives no reply for several hours.

  EVENT NODES

    E101: Message sent at 10:00.
    E102: No reply observed by 14:00.
    E103: Sender interprets the silence as intentional avoidance.

  SEPARATION OF KNOWLEDGE

    OBSERVED:
      The message was sent.
      No reply had been observed by the stated time.

    NOT ESTABLISHED:
      The recipient saw the message.
      The recipient was available to respond.
      The recipient intentionally ignored the message.
      The recipient's motive or emotional state.

  CANDIDATE LINKS

    CS101:
      E101 --PRECEDED--> E102
      status = OBSERVED_SEQUENCE

    CS102:
      "Recipient intentionally ignored the message"
        --CAUSED_BY--> E102
      status = UNRESOLVED

      Problem:
        Intent is not observable from silence alone.

    CS103:
      "Recipient was unavailable"
        --CONTRIBUTED_TO--> E102
      status = HYPOTHESIZED

      Possible explanations:
        - The recipient has not seen the message.
        - The recipient is occupied.
        - A technical issue prevented delivery.
        - The recipient needs time to respond.
        - The recipient chose not to respond.

  RESULT
    The lack of a reply is an observation.
    Intentional avoidance is one possible interpretation, not an established
    fact.

  UPDATE RULE
    If later evidence establishes that the message was delivered and seen,
    update the event graph accordingly. Do not automatically infer motive.

  PURPOSE
    Prevent the Truth Engine from turning uncertainty about other people's
    internal states into false certainty.


===============================================================================
08 :: REAL-WORLD EXAMPLE C -- REPEATEDLY LOW-PRODUCTIVITY MORNINGS
===============================================================================

  RECURRING OBSERVATION
    On several mornings, a person starts work later than planned.

  CANDIDATE EVENT NODES

    E201: Bedtime later than intended.
    E202: Wake-up later than intended.
    E203: Morning task begins late.
    E204: Work completion is lower than the person's target.

  INITIAL GRAPH

    [Late Bedtime] ---------?
                               \
                                > [Late Task Start] ---> [Reduced Output]
                               /
    [Late Wake-Up] ----------?

    [Notifications] ----------?
    [Unplanned Tasks] --------?
    [Task Difficulty] --------?

  POSSIBLE SYMLINKS

    CS201:
      Late bedtime
        -> late wake-up
      Status = HYPOTHESIZED

    CS202:
      Late wake-up
        -> late task start
      Status = PLAUSIBLE

    CS203:
      Late task start
        -> reduced output
      Status = PLAUSIBLE

    CS204:
      Unplanned tasks
        -> reduced output
      Status = HYPOTHESIZED

  DATA TO COLLECT
    - Intended and actual wake-up times.
    - Intended and actual task start times.
    - Planned versus unplanned workload.
    - Task completion and interruption records.
    - Relevant changes in the daily routine.

  TEST
    Compare days with similar workloads and differing wake-up or start times.

  INTERPRETATION
    If earlier starts consistently predict more completed work, this supports
    an association. Stronger causal conclusions require ruling out plausible
    differences in workload, sleep, difficulty, and other relevant conditions.

  ACTION
    Change one manageable factor when practical and observe the result.

  FEEDBACK LINK
    [Earlier Start Intervention]
            |
            v
      [Actual Start Time]
            |
            v
      [Task Completion]
            |
            v
      [Updated Causal Model]

  SAFEGUARD
    Do not interpret a single productive day as proof of a general rule.


===============================================================================
09 :: CAUSAL GRAPH GOVERNANCE
===============================================================================

  9.1 DIRECTED LINKS

      A --CAUSES--> B

      Direction matters. If A precedes B, that does not imply B caused A.
      Record causal direction separately from chronology.

  9.2 MULTIPLE CAUSES

      A ----\
      B -----+----> C
      D ----/

      An outcome may require several contributing factors. A single link
      should not erase the others.

  9.3 MEDIATION

      A ---> M ---> B

      A may affect B through intermediate event M.

      Example:
        A = Unexpected interruption
        M = Lost task focus
        B = Delayed task completion

      Each connection needs its own evidence and evaluation.

  9.4 CONFOUNDING

          U
         / \
        v   v
        A   B

      An unobserved or unrecorded condition U may influence both A and B.

      Example:
        A = Less sleep
        B = Reduced task performance
        U = Another condition affecting both sleep and performance

      If U is not considered, the engine may exaggerate the relationship
      between A and B.

  9.5 FEEDBACK LOOPS

      A --> B --> C --> A

      Genuine feedback loops are permitted, but event instances must be
      time-indexed so the graph does not create a circular explanation
      of a single event.

      Example:
        Day 1: Poor planning -> missed deadline
        Day 2: Missed deadline -> more urgent workload
        Day 3: Urgent workload -> less time for planning

      These are connected events across time, not a claim that every event
      simultaneously caused itself.

  9.6 DUPLICATE AND STALE LINKS

      - Deduplicate links representing the same proposition and event scope.
      - Retain multiple sources of evidence.
      - Mark invalidated links instead of deleting audit history.
      - Reevaluate links when their environmental conditions change.
      - Do not reuse an old relationship in a materially different setting.


===============================================================================
10 :: DAILY TRUTH LEDGER
===============================================================================

  A lightweight daily interface makes the framework usable without requiring
  formal analysis of every routine event.

  DAILY ENTRY

    DATE:
    OCCURRENCE:
    DIRECTLY OBSERVED:
    REPORTED BY OTHERS:
    MY INTERPRETATION:
    KNOWN CONTEXT:
    RELEVANT SETTING:
    POSSIBLE CAUSES:
    EVIDENCE FOR EACH CAUSE:
    EVIDENCE AGAINST EACH CAUSE:
    ALTERNATIVE EXPLANATIONS:
    RESULTING CAUSALITY-SYMLINKS:
    CURRENT CONCLUSION:
    WHAT WOULD CHANGE MY VIEW:
    FOLLOW-UP OBSERVATION:

  DAILY REVIEW

    1. Which occurrences are established?
    2. Which conclusions are interpretations rather than observations?
    3. Which causal links gained evidence today?
    4. Which links remain speculative?
    5. Which explanation best fits the available evidence?
    6. What important alternatives have not been checked?
    7. What should be observed next?

  PRACTICAL LIMIT
    Capture selectively. Focus on recurring issues, important decisions,
    surprising outcomes, conflicting accounts, and patterns with practical
    consequences. Avoid creating a burdensome record of every minor event.


===============================================================================
11 :: IMPLEMENTATION LOGIC
===============================================================================

  FUNCTION process_occurrence(occurrence):

      event = normalize_occurrence(occurrence)

      event.observation_status = classify_observation_source(event)
      event.context = resolve_relevant_context(event)
      event.setting = resolve_relevant_setting(event)

      store_event(event)

      candidates = generate_candidate_explanations(event)

      FOR EACH candidate IN candidates:

          source_events = identify_relevant_prior_events(candidate)
          link = create_causality_symlink(
              source_events = source_events,
              target_event = event,
              proposed_mechanism = candidate.mechanism,
              relation_type = candidate.relation_type
          )

          link.temporal_check = evaluate_temporal_order(link)
          link.mechanism_check = evaluate_mechanism(link)
          link.evidence_check = evaluate_support_and_opposition(link)
          link.alternative_check = evaluate_alternatives(link)
          link.confounder_check = evaluate_possible_confounders(link)
          link.scope_check = evaluate_conditions_of_validity(link)

          link.status = assign_evidence_bounded_status(link)

          store_link(link)

      result = summarize(
          observed_facts = event.observations,
          supported_links = current_supported_links(event),
          unresolved_links = current_unresolved_links(event),
          alternative_explanations = relevant_alternatives(event),
          missing_information = identify_evidence_gaps(event)
      )

      store_audit_record(event, result)

      RETURN result

  IMPLEMENTATION CONSTRAINTS
    - Candidate generation creates hypotheses, not facts.
    - Stored links must retain provenance and evaluation history.
    - A causal status must be traceable to supporting checks.
    - Missing evidence must not be treated as evidence of absence.
    - User observations, external reports, and system inferences remain distinct.
    - The process must be able to return "unknown" without forcing a conclusion.


===============================================================================
12 :: FINAL ARCHITECTURAL INTEGRATION
===============================================================================

  TRUTH ENGINE
  |
  +-- REALITY LAYER
  |     Stores observable events, entities, states, and outcomes.
  |
  +-- CONTEXT LAYER
  |     Establishes meaning, background, assumptions, and source provenance.
  |
  +-- SETTING LAYER
  |     Establishes conditions, boundaries, and applicable rules.
  |
  +-- DAILY OCCURRENCE ENGINE
  |     Captures and normalizes real-world events.
  |
  +-- CAUSALITY-SYMLINK ENGINE
  |     Connects events through typed, revisable causal hypotheses.
  |
  +-- EVIDENCE ENGINE
  |     Tests links against observations, records, alternatives, and mechanisms.
  |
  +-- TEMPORAL ENGINE
  |     Tracks recurrence, time boundaries, changed conditions, and history.
  |
  +-- CALIBRATION ENGINE
  |     Separates well-supported explanations from plausible or unknown ones.
  |
  +-- AUDIT ENGINE
        Records why each conclusion was reached and what could change it.

  FINAL RESULT

    A continuously updated model of everyday events in which:

      OCCURRENCE = What happened.
      CONTEXT    = What helps interpret it.
      SETTING    = The conditions under which it happened.
      CAUSE      = A relationship supported to some defined degree.
      SYMLINK    = The traceable connection between event records.
      TRUTH      = The best evidence-grounded assessment within scope.
      REVISION   = The update made when material evidence changes.

  DESIGN PRINCIPLE

    Connect events freely.
    Infer causes cautiously.
    Preserve uncertainty explicitly.
    Update relationships when evidence changes.
    Never confuse a connected narrative with a demonstrated causal chain.

===============================================================================
END :: DAILY TRUTH ENGINE + CAUSALITY-SYMLINKS
===============================================================================
