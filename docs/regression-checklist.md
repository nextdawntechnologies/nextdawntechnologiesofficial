# Website regression checklist

## ND Alarm Clock (`ndalarmclock/`)

Content reference: the native iOS app in `alarm-clock/ios-native/`. Page layout and the five website languages follow `ndfile/`; website language coverage is separate from the app's seven active languages.

- [x] Product, support and privacy pages each contain English, Simplified Chinese, Traditional Chinese, Korean and Japanese.
- [x] Language buttons show only one language section, update the document title, description and page language, and carry the selected language to internal links.
- [x] Opening the product page, selecting Simplified Chinese and following Support retains Simplified Chinese.
- [x] Local links and all three icon files resolve; the App Store URL matches the native app's `SettingsView.swift`.
- [x] No ND File branding, App Store ID or file-browser feature descriptions remain.
- [x] All 15 page/language combinations have no horizontal overflow at a 375 × 812 CSS-pixel viewport; language buttons have a minimum 44px height.
- [x] All three pages in Chinese and English remain free of horizontal overflow or clipped text at 150% text size in both light and dark appearances at 375px.
- [x] Support questions expand and reveal their answers.
- [x] JavaScript syntax and Git whitespace checks pass.
- [x] Content describes the eight-alert scheduling horizon, foreground-only sleep sounds, optional lifetime PRO and backups without imported audio. Privacy copy follows the app's current data handling, picker permissions and StoreKit behavior.

Last checked: October 24, 2026 using the local in-app Chromium browser. Text enlargement was emulated for QA and reset afterward. Screenshot review covered the Chinese light product page and English dark product/support pages. Actual Safari/iPhone rendering, public hosting propagation and App Store availability were not verified.

When changing app behavior or copy, update all five website translations and repeat the affected checks. Do not copy another product's privacy claims without checking the app implementation.
