|   Milestone      | Owner     | Target | Details |
| ---------------- | --------- | ------ | -------- |
| Broadcast roadmap| toxborrow | 13 Nov | All "external relationship contacts" alerted
| Final UX         | jgruen    | 13 Nov | Exactly what we're building, by EoD
| Reviewers chosen | spenrose  | 14 Nov |
| Alpha build      | jedp      | 14 Nov | Nightly try build for WMF?, MP
| Decisions made   | spenrose  | 15 Nov | Only execution left
| Review #1 (all)  | spenrose  | 21 Nov | Every patch has initial review returned
| Beta gut check   | jedp      | 26 Nov | Does 9 Dec look makeable?
| Broadcast status | toxborrow | 27 Nov | Beta status to all stakeholders
| Q/A Placehold1   | edwong    | 27 Nov | Details TBD
| Ready for 9 Dec  | jedp      | 02 Dec | All* 9 Dec tasks due
| Q/A Placehold2   | edwong    | 02 Dec | TBD

* for some definition of "All"

26 Nov Go / No Go Milestone: Criteria
-------------------------------------
 - all decisions made
 - all statuses re-verified
 - list of incomplete tasks must be:
   * short
   * 100% owned
   * 90% targetted by 02 December

Reviewers
---------

| Bug    |  scope   | assignee      | f?/r? candidates  | f? booked    | r? booked | details |
| ------ | -------- | ------------- | ----------------- | ------------ | --------- | -------|
| 929388 | gaia/sys | ferjm         | alive, vivien     |
| 929386 | gecko    | ferjm         | <spenrose>
| 930471 | gaia/UI  | stomlinson    | borja, sergi      | yes          | yes
| 930074 | gaia/UI  | olav (?)      | borja, sergi      | yes          | yes
| 935602 | gaia/UI  | borjasalguero | alive?
| 935232 | gecko    | zaach         | ferjm?
| 909967 | gecko    | zaach         | rnewman?          | 
| 929386 | gecko    | ferjm         | 
| 930598 | gecko    | ttaubert      | warner?           |              |    | Hawk
| 935234 | gecko    | warner        | ferjm?            |              |    | FxAccounts
| 936146 | gecko    | jedp          | warner?           |              |    | jwcrypto
| 936487 | gecko    | TBD           |             | | | Disable flag(s)
| 921344 | gaia     | jedp          |             | | | disable updates in FTU |

Current normative docs
----------------------
* https://wiki.mozilla.org/Identity/Firefox-Accounts
* https://wiki.mozilla.org/Identity/UX#FXOS
  - both screen flows have minor inaccuracies as of 7 November
    - examples: "or Persona Account", on-device password change
* https://bugzilla.mozilla.org/showdependencytree.cgi?id=920135&hide_resolved=1
  - jedp has kept this up to date
* http://www.gliffy.com/go/publish/image/5067437/L.png

Representatives
----------------

|   Owner    | Area |
| ---------- | ------------ |
|  arogers   | FxOS product
|  ckarlof   | FxA Services
|  cserran   | FxOS engineering
|  edwong    | Q/A
|  jgruen    | UX (including FxOS UX team)
|  kparlante | Metrics
|  lloyd     | Mozilla as a whole
|  toxborrow | Legal
|  toxborrow | Security


**Decisions we have to make by Tuesday 12 Nov**

|   Area  |   Owner    |   Decision                |  Decision   | UX Change ?
| ------- | ---------- | ------------------------- | ----------- | ---------- |
| UX       | toxborrow | COPPA needed for 1.3?     | ?           | Yes -> Y   |
| UX       | jgruen    | Password change, reset UX | web         | Y          |
| Gecko    | ckarlof   | certificate TTL?          | 6 hours     | N
| Gecko    | ckarlof   | use raw_password api      | Yes         | N
| FTU      | borja     | email capture/pre-pop     | No          | Y?
| System   | jedp      | push notif'n to device    | No          | N
| System   | jedp      | email FTU -> Mail app     | No          | Y?
| Settings | jedp      | Login state per-app?      | No          | Y
| Settings | jedp      | UX for Delete account?    | web         | Y
| MP/Legal | toxborrow | Marketplace & Deletion    | socialize   | N

c.f. decisions.md
