# Power Screw Workbench: maintainer handover

[One-screen summary](START-HERE.md) · [User manual](USER-MANUAL.md) · [Feature overview](../README.md) · [Recorded validation](../VALIDATION.md)

## Purpose and behaviour to preserve

Compare the geometry, torque and back-driving behaviour of a power screw using an interactive preliminary model. The workspace ties thread inputs to numerical results, an unwrapped-thread explanation and a 3D view, then keeps named design runs for comparison.

- **Geometry:** Load, major diameter, starts, thread angle, pitch or helix angle, and mean-diameter basis. (Browser-local.)
- **Materials and friction:** Screw/nut material, manufacturing process, lubrication and supplier/measured friction override. (Browser-local.)
- **Collar model:** Optional collar friction and mean collar diameter. (Browser-local.)
- **Live results:** Raising torque, back-drive/lowering behaviour, efficiency and disclosed assumptions. (Browser-local.)
- **3D and diagrams:** Orbit, zoom, side/end views, rotation and equivalent nut advance; compare thread starts. (Browser-local.)
- **Saved runs:** Named comparisons and Excel XML, Excel-compatible and JSON exports. (Browser-local.)

The [demo](../demo.html) is a smaller, labelled simulation with fictional data. It explains cause and effect without the real service; it is not evidence of a working production installation. Numbered screenshots in the user manual distinguish actual-app captures from demo captures.

## Files and sources of truth

| Actual package path | Maintainer role |
| --- | --- |
| [projects-host/site/power-screw/index.html](../projects-host/site/power-screw/index.html) | Complete browser calculator checkpoint |
| [demo-source](../demo-source) | Editable demo HTML/CSS/runtime and embedded screenshot tour |
| [SOURCE-MANIFEST.json](../SOURCE-MANIFEST.json) | Original copied-source paths and SHA-256 checkpoint values |

The original working source is under C:/Users/lamon/Desktop/AI TOOLS/NAS for NAS modules; adjacent CAD/watch source locations are recorded by the full backup’s reviewed source manifest. This package contains only the explicitly copied source, not an automatic mirror. The main private nas-projects backup retains the broader shared host context.

## Setup, run and tests

Run commands from this repository root unless a `cd` is shown. Use a disposable checkout and fictional data for first setup. Dependencies, SDKs, signing material and personal data are not bundled. The following are continuation instructions grounded in the retained source, **not commands executed or newly certified by this handover**.

```powershell
python -m http.server 8765 --bind 127.0.0.1
```

/projects-host/site/power-screw/index.html

Selected project check:

No independent automated production test suite is included for this module/single-file package. Use the project-specific checks below and the shared host test suite where applicable; do not invent an `npm test` command.

For the documentation demo alone, serve this repository on loopback with `python -m http.server 8765 --bind 127.0.0.1` and open `/demo.html`. Choose a free port if another preview is running. JavaScript syntax can be checked with `node --check demo-source/runtime.js`. `python demo-source/rebuild.py` rewrites demo.html, so run it only in a disposable checkout or an authorised demo-editing session. A local server cannot provide missing HA/CAD/NAS functions. Inspect browser tests for installed dependencies, fixture requirements and network targets before running them with the approved browser tooling.

## Data, configuration and backup boundaries

Runs/settings are browser-local. JSON is the editable transfer/restore format; spreadsheet output is a report. No server database or actuator integration is included.

Runs and current settings are stored on this device’s browser. Export JSON before clearing site data or changing computers. Spreadsheet exports are for review; JSON is the explicit restore format.

Git preserves reviewed source and documentation. It does not copy browser storage, application databases, uploaded models/photos, accepted device settings, SDKs or credentials. Maintain independent recovery copies of the data identified above, including matching configuration and asset versions. Never add real secrets to examples, issues or logs. Private source copies on GitHub are not proof of a complete NAS/offsite data backup.

## Current verification and Git state

Before these documentation edits on 14 October 2026, this package was clean on branch `main` at `b3d0ae7977c8d6192304e2239305c52ce7d40fb5` and its private upload was verified. All 1 manifest-listed source entries matched their stored checksums before editing. The upload follow-up has completed all 17 repositories and is paused; it does not run this tool or back up its live data.

These handover pages and README links accompany the source package. Preserve them when continuing; stage only reviewed changes. Recheck current `git status --short --branch` and `git diff` before starting. No project-specific background schedule was inspected or changed in this documentation pass. Any service schedules in older notes are historical claims to verify in the actual deployment.

Earlier package checks and limits are recorded in [VALIDATION.md](../VALIDATION.md). This handover adds documentation/link/whitespace/secret and source-preservation checks only. No current NAS release, real hardware state, fresh installation, complete data restoration or offsite-backup freshness was verified here.

## Recovery approach

1. Preserve the current installation/data before changing it. Identify the exact code commit and data snapshot required; do not assume this package matches the running service.
2. Recover source into a new folder. Verify the source manifest and restore the project-specific configuration/assets described above separately. Recreate dependencies from the retained project files and guides.
3. Restore user data into an isolated instance or clean test browser. Check a representative editable record, associated files and save/reload behaviour, then compare to the original. Do not test recovery by overwriting production.
4. Record what actually restored and what remains missing. A demo opening or a passing syntax check is not a production recovery drill. Real deployment/device actions need the existing authorised workflow.

## Known limits and next work

This is a preliminary geometry/friction model. It does not replace checking buckling, fatigue, thread strength, lubrication variation and the actual assembly. No new engineering validation was performed during documentation work.

**Priority:** Check hand-calculated unit cases, starts×pitch lead, friction and collar assumptions, then restore an exported run in a clean browser. Independently check buckling, fatigue, thread strength and the actual assembly; the demo uses a reduced square-thread/no-collar model.

Common symptoms to check for this tool:

- Torque looks wrong: check N versus kg, mm values, starts versus pitch, and collar state.
- Helix field is disabled: it is calculated when pitch is the selected independent input.
- Runs missing: confirm the same browser/origin or restore your JSON backup.

Keep [the release checklist](../RELEASE-CHECKLIST.md) and [third-party notes](../THIRD-PARTY.md) with the package. Original contributions use MIT; bundled/upstream code and assets keep their own licences. Public publication is a separate decision; preparing documentation is not permission to publish.
