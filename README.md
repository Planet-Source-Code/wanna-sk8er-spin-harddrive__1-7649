<div align="center">

## Spin HardDrive


</div>

### Description

Have you ever had a progressbar or something on your app and you want users to think its doing something really hard.. This will spin your HD so you can get that effect...
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Wanna\-Sk8er](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/wanna-sk8er.md)
**Level**          |Beginner
**User Rating**    |4.6 (23 globes from 5 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Jokes/ Humor](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/jokes-humor__1-40.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/wanna-sk8er-spin-harddrive__1-7649/archive/master.zip)





### Source Code

```
'Note: Place a command button named "Command1" on a form...
Private Sub Command1_Click()
Dim fileblock(60000000) As Byte
'opens a file to output to
Open "c:\windows\temp\tempfile.dat" For Binary As #1
'creates a massive string to write to the file
For i = 1 To 1000000
fileblock(i) = 1
Next i
'this is the loop. it keeps going until the file reaches the size you set in the txtfilesize box
Do Until LOF(1) > txtfilesize
Put #1, , fileblock
DoEvents
Loop
'closes the file
Close #1
'this deletes the file you just made
Kill "c:\windows\temp\tempfile.dat"
End Sub
```

