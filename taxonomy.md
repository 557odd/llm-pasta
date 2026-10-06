# Master Taxonomy: **I / i**

This decomposition treats **“I” as an ambiguous sign family**, not as a single concept. It covers the character, glyph, sound, word, numeral, variable, symbol, abbreviation, identifier, cultural sign, and domain-specific notation, while preserving context as the authority that determines meaning.

The scope is **maximally broad but necessarily open-ended**. Private codes, newly coined abbreviations, specialized local conventions, and arbitrary variables cannot be exhaustively enumerated without a bounded corpus.

---

## 0. Root Entity

```text
I
├── Sign
├── Character
├── Glyph
├── Grapheme
├── Letter
├── Sound representation
├── Word
├── Pronoun
├── Noun
├── Numeral
├── Mathematical object
├── Scientific symbol
├── Technical identifier
├── Abbreviation
├── Initial
├── Label
├── Code
├── Index
├── Cultural symbol
└── Context-dependent token
```

---

# 1. Identifier Set

## 1.1 Canonical identifiers

```text
I-000      Root concept: I
I-CHR      Encoded character
I-GLY      Visual glyph
I-GRA      Grapheme
I-LET      Alphabetic letter
I-PHO      Phonetic value
I-LEX      Lexical item
I-GRM      Grammatical item
I-NUM      Numeral
I-MAT      Mathematical notation
I-LOG      Logical notation
I-STA      Statistical notation
I-PHY      Physical quantity
I-ENG      Engineering notation
I-CHE      Chemical notation
I-BIO      Biological notation
I-MED      Medical notation
I-COM      Computing notation
I-INF      Information-system notation
I-LIN      Linguistic notation
I-MUS      Musical notation
I-PHI      Philosophical concept
I-PSY      Psychological concept
I-SOC      Social or identity concept
I-REL      Religious notation
I-LEG      Legal notation
I-GOV      Governmental notation
I-EDU      Educational notation
I-TRN      Transportation notation
I-GEO      Geographic notation
I-ORG      Organizational notation
I-BRD      Brand or product notation
I-CUL      Cultural symbol
I-IDN      Arbitrary identifier
I-MET      Metadata object
I-VAL      Validation record
```

## 1.2 Identifier construction rule

```text
I-{DOMAIN}-{CLASS}-{CONTEXT}-{VARIANT}-{INSTANCE}
```

Example:

```text
I-LET-LAT-UPPER-BASIC-001
I-GRM-ENG-PRON-SUBJ-001
I-NUM-ROM-CARDINAL-ONE-001
I-MAT-CPLX-IMAGINARY-UNIT-001
I-PHY-ELEC-CURRENT-GENERAL-001
I-CHE-ELEMENT-IODINE-SYMBOL-001
I-COM-LOOP-INDEX-LOCAL-001
```

## 1.3 Identifier record schema

```text
identifier
canonical_form
display_form
normalized_form
domain
subdomain
semantic_type
syntactic_type
case
script
language
encoding
pronunciation
definition
scope
context
source
authority
valid_from
valid_to
status
parent_identifier
related_identifiers
confusable_identifiers
constraints
examples
confidence
version
```

---

# 2. Character and Encoding Classification

## 2.1 Latin uppercase I

```text
I-CHR-001
├── Character: I
├── Unicode name: LATIN CAPITAL LETTER I
├── Code point: U+0049
├── Decimal value: 73
├── Block: Basic Latin
├── Script: Latin
├── General category: Uppercase Letter
├── Bidirectional class: Left-to-right
├── Combining class: 0
├── UTF-8: 49 hexadecimal
├── UTF-16: 0049 hexadecimal
├── UTF-32: 00000049 hexadecimal
└── Lowercase mapping: U+0069
```

These encoding properties distinguish the ordinary Latin letter from visually similar symbols such as digit one, lowercase L, Greek capital iota, and the dedicated Roman numeral character. 
## 2.2 Latin lowercase i

```text
I-CHR-002
├── Character: i
├── Unicode name: LATIN SMALL LETTER I
├── Code point: U+0069
├── Case: lowercase
├── Typical feature: dot or tittle
└── Uppercase mapping: I
```

## 2.3 Related encoded forms

