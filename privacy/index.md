---
title: "Sleep Well Privacy Policy"
---

[Support](../) · [简体中文](zh-Hans/) · [Sound Credits](../sound-credits/)

# Sleep Well Privacy Policy

Developer: Zihan Wang  
Contact: jxiaoai@icloud.com  
Effective date: July 25, 2026  
Last updated: November 1, 2026

This policy describes how Sleep Well (the “App,” “we,” or “our”) accesses, processes, stores, and protects information.

## 1. Privacy at a glance

Basic sleep, health, and night sound analysis takes place on your device. AI nightly analysis and weekly/monthly summaries are optional Pro features that use cloud processing. We send the summaries described below only after your separate consent and activation. Nightly AI analysis starts when you request it; enabled weekly/monthly summaries may be generated when you view the relevant period.

We use Cloudflare Workers and Workers AI for these AI features. We do not upload raw Apple Health samples, microphone audio, sound timelines, or night sound report files. The App has no advertising SDK, cross-app tracking, or third-party analytics SDK. We do not sell personal information or use health information for advertising, marketing, profiling, or data brokerage.

## 2. Apple Health and optional AI processing

With your permission, the App reads available sleep records and stages, heart rate, heart rate variability, blood oxygen, sleeping respiratory rate, and sleeping wrist temperature through HealthKit. These support sleep summaries, Sleep Charge, recovery estimates, sleep debt, consistency, health trends, and nightly or period analysis.

Sleep or nap intervals you confirm are saved locally and may be written to Apple Health. When you delete a synchronized manual record in the App, we first attempt to remove the corresponding Health record written by this App. We do not change records written by another app or device.

Basic analysis stays on-device. Raw HealthKit samples are not uploaded. You can change or revoke Health access in your iPhone’s Health or Settings app.

### Optional Cloudflare AI features

The App separately explains and requests permission before enabling AI. Period requests send aggregated values over HTTPS to Cloudflare Workers and Workers AI. These may include period type, recorded-night counts, sleep goal, average sleep duration and change, average Sleep Charge and change, schedule variability, sleep debt, below-goal night counts, weekday/weekend grouping statistics and relative wake-time differences, and recorded awake duration where coverage is sufficient.

When available, requests also include current and previous period totals for Light, REM, and Deep sleep with stage coverage; valid-night counts and averages/ranges of nightly heart rate, oxygen, HRV, respiratory rate, and wrist temperature summaries; and estimated sound-event counts/durations, valid monitoring duration, and complete-report counts. Physiological ranges describe nightly summaries rather than raw sample extremes. Missing values are not treated as zero.

Nightly analysis sends that night’s sleep duration, goal, and calculated Sleep Charge. Available summaries may add classified sleep, Deep and REM duration, physiological measurements, actual sound-monitoring duration, estimated snoring duration, and higher ambient-sound proportion. Recent context uses only valid-night counts from the preceding seven calendar days; averages and relative bedtime/wake-time shifts are included only with enough records. It does not send the specific sleep date or clock times. Basic records do not acquire invented stages or physiological measurements.

AI requests attach Apple-signed subscription proof to the Worker to verify Pro access. It contains Apple transaction information such as product, transaction identifiers, environment, and expiration, not payment-card details. The proof is not included in AI model prompts. A hashed transaction identifier is used for short-term rate limiting; raw transaction identifiers are not written to application logs or a database.

The model writes observations and suggestions from the aggregated evidence. The App validates the response and displays it without generating substitute text on failure. Full responses may be reused in the current process but are not saved to disk. Up to 24 focus selections and their feedback that you actively save remain locally. A follow-up may send the previous focus’s action type and tried/not-tried/no-feedback status, not its original text or period dates.

