# Multi-Threading
Con l'uso di due classi che estendevano un thread ognuno, mandandoli in output tramite dei for si è potuto notare che i messaggi non erano ordinati a seconda della loro classe di appartenenza, ma mischiati tra di loro senza logica. 
A causa dei due thread che agiscono in contemporanea, i messaggi di output sono mischiati.
Esempio 1:
hi
hello
hello
hello
hello
hello
hello
hello
hello
hi
hi
hi
hi
hi
hi
hi
Esempio 2:
hello
hello
hello
hi
hello
hi
hello
hi
hi
hello
hi
hi
hello
hello
hi
hi
Esempio 3:
hello
hi
hi
hi
hi
hello
hello
hello
hi
hello
hello
hello
hello
hi
hi
hi
hi
