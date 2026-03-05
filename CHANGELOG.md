# Changelog

Document meaningful changes in plain language. Focus on functional impact, not file churn.

---

## 2026-03-05
- changed archive ignore pattern from `**/inputs/archived/**` to `**/_archive/**` in both .cursorignore files — the underscore prefix keeps `_archive/` at the top of sorted file trees, and the broader glob catches archive folders anywhere (inputs, outputs, or project-level)
- updated README.md folder structure diagram and managing context section to reflect the `_archive/` convention

## YYYY-MM-DD
- example: what changed and why, in past tense
- mention file paths when helpful

