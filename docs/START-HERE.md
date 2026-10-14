# Power Screw Workbench: start here

**Continuing this tool? Read [the detailed handover](HANDOVER.md).** For pictures and operation, use the [manual](USER-MANUAL.md) and [offline demo](../demo.html).

Explores screw geometry, force, pitch/starts, friction and torque/backdriving assumptions. Units and the difference between pitch and lead are central to a valid calculation.

**Start with:** Define a meaningful case. Give the run a name, then enter axial force in N and dimensions in mm. Do not enter mass where a force is requested.

**Source:** this is a private source checkpoint, not a live-system mirror. Check [the source manifest](../SOURCE-MANIFEST.json) and current working files before merging.

**Keep your work safe:** Runs and current settings are stored on this device’s browser. Export JSON before clearing site data or changing computers. Spreadsheet exports are for review; JSON is the explicit restore format.

**Next maintainer action:** Check hand-calculated unit cases, starts×pitch lead, friction and collar assumptions, then restore an exported run in a clean browser. Independently check buckling, fatigue, thread strength and the actual assembly; the demo uses a reduced square-thread/no-collar model.

**Status:** private upload verified on 14 October 2026. These guides accompany the source package. Live runtime, data backups and full recovery were not retested. Public sharing was authorised on 14 October 2026; the NAS backup remains private.
