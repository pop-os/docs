# Application Settings

- [`Applications` settings](/customize-pop/application-settings.md#applications): Manage application permissions, allow system integration features, specify default handlers, and view disk space usage per app. These settings may not be available for all applications, depending on the functionality or access required by the application.
- [`Notifications` settings](/customize-pop/application-settings.md#default-applications): Control which applications display notifications, what notifications are displayed, and where they are displayed.
- [`Default Applications` settomgs](/customize-pop/application-settings.md#default-applications) Specify applications that should always open certain file types.

---

## Applications

Options to control application access to system features and resources are located in the `Settings` ➞ `Applications` tab.

![Application Settings](/images/application-settings/application-settings.png)

| Option | Function |
|---------|----------|
| Permissions & Access | View the data and system services requested or required by an application. Permissions can include access to system devices, using the system's network connection, reading and writing to the file system, and the ability to change settings. Many applications include built-in permissions that cannot be modified by the user. View permission granted to an application by clicking the `Built-in Permissions` button. |
| Integration | Disable or enable system-wide features used by an application. These features include the ability to appear in search, display notification, and running in the background. |
| Default Handlers | This determines which file types are associated with an application. Click an entry to display more information about the file types assigned to the application. Multiple programs can be associated with the same file types. See the [Default Applications](/customize-pop/application-settings.md#default-applications) to specify an application that should always open a certain media type. |
| Usage | Display an application's disk usage. Click on the `Storage` button to view space used by the application itself, data created by the application, and temporary data cached by the application. Click `Clear Cache` to clear an application's locally stored data.

## Notifications

Settings to control application notification behavior are located in the `Settings` ➞ `Notifications` tab.

![Notifications Settings](/images/application-settings/notifications-settings.png)

| Option | Function |
|--------|----------|
| Do Not Disturb | Disable all application notifications globally. |
| Lock Screen Notifications | Enable setting toggling for the `Lock Screen Notifications` and `Show Message Content on Lock Screen` options. |

Application notifications appear in the upper center of the screen. Click the date and time to view recent notifications.

![Recent Notifications](/images/application-settings/recent-notifications.png)

### Configure Notification Behavior for a Single Application

Select an application from the list to configure its notification behavior.

![Single App Options](/images/application-settings/single-app-options.png)

| Option | Function |
|--------|----------|
| Notifications | Toggle an application's notifications on or off. |
| Sound Alerts | Toggle sound alerts that will accompany notifications for this application. |
| Notification Popups | Enable notification popups on the desktop; notifications will continue to appear in the notification list. |
| Show Message Content in Popups | Include the notification's written content in the popup. |
| Lock Screen Notifications | Display application notifications at the login screen when the computer is locked. These settings cannot be enabled unless the Lock Screen Notifications setting is enabled. |
| Show Message Content on Lock Screen | Displays an application's written notification content in the login screen when the computer is locked. |

## Default Applications

Options to choose default applications for Web browsing, Email, Calendars, Music, Videos, and Photos are located in `Settings` ➞ `Default Applications`.

![Default Applications](/images/application-settings/default-applications.png)

Designate an application as the default by selecting it from the dropdown menu. If no appropriate application is installed to handle a media type, the dropdown selection will be grayed out. <!--link to installing applications section when complete-->

![Select Default](/images/application-settings/select-default.png)

> **Default Applications vs. Default Handlers**:
> Multiple applications can be designated as default handlers for file types. Use the `Default Applications` menu to specify which application should **always** launch when handling a specific media type, even if other appropriate applications are installed on the system.
