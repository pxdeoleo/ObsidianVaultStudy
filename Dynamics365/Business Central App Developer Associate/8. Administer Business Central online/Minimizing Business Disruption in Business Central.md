> [!summary] 
> Minimizing business disruption due to service changes is crucial for Microsoft. [[Business Central]] customers receive monthly updates, including a major update every six months. Updates include fixes, design enhancements, and new features that may change the user experience. Administrators can manage these changes, allowing customers to prepare and drive digital transformation confidently.

#### Definitions

- **Feature Management Page**: Interface for administrators to manage new features and enhancements in Business Central.

> [!info] New Features

- Features can be enabled ahead of time on sandbox and production environments.
- Allows early benefit from improvements and new features.
- Time to test and prepare for changes.

> [!info] Enabling Features

- Minor updates introduce new features that aren't immediately enabled.
- Administrators can enable features via the Feature Management page.
- Once enabled, features are available to all users on that environment.

> [!tip] Optional Features

- Features remain optional for a period before becoming mandatory.
- Check the "Automatically enabled from" field on the Feature Management page for dates.
- Features disappear from the page once mandatory.

> [!info] Feature Management Page Functions

- Learn about new features and enhancements.
- Turn features on and off for all users.
- Test features in a new browser tab.
- Plan testing and preparation for upcoming changes.

#### Process to Enable an Optional Feature

1. Sign in to the environment and navigate to the Feature Management page.
2. Choose **Edit List** if the page isn't editable.
3. Set **Enabled for** to **All users** for the desired feature.

> [!example] Try Out a Feature

1. Select the **Try it out** link to open a new browser tab with the feature enabled.
2. Close the browser window or sign out to stop the feature.

#### Irreversible Features

- Some features can't be turned off once enabled.
- A warning dialog appears when enabling an irreversible feature.
- Evaluate such features in a sandbox environment before enabling in production.

> [!info] Scheduling Data Updates

- Schedule updates per company to minimize disruption.
- Use the **Schedule** option in the Data Update action group.
- The Feature Data Update setup guide helps review and schedule the process.

#### Common Questions

- **No optional features listed?** Periods without optional features are normal.
- **All new features in the list?** Only a subset of features are listed, primarily platform changes affecting user experience.
- **Features under development?** No, listed features are ready and generally available.
- **Support for optional features?** Yes, they follow the standard support lifecycle.
- **Notifications for mandatory features?** No notifications are provided.
- **Features in Message Center?** Not listed in the Microsoft 365 admin center Message Center.
- **Difference from Early Access?** Early Access makes features available two months before a major update.
- **Difference from Preview Environments?** Preview environments include all new features bundled together.
- **Difference from Application Areas?** Application areas show or hide individual controls; no optional period.
- **Third-party contributions?** Not currently supported.
- **Enable feature for a single user?** Features apply to all users of an environment.
- **No "Try it out" link?** Some features don’t support this option.
- **Optional features in new environments?** Enabled by default unless irreversible.
- **Feature management in on-premises?** Applicable similarly to online deployments.

#### Features Not in On-Premises Deployments

- Certain features available in Business Central Online are not implemented on-premises.