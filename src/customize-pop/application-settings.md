# Application Settings

Installed applications can be customized to open specific file types, have unique notification behavior, and to access specific system services or resources.

- [The `Applications` tab](/customize-pop/application-settings.md#applications) provides settings to manage application permissions, system integration features, default handlers, and disk space usage. The availability of these settings depends on the functions and access required by the application.
- [The `Notifications`](/customize-pop/application-settings.md#default-applications) tab provides more fine-tuning of application-specific notification behavior by providing additional control over which applications display notifications, what notifications are displayed, and where they are displayed.
- [The `Default Applications`](/customize-pop/application-settings.md#default-applications) tab provides a simplified menu for specifying a specific app that should always open a certain media type.

## Applications

Control application access to system features and resources in Settings ➞ Applications.

![Application Settings](/images/application-settings/application-settings.png)

- `Permissions & Access`: These settings display data and system services the app has requested or requires. These can include access to system devices, using the system's network connection, reading and writing to the file system, and the ability to change settings. Many applications will include built-in permissions that cannot be modified by the user. You can view permission granted to an application by clicking the `Built-in Permissions` button.

- `Integration`: These settings refer to system-wide features used by an application. These features include the ability to appear in search, display notification, and running in the background.

- `Default handlers`: These settings determine which file types are associated with an application. Click an entry to display more information about the file types assigned to the application. Multiple programs can be associated with the same file types. See the [Default Applications](/customize-pop/application-settings.md#default-applications) to specify an application that should always open a certain media type.

- `Usage`: This displays the disk usage used by the application. Click on the `Storage` button to view space used by the application itself, data created by the application, and temporary data cached by the application. You can clear cache data by clicking `Clear Cache`.

## Notifications

Application notifications appear in the upper center of the screen. Click the date and time to view recent notifications.

![Recent Notifications](/images/application-settings/recent-notifications.png)

Control application notification behavior in Settings ➞ Notifications. App-specific notifications are configured in this menu.

- `Do Not Disturb` applies globally and disables all application notifications.
- `Lock Screen Notifications` applies globally and allows toggling `Lock Screen Notifications` and `Show Message Content on Lock Screen` for an individual application.

![Notifications Settings](/images/application-settings/notifications-settings.png)

### Configure Notification Behavior for a Single Application

Select one of the applications listed on the left to configure its notification behavior.

![Single App Options](/images/application-settings/single-app-options.png)

| Option | Function |
|--------|----------|
| Notifications | Toggle notifications on or off for this app. |
| Sound Alerts | Toggle sound alerts that will accompany a notification for this app. |
| Notification Popups | Toggle notification Popups on the desktop; notifications will continue to appear in the notification list. |
| Lock Screen Notifications | Turning this on will display app notifications at the login screen when the computer is locked. These settings cannot be enabled unless Lock Screen Notifications is enabled. |
| Show Message Content on Lock Screen | Displays the app's notification message content in the login screen when the computer is locked. |

## Default Applications

Choose default applications for Web browsing, Email, Calendars, Music, Videos, and Photos in Settings ➞ Default Applications. 

![Default Applications](/images/application-settings/default-applications.png)

Designate an application as the default by selecting it from the dropdown menu. If no appropriate application is installed to handle a media type, the dropdown selection will be grayed out. <!--link to installing applications section when complete-->

![Select Default](/images/application-settings/select-default.png)

> **Default Applications vs. Default Handlers**:
> Multiple applications can be designated as default handlers for file types. The `Default Applications` menu allows you to specify which application should **always** launch when handling a specific media type, even if other appropriate applications are installed on the system.