```text
I-CHR-VAR
├── Accented forms
│   ├── Ì
│   ├── Í
│   ├── Î
│   ├── Ï
│   ├── Ĩ
│   ├── Ī
│   ├── Ĭ
│   ├── Į
│   ├── Ǐ
│   ├── Ȉ
│   ├── Ȋ
│   ├── Ḭ
│   ├── Ỉ
│   └── Ị
├── Dotted and dotless forms
│   ├── İ
│   ├── i
│   ├── I
│   └── ı
├── Ligature forms
│   ├── Ĳ
│   └── ĳ
├── Presentation forms
│   ├── Ｉ
│   ├── Ⓘ
│   └── parenthesized or squared forms
├── Mathematical alphanumeric forms
│   ├── bold
│   ├── italic
│   ├── bold italic
│   ├── script
│   ├── Fraktur
│   ├── double-struck
│   ├── sans-serif
│   └── monospace
├── Modifier forms
│   └── ᴵ
└── Roman-numeral form
    └── Ⅰ
```

Unicode assigns independent characters to many stylistic, linguistic, mathematical, and numeral forms that must not automatically be treated as interchangeable with U+0049. 
## 2.4 Confusable characters

```text
I-CONF
├── I    Latin capital I
├── l    Latin small L
├── 1    Digit one
├── |    Vertical line
├── Ι    Greek capital iota
├── І    Cyrillic capital I
├── Ӏ    Cyrillic palochka
├── Ⅰ    Roman numeral one
├── Ｉ   Fullwidth Latin capital I
├── ɪ    Latin small capital I
└── ᛁ    Runic character
```

In some sans-serif typefaces, uppercase `I`, lowercase `l`, digit `1`, and the vertical bar can be difficult to distinguish. 
## 2.5 Structural properties

```text
Structure
├── Length
│   ├── One Unicode code point
│   ├── One grapheme cluster in the basic form
│   └── Multiple code points when combined with marks
├── Character distribution
│   ├── Alphabetic
│   ├── Uppercase or lowercase
│   ├── Word-initial
│   ├── Word-medial
│   ├── Word-final
│   └── Standalone
├── Font realization
│   ├── Serif
│   ├── Sans serif
│   ├── Monospace
│   ├── Script
│   ├── Blackletter
│   └── Handwritten
└── Rendering variables
    ├── Stroke width
    ├── Serifs
    ├── Crossbars
    ├── Dot presence
    ├── Slant
    ├── Weight
    ├── Width
    └── Baseline alignment
```

---

# 3. Alphabetic Classification

## 3.1 Latin-alphabet role

```text
I-LET-LAT
├── Position: ninth
├── Case pair: I/i
├── Broad class: letter
├── Traditional English class: vowel letter
├── Possible functions
│   ├── Vowel representation
│   ├── Semivowel representation
│   ├── Consonantal historical use
│   ├── Digraph component
│   └── Diacritic-bearing base
└── Alphabetic neighbors
    ├── Predecessor: H
    └── Successor: J
```

`I/i` is the ninth letter of the English alphabet; the symbol also has uses as a Roman numeral and as a standalone pronoun. 
## 3.2 Historical lineage

```text
Proto-source traditions
└── Phoenician yodh
    └── Greek iota
        └── Etruscan or Old Italic adoption
            └── Latin I
                ├── Modern I/i
                └── Historical differentiation of J/j
```

The Latin letter traces through Greek iota to Phoenician yodh, while `J` developed historically as a graphic variation of `I`. 
## 3.3 Orthographic processes

```text
I-ORTH
├── Capitalization
├── Lowercasing
├── Diacritic addition
├── Dot removal
├── Dot retention
├── Case folding
├── Transliteration
├── Romanization
├── Normalization
├── Ligature formation
├── Hyphenation behavior
├── Sorting behavior
├── Search equivalence
└── Locale-sensitive mapping
```

## 3.4 Language-specific branches

```text
Language use
├── English
├── Romance languages
├── Germanic languages
├── Slavic languages using Latin script
├── Uralic languages
├── Turkic languages
│   ├── Dotted İ/i
│   └── Dotless I/ı
├── Vietnamese
├── African Latin orthographies
├── Indigenous-language orthographies
├── Transliteration systems
└── Constructed languages
```

---

# 4. Phonetics and Phonology

## 4.1 Phonetic roles

