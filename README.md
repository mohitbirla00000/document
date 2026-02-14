# soit-website-docs
The main public website document repository for SOIT, RGPV, Bhopal.

# README.md for `soit-docs-cdn`

## 🏫 SoIT RGPV - Document Repository

This repository serves as the central storage for all official academic documents for the **School of Information Technology (SoIT), UTD-RGPV**. These files are served dynamically to the [SoIT Official Website](https://soitrgpv.ac.in).

### 📁 Directory Structure

To keep the website filters working correctly, please follow this naming convention:

```text
/
├── schemes/
│   ├── Scheme-<Branch>-<Semisters Covered>-Sem.pdf
│   ├── Scheme-AIML-I-VIII-Sem.pdf
│   └── Scheme-CSDS-I-VIII-Sem.pdf
├── syllabuses/
│    ├── Syllabus-<Branch>-<Semisters Covered>-Sem.pdf   
│   ├── Syllabus-AIML-I-VIII-Sem.pdf
│   └── Syllabus-CSDS-I-VIII-Sem.pdf
└── ordinances/
    └── Taken and used directly from RGPV official Website and CDN for efficiency.

```

### 🚀 How to Link Files to the Website

Since this is a public repository, you can access any file via the **jsDelivr CDN** (recommended for speed).

**Format:**
`https://cdn.jsdelivr.net/gh/[Your-Username]/[Repo-Name]@[Branch]/[Path-to-File]`

**Example for CSE Scheme:**
`https://cdn.jsdelivr.net/gh/your-username/soit-docs-cdn@main/schemes/btech-cse-2022-scheme.pdf`

### 🛠 How to Add New Documents

1. **Upload:** Drop the PDF into the appropriate folder.
2. **Naming:** Use lowercase and hyphens (e.g., `aiml-sem-5.pdf`)—avoid spaces to prevent URL encoding issues.
3. **Commit:** Use a descriptive message like `feat: add 2026 AI-ML syllabus`.
4. **Sync:** The website will reflect changes automatically if you are fetching the file list via the GitHub API.

---

## 💻 Developer Integration (Next.js)

If you want to automate the "Syllabus" page on the main site, you can fetch the file list using the **GitHub Octokit API**:

```typescript
// Example: Fetching all files in the 'syllabuses' folder
const response = await fetch('https://api.github.com/repos/[User]/[Repo]/contents/syllabuses');
const data = await response.json();
// This returns an array of file names and download URLs

```

### ⚖️ License & Usage

This repository contains official academic documents intended for public distribution to students and faculty of the School of Information Technology, UTD-RGPV.

---
