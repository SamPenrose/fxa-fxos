|   Milestone      | Status  | Owner     | Target | Details |
| ---------------- | ------- | --------- | ------ | -------- |
| Alpha build      | in prog | jedp      | 19 Nov | Nightly try build for WMF?, MP
| Reviews running  | in prog | spenrose  | 18 Nov | For major code bugs
| Review #1 (all)  |         | spenrose  | 22 Nov | Every patch has initial review returned
| Q/A Placehold1   |         | edwong    | 27 Nov | Details TBD
| Ready for 9 Dec  |         | jedp      | 02 Dec | All 9 Dec tasks due

Reviewers
---------

| Bug    |  scope   | assignee      | f/r candidates           | booked? | details |
| ------ | -------- | ------------- | ------------------------ | ------- | ------- |
| 929388 | gaia/sys | ferjm         | alive, vivien            | ?       | FxAManager (big)
| 930471 | gaia/UI  | stomlinson    | borja, sergi             | yes     | FTU UI
| 930074 | gaia/UI  | olav (?)      | borja, sergi, kaze       | yes     | Settings UI
| 935602 | gaia/UI  | borjasalguero | alive, vivien            | ?       | KB hints
| 935232 | gecko    | zaach         | markh, taubert, sec-info | y, y, ? | FxAccountsClient.jsm
| 909967 | gecko    | zaach         | markh, taubert           | yes     | FxAccounts.jsm
| 929386 | gecko    | ferjm         | fabrice, ttaubert, jedp  | ?       | DOMIdentity
| 936146 | gecko    | jedp          | warner                   | ?       | jwcrypto
| 936487 | gec/gaia | TBD           |                    |         | Disable flag(s)

Current normative docs
----------------------
* https://wiki.mozilla.org/Identity/Firefox-Accounts
* https://wiki.mozilla.org/Identity/UX#FXOS
* https://bugzilla.mozilla.org/showdependencytree.cgi?id=920135&hide_resolved=1
* http://www.gliffy.com/go/publish/image/5067437/L.png

Representatives
----------------

|  Owner    | Area |
| --------- | ------------ |
| arogers   | FxOS product
| ckarlof   | FxA Services
| cserran   | FxOS engineering
| edwong    | Q/A
| jgruen    | UX (including FxOS UX team)
| kparlante | Metrics
| lloyd     | Mozilla as a whole
| toxborrow | Legal
| toxborrow | Security

bugs yet?
| confirmation email tells server which service started it, service reminds user what app to load on phone
| send origin of flow to server for metrics (same as above?)