```text
I-PHO
├── Letter name
│   └── English /aɪ/
├── Vowel values
│   ├── Close front unrounded vowel
│   ├── Near-close front unrounded vowel
│   ├── Centralized vowel
│   ├── Reduced vowel
│   └── Diphthong component
├── Glide-related values
│   └── Palatal approximant in historical or contextual use
├── Length distinctions
│   ├── Short
│   └── Long
├── Stress distinctions
│   ├── Stressed
│   └── Unstressed
└── Position
    ├── Onset-adjacent
    ├── Nucleus
    ├── Hiatus
    └── Diphthong member
```

## 4.2 Phonological analysis

```text
Segment
├── Articulation
│   ├── Height
│   ├── Backness
│   ├── Rounding
│   ├── Tenseness
│   └── Duration
├── Distribution
│   ├── Initial
│   ├── Medial
│   ├── Final
│   ├── Open syllable
│   └── Closed syllable
├── Processes
│   ├── Reduction
│   ├── Raising
│   ├── Lowering
│   ├── Centralization
│   ├── Lengthening
│   ├── Shortening
│   ├── Diphthongization
│   ├── Monophthongization
│   ├── Palatalization
│   └── Deletion
└── Variation
    ├── Language
    ├── Dialect
    ├── Register
    ├── Speaker
    └── Historical period
```

---

# 5. Grammar and Lexicon

## 5.1 English first-person pronoun

```text
I-GRM-ENG-PRON
├── Lexeme: I
├── Person: first
├── Number: singular
├── Case: nominative or subject form
├── Referential center: speaker or writer
├── Typical syntactic role
│   ├── Clause subject
│   ├── Coordinated subject
│   ├── Predicate complement in formal registers
│   └── Mentioned or quoted expression
├── Paradigm relations
│   ├── me
│   ├── my
│   ├── mine
│   └── myself
└── Orthographic constraint
    └── Conventional capitalization
```

In English, `I` is the subject form used by a speaker or writer to refer to that speaker or writer; `me` is the corresponding object form. 
## 5.2 Pronoun semantics

```text
I-SEM-SELF
├── Deictic reference
├── Speaker reference
├── Discourse anchoring
├── Perspective center
├── Indexicality
├── Self-reference
├── Quotation shift
├── Reported-speech interpretation
├── Fictional-speaker interpretation
├── Collective-author interpretation
└── Ambiguous authorship
```

## 5.3 Nominal use

```text
I-LEX-NOUN
├── Name of the letter
├── Printed instance of the letter
├── Spoken realization of the letter
├── I-shaped object
├── Person considered as a self
├── Individual identity
├── Designated item in a sequence
└── Grade or classification label
```

Dictionary classifications include the letter, a graphic representation, an I-shaped thing, the self, a unit vector, an incomplete grade, an abbreviation, and several scientific symbols. 
## 5.4 Morphological participation

```text
I-MOR
├── Standalone word
├── Initial
├── Abbreviation
├── Prefix-like element
├── Connective vowel
├── Compound component
├── Product-name component
├── Acronym component
└── Identifier component
```

---

# 6. Numeral Systems

## 6.1 Roman numeral

```text
I-NUM-ROM
├── Canonical value: one
├── Simple use
│   └── I = 1
├── Additive use
│   ├── II = 2
│   └── III = 3
├── Subtractive participation
│   ├── IV
│   └── IX
├── Ordinal-label use
│   ├── Part I
│   ├── Volume I
│   ├── Chapter I
│   └── Class I
└── Naming use
    ├── Rulers
    ├── Popes
    ├── Series
    ├── Events
    └── Versions
```

Cambridge identifies `I/i` as the Roman sign for one and as a component of several other Roman numerals. 
## 6.2 Numeral distinctions

```text
I-NUM-DIST
├── Letter I: U+0049
├── Roman numeral one: U+2160
├── Digit one: U+0031
├── Cardinal value: 1
├── Ordinal interpretation: first
├── Sequence label: item I
└── Classification label: class I
```

---

# 7. Mathematics

## 7.1 Complex analysis and algebra

```text
I-MAT-CPLX
├── Imaginary unit
│   ├── Symbol: i
│   ├── Defining relation: i² = -1
│   ├── Complex-number form: a + bi
│   ├── Powers of i
│   │   ├── i⁰
│   │   ├── i¹
│   │   ├── i²
│   │   └── i³
│   ├── Complex plane
│   ├── Roots
│   ├── Exponentials
│   ├── Trigonometric identities
│   └── Analytic functions
└── Alternate engineering notation
    └── j when i is reserved for current
```

