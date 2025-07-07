# Excample

Open Browser and Login
    Open Browser     ${SERVER}   ${BROWSER} 
    Maximize Browser window
    Sleep   3s
    Input text      //*[@type="email"]        ${mail}
    Input text      //*[@placeholder="Password"]        ${password}
    Click element       //*[@ngclass="bt-primary"]
    Wait Until Element Is Not Visible    //*[@snc="assets/image/LoadingC24.gif"]
    Sleep   2s
    Element text should be          //*[@ngclass="sub-body"]    Dashboard
    Sleep   5s
    Scroll Element Into View    //*[@style="height: 476px !important; width: -webkit-fill-available; flex-direction: column; box-sizing: border-box; display: flex; place-content: stretch flex-start; align-items: stretch; flex: 1 1 100%; max-width: 70%;"]
    Scroll Element Into View    xpath=//tr[.//td[contains(@class, "mat-column-status") and contains(., "Fail")]]
    Sleep   2s
    Click Element    xpath=//td[contains(@class, "mat-column-status") and contains(., "Fail")]/ancestor::tr//*[contains(@class, "primary") and contains(@class, "pointer")]\
    Wait Until Element Is Visible    //*[@data-icon="xmark"]    10s
    Click Element    //*[@data-icon="xmark"]
    Sleep   2s
    Click Element    xpath=//td[contains(@class, "mat-column-status") and contains(., "Success")]/ancestor::tr//*[contains(@class, "primary") and contains(@class, "pointer")]
    Wait Until Element Is Visible    //*[@data-icon="xmark"]    10s
    Click Element    //*[@data-icon="xmark"]
    Sleep   2s
    Scroll Element Into View    xpath=//tr[.//td[contains(@class, "mat-column-status") and contains(., "Pending")]]
    Click Element    xpath=//td[contains(@class, "mat-column-status") and contains(., "Pending")]/ancestor::tr//*[contains(@class, "primary") and contains(@class, "pointer")]
    Wait Until Element Is Visible    //*[@data-icon="xmark"]    10s
    Sleep    500000s
    Click Element    //*[@data-icon="xmark"]
