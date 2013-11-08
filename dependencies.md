Meta-TODO:
  jedp re owners for each open loop
  headsup to lloyd, toxborrow with result
    -> note any controversial on etherpad for input
  jgruen re need for final UX by Weds
    which means we need delta between latest and final
      user stories match FX wiki (no "or Persona account")
      password reset -> web
      FTU email capture and pre-populate
      log out from settings
      delete account from settings?
      launch creation flow from RP
  walk through meta-bugs
  all stakeholders identified via toxborrow
    cserran for FxOS product
    edwong for Q/A
    jgruen for UX (including FxOS UX team)
    lloyd for Identity
    toxborrow for Legal
    XXX for FxOS engineering?

Current normative docs
----------------------
* https://wiki.mozilla.org/Identity/Firefox-Accounts
* https://wiki.mozilla.org/Identity/UX#FXOS
  - both screen flows have minor inaccuracies as of 7 November
    - examples: "or Persona Account", on-device password change
* https://bugzilla.mozilla.org/showdependencytree.cgi?id=920135&hide_resolved=1
  - jedp has kept this up to date
* https://github.com/jedp/fxa-fxos/blob/master/img/architecture.png
* http://www.gliffy.com/go/publish/image/5067437/L.png

|   Area  |   Owner    |   Open loop       | Bug?
| ------- | ---------- | --------------------- |----------- |
| UX       | lloyd?    | COPPA needed for 1.3? |
| UX       | jgruen    | Move password reset -> web
| FTU      | borja     | email stored between screens?
| System   | jedp      | email captured in FTU pre-populated elsewhere?
| Settings | jedp      | Can we log out from Settings? 
| Settings | jedp      | Can we delete account from Settings?
| Frontend | jedp      | Can we launch creation flow from MP/WMF?

|   Milestone    | Owner    | Target | Details |
| -------------- | -------- | ------ | -------- |
| Final UX       | jgruen   | 13 Nov | Exactly what we're building, by EoD
| Alpha build    | jedp     | 14 Nov | Screen to FxA server on device for WMF?, MP
| No open loops  | spenrose | 15 Nov | Only execution left
| Beta gut check | jedp     | 26 Nov | Does 9 Dec look makeable?
| Q/A Placehold1 | edwong   | 26 Nov | Details TBD
| Ready for 9 Dec| jedp     | 02 Dec | All* 9 Dec tasks due
| Q/A Placehold2 | edwong   | 02 Dec | TBD

* for some definition of "All"




26 Nov Go / No Go
 - no open loops
 - all statuses re-verified
 - list of incomplete tasks must be:
   * short
   * 100% owned
   * 90% targetted by 02 December

| Bug    |  scope   | assignee | f?/r? candidates  | f? booked    | r? booked | details |
| ------ | -------- | -------- | ----------------- | ------------ | --------- | -------|
| 929388 | gaia/sys | ferjm    | alive, vivien     |
|        | gaia/UI  | borja... | alive
| 929386 | BrowserID| ferjm    | <spenrose>
| 933981 | Legal    | 

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
| Pref/flag to disable?  | can be hooked to setting (fabrice dislikes) OR build time gaia variable
| fxa_manager.js         |  929388         ? alive and vivien
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

for UI work (borja/shane/olav) also alive