Our Worker does not persist health request bodies, subscription proof, or model responses in application logs, databases, or object storage. Cloudflare’s [Privacy Policy](https://www.cloudflare.com/privacypolicy/) and [Workers AI data policy](https://developers.cloudflare.com/workers-ai/platform/data-usage/) apply to its processing. Its current policy limits ordinary real-time inference content to servicing the request and excludes model training; operational metadata and security/legal exceptions remain governed by that policy. We do not enable AI Gateway content logs or AI-content storage features.

We do not send raw HealthKit samples, sleep-date timelines, sound timelines, snore clips, microphone audio, or transcripts to the model. You can turn AI off in Settings to stop future requests while continuing basic analysis. AI may be inaccurate and does not replace medical judgment. Cloud or response failures show an error and retry option.

## 3. Microphone and night sound monitoring

Night Sound Monitoring is optional and requires microphone access. Audio is analyzed on-device for possible snoring, coughing, sleep talking, ambient noise, and quiet periods. We do not save or upload a full-night raw recording or transcribe possible sleep talking.

Reports may be stored locally with monitoring duration, timestamps, detected categories, estimated sound levels, event counts, and completion/interruption status.

Saving snore clips is off by default. If you enable it before monitoring, only detected snoring segments are saved inside the local App sandbox and are not uploaded. Unpinned clips have a seven-day retention period; expired files are removed the next time the App runs its cleanup. Clips you choose to keep remain until you delete them or remove the App. Available controls let you delete individual clips or saved reports and their associated clips.

## 4. Local storage and sound downloads

The App may keep manual sleep/nap records, an active timer and Health synchronization state, night sound reports, optional snore clips, sleep goals, language/appearance/data-source preferences, and other necessary settings locally. Verified subscription information is used in the current session and refreshed from Apple; a local preference is not used to invent Pro access.

A local flag records whether the first free monitoring session has been used. It is consumed when monitoring actually starts, regardless of whether the session finishes normally. AI consent and up to 24 focus selections with their text, action type, and feedback are stored locally. Sound favorites, mixes, volumes, timers, downloaded files, and download indexes may also be saved.

These local reports, recordings, and preference files are not uploaded to our backend. Optional AI uses only the aggregated values and subscription proof described above. Removing the App normally removes its local data; Apple Health data remains managed by Apple Health.

The App does not offer a separate iCloud synchronization or backup switch. System backup and device-transfer behavior depends on your Apple device and iCloud settings; we do not promise that every local report or clip will or will not migrate in a system backup.

Sound assets are downloaded from our HTTPS catalog and file service, distributed by Cloudflare, checked, and played locally. The service receives technical connection information such as an IP address, requested file path, and user agent, not Health records, night recordings, or saved sound-report files. Cloudflare may process necessary operational and security metadata under its policies.

Downloads do not expire automatically and can be removed in the App. Downloaded sound files are excluded from the App’s system-backup participation. Authors, sources, licenses, and processing notes are available from Sound Credits in Settings.

## 5. Subscriptions and purchases

Apple handles Sleep Well Pro purchases through StoreKit and the App Store, including Apple Account information, payment, renewals, cancellation, and refunds. We do not receive or store payment-card details. The App uses Apple-verified subscription information to determine Pro access. Optional AI also uses signed subscription proof as described in section 2. Apple’s privacy policy and terms apply to Apple’s processing.

## 6. Customer support

If you email us, we receive what you choose to send, which may include your email address, message, device details, or screenshots. We use it to respond, investigate issues, and improve support. Please avoid sending Health records, recordings, or other sensitive information unless needed for the request. Support correspondence may be retained as reasonably necessary to resolve the request, maintain support records, or meet legal obligations.

## 7. Advertising, analytics, and tracking

The App has no third-party advertising, behavioral tracking, or third-party analytics SDK. We do not track users across apps/sites, sell health information, share it with advertising networks or data brokers, or create advertising profiles from sleep or sound information.

## 8. Sharing

After your separate AI consent, Cloudflare processes the specified summaries and subscription proof as a service provider. Raw HealthKit samples, microphone audio, report files, and snore clips are not shared. Cloudflare also distributes sound files as described in section 4.

Apple processes information when you authorize Health access, download/update the App, purchase/manage subscriptions, or use App Store services. Applicable Apple policies govern this processing. We may disclose information we actually hold when required by law, valid legal requests, or protection of users’ rights and safety; our Worker does not persist AI request content.

## 9. Retention and deletion

Apple Health manages raw HealthKit information; our service does not persist those samples. Optional AI real-time processing is described in section 2. Local reports and preferences remain until removed through the App or by uninstalling it. Unpinned clips expire after seven days and are deleted when the App next runs its cleanup; deleting a report also removes its associated clips. Sound downloads can be removed from the App.

To request deletion of information you previously sent to support, contact jxiaoai@icloud.com.

## 10. Security

We use iOS sandboxing and available device data protection for local information. No security method offers an absolute guarantee. Protect access to your iPhone, Apple Account, device passcode, and backups.

## 11. Children

Sleep Well is not specifically directed to children under 13. We do not knowingly collect children’s personal information through a developer-operated server. Contact us if you believe a child has sent personal information to support so we can investigate and remove it where appropriate.

## 12. Health disclaimer

Sleep Well supports general wellness and information, not medical advice, diagnosis, or treatment. Scores, recovery estimates, sound classifications, and other insights are estimates and must not be used to diagnose sleep apnea or another condition. Consult a qualified healthcare professional about health or sleep concerns and before making medical decisions.

## 13. Changes

We may update this policy when features, data practices, or legal requirements change. We publish the revised date on the policy page and communicate material changes as required.

## 14. Contact

Privacy, support, and deletion requests: jxiaoai@icloud.com.
