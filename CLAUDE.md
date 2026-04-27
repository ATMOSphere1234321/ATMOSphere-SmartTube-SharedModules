# CLAUDE.md — smarttube-player / MediaServiceCore / SharedModules

Nested SharedModules used by the MediaServiceCore YouTube backend. ATMOSphere
fork. This is the deepest submodule level — pointer cascade goes:

`SharedModules` → `MediaServiceCore` → `smarttube-player` → Android-15 parent.

This module is bound by the parent ATMOSphere Constitution and parent
`smarttube-player` submodule guidelines.

## MANDATORY ANTI-BLUFF VALIDATION (Constitution §8.1 + §11)

**This submodule inherits the parent ATMOSphere project's anti-bluff covenant.
A test that PASSes while the feature it claims to validate is unusable to an
end user is the single most damaging failure mode in this codebase.**

1. Tests MUST validate user-visible behaviour, not just metadata. Code
   changes here surface inside MediaServiceCore which surfaces inside
   SmartTube playback — verify the user-visible path on the flashed device.
2. PASS / FAIL / SKIP mechanically distinguishable.
3. Every parent-repo gate that depends on this submodule MUST have a paired
   mutation in `scripts/testing/meta_test_false_positive_proof.sh`.
4. The bar is not "tests pass" but "users can use the feature."

## MANDATORY COMMIT & PUSH CONSTRAINTS

1. **ONLY use `bash scripts/commit_all.sh "message"` from the PARENT REPO ROOT**
   (the Android-15 root). The 4-deep cascade is automated there.
2. Never use `git commit` / `git push` directly here.

## MANDATORY ABSOLUTE DATA SAFETY — ZERO RISK (Constitution §9)

EVERY destructive repository operation MUST follow parent Constitution §9.
