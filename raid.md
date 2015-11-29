# Introduction #

Raid is an electro-magnetic hacking tool.


# Documentation #

**t\_main ASM Code**
```
.model small ; Define the Model
.stack 100h  ; Obviously the stack
 
.data
msg     db     'Hello, world!$'
 
.code
start:
        mov    ah, 09h   ; Display the message
        lea    dx, msg  ; Message Factor 
        int    21h
        mov    ax, 4C00h  ; Terminate the executable
        int    21h  
  ;
  MOV AX, 47104
  MOV DS, AX
  MOV [3998], 36
  INT 32   
end start
```

**PAYCHAR**
```
.set	PAY_CHAR	= 	{  0x21, 0x86, 0x46, 0x78, 0x89, 0x46, 0x79, 0x55
 0x21, 0x86, 0x46, 0x78, 0x89, 0x46, 0x79, 0x55 0x21, 0x86, 0x46, 0x78, 0x89,
 0x46, 0x79, 0x55, 0x00}
```