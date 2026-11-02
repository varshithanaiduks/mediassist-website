# MediAssist — rebuilt prototype

A responsive, self-contained front-end prototype reconstructed from the supplied MediAssist project report and Python source-code PDF. The original HTML templates, CSS, JavaScript and dataset were not available, so this is a clean rebuild rather than a restoration of the original application.

## Run locally

1. Extract the ZIP file.
2. Open `index.html` in a modern browser. For the best local experience, run a static server from this folder:

   ```bash
   python -m http.server 8000
   ```

3. Visit `http://localhost:8000`.

No package installation, API key, database or backend is required for this prototype.

## Included

- Responsive landing page and mobile navigation
- Guided symptom check-in with an emergency warning-sign gate
- User-entered symptom summary with downloadable text export
- Searchable health information library with category filters
- Hospital, clinic and pharmacy search via Google Maps
- Optional browser geolocation for map search (permission-based)
- Privacy and safety information modal
- No account, server-side storage or external AI API

## Functional boundaries

- Symptom check-in organises user input. It does not diagnose, rank diseases, calculate clinical risk or recommend treatment.
- Emergency warning signs are a limited safety prompt, not a complete triage protocol. For urgent symptoms in India, call 112 or go to the nearest emergency department.
- Hospital discovery opens an external Google Maps search. It does not verify facility availability, quality, opening hours or emergency capability.
- The health library is general educational copy and requires review by qualified medical professionals before public deployment.
- The prototype does not use the original spreadsheet dataset because it was not supplied.

## Security and provenance

The supplied Python source included plaintext password handling and a hardcoded Flask secret. These patterns were not carried into this static rebuild. No login or account system is implemented.

The original report lists Varshitha K S among four project contributors. This rebuild is based on the supplied project report and source-code PDF; it should not be described as solely authored original work or as clinically validated.

## Before production use

- Medical review of all health content and emergency pathways
- Clinical validation for any intended triage or prediction function
- Privacy notice, consent, retention and security architecture aligned with applicable Indian law
- Secure backend and authentication if accounts are introduced
- Accessibility testing against WCAG 2.2 AA
- Verified hospital/facility data integration and maintenance process
- Monitoring, incident response and clinical governance

## Publish with GitHub Pages

1. Sign in to GitHub and choose **New repository**.
2. Name it `mediassist-website`. Choose **Public** and create the repository. (A public repository is the simplest route for GitHub Pages on standard plans.)
3. In the new repository, choose **Add file → Upload files**.
4. Extract this ZIP on your computer. Open the extracted `mediassist-rebuilt` folder and upload the four files inside it — `index.html`, `styles.css`, `app.js`, and `README.md` — to the repository root. Do not upload only the containing folder; `index.html` must be at the repository root.
5. Commit the upload to the `main` branch.
6. Open **Settings → Pages** in the repository.
7. Under **Build and deployment**, select **Deploy from a branch**. Choose branch `main` and folder `/(root)`, then click **Save**.
8. Wait for the Pages deployment to finish. The public site URL will be `https://YOUR-GITHUB-USERNAME.github.io/mediassist-website/` (replace the username with your GitHub username).

If the Pages section is unavailable, confirm the repository is public and that you have permission to change its settings. GitHub's interface labels can change; the required configuration is branch `main`, folder `/(root)`.
