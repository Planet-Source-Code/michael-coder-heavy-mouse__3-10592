<div align="center">

## Heavy Mouse


</div>

### Description

Moves the mouse cursor down your screen and prints the coordinates.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[michael coder](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/michael-coder.md)
**Level**          |Beginner
**User Rating**    |4.0 (24 globes from 6 users)
**Compatibility**  |C\+\+ \(general\), Microsoft Visual C\+\+, Borland C\+\+
**Category**       |[System Services/ Functions](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/system-services-functions__3-23.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/michael-coder-heavy-mouse__3-10592/archive/master.zip)

### API Declarations

```
#include &lt;iostream&gt;
#include &lt;windows.h&gt;
using namespace std;
```


### Source Code

```
#include <iostream>
#include <windows.h>
using namespace std;
int main(){
	bool on=false;
	cout<<"Heavy Mouse by mike\nTo exit press F11\n";
	Sleep(4000);
	while (1){
		Sleep(1);
		POINT pos;
		GetCursorPos(&pos);
		int x=pos.x;
		int y=pos.y;
		Sleep(10);
		SetCursorPos(x,y+1);
		if(GetAsyncKeyState(VK_F11)<0){
			break;
		}
		cout<<"x="<<x<<" y="<<y<<"\n";
	}
	return 1;
}
```

