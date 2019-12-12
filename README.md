# CalcExcelShortcuts
Use Excel Style Shortcuts with LibreOffice Calc

# Why
Are you an Excel Power User looking to switch to LibreOffice Calc?
Miss ALT-H-D-C to delete columns?
Not able to run Excel in a Virtual Machine?
Excel Style shortcuts are easy to set up! Here's how.

# Setup
Download [this xml](https://github.com/omeraliso111/CalcExcelShortcuts/blob/master/menubar.xml) file and place it in the following folder, replacing the original, remember to backup the original file first!

`~/.config/libreoffice/4/user/config/soffice.cfg/modules/scalc/menubar`

Restart LibreOffice Calc, and now you can use all of Excel's Shortcuts. To test it out hit ALT, type in "houc" (Excel's shortcut for Hide Column) and hit enter. 

# How it Works
While using linux, you may have seen this textbox popup when clicking ALT
[hud.png](/images/hud.png)

Pretty nifty feature, what it does it search through the menu options for what you typed in.
So if you hit ALT and type in "Hide Column" LibreOffice Calc will take you to menu option Format > Column > Hide.

[hide_column_calc.png](/images/hide_column_calc.png)

Knowing this, the simplest solution to using Excel's shortcuts is to change the menu options labels. For example, to use Excel's shortcut for hiding a column, change "Hide Column" to "Hide Column - houc". The only difference in LibreOffice is you need to hit "Enter" before running the action.

[houc_calc.png](/images/houc_calc.png)

# Further Customization

I've included most of the common actions that are preformed in Excel, but if you want to add more shortcuts, open the xml file in your favourite text editor, find the menu option you want to change

`<menu:menuitem menu:id=".uno:HideColumn"/>`

and add a menu:label parameter to it that includes Excel's equivalent shortcut

`<menu:menuitem menu:id=".uno:HideColumn" menu:label="Hide Column - houc"/>`

Restart LibrerOfice Calc, hit ALT, and type in your excel shortcut.
