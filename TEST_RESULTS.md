# Module 8 test results and improvement plan
October 24, 2026 — 30 JUnit 4 tests passed, zero failures, using Java 17 with Java 8 bytecode. Exact CLI output is in test-output.txt. Source compilation and packaged application checked separately.

Positive/negative coverage: add valid/duplicate/null; remove existing/missing; update existing/missing/duplicate ID and all nine fields; display stored/empty; file valid/missing/blank/directory/malformed rows; custom score known team/sample team/empty/over-six/duplicate team. Additional checks cover six-slot enforcement, T/F, invalid boolean, supported species, numbered menus and retries, invalid menu values, invalid numeric/date values, rejected setters, and exit.

Changes from Phase 1: T/F shortcuts accepted, numbered type/role menus supplied, species limited to a visible supported catalog. Business operations already take arguments and return results independently of Scanner, so JUnit tests exercise those methods directly.

A first test run caught an incorrect expected sample score in the test fixture: 64.4488888889. Independent arithmetic gave 527/720*40 + 9/18*25 + 4/4*20 + 17.8/100*15 = 64.4477777778. Corrected the expectation; application formula stayed unchanged. Rounded display is 64.45.

Remaining improvements: expand the supported species catalog using a maintained data source; later add persistent database storage and GUI in the assigned phases. Existing tests should run after each change. These tests verify the listed scenarios and do not guarantee every possible input is covered.
