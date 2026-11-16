---
version: alpha
name: Signal Android Design System
description: Canonical UI guidance for Signal Android, led by SignalTheme and Material 3 with XML compatibility for existing View screens.
colors:
  primary: "#2C58C3"
  primary-container: "#D2DFFB"
  secondary: "#586071"
  secondary-container: "#DCE5F9"
  surface: "#FBFCFF"
  surface-1: "#F1F3F8"
  surface-2: "#EDF0F6"
  surface-3: "#E8ECF4"
  surface-variant: "#E7EBF3"
  background: "#FBFCFF"
  on-primary: "#FFFFFF"
  on-primary-container: "#051845"
  on-secondary: "#FFFFFF"
  on-secondary-container: "#151D2C"
  on-surface: "#1B1B1D"
  on-surface-variant: "#545863"
  on-background: "#1B1D1D"
  outline: "#808389"
  error: "#BA1B1B"
  error-container: "#FFDAD4"
  on-custom: "#FFFFFF"
  on-custom-variant: "#FFFFFFB3"
  warning: "#B448281F"
  on-warning: "#B44828"
  alert: "#EF5350"
  scrim-light: "#00000014"
  scrim: "#00000066"
typography:
  display-large: { fontFamily: Roboto, fontSize: 57px, fontWeight: 400, lineHeight: 64px, letterSpacing: -0.25px }
  display-medium: { fontFamily: Roboto, fontSize: 45px, fontWeight: 400, lineHeight: 52px, letterSpacing: 0px }
  display-small: { fontFamily: Roboto, fontSize: 36px, fontWeight: 400, lineHeight: 44px, letterSpacing: 0px }
  headline-large: { fontFamily: Roboto, fontSize: 32px, fontWeight: 400, lineHeight: 40px, letterSpacing: 0px }
  headline-medium: { fontFamily: Roboto, fontSize: 28px, fontWeight: 400, lineHeight: 36px, letterSpacing: 0px }
  headline-small: { fontFamily: Roboto, fontSize: 24px, fontWeight: 400, lineHeight: 32px, letterSpacing: 0px }
  title-large: { fontFamily: Roboto, fontSize: 22px, fontWeight: 400, lineHeight: 28px, letterSpacing: 0px }
  title-medium: { fontFamily: Roboto, fontSize: 18px, fontWeight: 400, lineHeight: 24px, letterSpacing: 0.0125px }
  title-small: { fontFamily: Roboto, fontSize: 16px, fontWeight: 500, lineHeight: 22px, letterSpacing: 0.0125px }
  body-large: { fontFamily: Roboto, fontSize: 16px, fontWeight: 400, lineHeight: 22px, letterSpacing: 0.0125px }
  body-medium: { fontFamily: Roboto, fontSize: 14px, fontWeight: 400, lineHeight: 20px, letterSpacing: 0.0107px }
  body-small: { fontFamily: Roboto, fontSize: 13px, fontWeight: 400, lineHeight: 16px, letterSpacing: 0.0192px }
  label-large: { fontFamily: Roboto, fontSize: 14px, fontWeight: 500, lineHeight: 20px, letterSpacing: 0.0107px }
  label-medium: { fontFamily: Roboto, fontSize: 13px, fontWeight: 500, lineHeight: 16px, letterSpacing: 0.0192px }
  label-small: { fontFamily: Roboto, fontSize: 12px, fontWeight: 500, lineHeight: 16px, letterSpacing: 0.025px }
  legacy-giant: { fontFamily: Roboto, fontSize: 48px, fontWeight: 500 }
  legacy-mono: { fontFamily: monospace, fontSize: 14px, fontWeight: 400 }
rounded:
  small: 8
  medium: 16
  sheet: 18
  dialog: 28
  full: 9999
spacing:
  compact: 4
  small: 8
  gutter: 16
  gutter-wide: 24
