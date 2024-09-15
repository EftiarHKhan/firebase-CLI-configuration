# firebase-CLI-configuration

Manage multiple users via the CLI

You can manage multiple users without re-authenticating, as of version 9.9.0 of the Firebase CLI.

firebase login:add
firebase login:list
firebase login:use
Example:

firebase login:add david@example.com
firebase login:add alice@example.com
firebase login:add bob@example.com
firebase login:use alice@example.com
firebase login:list
firebase deploy --only hosting # deploy as alice@example.com
Get a URL printed to the terminal.

firebase login --reauth
Use that link in the browser with the needed profile.

Still working, less convenient older answer

The easiest way to handle this is to logout User-Alice and the login User-Bob.

firebase logout
firebase login
But, if you're logged as User-Alice with a Google account in the browser you'll need to sign out there first.
