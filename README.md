# Multi-Threading
Parte teorica:
Il Multithreading è una funzionalità del sistema operativo che consente di eseguire diverse parti di un programma contemporaneamente o in rapida successione.
Il Multithreading migliora le prestazioni dei programmi solamente quando questi sono stati sviluppati suddividendo il carico di lavoro su più thread,con la possibilità di questi ultimi di essere eseguiti in parallelo.
Abbiamo implementato il Multithreading per fare in modo che le due classi utilizzate stampassero contemporaneamente i messaggi in output.
Con l'uso di due classi che estendevano un thread ognuno, mandandoli in output tramite dei for, si è potuto notare che i messaggi non erano ordinati a seconda della loro classe di appartenenza, ma mischiati tra di loro senza logica. 
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


Descrizione Classe Say:
abbiamo creato la classe Say contenente l'attrubuto di tipo String che verrà visualizzata in output.
Con l'utilizzo del metodo run() e al suo interno un ciclo for{} abbiamo stampato la stringa.
Nel main abbiamo creato due oggetti dello stesso tipo successivamente, per entrambi abbiamo usato lo start(), in modo da avviare i thread cooperanti.
Avendo i due thread tempi di esecuzione differenti, l'output mostrava la cooperazione dei thread a stampare i messaggi.

start() serve per avviare il metodo run().

Il metodo run() contiene il codice che deve svolgere il thread; viene avviato tramite il metodo start().

Extends permette alla classe che ha usato questo comando di usare tutti i metodi della classe Thread.

wait() dice al thread che chiama questo metodo di mettersi in attesa e di aspettare che un altro thread chiami il notify().

notify() chiama solo un thread tra quelli in attesa. La scelta del thread da chiamare la compie Java Virtual Machine.

notifyAll() chiama tutti i thread in attesa. Il thread con la priorità maggiore si avvierà per primo.
