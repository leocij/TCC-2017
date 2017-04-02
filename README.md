# TCC-2017
Trabalho de Conclusão do Curso de Ciência da Computação - UNITRI - 2017

Exemplo de execução:

Teste em uma tela cmd:

------------------------

D:\github\testes>lvmc teste.lvmc

------------------------

D:\github\testes>lvm-v23 saida.lvm
Digite A: 10
Digite B: 20
Soma = 30
Estado final da Memoria.
00 00 00 0A 00 00 00 14 00 00 00 1E 44 69 67 69 74 65 20 41 3A 20 00 44 69 67 69 74 65 20 42 3A 20 00 53 6F 6D 61 20 3D 20 00

------------------------

D:\github\testes>type saida.lasm
[00000000h]
[00000004h]
[00000008h]

mov strControl, [0000000Ch]
int 00000000h, strControl

int [00000000h], bufferInt

mov strControl, [00000017h]
int 00000000h, strControl

int [00000004h], bufferInt

mov intControl, [00000004h]
add intControl, [00000000h]
mov [00000008h], intControl

convert strControl, [00000008h]
concat strControl, [00000022h]
int 00000000h, strControl

------------------------

D:\github\testes>type saida.txt
BA BA BA BE 00 00 00 48 00 00 00 2A 01 01 00 00 00 0C 02 01 00 00 00 00 03 04 00 00 00 00 01 01 00 00 00 17 02 01 00 00 00 00 03 04 00 00 00 04 05 02 00 00 00 04 07 02 00 00 00 00 04 02 00 00 00 08 0B 01 00 00 00 08 0C 01 00 00 00 22 02 01 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 44 69 67 69 74 65 20 41 3A 20 00 44 69 67 69 74 65 20 42 3A 20 00 53 6F 6D 61 20 3D 20 00 FF

------------------------
