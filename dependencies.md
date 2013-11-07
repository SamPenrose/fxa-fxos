Current normative docs (are we regularly reviewing them for accuracy?)
-----------------------------
https://wiki.mozilla.org/Identity/Firefox-Accounts
https://wiki.mozilla.org/Identity/UX#FXOS
  both screen flows have minor inaccuracies as of 7 November
    examples: "or Persona Account", on-device password change

https://bugzilla.mozilla.org/showdependencytree.cgi?id=920135&hide_resolved=1
  jedp has kept this up to date
https://github.com/jedp/fxa-fxos/blob/master/img/architecture.png
  I believe this is now slightly inaccurate

Meta-questions:
  How accurate do UX mocks / specs have to be?
  Who owns keeping them accurate?


|   Area  |   Owner   |          Issue         |
| ----------------------------------------|
| UX       | lloyd     | COPPA needed for 1.3? 
| UX       | jedp      | email verif: requires password?
| UX       | jgruen    | Move password reset -> web
| FTU      | borja     | email stored between screens?
| System   | jedp      | email captured in FTU pre-populated elsewhere?
| Legal    | ?         | ToS and Privacy Policy Ready?
| Settings | jedp      | Can we log out from Settings? 
| Settings | jedp      | Can we delete account from Settings?
| Frontend | jedp      | Can we launch creation flow from MP/WMF?


ETHERPAD HARVEST

|   Deliverable          |    Bug     |  Assignee  |    Ready    |     f?     |    r?      | Need By (default: 9 December) |
| ---------------------- | ---------- | ------------------ | ---------- | ---------- |
| FTU UX HTML/JS         |
| Settings UX HTML/JS    |
| Sign-In UX HTML/JS     |

|    **Gecko**           |
| Pref/flag to disable?  |
| FXAccounts.jsm           935234     Tue ?
| FXAccountsClient.jsm     935232     Mon ?
| [MinimalIdentity.jsm           ?                   ]
| DomIdentity.jsm          929386         ?
| SignInToFxA.jsm               ?
| jwcrypto	             936146         ?

|    **gaia/System**
| Pref/flag to disable?  |
| fxa_manager.js         |  929388         ?
| fxa_ui.js              |       ?
| fxa_client.js          |  929388
|    **gaia/shared**     |
| fxa_iac_helper.js      |       ?

|    **Web services**    |
| picl-idp/raw_password  |
| password reset         |
  
Q/A
  peformance recordability
