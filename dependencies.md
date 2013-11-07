Current normative docs (are we regularly reviewing them for accuracy?)
-----------------------------
https://wiki.mozilla.org/Identity/Firefox-Accounts
https://wiki.mozilla.org/Identity/UX#FXOS
  both screen flows have minor inaccuracies as of 7 November


|   Area  |   Owner   |          Issue         |
| ----------------------------------------|
|  UX     | lloyd     | COPPA needed for 1.3?|
|  UX     | jedp      | email verif: requires password? |
|  UX     | jgruen    | Move password reset -> web |
|  FTU    | borja     | email stored between screens? |
|  System | jedp    | email captured in FTU pre-populated elsewhere? |
|  Legal  | ?    | ToS and Privacy Policy Ready? |
| Settings | jedp | Can we log out from Settings?
| Settings | jedp | Can we delete account from Settings?
| Frontend | jedp | Can we launch creation flow from MP/WMF? |


ETHERPAD HARVEST

|   Deliverable          |    Bug     |  Assignee  |    Ready    |     f?     |    r?      |
| ---------------------- | ---------- | ------------------ | ---------- | ---------- |
|   FTU UX HTML/JS    
| Settings UX HTML/JS

UX:
  Launching creation flow from WMF/MP?
    screens built?
    does sign-in flow need custom screen(s) (vs invoking Persona)?
    
Code on device
  Based on https://github.com/jedp/fxa-fxos/blob/master/img/architecture.png
need to review 920135 tree w/ jedp

                                Bug    Ready    f      r
  Gecko
    FXAccounts.jsm           935234     Tue ?
    FXAccountsClient.jsm     935232     Mon ?
    [MinimalIdentity.jsm           ?                   ]
    DomIdentity.jsm          929386         ?
    SignInToFxA.jsm               ?
    jwcrypto	             936146         ?
  gaia/System
    fxa_manager.js           929388         ?
    fxa_ui.js                     ?
    fxa_client.js            929388
  gaia/shared
    fxa_iac_helper.js             ?

Services
  API: picl-idp/raw_password
    deployed (?)
  Web support for password reset
  
Q/A
  peformance recordability
