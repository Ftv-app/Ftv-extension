In order to properly link a Twitch account with Fansly and enable emote support, the following steps must be taken:

1. After the user clicks the link button they must first link their Twitch account with the Ftv-app Twitch app. This is a necessary step to ensure that only legitimate Twitch accounts are linked and to prevent any potential abuse. It is important to note that the Ftv-app Twitch app does not have access to any personal or sensitive information associated with the linked Twitch account.

2. Once the Twitch account has been linked, the API server will validate the authorization response from the Ftv-app Twitch app and issue a jwt (JSON Web Token) token for validation purposes.

3. The API server will then redirect the user back to Fansly with the jwt token.

4. The browser extension will automatically send a chat message on the user's behalf in the ZerGo0_Bot chatroom. This is used for server-sided validation, as it is the only way to confirm that the user is who they claim to be.

5. The API server will then retrieve the Fansly chatroom id based on the message sender's id (the Fansly account id) and validate the jwt token.

6. If all of the necessary information is correct, the API server will add a new entry to its database with the Fansly account id, Fansly chatroom id, and Twitch account id.

7. From this point forward, users will be able to visit the Fansly chatroom and access the emotes associated with their linked Twitch account id.

The entire process besides the Twitch authorization process is fully automated and requires no user interaction. The user will be redirected to their Fansly chatroom to validate that the process was successful.

The Fansly account id, Fansly chatroom id and Twitch account id are all publicly accessable by anyone registered to the associated services.
