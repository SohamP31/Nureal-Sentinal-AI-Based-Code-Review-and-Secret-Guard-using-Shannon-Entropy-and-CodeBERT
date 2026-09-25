Neural-Sentinel — AI-Based Code Security & Secret Detection
1. Project Title

Neural-Sentinel: AI-Based Code Security and Secret Detection System

2. Role

AI/ML Developer | Project Developer

If you developed it individually, write:

Role: AI/ML Developer — Personal Project

3. Short Description — 1–2 sentences

Developed a local-first AI-based code security system that detects hardcoded secrets and potential code vulnerabilities using Shannon Entropy, CodeBERT, and Augmented Program Dependency Graph (AUG-PDG) analysis. The system uses Git pre-commit hooks and IDE integration to detect and prevent security issues before code reaches remote repositories.

4. Technologies / Frameworks

Programming & Backend

Python
FastAPI
Bash

AI / ML

CodeBERT
Transformers
Shannon Entropy
Semantic Analysis
Classification

Code Analysis

AST
AUG-PDG
Data Flow Analysis
Control Flow Analysis
Use-Def Analysis

Development & Security

Git
Git Pre-commit Hooks
VS Code Extension API
DevSecOps
Zero-Knowledge Architecture

Frontend / Dashboard

React

The architecture described in the document specifically uses a Bash Git pre-commit hook, local FastAPI server, VS Code Extension API, CodeBERT, AUG-PDG, and a React-based dashboard.

5. Key Features
Automated Secret Detection
Shannon Entropy-Based Detection
CodeBERT Semantic Analysis
AUG-PDG-Based Vulnerability Analysis
Git Pre-Commit Security Enforcement
Real-Time IDE Feedback
Automatic Code Refactoring Suggestions
Risk-Based Block/Allow Decision
Local-First Processing
Zero-Knowledge Security Architecture
Audit Logging
React-Based Security Dashboard
Multi-Language Support
Protection Against Zombie Leaks
DevSecOps Integration
6. How the System Works

You can explain the workflow like this:

Developer writes code
        ↓
Git Commit / IDE Change
        ↓
Git Pre-Commit Hook
        ↓
Extract Changed Code
        ↓
Shannon Entropy Analysis
        ↓
Suspicious String?
        ↓
CodeBERT Semantic Analysis
        ↓
AUG-PDG Analysis
        ↓
Hybrid Risk Score
        ↓
   ┌───────────────┐
   │ Risk > 0.75?  │
   └───────┬───────┘
       Yes ↓       ↓ No
     BLOCK         ALLOW
       ↓
Auto-Refactoring /
Security Suggestion
       ↓
Audit Dashboard

The paper specifies that the entropy engine filters strings above an entropy threshold of 4.5, after which the deep-learning core performs contextual analysis and generates a hybrid risk score; a score above 0.75 results in the commit being blocked.

7. Main Modules
Module 1 — Input Capture & Delta Auditing
Captures changes during Git commits.
Uses git diff --cached.
Processes only modified code instead of the complete repository.
Sends the extracted changes to the local FastAPI service.
Module 2 — Shannon Entropy Pre-Filter
Calculates entropy for strings.
Uses 4.5 bits as the threshold.
Filters out low-probability secret candidates.
Reduces the number of strings requiring expensive semantic analysis.
Module 3 — CodeBERT Semantic Classification
Creates a contextual window around suspicious strings.
Uses CodeBERT for semantic understanding.
Classifies whether a suspicious string represents a secret.
The described model was fine-tuned using SecretBench and Big-Vul data.
Module 4 — Agentic Remediation & Policy Enforcement
Blocks commits when the risk score crosses the defined threshold.
Displays security diagnostics.
Provides Auto-Refactor, Inspect, and Ignore options.
Records decisions in the audit database.
8. Datasets
SecretBench

Used for secret/credential detection.

Contains examples such as:

AWS Access Keys
Google Cloud Credentials
Azure Tokens
Database Passwords
OAuth Tokens
API Keys
JWT Tokens
SSH Private Keys
GitHub Personal Access Tokens
Big-Vul

Used for code vulnerability analysis, including:

Buffer Overflow
SQL Injection
Infinite Loops
Dead Code
Data Leakage
Resource Leaks
Null Pointer Exceptions
Logic Errors
9. Results / Achievements

If these results are actually from your implemented project, they are strong points to put on your resume:

98.5% F1-score
98.3% Precision
98.7% Recall
1.7% False Positive Rate
186 ms detection latency
194 ms average commit processing time
4,200 commits/hour throughput
96.1% F1-score on zero-day secret formats
100% repository hygiene for detected secrets

The paper also reports that the hybrid approach achieved 98.5% F1, compared with 77.5% for the pure Regex baseline and 93.4% for CodeBERT alone.

Important: If these are research-paper/proposed-system results rather than results from your own implementation, don't present them on your resume as metrics you personally achieved. Instead write “Proposed/Reported performance: 98.5% F1-score.”