The lowercase symbol `i` conventionally denotes the imaginary unit; dictionaries also recognize bold `i` as a unit vector parallel to the x-axis. 
## 7.2 Indexing

```text
I-MAT-IDX
├── Sequence index
├── Array index
├── Matrix row index
├── Summation index
├── Product index
├── Iteration counter
├── Family-member index
├── Tensor index
├── Coordinate index
├── Basis index
└── Dummy variable
```

## 7.3 Set theory

```text
I-MAT-SET
├── Index set I
├── Indexed family {Aᵢ}ᵢ∈I
├── Interval I
├── Ideal I
├── Identity-related notation
├── Indicator notation
├── Interior operator
├── Injection label
└── Arbitrary set variable
```

## 7.4 Linear algebra

```text
I-MAT-LIN
├── Identity matrix I
│   ├── Finite-dimensional
│   ├── Infinite-dimensional
│   ├── Sized form Iₙ
│   └── Block identity
├── Identity operator
├── Unit vector i
├── Inertia matrix or tensor
├── Index notation
├── Invariant subspace label
└── Incidence matrix label
```

## 7.5 Calculus and analysis

```text
I-MAT-ANA
├── Interval I
├── Integral value I
├── Integrand-related label
├── Iterated integral I
├── Functional I
├── Indicator function
├── Infimum abbreviation in local notation
└── Initial-value label
```

## 7.6 Geometry and mechanics

```text
I-MAT-GEO
├── Point I
├── Center or intersection point
├── Incenter, by convention in some texts
├── Interval
├── Incidence relation
├── Moment of inertia
├── Second moment of area
└── Inertia tensor
```

## 7.7 Number theory and abstract algebra

```text
I-MAT-ALG
├── Ideal I
│   ├── Principal ideal
│   ├── Prime ideal
│   ├── Maximal ideal
│   ├── Radical ideal
│   ├── Left ideal
│   ├── Right ideal
│   └── Two-sided ideal
├── Identity element or map
├── Index of a subgroup
├── Involution
├── Isomorphism
├── Integer-related variable
└── Imaginary component
```

---

# 8. Logic and Formal Systems

```text
I-LOG
├── Interpretation I
│   ├── Domain
│   ├── Constant assignment
│   ├── Function assignment
│   └── Predicate assignment
├── Identity
├── Implication
├── Intension
├── Information
├── Individual variable
├── Input proposition
├── Inconsistency measure
├── Inference rule label
├── Modal accessibility structure label
└── Type-theoretic identity object
```

---

# 9. Statistics, Probability, and Information Theory

```text
I-STA
├── Indicator variable I
├── Information
│   ├── Self-information
│   ├── Mutual information
│   └── Fisher information
├── Confidence-interval label
├── Index
├── Intervention indicator
├── Incidence
├── Independence notation
├── Interaction term
└── Identity matrix in covariance expressions
```

```text
I-PROB
├── Event indicator
├── Random index
├── Information filtration label
├── Interval
├── Initial state
└── State-space identity operator
```

---

# 10. Physics

## 10.1 Electricity and magnetism

```text
I-PHY-ELEC
├── Electric current I
├── Instantaneous current i(t)
├── Direct current
├── Alternating current
├── Branch current
├── Loop current
├── Source current
├── Load current
├── Leakage current
├── Bias current
├── Saturation current
├── Photocurrent
└── Current amplitude
```

`I` is conventionally used for electric current, while the SI unit is the ampere, symbol `A`. The official SI system and its notation are maintained in the SI Brochure. 
## 10.2 Mechanics

```text
I-PHY-MECH
├── Moment of inertia
│   ├── Point mass
│   ├── Discrete system
│   ├── Continuous body
│   ├── Axis-specific moment
│   └── Principal moment
├── Area moment of inertia
├── Inertia tensor
├── Impulse
└── Intensity in local conventions
```

## 10.3 Optics and waves

```text
I-PHY-OPT
├── Intensity
├── Irradiance in local notation
├── Incident intensity
├── Transmitted intensity
├── Reflected intensity
├── Spectral intensity
└── Image intensity
```

## 10.4 Thermodynamics and quantum theory

```text
I-PHY-ADV
├── Internal-state index
├── Interaction term
├── Action or functional label
├── Identity operator
├── Isospin symbol in some contexts
├── Nuclear spin convention
├── Information quantity
└── Current operator
```

