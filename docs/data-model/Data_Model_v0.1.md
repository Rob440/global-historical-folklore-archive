# Global Historical & Folklore Geographic Archive

## Data Model Specification

Version:
0.1 — Initial Data Model Definition

Status:
Prototype Planning Phase

---

# Overview

The data model defines how information is stored, connected, and retrieved.

The purpose of the model is to represent complex historical material without forcing it into overly simple categories.

The archive separates:

- Sources
- Records
- Locations
- Context
- Relationships
- Research interpretation

---

# Core Entities

The first prototype contains the following primary entities:

1. Sources
2. Records
3. Locations
4. Classifications
5. Historical Context
6. Environmental Context
7. Relationships
8. Research Notes

---

# Sources

A Source is the original material from which information is collected.

Examples:

- Newspaper article
- Book
- Archive document
- Military report
- Maritime log
- Oral collection
- Interview

A Source contains:

- Source ID
- Title
- Creator / Author / Collector
- Source Type
- Publication or Archive
- Date
- Language
- Digital Reference
- Original Content
- Notes
- Quality Information

A source is never replaced by a summary.

---

# Records

A Record is a structured representation of information extracted from a source.

Possible record types:

- Incident
- Tradition
- Observation
- Report
- Claim
- Interpretation
- Research Note

A Record contains:

- Record ID
- Title
- Description
- Record Type
- Date Information
- Location Reference
- Classification
- Confidence Level
- Research Status
- Notes

A record may connect to multiple sources.

---

# Locations

Locations are treated as historical objects rather than simple coordinates.

A Location contains:

- Location ID
- Coordinates
- Original Description
- Modern Name
- Historical Name
- Location Accuracy
- Resolution Notes
- Related Context

Locations may change:

- Name
- Political ownership
- Language
- Cultural meaning
- Geographic interpretation

over time.

---

# Classifications

Classifications provide a shared vocabulary for organizing records.

Examples:

- Phenomenon Type
- Source Type
- Cultural Motif
- Geographic Setting
- Historical Period
- Documentation Quality

Classifications evolve through research.

---

# Historical Context

Historical Context connects records to the world as it existed at the time.

Examples:

- Political boundaries
- Settlement names
- Languages
- Cultural regions
- Historical events

Contains:

- Location
- Date Range
- Political Entity
- Settlement Information
- Language Region
- Historical Notes
- Supporting Sources

---

# Environmental Context

Environmental Context allows geographic comparison.

Examples:

- Elevation
- Terrain
- Waterways
- Geological features
- Climate
- Weather information

---

# Relationships

Relationships connect entities together.

Examples:

Record A

related_to

Record B


Source A

documents

Record A


Tradition A

associated_with

Location A

Relationships are stored separately from records.

---

# Research Notes

Research Notes represent the human analysis layer.

They contain:

- Observations
- Questions
- Uncertainties
- Proposed connections
- Future research needs

Research notes are separate from original evidence.

---

# Data Model Principle

Store what is known.

Preserve what is uncertain.

Document how conclusions are reached.

