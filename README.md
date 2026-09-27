# Practical 2 - Alternative Responsive Layouts

Student Name: Xiaoyiheng

Student ID: 20243007025

This Android Studio project builds on the LinearLayout version of Practical 1. The Practical 1 portrait layout structure is retained, with its on-screen titles updated for Practical 2, and two alternative XML layouts have been added. All layouts were written in XML.

| Configuration | Resource file | Design |
| --- | --- | --- |
| Default phone portrait | `app/src/main/res/layout/activity_main.xml` | Practical 1 layout structure with weighted vertical sections and updated titles |
| Phone landscape | `app/src/main/res/layout-land/activity_main.xml` | Two columns, with titles on the left and colored words, application label, and buttons on the right |
| Tablet, smallest width 600dp or greater | `app/src/main/res/layout-sw600dp/activity_main.xml` | Spacious two-column layout with larger text and padding |

The same `activity_main.xml` resource name is used in all three directories. Android chooses the resource for the current configuration; `MainActivity` still calls `setContentView(R.layout.activity_main)`. Widths and heights adapt using weights, `0dp`, `match_parent`, and `wrap_content`. `dp` and `sp` are used for spacing and text.

## Build and run

1. Open this directory as a project in Android Studio.
2. Let Gradle sync, then run the `app` configuration on a phone emulator.
3. Rotate the phone to landscape and verify that the two-column layout appears.
4. Run on a tablet emulator with a smallest width of at least 600dp and verify the tablet layout.

The Change and Cancel buttons come from Practical 1 and demonstrate layout only; no click behavior was requested for this practical.

## Validation

- `:app:assembleDebug --offline --no-daemon` completed successfully with Android SDK 37.
- Installed and visually checked the app on the Pixel 6 API 37.1 emulator in portrait and landscape.
- Checked the `sw600dp` layout at exactly 600dp and 1067dp smallest widths using emulator display size and density overrides; all content and buttons remained visible.
- Booted a Pixel Tablet API 35 emulator at 800dp smallest width and visually verified that the tablet layout and updated Practical 2 titles appear.