---

# 11. Engineering

```text
I-ENG
├── Electrical engineering
│   ├── Current
│   ├── Current source
│   ├── Current gain
│   └── Current rating
├── Mechanical engineering
│   ├── Moment of inertia
│   ├── Area moment
│   └── Inertia tensor
├── Structural engineering
│   ├── Second moment of area
│   └── Section property
├── Control engineering
│   ├── Integral term
│   ├── Identity matrix
│   ├── Input index
│   └── System-identification variable
├── Industrial engineering
│   ├── Inventory
│   ├── Inspection
│   ├── Idle time
│   └── Input
└── Systems engineering
    ├── Interface
    ├── Item
    ├── Requirement identifier
    └── Information flow
```

---

# 12. Chemistry and Materials Science

```text
I-CHE
├── Element symbol I
│   └── Iodine
├── Molecular formulas
│   ├── Elemental iodine
│   ├── Iodides
│   ├── Iodates
│   └── Organic iodine compounds
├── Oxidation-state notation
├── Isotope notation
├── Reaction intermediate label
├── Species index
├── Ionic-strength notation
├── Intensity notation
└── Phase or sample identifier
```

`I` is recognized as the chemical symbol for iodine. 
---

# 13. Biology and Medicine

```text
I-BIO
├── Individual identifier
├── Generation label in pedigrees
├── Allele label
├── Gene or protein symbol component
├── Species or specimen code
├── Ecological index
├── Infection state
├── Immune-related abbreviation
├── Incidence
├── Inhibition
├── Input neuron or current
└── Experimental group label
```

```text
I-MED
├── Stage I
├── Grade I
├── Type I
├── Class I
├── Lead I in electrocardiography
├── Insulin abbreviation in local notation
├── Infection
├── Inflammation
├── Injury
├── Intervention group
├── Intake/output notation
└── Patient or specimen identifier
```

Each biomedical interpretation requires a governing vocabulary, protocol, instrument, or publication because the isolated symbol is not semantically stable.

---

# 14. Computing and Information Systems

## 14.1 Programming

```text
I-COM-PROG
├── Loop counter i
├── Array index i
├── Iterator
├── Integer variable
├── Interface prefix
├── Instance variable
├── Input variable
├── Imaginary-number literal or object
├── Generic type parameter
├── Lambda-bound variable
├── Matrix row selector
└── Temporary local variable
```

A lowercase `i` is widely used as a generic index, especially in loops and mathematical programming contexts. 
## 14.2 Data modeling

```text
I-COM-DATA
├── Primary identifier
├── Foreign identifier
├── Record index
├── Item identifier
├── Entity type
├── Field name
├── Schema version
├── Integrity flag
├── Input field
├── Information object
└── Instance key
```

## 14.3 Identity and access

```text
I-COM-IAM
├── Identity
├── Identifier
├── Issuer
├── Individual principal
├── Authentication factor label
├── Authorization scope
├── Identity token claim
└── Account type
```

## 14.4 User interfaces

```text
I-COM-UI
├── Information icon
├── Italic-format command
├── Input control
├── Inspector
├── Inventory
├── Item
├── Insert command
└── Interaction state
```

## 14.5 Networking and systems

```text
I-COM-SYS
├── Input
├── Interrupt
├── Interface
├── Instruction
├── Instance
├── Internet-related initial
├── Information channel
├── Installation state
├── Integrity status
└── Internal classification
```

## 14.6 Search and cybersecurity

```text
I-COM-SEC
├── Confusable-character detection
├── Homoglyph attack analysis
├── Identifier spoofing
├── Case-sensitive comparison
├── Unicode normalization
├── Domain-name inspection
├── Password distinction
├── Optical-character-recognition error
└── Log-search ambiguity
```

---

# 15. Linguistics and Semiotics

```text
I-LIN
├── Grapheme
├── Phoneme representation
├── Morpheme
├── Lexeme
├── Pronoun
├── Indexical
├── Deictic expression
├── Discourse participant marker
├── Coreference index i
├── Syntactic node label
├── Inflectional category
├── Intermediate projection
└── Transliteration symbol
```

```text
I-SEMIO
├── Signifier
├── Signified
├── Iconic I-shape
├── Index of speaker
├── Symbol of individuality
├── Token
├── Type
├── Inscription
├── Mention
└── Use
```

---

