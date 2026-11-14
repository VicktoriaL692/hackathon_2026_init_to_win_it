# VaultGuard

**An additional security layer for evaluating AI requests and intended
actions.**

VaultGuard is a project focused on improving the safety of AI
interactions. It is designed to evaluate requests, identify potentially
unsafe instructions, and help prevent actions that fall outside approved
security boundaries.

> **Project status:** Development / prototype. This README describes the
> project goals and the functionality reported by the team. Confirm
> implementation details against the current source code before
> presenting them as completed features.

## Table of Contents

-   [The Problem](#the-problem)
-   [Our Solution](#our-solution)
-   [Core Security Functions](#core-security-functions)
-   [How It Works](#how-it-works)
-   [Technology](#technology)
-   [Testing](#testing)
-   [Limitations](#limitations)
-   [Future Development](#future-development)
-   [Project Team](#project-team)

## The Problem

AI systems can be exposed to security risks, including:

-   **Prompt injection:** Instructions intended to manipulate an AI
    system's behavior.
-   **Sensitive information exposure:** Requests that could reveal
    confidential or private information.
-   **Unauthorized actions:** Attempts to access resources or perform
    actions without the required permission.
-   **Safety bypass attempts:** Instructions that attempt to override or
    disable established safety restrictions.

As AI becomes more capable and is used to perform more tasks, users need
greater control over what AI systems can access and do.

## Our Solution

VaultGuard is designed to act as a security checkpoint between an AI
request and its intended action.

It evaluates requests against security requirements and determines an
appropriate outcome:

-   **Allow:** The request meets the checks implemented by the system.
-   **Block:** The request violates a security restriction.
-   **Review:** The request needs additional evaluation or human
    oversight, if this outcome is supported by the current
    implementation.

The goal is to help ensure that AI only accesses information it needs,
performs actions it is authorized to perform, and remains within
approved boundaries.

## Core Security Functions

VaultGuard is organized around four security functions:

### 1. Threat Detection

Identifies suspicious or potentially malicious instructions, including
prompt injection attempts and attempts to bypass safety restrictions.

### 2. Privacy Protection

Focuses on identifying sensitive information that could be exposed or
improperly shared.

### 3. Permission Control

Focuses on whether a requested resource or action is authorized.

### 4. Behavior Monitoring

Focuses on whether AI actions remain within approved boundaries.

**Implementation note:** These are the project's four security
functions. The exact checks available in the current prototype should be
verified in the source code; do not assume every function is fully
implemented.

## How It Works

The intended request-evaluation flow is:

1.  Receive an AI-related request.
2.  Examine what the prompt is asking the system to do.
3.  Perform the applicable browser-related verification.
4.  Check for suspicious instructions or attempts to bypass or disable
    safety restrictions.
5.  Evaluate the request against the security checks implemented in
    VaultGuard.
6.  Return the applicable decision, such as allow or block; route for
    review only if supported by the implementation.

This process is intended to identify unsafe requests before the
associated action is carried out. The current level of integration with
external AI systems and action execution should be confirmed from the
project code.

## Technology

-   **Programming language:** Python
-   **Reason for choosing Python:** The programmers on the team were
    more familiar with Python, allowing the group to focus on developing
    and testing the project.

Add the specific Python version, libraries, modules, browser tools, and
other technologies used by the project here:

-   Python version: `TODO`
-   Libraries / dependencies: `TODO`
-   Browser verification tools: `TODO`
-   Other tools: `TODO`

## Getting Started

The exact installation and run commands depend on the files and
dependencies in the project repository. Add the verified commands below
before publishing this README.

### Prerequisites

-   Python: `TODO — add the version used`
-   Dependencies: `TODO — list packages or link to requirements.txt`

### Installation

``` bash
# Clone the repository
git clone <repository-url>

# Move into the project directory
cd <project-directory>

# Install dependencies, if a requirements file is provided
pip install -r requirements.txt
```

### Run

``` bash
# Replace this with the verified command for the project's entry point
python <entry-point>.py
```

> The commands above are a template. Replace the placeholders with the
> repository URL, directory name, dependency file, and entry point used
> by the actual project.

## Testing

The team plans to evaluate VaultGuard using a set of 10 test cases
covering different request types and security scenarios.

Examples of areas to test include:

-   Ordinary, safe prompts.
-   Prompt injection attempts.
-   Attempts to bypass or disable safety restrictions.
-   Requests involving sensitive information.
-   Browser-related requests.
-   Requests that may involve unauthorized access or actions.

Record the actual outcome of each test and compare it with the expected
outcome.

  Metric                                          Result
  ------------------------------ -----------------------
  Total test cases                 10 planned / reported
  Correctly classified cases                      `TODO`
  Incorrectly classified cases                    `TODO`
  False positives                                 `TODO`
  False negatives                                 `TODO`
  Accuracy                                        `TODO`

Accuracy can be calculated as:

``` text
Accuracy = (number of correct classifications / total test cases) * 100
```

Do not enter benchmark figures until the test results have been
collected and verified.

## Limitations

VaultGuard is a developing project. Its effectiveness depends on the
security checks implemented, the scenarios tested, and how it is
connected to the AI system or actions it is intended to protect.

Initial testing with 10 cases is not enough to establish that the system
can detect every prompt injection technique or prevent every
unauthorized action. Additional testing is needed, including more varied
and sophisticated attack scenarios.

## Future Development

Planned areas for improvement include:

-   Creating a visual dashboard to display security decisions and
    activity.
-   Improving threat detection.
-   Expanding testing with additional attack scenarios.
-   Integrating VaultGuard with actual AI systems.
-   Improving performance and reliability.

## Project Team

**Team:** `__INIT__ TO WIN IT`

-   Vicktoria Lee
-   Gabby Ferguson
-   Diana Ebob

## Project Goal

VaultGuard is designed to make AI safer by helping ensure that it only
accesses information it needs, only performs actions it is authorized to
perform, and stays within approved boundaries.
