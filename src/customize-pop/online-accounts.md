# Online Accounts

Settings to connect online accounts are located in `Settings` ➞ `Online Accounts`. These settings provide single sign-on for online providers. Connected accounts can directly access services like Mail, Calendar, Contacts, Maps, Photos, Files, and Music, without requiring sign-on through a web browser.

![Online Account Settings](/images/online-accounts/online-account-settings.png)

## Required Data Access

An up-to-date version of this chart can also be found on the [GNOME wiki](https://wiki.gnome.org/Projects/GnomeOnlineAccounts/Providers).

| Provider | Mail | Calendar | Contacts | Maps | Photos | Files | Ticketing | Printers | Music |
|----------|------|----------|----------|------|--------|-------|-----------|----------|-------|
| Facebook |      |          |          | Yes  | Yes    |       |           |          |       |
| Flickr   |      |          |          |      | Yes    |       |           |          |       |
| Foursquare |    |          |          | Yes  |        |       |           |          |       |
| Google   | Yes  | Yes      | Yes      |      | Yes    | Yes   |           | Yes      |       |
| Microsoft| Yes  |          |          |      |        |       |           |          |       |
| Microsoft Exchange | Yes | Yes | Yes  |      |        |       |           |          |       |
| Nextcloud |     | Yes      | Yes      |      |        | Yes   |           |          |       |
| IMAP & STMP | Yes |        |          |      |        |       |           |          |       |
| Kerberos |      |          |          |      |        |       | Yes       |          |       |
| Last.fm  |      |          |          |      |        |       |           |          | Yes   |

## Connecting an Online Account

Connecting an account authorizes Pop!\_OS to enable system integrations with the account provider. The registration process for each provider will vary.

1. Select a provider and enter your login information.

    ![Select Provider](/images/online-accounts/select-provider.png)

2. Review the account data that will become accessible to GNOME, then click `Allow`.

    ![Click Allow](/images/online-accounts/click-allow.png)

3. Toggle switches to enable or disable specific integrations to the service. Close the window when finished.

    ![Toggle Switches](/images/online-accounts/toggle-switches.png)

4. Connected accounts appear above the list of selectable providers.

    ![Connected Account](/images/online-accounts/connected-account.png)