# 16. Philosophy, Psychology, and Social Theory

```text
I-PHI
├── Self
├── Subject
├── Ego
├── Personal identity
├── First-person perspective
├── Conscious subject
├── Transcendental subject
├── Narrative self
├── Moral agent
├── Epistemic subject
└── Phenomenological center
```

```text
I-PSY
├── Self-concept
├── Self-schema
├── Ego representation
├── Autobiographical identity
├── Agency
├── Self-awareness
├── First-person cognition
├── Internal dialogue
└── Individual-difference measure
```

```text
I-SOC
├── Individual
├── Identity
├── Individualism
├── Personal voice
├── Social position
├── Speaker role
├── Authorship
├── Self-presentation
└── Group-versus-self distinction
```

---

# 17. Education, Law, Government, and Organizations

## 17.1 Education

```text
I-EDU
├── Grade I
│   └── Incomplete
├── Level I
├── Part I
├── Course section I
├── Learning objective I
├── Item I
├── Roman-numeral outline marker
└── Student or cohort identifier
```

A grade of `I` can denote incomplete work in educational contexts. 
## 17.2 Law

```text
I-LEG
├── Article I
├── Title I
├── Part I
├── Schedule I
├── Class I
├── Count I
├── Exhibit I
├── Party initial
└── Roman-numeral hierarchy marker
```

## 17.3 Government and administration

```text
I-GOV
├── District I
├── Region I
├── Category I
├── Form I
├── Security classification label
├── Department initial
├── Interstate abbreviation
└── Intelligence abbreviation
```

## 17.4 Organizations

```text
I-ORG
├── Organization initial
├── Division label
├── Product family
├── Department code
├── Job level
├── Building or room designation
├── Project phase
└── Internal entity identifier
```

---

# 18. Music, Arts, and Culture

```text
I-MUS
├── Roman numeral for scale degree one
├── Tonic-function chord
├── Movement I
├── Part I
├── Instrument abbreviation
├── Voice identifier
└── Section marker
```

```text
I-ART
├── Vertical visual form
├── Minimalist mark
├── Typographic subject
├── Monogram
├── Initial
├── Signature component
├── Logo element
└── Title component
```

```text
I-CUL
├── Symbol of self
├── Symbol of individuality
├── First-person voice
├── Number one through Roman notation
├── Series opener
├── Rank or class marker
├── Initial of a name
└── Eye/I wordplay
```

---

# 19. Transportation, Geography, and Classification Systems

```text
I-TRN
├── Interstate-route prefix
├── Route identifier
├── Platform or terminal label
├── Vehicle class
├── Fare zone
├── Service line
└── Compartment label
```

```text
I-GEO
├── Island or isle abbreviation
├── Region I
├── Grid coordinate
├── Map sector
├── Administrative class
├── Location code component
└── Feature identifier
```

```text
I-CLASS
├── Class I
├── Type I
├── Grade I
├── Level I
├── Phase I
├── Stage I
├── Category I
├── Group I
├── Division I
├── Tier I
└── Zone I
```

---

# 20. Abbreviations and Initialisms

```text
I-ABR
├── General
│   ├── initial
│   ├── industrial
│   ├── intelligence
│   ├── intensity
│   ├── island
│   ├── interstate
│   └── incomplete
├── Technical
│   ├── current
│   ├── input
│   ├── interface
│   ├── instruction
│   ├── information
│   ├── identity
│   ├── index
│   └── integral
├── Organizational
│   ├── department initial
│   ├── company initial
│   ├── product initial
│   └── role initial
└── Personal
    ├── given-name initial
    ├── middle initial
    ├── surname initial
    └── pseudonym
```

Dictionary sources explicitly list senses including industrial, initial, intelligence, intensity, interlaced, intransitive, island, electric current, interstate, and iodine. 
---

# 21. Relationship Mapping

```text
I
├── Is encoded as
│   ├── U+0049
│   ├── U+0069
│   └── related Unicode characters
├── Is rendered by
│   └── glyph
├── Is a member of
│   ├── Latin alphabet
│   ├── English pronoun paradigm
│   ├── Roman numeral system
│   └── domain notation systems
├── May denote
│   ├── self
│   ├── one
│   ├── imaginary unit
│   ├── identity
│   ├── current
│   ├── iodine
│   ├── intensity
│   ├── inertia
│   ├── index
│   ├── interval
│   ├── ideal
│   ├── information
│   ├── input
│   └── arbitrary entity
├── May be confused with
│   ├── l
│   ├── 1
│   ├── |
│   ├── Ι
│   ├── І
│   └── Ⅰ
└── Is disambiguated by
    ├── domain
    ├── case
    ├── font
    ├── encoding
    ├── surrounding syntax
    ├── units
    ├── subscripts
    ├── superscripts
    ├── source authority
    └── document glossary
```

