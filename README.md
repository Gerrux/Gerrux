# Ilya Kalinin

ML Engineer — Computer Vision & LiDAR. I build the automated forest inventory stack at Open Forest: from raw ALS point clouds to inventory reports and regulatory XML.

Performance and measurable model quality over everything else. Every metric below was earned against curated ground truth, and most of the dead ends are documented too.

### Work

- **Individual tree detection on airborne LiDAR.** 3D ResUNet voxel detector with apex refinement and density-aware NMS. F1 0.885 and sub-meter height error on a 44-plot, 22k-tree benchmark spanning summer and winter scans across Russia.
- **Tree species classification.** Regional CatBoost models on hand-designed geometric, spectral and penetration features, exported to ONNX so inference has no training-framework dependency. Leave-one-dataset-out validation is the gate, not in-sample F1.
- **Rust point cloud core.** A 12-crate Rust monorepo behind the desktop app and the cloud worker via PyO3: ground filtering (SMRF, 5–20× faster than the Python CSF it replaced), segmentation, chunked processing of 100M+ point scenes. Started as an R and C++ prototype pipeline; now one codebase for desktop and cloud.
- **Products around the models.** Arboritm, a PySide6 desktop app for forest inventory with regulatory TOL/XML export. Arbogeo, a Tauri desktop GIS with point clouds as first-class layers. A web platform on Yandex Cloud with on-demand GPU workers. An annotation tool for LiDAR ground truth with OBB-rotated chunking and GPU-side filtering.

### How I build

- Agent-driven development is the default workflow. Daily across **Claude Code**, **Codex** and **OpenCode**; skills, memory and project instructions are kept portable between harnesses.
- Experiment logs, dead ends and decisions live in agent-readable memory next to the code, so the next session starts where the last one stopped.
- I build tooling for that workflow too: an ML experiment runner for Kaggle and Vast.ai with a Claude Code skill, a fail-closed traffic guard for Windows, focus and note utilities in Rust.
- The stack is whatever the task needs. Agents removed most of the cost of switching languages, so I pick by fit, not by habit.

### Contact

[![Telegram](https://img.shields.io/badge/Telegram-@gerrux-2CA5E0?style=flat-square&logo=telegram&logoColor=white)](https://t.me/gerrux)
[![Email](https://img.shields.io/badge/Email-kalinin.ilya06@yandex.ru-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:kalinin.ilya06@yandex.ru)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-gerrux-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gerrux/)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://awesome-github-stats.azurewebsites.net/user-stats/Gerrux?cardType=github&theme=dark&preferLogin=false">
  <img alt="GitHub stats" src="https://awesome-github-stats.azurewebsites.net/user-stats/Gerrux?cardType=github&theme=default&preferLogin=false">
</picture>

Pinned repositories below show the rest.
