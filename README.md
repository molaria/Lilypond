# Lilypond
 My Swedish settings for Lilypond

 Samlingsplats för mina egna inställningsfiler till LilyPond.
 Alla filer är fria att använda, ändra och sprida vidare – se licensen (MIT).

 ## Innehåll

 - `svenska.ly`
   Svenska notnamn och ackordbeteckningar enligt svensk tradition:
   - `B` istället för `H`
   - `Bb` istället för `B`

 Filerna är tänkta att användas som moduler du kan inkludera i egna LilyPond-partitur.

 ## Användningsexempel

 Skapa en egen LilyPond-fil och inkludera dina inställningar:

 ```lilypond
 \include "svenska.ly"

 \version "2.25.25"

 \score {
   <<
     \new ChordNames {
       \chordmode { c1 f b:7 bb }
     }
     \new Staff {
       \relative c' {
         c4 ciss d diss
         e f fiss g
         gis a ass b
       }
     }
   >>
 }
 ```

 ## Exempelfil

 Här är en enkel `exempel.ly` som använder `svenska-notnamn.ly`:

 ```lilypond
 \include "svenska-notnamn.ly"

 \version "2.24.0"

 \score {
   <<
     \new ChordNames {
       \chordmode { c1 f b:7 bb }
     }
     \new Staff {
       \relative c' {
         c4 ciss d diss
         e f fiss g
         gis a ass b
       }
     }
   >>
 }
 ```

 För att använda denna `exempel.ly`-fil, följ dessa steg:

 1. Skapa en ny fil i din `Lilypond`-mapp.
 2. Döp den till `exempel.ly`.
 3. Klistra in innehållet ovan.
 4. Spara filen.

 Du kan sedan rendera noterna med LilyPond genom att köra kommandot `lilypond exempel.ly` i din terminal.

 Om du vill inkludera detta i ditt GitHub-repo, följ samma steg som för `README.md`:

 1. Öppna **GitHub Desktop**.
 2. Skriv ett meddelande som "Lade till exempel.ly".
 3. Klicka på **Commit** och sedan **Push origin**.

 Nu finns både `README.md` och `exempel.ly` i ditt GitHub-repo, och andra kan enkelt förstå hur de ska använda dina inställningsfiler.