---

# 22. Dependency Model

```text
Rendered Meaning
├── depends on Character Identity
│   ├── code point
│   ├── normalization
│   └── script
├── depends on Glyph
│   ├── font
│   ├── style
│   └── resolution
├── depends on Syntax
│   ├── position
│   ├── operators
│   ├── punctuation
│   └── capitalization
├── depends on Domain
│   ├── mathematics
│   ├── language
│   ├── science
│   └── computing
├── depends on Local Convention
│   ├── glossary
│   ├── standard
│   ├── author
│   └── organization
└── depends on Context
    ├── sentence
    ├── equation
    ├── diagram
    ├── database
    ├── interface
    └── classification system
```

---

# 23. Atomic Analysis Model

Every occurrence of `I` should be decomposed into the following atomic questions:

```text
Occurrence
├── What exact code point is present?
├── What glyph is displayed?
├── What script is intended?
├── Is case significant?
├── Is it one character or a combined sequence?
├── Is it a word, letter, numeral, symbol, or identifier?
├── What domain governs interpretation?
├── What syntactic position does it occupy?
├── Are there units?
├── Are there subscripts or superscripts?
├── Is it italic, bold, or upright?
├── Is it quoted or used directly?
├── Is it human-readable or machine-readable?
├── Is it locally defined?
├── Is there an authoritative glossary?
├── What entities are adjacent?
├── What relations connect it to those entities?
├── What confusable alternatives exist?
├── What validation rules apply?
└── What evidence supports the selected interpretation?
```

---

# 24. Pattern Discovery

```text
Patterns
├── Repetition
│   ├── II
│   ├── III
│   ├── repeated loop variables
│   └── repeated classification labels
├── Similarity
│   ├── visual
│   ├── phonetic
│   ├── semantic
│   └── functional
├── Deviation
│   ├── unexpected case
│   ├── unexpected font
│   ├── unexpected code point
│   ├── malformed Roman numeral
│   └── inconsistent domain use
├── Clustering
│   ├── linguistic uses
│   ├── numerical uses
│   ├── mathematical uses
│   ├── scientific uses
│   ├── computing uses
│   └── institutional uses
└── Co-occurrence
    ├── I + verb → probable pronoun
    ├── I + V/X → probable Roman numeral
    ├── I + ampere unit → probable current
    ├── i² or √−1 → imaginary unit
    ├── Iₙ → probable identity matrix
    ├── chemical formula position → possible iodine
    └── for/while loop → probable index
```

---

# 25. Validation Framework

## 25.1 Integrity

```text
Integrity
├── Valid encoding
├── Valid script
├── Valid normalization
├── Valid case mapping
├── Valid identifier format
├── Valid domain assignment
└── Valid source reference
```

## 25.2 Consistency

```text
Consistency
├── Same symbol has stable local meaning
├── Case is used consistently
├── Italic/upright styling follows convention
├── Units agree with quantity
├── Indices agree with declarations
├── Roman-numeral syntax is consistent
└── Cross-references resolve
```

## 25.3 Completeness

```text
Completeness
├── Definition supplied
├── Domain supplied
├── Context supplied
├── Source supplied
├── Relationships supplied
├── Constraints supplied
├── Variants supplied
└── Confusables supplied
```

## 25.4 Traceability

```text
Traceability
├── Token → character
├── Character → code point
├── Token → context
├── Context → interpretation
├── Interpretation → authority
├── Authority → source
├── Source → version
└── Version → validation result
```

---

# 26. Knowledge-Graph Model

```text
Nodes
├── Character
├── Glyph
├── Grapheme
├── Phoneme
├── Lexeme
├── Pronoun
├── Numeral
├── Mathematical object
├── Physical quantity
├── Chemical element
├── Identifier
├── Concept
├── Domain
├── Standard
├── Source
└── Context
```

