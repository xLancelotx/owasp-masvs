# V6: Environmental Interaction Requirements

## Control Objective

The controls in this group ensure that the app uses platform APIs and standard components in a secure manner. Additionally, the controls cover communication between apps (IPC).

## Security Verification Requirements

| # | Description | L1 | L2 |
| --- | --- | --- | --- |
| **6.1** | The app only requires the minimum set of permissions necessary. | ✓ | ✓ |
| **6.2** | All inputs from external sources and the user are validated and if necessary sanitized. This includes data received via the UI, IPC mechanisms such as intents, custom URLs, and network sources.| ✓ | ✓ |
| **6.3** | The app does not export sensitive functionality via custom URL schemes, unless these mechanisms are properly protected. | ✓ | ✓ |
| **6.4** | The app does not export sensitive functionality through IPC facilities, unless these mechanisms are properly protected. | ✓ | ✓ |
| **6.5** | JavaScript is disabled in WebViews unless explicitly required. | ✓ | ✓ |
| **6.6** | WebViews are configured to allow only the minimum set of protocol handlers required (ideally, only https). Potentially dangerous handlers, such as file, tel and app-id, are disabled. | ✓ | ✓ |
| **6.7** | The app does not load user-supplied local resources into WebViews. | ✓ | ✓ |
| **6.8** | If Java objects are exposed in a WebView, verify that the WebView only renders JavaScript contained within the app package. | ✓ | ✓ |
| **6.9** | Object serialization, if any, is implemented using safe serialization APIs. | ✓ | ✓ |
| **6.10** | The app checks its installation source, and only runs if installed from a trusted source (e.g. Google Play Store / Apple App Store). |  | ✓ |
| **6.11** | The app detects whether it is being executed on a rooted or jailbroken device. Depending on the business requirement, users are warned, or the app is terminated if the device is rooted or jailbroken. |  | ✓ |

## References

For more information, see also:

- OWASP Mobile Top 10: M1 - Improper Platform Usage
- CWE: https://cwe.mitre.org/data/definitions/20.html
- CWE: https://cwe.mitre.org/data/definitions/749.html