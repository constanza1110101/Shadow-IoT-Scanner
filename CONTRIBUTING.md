Contributing to Shadow IoT Scanner
Thank you for your interest in contributing to Shadow IoT Scanner! This document provides guidelines and instructions for contributing to this project.

Code of Conduct
By participating in this project, you agree to uphold our Code of Conduct. Please report unacceptable behavior to [security@example.com].

How Can I Contribute?
Reporting Bugs
Before submitting a bug report:

Check the issue tracker to avoid duplicates
Collect information about your environment (OS, Ruby version, network setup)
Describe the exact steps to reproduce the problem
Explain the behavior you observed and what you expected to see
Submit your bug report using the issue template, including as much detail as possible.

Suggesting Enhancements
Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion:

Use a clear and descriptive title
Provide a detailed description of the suggested enhancement
Explain why this enhancement would be useful to most users
Include examples of how the feature would work
List any similar implementations in other projects
Device Fingerprints Contributions
One of the most valuable ways to contribute is by adding device fingerprints to our database:

Follow the fingerprint template in data/fingerprint_template.json
Include as much detail as possible (HTTP headers, DHCP options, mDNS records)
Verify the fingerprint works with at least 2 devices of the same model
Submit a pull request with your fingerprint additions
Code Contributions
Fork the repository
Create a new branch for your feature or bugfix
Write your code following our coding standards
Add tests for your changes
Ensure all tests pass
Submit a pull request
Development Setup
Install development dependencies:

bash

Hide
bundle install --with development
Set up the test environment:

bash

Hide
rake setup_test_env
Run the test suite:

bash

Hide
rake test
Coding Standards
Follow Ruby style guidelines
Use meaningful variable and method names
Write comments for complex logic
Include docstrings for all methods
Keep methods focused on a single responsibility
Write tests for all new functionality
Pull Request Process
Update the README.md with details of changes if applicable
Update the CHANGELOG.md following semantic versioning
Include relevant issue numbers in your PR description
Your PR will be reviewed by at least one maintainer
Address any requested changes promptly
Once approved, a maintainer will merge your PR
Device Fingerprinting Guidelines
When contributing device fingerprints:

Ensure accurate manufacturer and model information
Include firmware version if available
Document all network signatures (MAC OUI, DHCP, mDNS, UPnP, etc.)
Note any default credentials (securely)
Document known vulnerabilities with CVE references
Include typical network behavior patterns
Security Vulnerability Reporting
Please do NOT report security vulnerabilities through public GitHub issues.

Instead, send an email to [security@example.com] with:

Type of issue
Full paths of source files related to the issue
Location of the affected source code
Any special configuration required to reproduce the issue
Step-by-step instructions to reproduce the issue
Proof-of-concept or exploit code (if possible)
Impact of the issue, including how an attacker might exploit it
We will acknowledge receipt of your vulnerability report and send you regular updates about our progress.

Documentation Contributions
We welcome improvements to documentation:

Fix typos and clarify existing documentation
Add examples and use cases
Create tutorials for specific scenarios
Improve inline code documentation
Add diagrams and visual aids
Community
Join our community channels:

Slack Channel
Mailing List
Twitter
Thank you for contributing to Shadow IoT Scanner!
