# Privacy Policy

**GTA Offline Transit** operates **100% offline** on your device.

## Zero Network Access
- The app declares **no `android.permission.INTERNET`** permission (`tools:node="remove"` in `AndroidManifest.xml`).
- It cannot send telemetry, analytics, crash reports, location coordinates, or search queries to any server.
- No account, sign-in, cloud sync, or third-party ad SDK exists in the app.

## Permissions Used & Why
| Permission | When Used | Scope |
|---|---|---|
| `ACCESS_FINE_LOCATION` / `ACCESS_COARSE_LOCATION` | Only when you tap **My location**, **Your location**, **Nearby**, or **Start trip** | Foreground-only (`LocationManager`). Never requested in background (`ACCESS_BACKGROUND_LOCATION` is absent). |
| `VIBRATE` | Only during an active foreground **Start trip** session | One-shot 250 ms haptic alert 1 stop before your exit stop. |
| `POST_NOTIFICATIONS` | Only if you tap **Remind me** on the evening **Last ride home** banner | Schedules one local offline `AlarmManager.setAndAllowWhileIdle` notification via a non-exported receiver (`android:exported="false"`). Zero `SCHEDULE_EXACT_ALARM` or `RECEIVE_BOOT_COMPLETED`. |

## On-Device Storage
Your **Saved Places** (`Home`, `Work`, `Favorites`, `Want to go`, custom labels), **Starred Stops**, and **Recent Searches** are stored solely in private app `SharedPreferences` on your device and can be cleared anytime inside the app.
