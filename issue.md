## Bug Report

### Capacitor Version
<!--
Paste the output from the `npx cap doctor` command into the code block below. This will provide the versions of Capacitor packages and related dependencies.
-->

```
PASTE OUTPUT HERE
```

### Platform(s)
<!--
List the platforms that this bug affects.
-->

Android

### Current Behavior
<!--
Describe how the bug manifests. Be specific.
-->

When the app is open and you change the device's theme, media queries watching for `prefers-color-scheme` are updated exactly once. This happens in when in CSS or listening to the change event of `MediaQueryLists`. To have listeners and style updated it is needed to completely close the app and open it again.

The theme change is made via notification tray controls, so the app is never in background during the change.

### Expected Behavior
<!--
Describe what the behavior should be.
-->

It was expected that the styles would be updated and the `MediaQueryList` change event would be fired every single time the device changes theme while the app is open.

### Code Reproduction
<!--
To isolate the cause of the problem, we ask you to provide a minimal sample application that demonstrates the issue.
For full instructions, see: https://github.com/ionic-team/capacitor/blob/HEAD/CONTRIBUTING.md#creating-a-code-reproduction
-->



### Other Technical Details
<!--
Please provide the following information with your request and any other relevant technical details (versions of IDEs, local environment info, plugin information or links, etc).
-->

`npm --version` output:

`node --version` output:

`pod --version` output (iOS issues only): -

### Additional Context
<!--
List any other information that is relevant to your issue. Stack traces, related issues, suggestions on how to fix, Stack Overflow links, forum links, etc.
-->


