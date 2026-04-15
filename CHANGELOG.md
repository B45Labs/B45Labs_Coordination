## Changelog
All notable changes to this project will be documented in this file.

This project adheres to [Semantic Versioning](https://semver.org/) and follows the [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) standard.

---

## [1.1.0] – 2026-05-01

> Check Spelling, Find & Replace, major command rebuilds, and a full platform upgrade.

### Added
- **New Commands (3)**
  - **Check Spelling** — detects spelling errors across text parameters in the model,
    with offline dictionary support (en-US, pt-BR, es-ES) and a custom BIM vocabulary
    filter. Project dictionary supports Export/Import.
  - **Find & Replace** — batch find and replace text across parameters and elements
    throughout the model in a single non-modal operation.
  - **Find** — quick single-term search across model text parameters.
- **Website** — full documentation hub accessible directly from the ribbon. Includes
  command-by-command explanations, short video tutorials, step-by-step guides,
  screenshots, and a user roadmap where users can request features, track
  development, and report issues.
- **Stripe** — support/donation platform upgraded to Stripe for a smoother,
  more reliable experience.
- **Platform — Revit 2027 (Beta)** — experimental support for Revit 2027 via
  `net10.0-windows` build configuration.

### Changed
- **Copy Detail Sheets** — fully rebuilt engine and UX. Faster, more reliable,
  and significantly smoother to use.
- **Create Sheets** — rebuilt from the ground up with a more fluid UX and
  improved error handling throughout.
- **Check Levels, Check Walls, Check Rooms** — UX improvements and expanded
  usage data collection for better analytics.
- **Check Coordinates** — graphical and UX improvements.
- **Parameter Control** — UX refinements.
- **User Profile** — Complete window redesign. New two-column layout with avatar
  card and profile-completion progress. Added *Experience with Revit* selector and
  multi-select discovery tags (with free-text detail for *Other* and
  *Conference / talk*). Legacy saved profiles are migrated automatically.
  Ribbon button label updated to *User Profile*.
- **Sync Sheet Issue Date** — UX improvements.
- **Move Views, Copy View to Sheet, Copy Legends, Copy Schedules** — stability
  improvements across the Documentation panel commands.
- **Documentation panel availability** — *Copy Legends* and *Copy Schedules*
  now require an active sheet (were always enabled); *Create Sheets* and
  *Sync Sheet Issue Date* are now always enabled (previously required an
  active sheet). Behavior now matches what each command actually needs.
- **Check Model Version / Upgrade Model Version** — now accessible without
  an open model.
- **Security** — security improvements across all commands and data collection
  paths; usage and performance telemetry refined and validated.

### Fixed
- PDF, Excel, and other export operations — stability and output corrections.

### Notes
- Full support: **Revit 2023, 2024, 2025, and 2026**.
- Beta support: **Revit 2027**.
- Feedback and bug reports: [support@b45labs.com](mailto:support@b45labs.com)

---

## [1.0.4] – 2026-04-06

> The biggest update yet — 4 new features, a smarter parameter workflow,
> and a full stability pass across the entire add-in.

### Added
- **New Commands (4)**
  - **Parameter Control** — the most requested feature is here. Create, manage, and
    export shared and project parameters without ever leaving Revit. Batch-create
    parameters across multiple categories and groups, inspect everything bound to
    your model, and export to a Revit-ready `.txt` or Excel file in one click.
  - **Model Progress Analyzer** — track your model's evolution over time. Capture
    snapshots of 14+ key metrics and compare them as the project develops. Snapshots
    travel with your `.rvt` file — no external database, no extra steps.
  - **My Profile** — personalize your B45 Labs experience. Set your name, company,
    role, and industry. Your preferred name appears in your greeting every time you
    open the add-in.
  - **Website Button** — quick access to the B45 Labs website directly from the
    ribbon. Release notes, documentation, and roadmap always one click away.

### Changed
- **Check Levels** — more reliable, with improved error handling and edge case coverage.
- **Check Walls** — batch processing stability improvements.
- **Check Parameters** — broader parameter coverage and cleaner error reporting.
- **Code Quality** — general stability pass across all existing commands.
- **Security** — full audit completed. No sensitive data is collected, stored,
  or transmitted.

### Fixed
- **Telemetry** — resolved stability issues in the background data pipeline,
  including session tracking and thread-safety fixes.

### Notes
- Compatible with **Revit 2023, 2024, 2025, and 2026**.
- Feedback and bug reports: [support@b45labs.com](mailto:support@b45labs.com)

---

## [1.0.3] – 2026-03-18 *(Beta)*

### Added

- **New Commands (6)**
  - Check Levels — validates level naming, elevation consistency, and ordering.
  - Check Walls — audits wall types, constraints, and structural parameters.
  - Check Rooms — checks room naming, area, and placement validity.
  - Sync Sheet Issue Date — batch-updates the issue date parameter across sheets.
  - Check Model Version — inspects and reports the Revit version of external files.
  - Upgrade Model Version — batch-upgrades external files to the current Revit version.

- **User Profile**
  - New *My Profile* tab in the About window.
  - Fields: Full Name, Preferred Name, Email, Company, Role, Industry, Sector, How you found us.
  - Preferred Name is used for avatar initials and the greeting message.
  - Profile is saved locally (`%AppData%\B45Labs\user-profile.json`) and synced to Bubble in the background.

- **Platform — Revit 2023 and 2024**
  - Expanded support from Revit 2025/2026 to all four versions: 2023, 2024, 2025, 2026.
  - Unified build system (R23/R24 via `net48` legacy project; R25/R26 via `net8.0-windows`).

### Changed

- **UI — Complete Redesign**
  - All command windows and dialogs rebuilt with the new Autodesk-style visual language.
  - Unified dark theme: consistent colors, spacing, typography, and corner radii throughout.
  - Autodesk brand blue (`#0696D7`) replaces the previous accent (`#2E7CF6`) across all surfaces.
  - Blue divider accent line below every title bar — consistent across all windows.
  - Flat button style (no drop shadows), uniform input field height (`34px`), and tighter spacing.
  - Icons, status bars, toolbar buttons, and DataGrid row styles aligned to the new design system.

- **Code Quality**
  - General stability improvements and internal refactors aligned with B45 coding standards.
  - Improved error handling and best-effort patterns across all commands.
  - `ElementId.Value` used consistently throughout (removed all `.IntegerValue` usages for R25/R26 compatibility).

- **Security**
  - Full security review pass on all commands and telemetry paths.
  - Confirmed: no sensitive data is collected, stored, or transmitted.

### Notes
- This is a **beta release**. Installer distributed as `B45Labs_Installer_v1.0.3_Beta`.
- Compatible with **Revit 2023, 2024, 2025, and 2026**.
- Feedback and bug reports: [support@B45Labs.com](mailto:support@B45Labs.com)

---

## [1.0.2] – 2026-03-01

### Added
- **Documentation Tab (6 new commands)**
  - Move Views
  - Duplicate Views
  - Copy Legends
  - Copy Schedules
  - Create Multiple Sheets
  - Copy Sheet From Another Model
- **UI / About**
  - Updated the About Me content and added an optional donation button.

### Changed
- **UI & Experience**
  - Improved UI consistency across dialogs, icons, and output messages.
  - Rebuilt the About Me experience (layout, content, and behavior).
- **Core Tools**
  - Refactored Check Coordinates for higher reliability and maintainability.
- **Telemetry & Insights**
  - Upgraded usage/error tracking to better understand command distribution and error patterns.
  - Improved mapping consistency for higher reporting quality.
- **Security & Privacy**
  - Completed a code + telemetry security review (no sensitive data is collected).
- **Stability & Maintainability**
  - General stability improvements and internal refactors aligned with B45 coding standards.

### Fixed
- Fixed YouTube link (PT-BR tutorials recorded and currently being published; EN tutorials coming soon).
- Fixed installer issues that could cause installation failures.

### Distribution
- Implemented digital signing for trusted distribution.

---

## [1.0.1] – 2026-01-27

### Changed
- **Legal / Compliance**
  - Updated Terms of Use (EULA) to clarify that B45 Labs is not a technical authority and that all outputs must be independently validated by the user.
  - Updated Privacy Policy wording to clarify telemetry motivations, limitations, and that no sensitive personal data is intentionally collected.
- **Documentation**
  - Updated README telemetry/diagnostics description and references to PRIVACY.md and TERMS.md.
  - Updated SECURITY and SUPPORT references for consistency.

---

## [1.0.0] – 2026-01-01

### Improved
- **Rebrand (BIM Genie → B45 Labs)**
  - Updated naming across UI, ribbon tabs, commands, and documentation.
  - Plugin identity surfaces aligned with the new B45 Labs brand (labels, dialogs, and messaging).
- **Platform & Architecture**
  - Internal refactor to improve stability, maintainability, and long-term scalability.
  - Cleaner separation between UI, core services, and Revit API logic.
- **User Experience**
  - More consistent dialogs, icons, and output formatting across tools.
  - Improved clarity of execution messaging and results for QA/QC review workflows.
- **Reliability & Diagnostics**
  - Best-effort behavior expanded: isolated failures are less likely to break entire operations.
  - Logging and error handling refined for more stable sessions and easier troubleshooting.

### Added
- **New Commands / Toolset Expansion**
  - New commands introduced as part of the ongoing B45 Labs roadmap.
  - Feature coverage expanded across existing tool categories.
- **Compatibility**
  - Added support and validation for Revit 2026 (while maintaining Revit 2025 compatibility).

### Notes
- First stable release, focused on rebranding and platform stabilization.
- Compatible with **Revit 2025** and **Revit 2026**.

---

## [0.0.11-beta] – 2025-08-30

### Improved
- **Get Element Coordinates**
  - Rewritten for higher precision using cross-reference with Spot Elevation.
  - Now automatically detects Survey Point clip status (clipped/unclipped).
  - Fixed X/Y value inversion in specific project contexts.
  - Results are now formatted for better readability (X, Y, Z in clear columns).
  - Organized presentation: Survey Point → Base Point → Internal Origin.
- **Check Coordinates**
  - Now powered by the new `Get Element Coordinates` engine with full precision.
  - Added detection of misalignment between Survey and Base Points.
  - Output messages are clearer and more consistent, with feedback on detected issues.
  - Logic simplified for easier maintenance.
- **Check Model Health**
  - New command: **Links & Imports Breakdown** – analyzes linked RVT and CAD files.
  - Performance optimized in data collection using `FilteredElementCollector`.
  - Better segmentation of internal checks by theme (Overview, Views, Elements, Links...).
  - Outputs are now more user-friendly for reading and auditing.

### Fixed
- Fixed bug where coordinates were mirrored in some models.
- Visual and rotation adjustments to icons in the "Model Check" tab.
- Fixed bug affecting models with multiple active survey points.

### Notes
- Beta release, compatible with **Revit 2025** only.

---

## [0.0.10-beta] – 2025-07-23

### Added
- Move Views, Toggle Reference Points, Clear View With/Without Links, Reset Chat.
- New icons for all tools, including light/dark variants.
- New command groups in the Ribbon.

### Changed
- Full Ribbon redesign with commands grouped by category.
- Improved dark/light theme detection with dynamic icon switching.

### Fixed
- Command routing inconsistencies due to refactoring.
- Tooltip duplication and icon flickering in light mode.
- Issue where painted elements were not being correctly reset.

### Notes
- Beta release, compatible with **Revit 2025** only.

---

## [0.0.9-beta] – 2025-06-05

### Changed
- Reorganized ribbon commands across appropriate categories.
- Standardized internal command naming for consistency across UI, Assistant, and tracking.

### Fixed
- Button order inconsistencies, tooltip mismatches, and internal mapping issues.

---

## [0.0.8-beta] – 2025-05-30

### Added
- Check Model Health, Check Parameters, Check Painted Elements.
- Export/Import Worksets, Select All In-Place Elements, Clear/Reset Painted Elements.
- External Tools tab (Check Model Version, Upgrade Model Version).
- Change Language, Plug-in Info, YouTube Tutorials.

### Changed
- NWC View, Clash Map, Clear View Preserve Links enhanced.
- Ribbon restructured into consistent user-friendly groups.
- B45 Labs Assistant: dark/light mode, Enter key, Clear Chat button.

### Fixed
- Duplicate `.addin` file creation, JSON serialization issues, visual layout in light theme.

---

## [0.0.7-beta] – 2025-04-12

### Changed
- Clear View command now supports views with View Templates.

### Fixed
- Scroll behavior issue in the B45 Labs Assistant panel.

---

## [0.0.6-beta] – 2025-04-03

### Added
- Analytics: continent, country, city, screen resolution.
- Geolocation API integration.

### Changed
- Assistant personality refined; improved UI/UX interactions.

---

## [0.0.5-beta] – 2025-04-02

### Added
- Bubble sync fully operational.
- "Clear Conversation" button in Assistant.

### Changed
- Clash Map performance improved; Clear View refined.

---

## [0.0.4-beta] – 2025-03-25

### Changed
- Stability, memory, and error handling improvements.
- Unified focus on Revit 2025+ API.

---

## [0.0.3-beta] – 2025-03-23

### Changed
- SQLite database path updated to `C:\ProgramData\B45Labs`.
- Improved version check system and update prompt UX.

---

## [0.0.2-beta] – 2025-03-21

### Changed
- Plugin metadata and text refinements for public testing.

---

## [0.0.1-beta] – 2025-02-20

### Added
- Initial release: core activity tracking, command usage logging, error reporting.
- Local SQLite database and background Bubble sync structure.
