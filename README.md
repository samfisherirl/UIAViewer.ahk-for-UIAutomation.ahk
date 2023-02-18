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





       el := WinExist(" github.com/Descolada/UIAutomation ahk_exe AutoHotkey.exe")


       el := UI(el)
       ; the handle can be re-used for various actions

       Do_Click(el)


       UI(el){
           return el
       }

       Do_Click(el){
         }
       el.Click()  
         }
