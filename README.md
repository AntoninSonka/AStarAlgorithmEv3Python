Manuál

poznámka: -

možný problém a jak ho spravit: *

Tlačítko je tlačítko v pravo

2. tlačítko je tlačítko vlevo


Jak připravit pole a program pro spuštění algoritmu

    Robot jezdí po poli 4x4. Kostky by měli být od sebe vzdáleny 26cm, né více, né méňe.
        - Pokud je možné krabice přilepi, tak to udělejte.

    Je důležité aby ve vytváření cesty robot měl vždy alespoň jednu možnou cestu do cíle.
        - Pokud nemá, program spadne.

    Po vytvoření bludiště musíte nastavit v programu startovací souřadnice a cílové souřadnice.

    Ty se nacházejí na konci programu pod názvem:
        - startY
        - startX
        - finishY
        - finishX

        - Souřadnice se indexují od 0 do 3.
        - Souřadnice y = 0 je horní řádek.
        - Souřadnice x = 0 je levý sloupec.

Spuštění programu
    
    Spusťte předem nahraný program.

    Kostka zahraje tón, C3.
        - To značí správné nahrání programu a správná inicializace všech portů.
        - Pokud tento tón zazní v programu, čeká na zmáčknutí tlačítka.
        - Je to ten nejnižší tón, který program zahraje.
        * Pokud se tento tón nepřehraje, zkontrolujte na vašem počítači output programu, nejčastěji poblém bývají špatně zapojené porty.

    Postavte robota na předem určenou souřadnici, směřující ultrazvukovým senzorem směrem nahoru.

    Zmáčkněte tlačítko.
    
    Robot zahraje tón C5.
        - To značí start algoritmu.

Průběh programu a starání se o robota v průběhu
    
    Pokud robot udělá stupnici zezhora dolů, bude se rozhlížed a zjišťovat, jestli je před ním zeď.
    Až se robot pootočí, nasměrujte ho na zeď správným směrem.

    Pokud robot zeď uviděl, zahraje 2 tóny vzestupně.
    Pokud robot zeď neviděl, zadraje 2 tóny sestupně.

        -robot začne čekat na stisknutí tlačítka, pokud zeď správně neviděl, jinak stiskněte 2. tlačítko a robot to vezme jako že je před ním zeď.

    Po zjištění jestli zde zdi jsou přijde přejížděcí sekvence.
    
    Robot se natočí správným směrem a rozjede se, následně se otočí zpět směrem nahoru.

    Robot pak počká na stisk tlačítka.
        - To souží k nastavení robota správným směrem, aby neujížděl do strany.

Konec programu

    Jakmile robot dojede na cílové políčko, rozjede se tou nejefektivnější cestou směrem na start, aby ukázal, že cestu doopravdy našel.

    Tyto sekvence budou přejížděcí, tak je nutné robota pokaždé srovnat a následně stisknout tlačítko, jako v přejížděcí sekci.

    Až robot dojede na do cíle, zahraje vzestupnou stupnici a program se ukončí.
        * Pokud se program neukončil, je chyba v softwaru ev3 a musí se vypnout manuálně stiskem tlačítka 'zpět'.
