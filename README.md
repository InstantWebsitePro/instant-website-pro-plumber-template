# Instant Website Pro Plumber Publishing System V7

This repository is a **nonvisual publishing and safety foundation** for the V7 plumber program. It protects imports, public/private boundaries, checks, deployment, optional configured monitoring, and rollback without deciding what a plumber’s website should look like.

The two supported routes share one public contract:

- **Desktop:** ChatGPT/Codex builds the approved website in `public/`, runs the checks, and publishes through an isolated private GitHub repository.
- **Phone fallback:** ChatGPT produces one complete approved `website.zip`; the owner uploads that one file when connected tools cannot complete the GitHub step. A workflow validates it before atomically replacing `public/`.
- **Hosting:** Cloudflare Pages Git integration deploys `public/` from GitHub `main`, plus optional Pages Functions under `functions/`.

A rejected phone package never changes the existing public site.

## Blank-canvas rule

The committed `public/` directory is a neutral waiting shell, not a design template. The real website begins with an owner-reviewed homepage concept derived from approved facts, media, trade, customers, service area, proof, and business personality. Only after the owner approves that concept does ChatGPT build the full site. The full build may replace every file in `public/` and use an original page structure, local fonts, SVG graphics, icons, imagery, animation, CSS, and JavaScript permitted by the safety policy.

## Privacy boundary

```text
private business-assets source      owner facts, originals, approvals; never commit
                |
                v
handoff/                            minimum approved public facts and decisions
                |
                v
public/                             deployable website files only

protected infrastructure
  .github/ functions/ infrastructure/ scripts/ tests/ templates/ AGENTS.md
```

## Repository map

```text
.github/workflows/                validation, phone import, rollback, health checks
public/                           public website files only
functions/api/                    optional Cloudflare Pages form endpoints
handoff/                          minimum approved public build context
infrastructure/                   protected V7 contracts and activation record
scripts/                          validator, packager, importer, live checker
tests/                            production and hostile-input regression tests
templates/                        optional implementation snippets
website.zip                       one-file phone transport; initial copy is a placeholder
```

## V7 package contract

`website.zip` must contain the whole production website with `index.html` at ZIP root, pass `infrastructure/importer-policy.json`, and use manifest/workflow/repository package version `6.0`. It must contain no wrapper folder, nested archive, bundled video, secret, private business source, raw capture, office workbook, or protected program file.

The manifest records every page, preserved old route, public document, icon, external media item, optional form, and the confirmed plumber profile. Old working URLs stay at the same path and purpose by default. Exact permanent redirects are exceptions; wildcard-to-home migration is rejected.

## Standard Cloudflare Pages setup

Use **Git integration**, no framework preset, the repository root, a blank build command, `public` as the build output directory, and `main` as the production branch. Authorize the Cloudflare GitHub app only for the intended repository when possible. A tested `exit 0` build command is acceptable only if a particular existing Pages project refuses an empty field and is rehearsed with this exact static contract.

Dashboard upload of this repository does not compile its `functions/` folder. A correctly compiled API/Wrangler deployment can exercise the live runtime, but is separate from Git integration and does not prove Git-triggered deployment. A Direct Upload project requires a new project to adopt Git integration. See `infrastructure/ACTIVATION_REHEARSAL.md` for the evidence boundaries.

## Local checks

```bash
python3 scripts/release_check.py
python3 scripts/validate_site.py public --mode production --repo-root .
python3 scripts/package_site.py --source public --output website.zip --repo-root .
```

The packager creates a deterministic ZIP, imports it into a temporary directory, reruns production validation, and compares the extracted files before replacing the previous package.

## Launch and rollback

The owner approves the homepage concept, reviews the exact finished website and approves final public launch. Reuse existing setup authorization; ask once only if the intended technical scope is not already authorized. Routine repository, Pages, HTTPS, redirect, checks and restore-point work then proceeds without repeated technical questions. Configure monitoring only when it is actually part of the agreed service. Disclose a hosted preview’s public reachability before upload, and verify access controls if confidentiality is required. An unchanged finished version does not need a second hosted-preview approval. Material changes, unresolved review requests and final go-live still require the appropriate owner decision.

For immediate hosting recovery, use Cloudflare deployment history. For source recovery, run **Roll back website files** with a known-good full commit SHA. Never force-push or erase normal history.

Use `infrastructure/ACTIVATION_REHEARSAL.md` to verify a new shared template revision. Record publication, Git integration acceptance and any separate runtime test honestly. The blank template does not need a customer domain migration, inbox recipient or phone number; those checks apply when that customer’s site is built.

## V7 plumber release and transport compatibility

This is the **Plumber Program V7** starter. It contains no customer's approved business facts and no completed plumbing website. The `business_type: contractor`, `contractor_profile` and 6.0 schema/package fields are retained for compatibility with the tested publishing protocol; they are internal fields. The public starter identifies the plumbing trade and makes no service, credential, availability or emergency promise.

Forms are disabled until the owner's destination and Turnstile settings are configured and tested. V7 requires an explicit allowed HTTPS origin and server-verified Turnstile. `REQUIRE_TURNSTILE=false` does not bypass verification. Use encrypted deployment secrets and retain a visible verified telephone fallback. “Submitted” is a request for contact, not a dispatch or confirmed booking.

Noindex rules cover the Pages project and preview aliases. These URLs remain publicly reachable unless access controls are separately configured and tested. The production custom-domain launch must remove starter noindex/robots blocks only after the real site is approved.

The template URL is https://github.com/InstantWebsitePro/instant-website-pro-plumber-template. Publication, template status, source parity, GitHub Actions and the advertised Git-to-Pages route are verified against the exact released source. A separate API/Wrangler deployment is runtime evidence only. A previous version's validation is not evidence for V7. Contact program support at support@instantwebsitepro.com without sending passwords, tokens or customer details.
