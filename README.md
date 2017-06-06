# threadFunc
For calling a function in a new (ahk) thread.
Basic  usage:
	fn := new threadFunc("functionNameOrObject")
	fn.call()
Example:

fn:= new threadFunc("g")
f1::
	SendMode,Play
	g()
	fn.call()
return
g(){
	Msgbox, % A_SendMode
}
esc::exitapp