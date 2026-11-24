# Contributing to Masjid Musab bin Umair

*Assalamu Alaikum Warahmatullahi Wabarakatuh!* Thank you for considering contributing your time and skills to **Masjid Musab bin Umair (West Forsyth Islamic Center)**. As a 501(c)(3) non-profit organization, our digital platforms rely on volunteers like you to serve our community as *Sadaqah Jariyah*.

Please read through these guidelines before opening an issue or submitting a Pull Request.

---

## 1. Where Should I Contribute?

Before writing code, make sure you are working in the right repository:

* **[`musab-connect`](https://github.com/masjidmusab/musab-connect) (Next-Gen React & Next.js Platform):** Our active development web application. **All new UI components, features, and improvements belong here.**
* **[`website`](https://github.com/masjidmusab/website) (Live Production Site):** Maintenance and critical bug fixes only.

---

## 2. How to Get Started

1. **Review our Code of Conduct:** All contributors must abide by our [Code of Conduct](https://github.com/masjidmusab/.github/blob/main/CODE_OF_CONDUCT.md).
2. **Find an Issue:** Browse open issues labeled `good first issue` or `help wanted` in the target repository.
3. **Claim the Issue First:** Leave a comment on the issue asking to be assigned before starting work. This prevents multiple volunteers from duplicating effort.
4. **Propose a New Idea:** If you want to build something that does not have an open issue yet, open a Feature Request first so our tech team can confirm alignment with Masjid priorities.

---

## 3. Development Workflow

We follow a **Fork & Pull Request** workflow using two permanent branches: **`staging`** (integration and preview branch) and **`main`** (default branch and live production).

1. **Fork & Clone:** Fork the repository to your personal GitHub account and clone it locally.
2. **Create a Feature Branch off `staging`:** Never commit directly to `staging` or `main`. Always branch off **`staging`** using a descriptive `kebab-case` name:
   ```bash
   git checkout staging
   git pull origin staging
   git checkout -b feat/prayer-times-widget
   ```
   *Branch naming examples:* `feat/prayer-times-widget`, `fix/mobile-donation-button`, `docs/update-setup-guide`
3. **Keep Secrets Out of Git:** Never commit `.env` files, `wp-config.php`, API keys, database credentials, or donor/member data. Use `.env.example` with dummy values if adding new configuration variables.
4. **Test Your Changes:**
   * Verify the build succeeds without errors or linter warnings.
   * Test responsiveness on both desktop and mobile viewports.
   * Double-check critical community flows (prayer times, Jummah schedules, and donation links).
5. **Use Clear Commit Messages:** We follow [Conventional Commits](https://www.conventionalcommits.org/) (e.g., `feat: add Jummah khutbah schedule card`, `fix: resolve mobile navbar overflow`).
6. **Open a Pull Request into `staging`:**
   * Change the **base** branch dropdown from `main` to **`staging`** (GitHub pre-selects `main` by default, and direct PRs to `main` from feature branches or forks are blocked automatically).
   * Fill out the Pull Request checklist completely and link the related issue (e.g., `Closes #12`).

### Maintainer Merge & Release Policy

* **Feature PRs (`feat/*`, `fix/*`, `docs/*` -> `staging`):** Merged using **Squash and merge** to keep history clean.
* **Production Releases (`staging` -> `main`):** Promoted once verified on staging using **Create a merge commit** (never squash merge `staging` into `main`).
* **Urgent Hotfixes (`hotfix/*` -> `main`):** Branched off `main` for critical production issues, merged into `main`, and synced back into `staging`.

---

## 4. Need Help?

* **Technical & Onboarding Questions:** Reach out to our engineering team at **[tech@masjidmusab.com](mailto:tech@masjidmusab.com)**.
* **General Inquiries:** For non-technical questions regarding prayers, events, or Masjid services, contact **[info@masjidmusab.com](mailto:info@masjidmusab.com)**.
