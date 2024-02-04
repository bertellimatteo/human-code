#  il gioco del blackjack 

## 21 vittoria, grande baldoria! 
  ### problem
  - il problema sta nel cercare di minimizzare le perdite e massimizzare le vincite contro il banco o mazziere, così che il capitale finale sia superiore di quello iniziale, in questo caso avremo un surplus positivo, mentre nel caso contraio si avra realizzarto un surplus negativo

  ### basic rules
    
   > Il blackjack è molto semplice: lo scopo del gioco è quello di ottenere un punteggio superiore a quello del banco, avvicinandosi il più possibile a 21, senza però superarlo. Se si va oltre 21 si “sballa” e si perde. 
     Ad ogni partecipante vengono distribuite inizialmente 2 carte, poi il giocatore deciderà se chiederne altre o se fermarsi.
     Si utilizzano le carte a semi francesi (cuori, quadri, fiori e picche), ma in questo gioco il seme e il colore non hanno alcuna importanza, infatti si prende in considerazione solo il valore numerico.
     Tutte le carte numerate da 2 a 10 mantengono il loro valore, le figure (J, Q e K) valgono 10 e gli assi possono valere 1 oppure 11. Il valore dell'asso è a discrezione del giocatore: se una mano è composta da un asso e un 8 conviene considerarlo un 11 (11 + 8 = 19, un buon punteggio), mentre in una mano composta da asso e 6 conviene considerarlo uno (6 + 1 = 7) per poter chiedere un'altra carta alla casa.
     Una mano composta da carta di valore 10 ed un asso prende il nome di Blackjack e rappresenta numericamente il valore più alto realizzabile, cioè 21.
     Prima di iniziare la partita, il giocatore deve effettuare una puntata collocando l'ammontare di fiches scelto nell'apposita casella sul tavolo. Una volta fatta la puntata, il gioco ha inizio e le carte vengono distribuite.
     Sia il banco che il giocatore ricevono due carte: quelle del giocatore sono entrambe scoperte, mentre una di quelle del banco è coperta. Il giocatore quindi può solo ipotizzare quale possa essere il punteggio del banco.
     Senza considerare situazioni particolari, le azioni che può compiere il giocatore a questo punto sono essenzialmente due:
     Chiedere un'altra carta (hit): il giocatore riceve una ulteriore carta, il cui punteggio si somma a quello delle due carte della mano di apertura. Questa azione può essere fatta più di una volta a patto che il punteggio non superi il 21. Se il giocatore sballa la mano è considerata perdente.
     Decidere di fermarsi (stare): il giocatore chiude la mano con il punteggio attuale senza ulteriori azioni.
     Una volta che il giocatore ha terminato le sue azioni e il suo punteggio è deciso, il banco prende l'iniziativa, mostrando anche la sua carta coperta. Il banco non ha totale libertà di scelta, ma deve seguire due regole:
     Se il suo punteggio è inferiore a 17, è costretto a chiedere ulteriori carte (hit) finché il punteggio non è uguale o superiore a 17.
     Se il suo punteggio è uguale o superiore a 17, deve stare.
     A questo punto, se nessuno ha sballato (e quindi perso), si confrontano i punteggi del banco e del giocatore: il più alto decreta il vincitore.

  ### context 
  - la persona "x" è seduta ad un tavolo da gioco mentre il mazziere, o in questo caso persona "y", tiene le redine del gioco. 
  - sul banco ci sono delle carte a semi francesi 
  - la persona "x" e il mazziere hanno un capitale a dispozione che non può mai andare sotto lo zero

  ### solution
  - se il soggetto x ha capitale a disposizone maggiore di zero può effettuare una puntata al tavolo di y

    - se la puntata di x è sotto la chip minima y deve rifiutare

    - se la puntata di x è sopra la chip minima y deve accettare

      - se la giocata viene accettata y deve distribuire le carte

        - y inizia a ditribuisce le carte in senso orario  

          - y da la prima carta al giocatore x di faccia posandola davanti a x sul banco
          - se non ci sono altri giocatori y può dare la carta a se stesso di retro posandola davanti a y sul banco
          - se y ha finito il primo giro di carte può iniziare il secondo giro di carte
          - y distribuisce la seconda carta al giocatore x di faccia posandola davanti a x sul banco
          - se non ci sono altri giocatori y può dare la carta a se stesso posta di faccia posandola davanti a y sul banco
          - se tutti hanno due carte si può continuare

        - se y ha fintio di distribuire le carte il giocatore x può iniziare la giocata
       
        - se la somma delle carte di x fa ventuno e la somma delle carte di y non fa ventuno il banco paga due volte la puntata iniziale di x e la partita finisce

        - se x è soddisfatto della somma delle sue carte può sceglie di stare e x rimane con la somma della prima e della seconda carta

        - se la somma delle carte di x non fa ventuno x ha la possibilta di scegliere

          - se x sceglie di chiedere un altra carta y da un'altra carta ad x
            - y da la carta al giocatore x di faccia posandola davanti a x sul banco

          - se x ha un'asse x può scegliere il valore di essa tra uno e undici 

          - se la somma delle carte d x è maggiore di ventuno x perde la mano
            - se x perde la mano y prende la puntata e la partita finisce

          - se la somma è minore di ventuno x può scegliere di chiedere un'altra carta 
            - se la somma delle carte di x è maggiore di ventuno x perde la mano
              - se x perde la mano y prende la puntata e la partita finisce

          - viene ripetuto finchè x non è soddisfatto delle sue carte

        - se x è soddisfatto delle sue carte il turno passa il tunro ad y

        - y gira la sua unica carta coperta carta

          - se la somma delle carte di y è maggiore o pari a diciasette il banco può decidere se chiedere un'altra carta o stare

            - se la somma delle carte di y è maggiore della somma delle carte di x il banco sta e vince
              - se y vince la mano, y prende la puntata di x e la partita finisce

            - se la somma delle carte di y è minore della somma delle carte di x, y può scegliere di pescare un'altra carta
              
              - se y ha un'asse y può scegliere il valore di essa tra uno e undici 
              - se la somma delle carte di y è maggiore di ventuno y perde la mano
                - se x vince la mano y paga il doppio la puntata ad x e la partita finisce

              - se y decide di pescare, y si da una carta di faccia posandola davanti a se sul banco

                - se la somma delle carte di y è maggiore di quella di x, y vince la mano 
                - se y vince la mano, y prende la puntata d x e la partita finisce

              - se la somma delle carte di y è minore di ventuno, y può scegliere di pescare un'altra carta 
              - viene ripetuto finchè y non è soddisfatto delle carte  

          - se la somma delle carte di y è minore a diciasette il banco deve chiedere un'altra carta
              - se y ha un'asse y può scegliere il valore di essa tra uno e undici 

              - se la somma delle carte di y è maggiore di ventuno y perde la mano
                - se y perde la mano, y paga il doppio la puntata ad x e la partita finisce
                
              - se il banco pesca e la somma delle carte di y è maggiore di quella di x, y vince la mano
                - se y vince la mano, y prende la puntata ad x e la partita finisce

              - se la somma è minore di ventuno y può scegliere di chiedere un'altra carta 

              - viene ripetuto finchè x non è soddisfatto delle carte  

        - se la somma delle carte di y è maggiore della somma delle carte di x, y vince la mano
          - se y vince la mano, y prende la puntata di x e la partita finisce

- se la partita finisce tutto può esssere ripetuto



          


            


  
        
        
          
         




     
       
    
  



  




