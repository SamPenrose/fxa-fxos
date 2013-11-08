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
* ferjm gaia->gecko API to review: https://pastebin.mozilla.org/3456934 (see postscript)

26 Nov Go / No Go Milestone: Criteria
-------------------------------------
 - all decisions made
 - all statuses re-verified
 - list of incomplete tasks must be:
   * short
   * 100% owned
   * 90% targetted by 02 December

**Decisions we have to make by Tuesday 12 Nov**

|   Area  |   Owner    |   Decision                |  Decision   | UX Change ?
| ------- | ---------- | ------------------------- | ----------- | ---------- |
| UX       | lloyd?    | COPPA needed for 1.3?     | <toxborrow> | Yes -> Y   |
| UX       | jgruen    | Password change, reset UX | web         | Y          |
| Gecko    | ckarlof   | certificate TTL?          | 6 hours     | N
| FTU      | borja     | email capture/pre-pop     | No          | Y?
| System   | jedp      | push notif'n to device    | No          | N
| System   | jedp      | email FTU -> Mail app     | No          | Y?
| Settings | jedp      | Login state per-app?      | No          | Y
| Settings | jedp      | UX for Delete account?    | web         | Y
| Frontend | jedp      | Launch SignUp flow fr. RP | Y           | N

c.f. decisions.md

Password reset/change and account deletion
------------------------------------------
All user actions performed on Web -> jgruen please update UXv.0.10
  May require design phase: jgruen and ???

What is on-device experience post-invalidation?
  With push notification (may not ship, not 100% reliable)
  W/o notification:
    1) Expiration time for public key signing (current: 6 hours)
       latency vs network traffic tradeoff
    2) Can re-check on assertion generation:
       Problem: if assertion in use and check returns invalid requires firing event to App

What is service/data experience for deletion?
  How do we delete user data from e.g. Marketplace?
  What on-device storage needs clearing?


|   Milestone      | Owner     | Target | Details |
| ---------------- | --------- | ------ | -------- |
| Broadcast roadmap| toxborrow | 12 Nov | All "external relationship contacts" alerted
| Final UX         | jgruen    | 13 Nov | Exactly what we're building, by EoD
| Reviewers chosen | spenrose  | 13 Nov |
| Alpha build      | jedp      | 14 Nov | Nightly try build for WMF?, MP
| Decisions made   | spenrose  | 15 Nov | Only execution left
| Review #1 (all)  | spenrose  | 21 Nov | Every patch has initial review returned
| Beta gut check   | jedp      | 26 Nov | Does 9 Dec look makeable?
| Broadcast status | toxborrow | 27 Nov | Beta status to all stakeholders
| Q/A Placehold1   | edwong    | 27 Nov | Details TBD
| Ready for 9 Dec  | jedp      | 02 Dec | All* 9 Dec tasks due
| Q/A Placehold2   | edwong    | 02 Dec | TBD

* for some definition of "All"

External relationship contacts
------------------------------
  arogers for FxOS product
  ckarlof FxA Services
  cserran for FxOS engineering
  edwong for Q/A
  jgruen for UX (including FxOS UX team)
  kparlante for Metrics
  lloyd for general vetting
  toxborrow for Legal
  toxborrow / Rob Fletcher for Security

The next table is for tracking reviewer assignments. It's a mess, updates coming

| Bug    |  scope   | assignee | f?/r? candidates  | f? booked    | r? booked | details |
| ------ | -------- | -------- | ----------------- | ------------ | --------- | -------|
| 929388 | gaia/sys | ferjm    | alive, vivien     |
|        | gaia/UI  | BOS*     | alive
| 929386 | DomIdentity.jsm  | ferjm    | <spenrose>
| 936487 | Hide FxA flag | 
| 933981 | Legal    |
| 936281 | COPPA    |
|        | FTU UX HTML/JS         |
| Settings UX HTML/JS    |
| Sign-In UX HTML/JS     |
| Integration Tests      |
|    **Gecko**           |                   taubert, gavin, rnewman
| Pref/flag to disable?  |
| FXAccounts.jsm         |  935234    |                            
| FXAccountsClient.jsm   |  935232    | 
| MinimalIdentity.jsm    |       ?    |
| SignInToFxA.jsm        |       ?
| jwcrypto	         |  936146
|    **gaia/System**
| Pref/flag to disable?  | can be hooked to setting (fabrice dislikes) OR build time gaia variable
|    **gaia/shared**     |
| fxa_iac_helper.js      |       ?
|    **Web services**    |
| picl-idp/raw_password  |
| password reset         |

* "BOS": borjasalguero, olavnymoen, stomlinson

---------------
spenrose Meta-TODO for this doc:
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
    which means we need to walk through latest

  walk through meta-bugs
    do we have security meta-bug?

------ ferjm gaia <-> gecko 08 Nov -------
          case 'delete':
            // TODO: FxAccounts.? Maybe remote
            break;
          case 'getAccounts':
            // TODO: FxAccounts.getSignedInUser                                   
            break;                                                                 
          case 'logout':
            // TODO: FxAccounts.signOut
            break;
          case 'signIn':
            // TODO: FxAccountsClient.signIn
            break;
          case 'signUp':                                                           
            // TODO: FxAccountsClient.signUp                                       
            break;
          case 'verificationStatus':                                               
            // TODO: FxAccounts.verificationStatus or maybe FxAccounts.getSignedUser if we do it async
            break; 
