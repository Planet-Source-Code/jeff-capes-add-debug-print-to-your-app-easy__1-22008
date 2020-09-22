<div align="center">

## Add Debug\.Print to your app easy


</div>

### Description

The Debug.Print is most important as long as your program runs! If there is something wrong, error/problem, the user can always report to you what he did, by showing you the debugtext. BUT when it's compiled the user of your app. can't see the Debug.Print window!!! The thing I add (always) into my program is showed beneeth here following (simple but efficient):
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[\~:\. Jeff 'Capes' \.:\~](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/jeff-capes.md)
**Level**          |Beginner
**User Rating**    |3.0 (21 globes from 7 users)
**Compatibility**  |VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Debugging and Error Handling](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/debugging-and-error-handling__1-26.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/jeff-capes-add-debug-print-to-your-app-easy__1-22008/archive/master.zip)





### Source Code

```

1. make a Form called frmDebug
2. add a textbox called txtDebug (multiline+scrollbar(s))
3. Add a Module and Copy this into the module:
Option Explicit
Public ShowDebugWindow As Boolean
Public Function DebugPrint(DebugStr As String)
 If ShowDebugWindow = True Then
   frmDebug.Show
   frmDebug.txtDebug = frmDebug.txtDebug & vbCrLf & "[" & Time & "] " & DebugStr
 Else
   frmDebug.Hide
 End If
End Function
For those who read this but don't understand what to do exactly:
1. Add a Form to the project (Form1)
2. Add a button into Form1
3. (Click) Code for the button is:
Private Sub Command1_Click()
  ShowDebugWindow = True
  DebugPrint "Button clicked!"
End Sub
when you run yer program (startup object is Form1) press the button and the DebugWindow will popup!
Good Luck!
http://start.at/iseekyou
```

