# UIAViewer.ahk-for-UIAutomation.ahk

UIAViewer.ahk for UIAutomation.ahk, with some modifications. All credit for the original goes to: https://github.com/Descolada/UIAutomation



UIAutomation is tough. I was going to start by building a tool side by side with UIAViewer, and figured its just easier diving into an edit of the original.

Problems I had with UIAViewer (I love the tool, but these can be challenging for new users):

1- Too specific. 99% of the time, if I want target VSCode, or Notepad, the concern of the class, title, etc for multiple windows I BELIEVE is down stream as a new user, from just trying to get UIAutomation to work. Once you get it working, which can take hours, then you can worry about multiple windows. Notepad, Chrome, VSCode, they all include document or page details in teh title and that muddies up results (especially for ametuer users).

2 - Defaults are set to case sensitive, exact title match, and waitelementexist. I find this also to be downstream from where new users should be entering. New users should be setup with a try{} catch e{} matchmode=2 and findallby or findfirstby.

The most discouraging thing was the dozens of hours spent pouring over documentation, not knowing that a simple title or window change rendered a code inoperable.


These are just opinions and to this day, a bit of chip on my shoulder for why I wanted to make some changes.

This was all done in the last couple days, I'll outline changes, and take feedback as well as continue to work on other things and todos. Please let me know of any mistakes.


changes:
- if title > 20 characters, it splits by "-", most popular windows split (document_name) - (program_name)
- WinGet replaces WinExist
- Try Catch added for FindAllBy
- Remove Defaults of WaitElementExist and Match Case Sensitive

later today and this week Ill be adding:
- Robust notes for new users, including comments on each line
- options to drill down or loop through just a given control
- credit to the original creator (sorry I will add asap)
- more ideas flowing



The [1] is going to be for findallby which I will be changing. Please ignore for now. 

![image](https://user-images.githubusercontent.com/98753696/217550580-17a22ce3-a662-4223-bd87-1b96221e8971.png)


