# Lab 4: Advanced Deployment Strategies & Enterprise DevOps

**Course:** DevOps and Automation Lab | B.Tech CSE (AI & ML)
**Author:** Harsh Sen (2301730194) | K.R. Mangalam University, Gurugram

Seven experiments covering disaster recovery, CI/CD testing, release strategies, GitOps, secret management and a comparative report. Everything runs locally on Linux with Python 3, Bash and Git.

## Experiments

| # | Experiment | Key result |
|---|------------|-----------|
| 4.1 | [Disaster Recovery](Lab4_Q1_Disaster_Recovery_Harsh_Sen_2301730194.pdf) | Restore in 0.056 s, failover in 1.00 s, RPO = 1 h |
| 4.2 | [CI/CD Automated Testing](Lab4_Q2_CICD_Automated_Testing_Harsh_Sen_2301730194.pdf) | Buggy build blocked at unit-test gate; 100% coverage on clean build |
| 4.3 | [Blue-Green Deployment](Lab4_Q3_Blue_Green_Deployment_Harsh_Sen_2301730194.pdf) | 100% availability (0 of 1,399 failed) vs 58.33% in-place; 15 ms rollback |
| 4.4 | [GitOps Delivery](Lab4_Q4_GitOps_Delivery_Harsh_Sen_2301730194.pdf) | About 1 s drift correction and rollback via `git revert` |
| 4.5 | [Advanced Strategies Report](Lab4_Q5_Advanced_Deployment_Strategies_Report_Harsh_Sen_2301730194.pdf) | Comparison, risk analysis and recommendations |
| 4.6 | [Secret Management (Vault)](Lab4_Q6_Secret_Management_Vault_Harsh_Sen_2301730194.pdf) | AppRole short-lived tokens, least privilege, rotation, audit, encryption at rest |
| 4.7 | [Canary Deployment](Lab4_Q7_Canary_Deployment_Harsh_Sen_2301730194.pdf) | Bad builds rolled back at the 10% step, about 10% of users exposed |

## Tools

- **Languages and CLI:** Python 3, Bash, Git, cron
- **CI/CD:** GitHub Actions, pytest, pytest-cov, flake8, Flask
- **Data and DR:** SQLite, gzip, SHA-256 checksums
- **Secrets:** OpenBao (Vault fork), KV v2, AppRole, `hvac`
- **GitOps reference:** Argo CD / Flux (simulated with a Python reconciler)

## Takeaway

No single approach covers every risk. An enterprise pipeline combines **GitOps** for delivery, **Canary or Blue-Green** for releases, **vault-managed secrets**, and **tested disaster recovery**.