components:
  primary-button: { backgroundColor: "{colors.primary}", textColor: "{colors.on-primary}", typography: "{typography.label-large}", rounded: "{rounded.full}", height: 44 }
  tonal-button: { backgroundColor: "{colors.primary-container}", textColor: "{colors.on-primary-container}", typography: "{typography.label-large}", rounded: "{rounded.full}", height: 44 }
  small-button: { backgroundColor: "{colors.surface-1}", textColor: "{colors.on-surface-variant}", typography: "{typography.label-medium}", rounded: "{rounded.full}", height: 32 }
  dialog: { backgroundColor: "{colors.surface-1}", textColor: "{colors.on-surface}", rounded: "{rounded.dialog}" }
  bottom-sheet: { backgroundColor: "{colors.surface}", textColor: "{colors.on-surface}", rounded: "{rounded.sheet}" }
  navigation-bar: { backgroundColor: "{colors.surface-2}", textColor: "{colors.on-surface}", height: 80 }
  compact-navigation-bar: { backgroundColor: "{colors.surface-2}", textColor: "{colors.on-surface}", height: 48 }
  top-bar: { backgroundColor: "{colors.surface}", textColor: "{colors.on-surface}", typography: "{typography.title-large}", height: 64 }
x-stag:
  schema: 1
  platform: android
  peer: none
  facts:
    ui_framework: { primary: mixed, compose_files: 533, view_files: 435, layout_files: 531 }
    min_sdk: 23
    material: { generation: m3, m3_files: 243, m2_files: 0 }
    token_source: mixed
    generated: false
    accessor: "MaterialTheme.colorScheme / SignalTheme.colors"
    dark_mode:
      status: user
      mechanism: "User selects system, light, or dark; AppCompatDelegate and night resources feed SignalTheme."
      evidence: [app/src/main/java/org/thoughtcrime/securesms/util/DynamicTheme.java, app/src/main/java/org/thoughtcrime/securesms/keyvalue/SettingsValues.kt, core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt, core/ui/src/main/res/values-night/material3_colors.xml]
    spacing_scale: none
    dynamic_color: false
    migration: "SignalTheme and Material 3 are canonical for new UI; XML styles remain the compatibility path for existing View screens."
    confirmed:
      overall_feel: "Calm, private, and trustworthy—quiet surfaces, clear hierarchy, restrained color, and friendly but purposeful interactions."
      canonical_system: "SignalTheme and Material 3 for new UI; XML styles for existing classic screens."
      customizable_colors: "User content, not core design-system tokens."
      off_system: "Record as exceptions; reuse only when matching the exact feature."
  themes: { default: light, selection: system_and_user, list: [{ id: light, kind: appearance }, { id: dark, kind: appearance }] }
  values:
    colors.primary: { dark: "#B6C5FA" }
    colors.primary-container: { dark: "#464B5C" }
    colors.secondary: { dark: "#C1C6DD" }
    colors.secondary-container: { dark: "#414659" }
    colors.surface: { dark: "#1B1C1F" }
    colors.surface-1: { dark: "#23242A" }
    colors.surface-2: { dark: "#272A31" }
    colors.surface-3: { dark: "#2C2F37" }
    colors.surface-variant: { dark: "#303133" }
    colors.background: { dark: "#1B1C1F" }
    colors.on-primary: { dark: "#1E2438" }
    colors.on-primary-container: { dark: "#DBE1FC" }
    colors.on-secondary: { dark: "#2A3042" }
    colors.on-secondary-container: { dark: "#DCE1F9" }
    colors.on-surface: { dark: "#E2E1E5" }
    colors.on-surface-variant: { dark: "#BEBFC5" }
    colors.on-background: { dark: "#E2E1E5" }
    colors.outline: { dark: "#5C5E65" }
    colors.error: { dark: "#FFB4A9" }
    colors.error-container: { dark: "#930006" }
    colors.on-custom: { dark: "#FFFFFF" }
    colors.on-custom-variant: { dark: "#FFFFFF18" }
    colors.warning: { dark: "#EB977D1F" }
    colors.on-warning: { dark: "#EB977D" }
    colors.alert: { dark: "#F44336" }
    colors.scrim-light: { dark: "#FFFFFF1F" }
    colors.scrim: { dark: "#00000029" }
  bindings:
    colors.primary: { native: "MaterialTheme.colorScheme.primary", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightColorScheme" }
    colors.primary-container: { native: "MaterialTheme.colorScheme.primaryContainer", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightColorScheme" }
    colors.secondary: { native: "MaterialTheme.colorScheme.secondary", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightColorScheme" }
    colors.secondary-container: { native: "MaterialTheme.colorScheme.secondaryContainer", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightColorScheme" }
    colors.surface: { native: "MaterialTheme.colorScheme.surface", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightColorScheme" }
    colors.surface-1: { native: "SignalTheme.colors.colorSurface1", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightExtendedColors" }
    colors.surface-2: { native: "SignalTheme.colors.colorSurface2", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightExtendedColors" }
    colors.surface-3: { native: "SignalTheme.colors.colorSurface3", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightExtendedColors" }
    colors.surface-variant: { native: "MaterialTheme.colorScheme.surfaceVariant", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightColorScheme" }
    colors.background: { native: "MaterialTheme.colorScheme.background", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightColorScheme" }
    colors.on-primary: { native: "MaterialTheme.colorScheme.onPrimary", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightColorScheme" }
    colors.on-primary-container: { native: "MaterialTheme.colorScheme.onPrimaryContainer", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightColorScheme" }
    colors.on-secondary: { native: "MaterialTheme.colorScheme.onSecondary", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightColorScheme" }
    colors.on-secondary-container: { native: "MaterialTheme.colorScheme.onSecondaryContainer", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightColorScheme" }
    colors.on-surface: { native: "MaterialTheme.colorScheme.onSurface", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightColorScheme" }
    colors.on-surface-variant: { native: "MaterialTheme.colorScheme.onSurfaceVariant", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightColorScheme" }
    colors.on-background: { native: "MaterialTheme.colorScheme.onBackground", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightColorScheme" }
    colors.outline: { native: "MaterialTheme.colorScheme.outline", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightColorScheme" }
    colors.error: { native: "MaterialTheme.colorScheme.error", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightColorScheme" }
    colors.error-container: { native: "MaterialTheme.colorScheme.errorContainer", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightColorScheme" }
    colors.on-custom: { native: "SignalTheme.colors.colorOnCustom", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightExtendedColors" }
    colors.on-custom-variant: { native: "SignalTheme.colors.colorOnCustomVariant", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightExtendedColors" }
    colors.warning: { native: "SignalTheme.colors.colorWarning", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightExtendedColors" }
    colors.on-warning: { native: "SignalTheme.colors.colorOnWarning", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightExtendedColors" }
    colors.alert: { native: "SignalTheme.colors.colorAlert", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightExtendedColors" }
    colors.scrim-light: { native: "SignalTheme.colors.colorTransparentInverse2", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightExtendedColors" }
    colors.scrim: { native: "SignalTheme.colors.colorTransparentInverse3", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#lightExtendedColors" }
    typography.display-large: { native: "MaterialTheme.typography.displayLarge", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#typography" }
    typography.display-medium: { native: "MaterialTheme.typography.displayMedium", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#typography" }
    typography.display-small: { native: "MaterialTheme.typography.displaySmall", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#typography" }
    typography.headline-large: { native: "MaterialTheme.typography.headlineLarge", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#typography" }
    typography.headline-medium: { native: "MaterialTheme.typography.headlineMedium", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#typography" }
    typography.headline-small: { native: "MaterialTheme.typography.headlineSmall", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#typography" }
    typography.title-large: { native: "MaterialTheme.typography.titleLarge", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#typography" }
    typography.title-medium: { native: "MaterialTheme.typography.titleMedium", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#typography" }
    typography.title-small: { native: "MaterialTheme.typography.titleSmall", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#typography" }
    typography.body-large: { native: "MaterialTheme.typography.bodyLarge", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#typography" }
    typography.body-medium: { native: "MaterialTheme.typography.bodyMedium", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#typography" }
    typography.body-small: { native: "MaterialTheme.typography.bodySmall", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#typography" }
    typography.label-large: { native: "MaterialTheme.typography.labelLarge", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#typography" }
    typography.label-medium: { native: "MaterialTheme.typography.labelMedium", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#typography" }
    typography.label-small: { native: "MaterialTheme.typography.labelSmall", source: "core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt#typography" }
    rounded.sheet: { native: "dimensionResource(R.dimen.bottom_sheet_corner_size)", source: "core/ui/src/main/res/values/dimens.xml#bottom_sheet_corner_size" }
    spacing.gutter: { native: "dimensionResource(R.dimen.gutter)", source: "core/ui/src/main/res/values/dimens.xml#gutter" }
    spacing.gutter-wide: { native: "dimensionResource(R.dimen.gutter)", source: "core/ui/src/main/res/values-sw360dp/dimens.xml#gutter" }
  fonts:
    - { family: Roboto, files: [], registered_via: system, preview: system, used_by: "Material 3 typography and classic Android text styles" }
    - { family: monospace, files: [], registered_via: system, preview: system, used_by: legacy-mono }
  examples:
    - { screen: Main navigation, path: app/src/main/java/org/thoughtcrime/securesms/main/MainNavigationBar.kt, shows: [surface hierarchy, navigation states, badges, compact and standard bars] }
    - { screen: Main toolbar, path: app/src/main/java/org/thoughtcrime/securesms/main/MainToolbar.kt, shows: [top app bar, search state, icon actions, responsive layout] }
    - { screen: Avatar, path: app/src/main/java/org/thoughtcrime/securesms/avatar/compose/AvatarImage.kt, shows: [circular media, personalized content colors, adaptive initials] }
    - { screen: Conversation, path: app/src/main/java/org/thoughtcrime/securesms/conversation/v2/ChatScreen.kt, shows: [conversation surface, keyboard transition, theme usage] }
    - { screen: Call controls, path: app/src/main/java/org/thoughtcrime/securesms/components/webrtc/v2/CallButton.kt, shows: [fixed circular buttons, feature-specific color exception] }
  known_off_system:
    - { id: compose-color-literals, pattern: "Color(0x...) in feature Compose code", count: 43, replacement: "Use MaterialTheme.colorScheme or SignalTheme.colors unless matching the exact existing feature." }
    - { id: drawable-color-literals, pattern: "Hex colors in drawable XML", count: 2391, replacement: "Treat illustration artwork as an exception; use semantic color resources for UI chrome." }
    - { id: raw-compose-dimensions, pattern: "Numeric .dp values in app Compose code", count: 2452, replacement: "Reuse established component dimensions and shared gutter before adding a local value." }
  sizes:
    - { kind: avatar, name: standard-avatar, width: 48, height: 48, radius: 9999 }
    - { kind: avatar, name: contact-photo-target, width: 64, height: 64, radius: 9999 }
    - { kind: avatar, name: avatar-picker, width: 100, height: 100, radius: 9999 }
    - { kind: button, name: large-button, height: 44, radius: 9999 }
    - { kind: button, name: medium-button, height: 40, radius: 9999 }
    - { kind: button, name: small-button, height: 32, radius: 9999 }
    - { kind: button, name: call-control, width: 48, height: 48, radius: 9999 }
    - { kind: bar, name: top-bar, height: 64 }
    - { kind: bar, name: navigation-bar, height: 80 }
    - { kind: bar, name: compact-navigation-bar, height: 48 }
    - { kind: gutter, name: standard-gutter, width: 16 }
    - { kind: gutter, name: wide-gutter, width: 24 }
    - { kind: icon, name: standard-action-icon, width: 24, height: 24 }
    - { kind: divider, name: standard-divider, thickness: 1 }
  roles:
    primary: accent
    primary-container: fieldFill
    secondary: other
    surface: surface
    surface-1: surface
    surface-2: surface
    surface-3: surface
    background: background
    on-primary: text
    on-surface: text
    on-surface-variant: textSecondary
    outline: border
    error: error
    scrim: scrim
  usage:
    primary: Primary actions, selection, and active emphasis.
    surface: Main screen and elevated component surface.
    surface-1: Subtle raised or grouped surface.
    surface-2: Navigation and stronger grouped surface.
    on-surface: Primary text and icons.
    on-surface-variant: Secondary text and icons.
    outline: Borders and low-emphasis separators.
    error: Destructive actions and error states.
  gaps:
    - "Compose and XML duplicate the core palette; the designer confirmed SignalTheme is canonical for new UI."
    - "Personalized chat and avatar colors intentionally sit outside the core interface token set."
    - "Legacy View screens still render older text appearances in addition to the canonical Material 3 roles."
    - "Raw dimension counts include legitimate one-off layout geometry as well as reusable values."
  deviations: none
  generated_from:
    at: 2026-11-16T19:54:09Z
    inputs:
      - path: app/build.gradle.kts
        sha256: 01a3f03e9b079ae62856e53209fd0419c6af0e06c2c9dc4c41921daac5b4baca
      - path: gradle/libs.versions.toml
        sha256: 0cfcef948b6f6e2f210af1d859f068f01464a7eb4d4bfcb42b2381bb10c0871d
      - path: app/src/main/res/values/colors.xml
        sha256: dbd793c7c64e4c0903d957089ff953796a34ccededf43987f60d0dcb9da8504d
      - path: app/src/main/res/values/light_colors.xml
        sha256: 8e668feb6b83b263c804587a83bd5973f064e975ccbd8698626992347cab1d84
      - path: app/src/main/res/values-night/dark_colors.xml
        sha256: dc0197f00966ac221673c2a6ffafc220e936b2bfb084e1f8432581f85b1e0e9f
      - path: app/src/main/res/values/dimens.xml
        sha256: 8a9fd510bdddd09eb2bf5db497e06f8a651bde52858781f8287d9abdfd59d7df
      - path: app/src/main/res/values/material3_dimens.xml
        sha256: e0d7830c219822c6da166e2c4182f8b0ff75bc2c950bd466f72dc71ffc56e051
      - path: app/src/main/res/values/styles.xml
        sha256: 3757819297db8d52e16f9bedabd7b5468b60b9b7170fc5a99a6a61f50a9d0e1e
      - path: app/src/main/res/values/themes.xml
        sha256: b0e6d88811531ac357dbe5d669b0195b68e1cb994dadf88943495c8549509901
      - path: app/src/main/res/values/signal_styles.xml
        sha256: 6e0f24f436b21f6010863709fbe88cc00ebf6222a5535078a7aa9f02f8c720c7
      - path: core/ui/src/main/java/org/signal/core/ui/compose/theme/SignalTheme.kt
        sha256: f37672b4cf85a69445a422a5c84fd565aeb0edcf72bc2902a90af362f3beee38
      - path: core/ui/src/main/java/org/signal/core/ui/compose/theme/ExtendedColors.kt
        sha256: a330120c15a93977cc22a75175823bae193d9c4b09f538e2b178524255ad32c2
      - path: core/ui/src/main/res/values/material3_colors_light.xml
        sha256: e36b4a127280502e9d8eab611e2e6398b8d4386ee900a5f0878bce4d17ae84fa
      - path: core/ui/src/main/res/values/material3_colors_dark.xml
        sha256: acb292fdbf2c1f1242b3cd47e2242908aad3365b84263ffc2d2d8e7d45a8a92e
      - path: core/ui/src/main/res/values/material3_colors.xml
        sha256: 6667f2ebb31d3a66388e3748a08538aaa8387b8cbbb820ec8c2abaf75df18eb3
      - path: core/ui/src/main/res/values-night/material3_colors.xml
        sha256: fe611b34e6e553e8d082ecc8d67ad67d2ffdda7a5293a80548edc7bb9f531e84
      - path: core/ui/src/main/res/values/text_styles.xml
        sha256: 5ece56c1bb5f8c3ce9230c92abce5bf5d3cb66a1243cc2573e956834a15a0075
      - path: core/ui/src/main/res/values-v28/text_styles.xml
        sha256: 9491c608b0a18800efd9c1f56b03bc0f1df08b5a13772db0f3e33467870be0ed
      - path: core/ui/src/main/res/values/dimens.xml
        sha256: 3cd7688e7b07262fbbe65522fcdf84400e69eb2a03bdf4a11dfb7e8b3f597131
      - path: core/ui/src/main/res/values-sw360dp/dimens.xml
        sha256: 1420edde2a3f01002c1aebda4b5443155fb29a0014c992c9dcf7e15f5b3541c5
      - path: app/src/main/java/org/thoughtcrime/securesms/util/DynamicTheme.java
        sha256: abfadd4212c1cb958a01ad932aafe6d040a57a9cf876841a55bc2729d9b599ad
      - path: app/src/main/java/org/thoughtcrime/securesms/keyvalue/SettingsValues.kt
        sha256: d3c27fa4672c405c13c1f00d142b4ca37ae7926c653f258da9dba322b35afc70
      - path: app/src/main/java/org/thoughtcrime/securesms/main/MainNavigationBar.kt
        sha256: ec378f49c59bb33a1561134c6f36b41cdd299afb3a83a76f1eebbc5bea7c0bc0
      - path: app/src/main/java/org/thoughtcrime/securesms/main/MainToolbar.kt
        sha256: 73ffd003847cbbf330b3fb4d390ccee1a285b927498f96abed1d6251ed08ef5f
      - path: app/src/main/java/org/thoughtcrime/securesms/avatar/compose/AvatarImage.kt
        sha256: d2ac0c09f14f981a0b8da37aeeeffea43d4376f54f9d5454cb62743514892425
---
## Overview
- Keep Signal calm, private, and trustworthy through quiet surfaces, clear hierarchy, restrained color, and friendly but purposeful interactions.
- Build new UI with SignalTheme and Material 3; preserve XML styles as the compatibility path for existing classic screens.

## Colors
- Use semantic Material color roles and SignalTheme extended surfaces; never copy their hex values into a screen.
- Preserve strong contrast for privacy, error, warning, and destructive states in both appearances.
- Treat chat, avatar, wallpaper, and profile personalization as user content layered over the interface, not as core UI tokens.

## Typography
- Use MaterialTheme typography roles and Roboto system faces.
- Keep hierarchy compact and readable; prefer body and title roles over local font sizes.
- Use legacy appearances only while maintaining an existing classic screen.

## Layout
- Start with the 16dp gutter and allow the resource to widen to 24dp on larger widths.
- Keep touch targets at least 48dp even when the visible icon or control is smaller.
- Reuse the established 64dp top bar and 80dp or 48dp navigation modes.

## Elevation & Depth
- Create hierarchy with the surface, surface-1, surface-2, and surface-3 progression before adding shadows.
- Keep overlays quiet and use semantic scrims for temporary layers.

## Shapes
- Use fully rounded buttons, avatars, pills, and circular icon controls.
- Use 18dp top corners for sheets and 28dp corners for Material dialogs.
- Reserve smaller 8dp corners for compact legacy surfaces and media where the existing component establishes them.

## Components
- Use Material 3 components inside SignalTheme before creating custom controls.
- Keep primary actions visually singular; use tonal or text actions for supporting choices.
- Preserve component behavior and accessibility across light, dark, and system-selected appearance.

## Do's and Don'ts
- Do use MaterialTheme.colorScheme, MaterialTheme.typography, and SignalTheme.colors in new Compose UI.
- Do match a feature-specific exception only inside that exact feature.
- Don't promote personalized content colors into the interface palette.
- Don't introduce local color literals or raw repeated sizes when a shared role or established component exists.
