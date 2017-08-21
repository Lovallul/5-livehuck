from tkinter import *
import winreg as reg

AeroPeek = reg.OpenKey(reg.HKEY_CURRENT_USER,
	r"SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Advanced",
	0,
	reg.KEY_ALL_ACCESS)
#AeroPeekChange = reg.SetValueEx(AeroPeek, "DisablePreviewDesktop", 0, reg.REG_DWORD, 0x00000001)
AeroPeekValue = reg.QueryValueEx(AeroPeek, "DisablePreviewDesktop")[0]
reg.CloseKey(AeroPeek)

master = Tk()
var = StringVar()
if AeroPeekValue == 1:
	c = Checkbutton(master, text="Aero Peek", variable=var)
else:
	c = Checkbutton(master, text="Aero Peek")
c.pack()
c = Button(master, text="Save")
c.pack()
mainloop()