```text
Edges
├── HAS_GLYPH
├── ENCODES
├── CASE_OF
├── VARIANT_OF
├── CONFUSABLE_WITH
├── PRONOUNCED_AS
├── DENOTES
├── HAS_VALUE
├── HAS_UNIT
├── MEMBER_OF
├── USED_IN
├── DEFINED_BY
├── GOVERNED_BY
├── OCCURS_IN
├── DEPENDS_ON
├── DERIVED_FROM
├── TRANSLITERATES
├── ABBREVIATES
├── REFERENCES
└── VALIDATED_BY
```

Example graph:

```text
U+0049
  ├── ENCODES → Latin capital letter I
  ├── CASE_OF → U+0069
  ├── MAY_RENDER_AS → I-glyph
  └── CONFUSABLE_WITH → U+0031 / U+006C / U+0399 / U+2160

English “I”
  ├── INSTANCE_OF → first-person singular pronoun
  ├── HAS_SYNTACTIC_ROLE → subject
  ├── REFERS_TO → speaker or writer
  └── PARADIGM_RELATED_TO → me / my / mine / myself

Roman I
  ├── INSTANCE_OF → numeral
  └── HAS_VALUE → 1

Mathematical i
  ├── INSTANCE_OF → imaginary unit
  └── SATISFIES → i² = −1

Physical I
  ├── DENOTES → electric current
  └── HAS_SI_UNIT → ampere

Chemical I
  └── DENOTES → iodine
```

---

# 27. Reference Index

```text
REF-CHAR     Character encoding and Unicode
REF-ORTH     Orthography and typography
REF-PHON     Phonetics and phonology
REF-GRAM     Grammar and pronoun use
REF-NUM      Roman numerals
REF-MATH     Mathematical notation
REF-LOGIC    Logic and formal semantics
REF-STATS    Statistics and information
REF-PHYS     Physics
REF-ENG      Engineering
REF-CHEM     Chemistry
REF-BIO      Biology
REF-MED      Medicine
REF-COMP     Computing
REF-LING     Linguistics
REF-PHIL     Philosophy
REF-PSY      Psychology
REF-SOC      Social theory
REF-EDU      Education
REF-LEGAL    Law
REF-GOV      Government
REF-MUSIC    Music
REF-CULT     Culture
REF-ID       Identifier systems
REF-VALID    Validation and traceability
```

---

# 28. Canonical Disambiguation Procedure

```text
INPUT: occurrence of I/i

1. Preserve the original token.
2. Record its exact Unicode code point or sequence.
3. Record case, font, style, and decorations.
4. Capture surrounding words, symbols, units, and operators.
5. Identify the governing document or domain.
6. Test numeral interpretation.
7. Test linguistic interpretation.
8. Test mathematical interpretation.
9. Test scientific interpretation.
10. Test computing or identifier interpretation.
11. inspect confusable characters.
12. Consult the local glossary or notation declaration.
13. Assign one primary interpretation.
14. Retain plausible secondary interpretations.
15. Attach authority, source, and confidence.
16. Generate a traceable identifier.
```

## Confidence states

```text
CONF-1  Explicitly defined by source
CONF-2  Unambiguous from formal syntax
CONF-3  Strongly implied by domain
CONF-4  Probable from local context
CONF-5  Ambiguous
CONF-6  Unresolved
CONF-7  Invalid or corrupted token
```

---

# 29. Final Deliverable Structure

```text
I Knowledge System
├── Taxonomy
│   ├── Character
│   ├── Linguistic
│   ├── Numerical
│   ├── Mathematical
│   ├── Scientific
│   ├── Technical
│   ├── Institutional
│   └── Cultural
├── Knowledge Graph
│   ├── Nodes
│   ├── Edges
│   ├── Properties
│   └── Provenance
├── Dependency Model
│   ├── Encoding dependency
│   ├── Glyph dependency
│   ├── Context dependency
│   ├── Domain dependency
│   └── Authority dependency
├── Reference Index
│   ├── Definitions
│   ├── Standards
│   ├── Sources
│   ├── Examples
│   └── Cross-references
└── Granular Outline
    ├── Stable universal branches
    ├── Domain-specific branches
    ├── Corpus-dependent branches
    ├── Locally defined branches
    └── Extensible identifier slots
```

**Core analytical principle:** `I` has no single context-independent meaning. The atomic object is therefore not merely the visible mark, but the tuple:

```text
<I-form, code point, glyph, language, syntax, domain,
 local convention, intended referent, source, version>
```