# UIAViewer.ahk-for-UIAutomation.ahk

All credit for the original goes to: https://github.com/Descolada/UIAutomation

List of Changes:

- Option to select how to find a window, exe, class, or title
- Function based actions! Everything is abstracted to functions
- Functions as they multiply receive numbers appended to their name instead of more code in the box
- No need to restart to build/test more code
- Code receives proper indentation (for the most part (;)
- Large applications like Chrome or VSCode split titles by dash to manage unique titles vs application

New keybind of f3 for generating code, macro creator is front and center.

Basics: 

This application helps navigate Windows desktop applications. 

- Download all code 

- Run viewer

- F1 to scan UI items

- F3 to generate code


 ![image](https://user-images.githubusercontent.com/98753696/219829487-d62bd4bc-a708-410d-9deb-cb8c03ddff76.png)



       #Include lib\UIA_Interface.ahk
       SetTitleMatchMode, 2
       global UIA := UIA_Interface()
       ;learn more here https://github.com/Descolada/UIAutomation/wiki/04.-Elements


       el := WinExist(" github.com/Descolada/UIAutomation ahk_exe AutoHotkey.exe")


       el := UI(el)
       ; the handle can be re-used for various actions

       Do_Click(el)


       UI(el){
          WinActivate, ahk_id %el%
          WinWaitActive, ahk_id %el%
         el := UIA.ElementFromHandle(el)
           return el
       }

       Do_Click(el){
         loop, 10
         {
         try {
       el := el.FindFirstBy("ControlType=Document AND Name='Start capturing and press the F3 Key to add action.' AND AutomationId='41'",,2)
              break
          } catch e{
             Sleep, 100
            }
         }

       loop, 10
         {
         try {
       el.Click()  
              break
          } catch e{
             Sleep, 100
            }
         }

         }
