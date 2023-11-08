### asm3
## Objetivo

What does asm3(0xba6c5a02,0xd101e3dd,0xbb86a173) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/cb753ae52bca4aa303deca5fbfb01bfb/test.S)
## Solución
```bash
- Vamos a un emulador de Assembler y escribimos lo siguiente:

start:
    push 0xbb86a173
    push 0xd101e3dd
    push 0xba6c5a02
    call asm3

asm3:
	push   ebp
	mov    ebp,esp
	xor    eax,eax
	mov    ah,BYTE PTR [ebp+0xb]
	shl    ax,0x10
	sub    al,BYTE PTR [ebp+0xd]
	add    ah,BYTE PTR [ebp+0xc]
	xor    ax,WORD PTR [ebp+0x12]
	nop
	pop    ebp
	ret

- Ejecutamos paso por paso y nos da la bandera.
```
## Notas adicionales

## Bandera

0x669B
## Hints

- more(?) [registers](https://wiki.skullsecurity.org/index.php?title=Registers)

### Referencia

- https://carlosrafaelgn.com.br/Asm86/