# Security Review Checklist

- Confirm that public material contains no production Kurogane Hub source code.
- Confirm that no sensitive detection logic is disclosed.
- Confirm that examples use synthetic data only.
- Confirm that credentials, tokens, internal endpoints, customer IP addresses, and real plant details are absent.
- Review trust boundaries between hub, satellite, customer, operator, OT network, and IT network.
- Review data sovereignty assumptions.
- Review SBOM and dependency evidence where access is granted.
- Review hardening principles and operational rollback considerations.
- Use controlled technical review for private core assessment.
