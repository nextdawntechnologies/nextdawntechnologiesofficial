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

## ND Countdown (`ndcountdown/`)

Content reference: `countdown/ios-native/README.md`, the current StoreKit entitlements, settings, encrypted storage, CloudKit, import, widget and Watch implementations. Structure, responsive layout and language switching follow `ndfile/`. The website supports five languages; the app currently supports Simplified Chinese and English.

- [x] Added the same six files as `ndfile/`: `index.html`, `support.html`, `privacy.html`, `app-icon.png`, `apple-touch-icon.png` and `favicon-32.png`. The main icon is an exact copy of the native app icon; the smaller icons are 180px and 32px derivatives.
- [x] All three pages include complete English, Simplified Chinese, Traditional Chinese, Korean and Japanese copy. Titles, descriptions, document language and language-control labels follow the selected language. Only one language section is visible.
- [x] Language controls update the selected state, and internal links preserve the language. Clicking Simplified Chinese on the product page and following Support opens Chinese support content.
- [x] Every local link and image resolves. The App Store ID is `6826122901`, matching the native app. No ND File branding, store ID or media-browser claims remain.
- [x] All 15 page/language combinations fit a 375 × 812 CSS-pixel viewport without horizontal overflow; language buttons are at least 44px tall.
- [x] All 30 page/language/appearance combinations at 150% text size fit the same viewport without horizontal overflow or clipped visible paragraphs, headings or language buttons. Light/dark appearance and text-size overrides were reset after QA.
- [x] All 50 localized FAQ answers expand and are visible after clicking their questions.
- [x] JavaScript syntax, HTML/link/content structure, icon identity, browser console and Git whitespace checks pass.
- [x] Product and support copy distinguish free five-event/single-reminder limits from one-time PRO, optional iCloud, the 60-notification planning limit, iOS 26 alarms and system-controlled widget refresh. No fixed launch price or release date is promised.
- [x] Privacy copy covers encrypted local storage, device-only Keychain keys, exclusion from system backups, optional private CloudKit sync, picker/import permissions, widget/Watch display copies, separate privacy controls, StoreKit, deletion/sharing, website language storage and voluntary support email.

Last checked: October 29, 2026 in local in-app Chromium. Screenshot review covered the Chinese light desktop product page, English dark mobile product/privacy pages and Chinese support with enlarged text and an expanded answer. First-pass QA found the contact text inheriting the reference layout's non-shrinking icon rule; removing that inapplicable rule resolved the overflow, and the complete layout matrix then passed. A subsequent QA assertion initially read the first hidden language heading; it was corrected to inspect the visible heading and all 15 title checks passed.

Not verified: actual Safari/iPhone rendering, VoiceOver, public hosting propagation or App Store availability. Native app code was not changed or rebuilt. The native app's privacy URL currently points to `ndcountdown/index.html`; the new homepage provides a prominent Privacy Policy link, but changing the app URL directly to `privacy.html` is outside this website-only change.

When behavior changes, update all five translations together and repeat the affected checks. Website language availability must not be described as app language availability.
