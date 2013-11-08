Current normative docs (are we regularly reviewing them for accuracy?)
-----------------------------
* https://wiki.mozilla.org/Identity/Firefox-Accounts
* https://wiki.mozilla.org/Identity/UX#FXOS
  - both screen flows have minor inaccuracies as of 7 November
    - examples: "or Persona Account", on-device password change
* https://bugzilla.mozilla.org/showdependencytree.cgi?id=920135&hide_resolved=1
  - jedp has kept this up to date
* https://github.com/jedp/fxa-fxos/blob/master/img/architecture.png

Meta-questions:
  How accurate do UX mocks / specs have to be?
    jedp: "pixel-accurate"
    Who owns keeping them accurate?: jgruen


|   Area  |   Owner    |   Open loop       | Needs Bug?
| ------- | ---------- | ----------------- |----------- |
| UX       | lloyd?    | COPPA needed for 1.3? | (new bug)
| UX       | jgruen    | Move password reset -> web
| FTU      | borja     | email stored between screens?
| System   | jedp      | email captured in FTU pre-populated elsewhere?
| Legal    | ?         | ToS and Privacy Policy Ready?
| Settings | jedp      | Can we log out from Settings? 
| Settings | jedp      | Can we delete account from Settings?
| Frontend | jedp      | Can we launch creation flow from MP/WMF?


| Milestones     | Owner   | Target | Details |
| -------------- | ------- | ------ | -------- |
| Alpha build    | jedp      | 14 Nov | Screen to FxA server on device
| No open loops  | spenrose? | 15 Nov | Only execution left
| Beta gut check | jedp | 26 Nov | Does 9 Dec look makeable?
| Ready for 9 Dec| jedp | 02 Dec | All 9 Dec tasks due
| Q/A Placeholder 1 | edwong | ?
| Q/A Placeholder 2 | edwong | ?

26 Nov Go / No Go
 - no open loops
 - all statuses re-verified
 - list of incomplete tasks must be:
   * short
   * 100% owned
   * 90% targetted by 02 December



|   Deliverable          |    Bug     |  Assignee  |    Ready    |     f?     |    r?      | Need By (default: 9 December) |
| ---------------------- | ---------- | ---------- | ----------- | ---------- | ---------- | ----------------------------- |
| Final UX (?)           |            | jgruen
| FTU UX HTML/JS         |
| Settings UX HTML/JS    |
| Sign-In UX HTML/JS     |
| Integration Tests      |
|    **Gecko**           |
| Pref/flag to disable?  |
| FXAccounts.jsm         |  935234    | 
| FXAccountsClient.jsm   |  935232    | 
| MinimalIdentity.jsm    |       ?    |
| DomIdentity.jsm        |  929386         ?
| SignInToFxA.jsm        |       ?
| jwcrypto	         |  936146
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

| Vetting                |
| Legal                  |
| Security               | Rob Fletcher |

