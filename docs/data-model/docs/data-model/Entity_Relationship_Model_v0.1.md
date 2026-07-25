# Global Historical & Folklore Geographic Archive

## Entity Relationship Model

Version:
0.1 — Initial Relationship Definition

Status:
Prototype Planning Phase

---

# Overview

The Entity Relationship Model defines how archive components connect.

The design intentionally separates:

- Evidence
- Extracted information
- Context
- Relationships
- Interpretation

---

# Core Relationship Model
SOURCE

|
| documents
|
v

RECORD

|
| associated_with
|
v

LOCATION

|
| has_context
|
v

HISTORICAL CONTEXT
RECORD

|
| classified_as
|
v

CLASSIFICATION

RECORD

|
| connected_by
|
v

RELATIONSHIP

RESEARCH NOTE
|
| analyzes
|
v

RECORD


---

# Source Relationships

A Source may document multiple Records.

Relationship:


Source 1 ---- documents ----> Record Many
A Record may also have multiple Sources.

Relationship:

Record Many ---- supported_by ---- Source Many
This allows:

- independent sources
- conflicting accounts
- source comparison

---

# Record Relationships

Records are independent research objects.

A Record may connect to:

- Sources
- Locations
- Classifications
- Historical Context
- Environmental Context
- Research Notes
- Other Records

---

# Location Relationships

Locations are historical entities.

A Location may contain:

- Modern name
- Historical names
- Alternate names
- Estimated coordinates
- Accuracy information

Relationship:

Record Many ---- occurs_at ---- Location One
or when uncertain:

Record Many ---- possibly_associated_with ---- Location Many
---

# Classification Relationships

Records may have multiple classifications.

Example:

Record

classified_as:

Maritime
Visual Report
Coastal Environment
Primary Source
Classification is descriptive, not explanatory.

---

# Relationship Entity

Relationships are stored independently.

A relationship contains:

- Relationship ID
- Source Entity
- Target Entity
- Relationship Type
- Confidence Level
- Supporting Sources
- Research Notes
- Date Created
- Version

This allows relationships themselves to be researched.

---

# Research Notes

Research Notes do not modify original evidence.

They provide:

- observations
- questions
- proposed connections
- uncertainty discussion
- future research directions

---

# Design Rule

Evidence remains stable.

Interpretations remain separate.

Relationships may evolve as research develops.
