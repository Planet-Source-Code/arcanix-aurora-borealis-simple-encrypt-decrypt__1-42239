<div align="center">

## \[Aurora Borealis\] Simple Encrypt/Decrypt

<img src="PIC200317053224082.JPG">
</div>

### Description

A simple encryper/decrypter I made for a friend...

It converts each char into the asc value for that char and reverses it later...
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Arcanix](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/arcanix.md)
**Level**          |Intermediate
**User Rating**    |3.5 (28 globes from 8 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Complete Applications](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/complete-applications__1-27.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/arcanix-aurora-borealis-simple-encrypt-decrypt__1-42239/archive/master.zip)





### Source Code

<pre><font color="#008000">' Place 2 textboxes (txtCoded and txtRea ' l) and 2 command buttons (btndecrypt and ' btnencrypt) on a form</font>
<font color="#000080">Private Sub</font> btndecrypt_Click()
<font color="#000080">Dim</font> MyValue <font color="#000080">As String</font>
MyValue = 3
txtReal.Text = ""
<font color="#000080">If </font>Len(txtCoded) < 1 <font color="#000080">Then Exit Sub</font>
<font color="#000080">For</font> i = 1 To Len(txtCoded) / 3
<font color="#000080">If</font> MyValue = 3 <font color="#000080">Then</font>
txtReal = txtReal & Chr(Left(txtCoded, MyValue))
<font color="#000080">Else</font>
txtReal = txtReal & Chr(Right(Left(txtCoded, MyValue), 3))
<font color="#000080">End If</font>
MyValue = MyValue + 3
<font color="#000080">Next</font> i
<font color="#000080">End Sub</font>
<font color="#000080">Private Sub</font> btnEncrypt_Click()
<font color="#000080">Dim</font> MyValue <font color="#000080">As String</font>
<font color="#000080">Dim</font> MyValue2 <font color="#000080">As String</font>
MyValue = 0
MyValue2 = 1
txtCoded = ""
<font color="#000080">If Len</font>(txtReal) < 1 <font color="#000080">Then Exit Sub</font>
<font color="#000080">For</font> i = 1 To Len(txtReal)
txtCoded = txtCoded & Asc(Mid(txtReal, i, 1))
MyValue = MyValue + 1
<font color="#000080">If</font> Len(txtCoded.Text) < 3 * MyValue <font color="#000080">Then</font>
 MyValue2 = Right(txtCoded.Text, 2)
 txtCoded.Text = Left(txtCoded.Text, Len(txtCoded.Text) - 2)
 txtCoded.Text = txtCoded.Text & "0" & MyValue2
<font color="#000080">End If</font>
<font color="#000080">Next</font> i
<font color="#000080">End Sub</font>
</pre>

