# Audit and improvement plan for clockblind

## Current state

- The repository contains a CSV data file `occult_anomalies.csv` and a minimal `README.md` that only states the project name and a brief tagline.
- There is no license file or contribution guidelines.
- No continuous integration or automated checks are configured.
- Security and dependency update notifications (Dependabot) are not enabled.
- Branch protection is not configured on the `main` branch.

## Recommended improvements

1. **Add an open source license**: Include an MIT license so others know how they can use the content.
2. **Improve the README**: Write a clear, professional README explaining:
   - The purpose of the clockblind project as a mapping prototype using the `occult_anomalies.csv` data.
   - Features and technologies used (e.g., data exploration, potential visualization).
   - Instructions to clone the repo and explore the CSV file (and any future code).
   - Usage examples or how to extend the prototype.
   - A license section referencing the MIT license.
   Avoid emojis or decorative hyphens; use simple bullet points.
3. **Set up continuous integration**: Add a `.github/workflows/ci.yml` workflow that runs on push and pull requests to `main`. For now this can simply check out the repository and run a placeholder script (e.g., `echo "CI check passed"`). This creates a required status check for branch protection.
4. **Enable Dependabot and GitHub Actions**: Turn on automated dependency and security alerts in the repository settings to keep the project up to date.
5. **Enable branch protection**: Require pull requests for changes to `main` and enforce the CI check.
6. **Data organisation** (optional): Consider moving the CSV file into a `data/` directory for clarity if more files are added.
