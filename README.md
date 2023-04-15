# Strings
**Programma C# per lo studio delle stringhe.**
## Problema assegnato:
Ci è stato assegnato di creare diversi codici con il quale, andando a leggere una stringa inserita in input dall'utente, la trasformiamo per primo in un array di char, tramite la funzione ToCharArray(); e successivamente modifichiamo l'array dato per ottenere il risultato voluto. Non è possibile utilizzare le funzioni fornite da Visual Studio Code (Proprio come se stessimmo lavorando in C). Tutti i vari metodi saranno inseriti all'interno di una classe a parte chiamata MiaStringLib, dalla quale richiameremo ciò di cui abbiamo bisogno per mostrare in output il risultato desiderato. Tutto il programma sarà fatto per creare una app MAUI.

## Varie ricreazioni di funzioni normalmente utilizzabili nelle stringhe:

* Lunghezza (Permette, una volta data una stringa di ritornare In una variabile Int)
```
public static int Lunghezza(string Smadiversa)   //nome di un metodo che ritorna un intero accenttando una stringa
        {
            char[] caratteri = Smadiversa.ToCharArray();
            int retVal = 0;                 //RetVal è il valore del vettore.

            foreach (char carattere in caratteri)           //Divide la stringa
            {
                retVal++;                                  //Somma le varie lettere che compongono la stringa
            }

            return retVal;
        }
```
* ToUpper (Permette, una volta inserito un char che sia una lettera, di renderla maiuscola).
* ToLower (Permette, una volta inserito un char che sia una lettera, di renderla minuscola).
* IsLetter (Permette, una volta inserito un char, di verificare se è una lettera o meno).
* IsNumber(Permette, una volta inserito un char, di verificare se è un numero o meno).

## Vari metodi utilizzati per la creazione del programma:

* Minuscolo (Rende i char inseriti, se lettere, minuscoli).
```
 //Minuscolo con metodo
        public static string Minuscolo(string s)   //ECCO COME CREARE TOLOWER SENZA USARE LA FUNZIONE TOLOWER.
        {
            int len = Lunghezza(s);

            char[] caratteri = s.ToCharArray();         //trasformo la stringa che mi arriva in un vettore di carattere,
                                                        non posso modificare le stringhe pk sono degli invarianti
            for (int x = 0; x < len; x++) 
            {
                caratteri[x] = ToLower(caratteri[x]);
            }
            return new String(caratteri);            // crea una nuova stringa basandosi sulla stringa che ti dono (caatteri)
        }
```
* Maiuscolo (Rende i char inseriti, se lettere, Maiuscoli)
* Alfabetica (Controlla se la stringa inserita è costituita solamente da lettere)
* Alfanumerica (Controlla se la stringa inserita è costituita sia da lettere che da numeri)
* NumeroLettere (Conta il numero di lettere all'interno della stringa)
* NumeroParole (Conta il numero di parole all'interno della stringa inserita)
* Reverse (Inverte la stringa inserita).
* Capitalized (Rende la prima Lettera di ogni parola maiuscola).
* Palindroma (Controlla se la parola è palindroma).
