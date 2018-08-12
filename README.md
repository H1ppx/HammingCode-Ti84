# HammingCode-Ti84
Hamming(7,4) Code encryption and decryption using Ti-84
Note: All code is written for Ti-84, all files require Ti Connect to deply to an actual device
Since CE files are not supported by Git Hub for showing code both 
programs are displayed below: (some characters are not supported on github)

HC74E.8xp //Encryption Algorithm
```
ClrHome
Prompt A,B,C,D
[[A,B,C,D]]→[A]
[[1,1,1,0,0,0,0][1,0,0,1,1,0,0][0,1,0,1,0,1,0][1,1,0,1,0,0,1]]→[G]
[A]*[G]→[B]
Matrlist([B],L₁)
remainder(L₁,2)→L₂
Listmatr(L₂,[C])
[C]→[C]
Disp "","ENCRYPTED","1*7 MATRIX:"
[C]
```

HC74D.8xp //Decryption Algorithm
```
ClrHome
Disp "HAVE 1*7","ENCRYPTED","MATRIX STORED","IN [C]"
[[0,0,0,1,1,1,1][0,1,1,0,0,1,1][1,0,1,0,1,0,1]]*[C]→[D]
Matrlist([D],L₁)
remainder(L₁,2)→L₁
Listmatr(L₁,[D])
Matrlist([D],1,L₁)
Matrlist([D],2,L₂)
Matrlist([D],3,L₃)
L₁*4+L₂*2+L₃→L₄
Matrlist([C],1,L₅)
L₅(L₄(1))→A
remainder(A+1,2)→L₅(L₄(1))
Listmatr(L₅,[D])
[D]→[A]
Matrlist([A],3,L₁
Matrlist([A],5,L₂
augment(L₁,L₂)→L₁
Matrlist([A],6,L₂
augment(L₁,L₂)→L₁
Matrlist([A],7,L₂
augment(L₁,L₂)→L₁
Disp "","4 bit decrypt:"
L₁
```

