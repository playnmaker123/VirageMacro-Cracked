# VirageMacro-Cracked
The premium version of virage's grow a garden macro for free.  
Just download the .zip file above

# How can you do this yourself?
Follow these steps below to crack Virage's premium macro yourself!


# 1: Download the official file
Join [virage's discord server](https://discord.gg/virage) and get the paid verion of Virage's macro in the "macro-link" channel  
Note: If you attempt to use these steps to crack the free version it will not work!  
After you do this, extract the file.  

# 2: Open up the ahk code
Find main.ahk in the extracted file, and right click it.  
Click on "edit in notepad"

# 3: Find the paywall and delete it
Use Control F, and search up "username := Trim(username)".  
Select all of the paywall (it usually looks something like this):  

```ahk
/*
VerifyUser(username) {
    global GAME_PASS_ID
    username := Trim(username)

    reqBody := "{""usernames"":[""" username """],""excludeBannedUsers"":true}"
    whr := ComObjCreate("WinHttp.WinHttpRequest.5.1")
    whr.Open("POST","https://users.roblox.com/v1/usernames/users",false)
    whr.SetRequestHeader("Content-Type","application/json")
    whr.Send(reqBody),  whr.WaitForResponse()
    if (whr.Status!=200 || !RegExMatch(whr.ResponseText,"""id"":\s*(\d+)",m))
        return 0
    userId := m1

    ownURL := "https://inventory.roblox.com/v1/users/" userId
           .  "/items/GamePass/" GAME_PASS_ID
    whr2 := ComObjCreate("WinHttp.WinHttpRequest.5.1")
    whr2.Open("GET",ownURL,false), whr2.Send(), whr2.WaitForResponse()
    if (whr2.Status!=200)                        ; request itself failed
        return 0

    return !RegExMatch(whr2.ResponseText, """data"":\s*\[\s*\]")
}


IniRead, isVerified, %settingsFile%, Main, %VERIFIED_KEY%, 0
if (!isVerified) {
    InputBox, rbUser, Premium Access, Please enter your Roblox username:
    if (ErrorLevel)
        ExitApp   ; user cancelled

    if (VerifyUser(rbUser)) {
        IniWrite, 1,              %settingsFile%, Main, %VERIFIED_KEY%
        IniWrite, %rbUser%,       %settingsFile%, Main, VerifiedUsername
        MsgBox, 0, Success, Verification successful, enjoy the macro!
    } else {
        MsgBox, 16, Access Denied, Sorry, that account does not own the required game-pass.
        ExitApp
    }
}
*/
```

and delete it.  
In the future, virage might make small changes to the paywall, and if that happens you can ctrl-f anything in the code above to try to locate it, as there is a very small chance he can redo all of the paywall.  

# If you want an actually good macro (that is also free!)...
Go to https://github.com/epicisgood/Grow-a-Garden-Macro


