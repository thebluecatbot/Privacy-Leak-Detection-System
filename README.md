# Privacy Leak Detection & Risk Analysis

A local, read-only system for detecting sensitive data leaks in code and documents using a two-stage NLP pipeline.

---

## Overview

SecureLens is designed to identify privacy and security risks such as:
- API keys
- Tokens
- Email addresses
- Credentials
- Contextual secrets hidden in variable names or logic

The system never modifies files and never stores data.

---

## How It Works

### Stage 1 — Fast Pattern Scan
Uses regex rules to detect obvious secrets such as:
- Emails
- Tokens
- API keys
- Password patterns  

This stage is cheap and filters most cases quickly.

### Stage 2 — LLM Semantic Scan
Only suspicious segments are sent to an LLM to detect:
- Conceptual leaks
- Hardcoded secrets hidden in variable context
- Indirect credential exposure

This minimizes API usage while preserving high recall.

---

## Privacy Guarantees

- Runs locally
- Read-only analysis
- No file modification
- No data persistence
- No automatic sanitization

---

## Output

SecureLens generates explainable risk reports that:
- Highlight risky code segments
- Explain why they are risky
- Provide human-review recommendations

---

## Use Cases

- Code audits
- Pre-deployment checks
- Developer self-review
- Compliance validation

---

## Domain

Applied NLP, Static Analysis, Responsible AI, Developer Tooling

