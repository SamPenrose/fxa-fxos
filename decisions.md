**Decisions we have to make by Tuesday 12 Nov**

Summary
-------
To land FxA on FxOS 1.3, we have to make these choices immediately. For many of them, we need quick turnaround on UX updates from John.

Your responsibilities
---------------------
Everyone: read. Own each decision or object now. If you can think of an unmade decision that effects our ability to hit 1.3 and is not listed, add it now.

John: note which changes require UX updates (all the 'Y' in the rightmost column below). We are going to ask you to fast-track them.

Tauni: own landing the COPPA decision, or tell me who else to ask.

Summary
-------
|   Area   |   Owner   |   Decision                |  Decision   | UX Change ?
| -------  | --------- | ------------------------- | ----------- | ---------- |
| UX       | toxborrow | COPPA needed for 1.3?     | ?           | Yes -> Y   |
| UX       | jgruen    | Password change, reset UX | web         | Y          |
| Gecko    | ckarlof   | certificate TTL?          | 6 hours     | N
| FTU      | borja     | email capture/pre-pop     | No          | Y?
| System   | jedp      | push notif'n to device    | No          | N
| System   | jedp      | email FTU -> Mail app     | No          | Y?
| Settings | jedp      | Login state per-app?      | No          | Y
| Settings | jedp      | UX for Delete account?    | web         | Y
| Frontend | jedp      | Launch SignUp flow fr. RP | Y           | N

1) Do we need COPPA verification in 1.3?

2) Password change and reset flows will NOT happen on device; instead the user will click a link which takes them to the web. We need to update the DEVICE UX immediately. The web UX can follow less urgently.

3) The expiration time for FxA certificates is currently set to 6 hours, which means 6 hours without extra data over the network, and up to 6 hours before the phone knows of e.g. password resets. Changing the value in either direction makes some issues better and some worse.

4) UX mocks show email being captured in the FxA FTU and used later in the FTU. Decision: this is a nice-to-have for which we have not currently identified a code path, so do not attempt to deliver. John please conform final UX.

5) Push notification to the device would be excellent for email verification, password reset, and account deletion UXs. We are NOT going to have it for 1.3. Nor will we have on-device web flow notifying apps.

6) UX mocks show email address from the FTU being auto-filled into the Mail app. This will NOT happen in 1.3, and the final UX should not show it.

7) Logged-in state is device-wide, not per-app. Settings UX should show "log out" accordingly (a change from the current separate toggles for Marketplace and WMF?).
