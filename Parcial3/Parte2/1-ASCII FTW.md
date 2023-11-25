### ASCII FTW
## Objetivo

This program has constructed the flag using hex ascii values. Identify the flag text by disassembling the program.You can download the file from [here](https://artifacts.picoctf.net/c/506/asciiftw).
## Solución
```bash
- Inicie ghindra
- inicialice un nuevo proyecto
- abri la ventana donde descargue el archivo y lo arraste a la ventana de ghindra sobre la carpeta del nuveo proyecto que cree
- abri el archivo que arrastre
- le di click en el boton de play en la parte superior de la ventana
- me fui a la carpeta DATA
- cree un nuevo scrip
- dentro del scrip se eyecuta el siguite codigo

from ghidra.program.model.mem import MemoryAccessException start_addr = currentProgram.getAddressFactory().getAddress("00101184") end_addr = currentProgram.getAddressFactory().getAddress("001011fc") byte_list = [] current_addr = start_addr while current_addr <= end_addr: instruction = getInstructionAt(current_addr) if instruction is not None:  
    operand = instruction.getOpObjects(1)[0] # get second operand byte_val = operand.getValue() & 0xFF # convert to unsigned byte byte_list.append(byte_val)  
      
    current_addr = current_addr.next() flag = list(map(chr, byte_list)) print("Flag:", "".join(flag))

- y por ultimo me salio este resultado

NewScript.py> Running... 
('Flag:', 'picoCTF{ASCII_IS_EASY_3CF4BFAD}') 
NewScript.py> Finished!
```
## Notas adicionales

## Bandera

picoCTF{ASCII_IS_EASY_3CF4BFAD}
## Hints

- The combined range of hex-ascii for English alphabets and numerical digits is from 30 to 7A.
- Online hex-ascii converters can be helpful.
### Referencia