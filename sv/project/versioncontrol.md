Versionshantering är ett viktigt verktyg att kunna använda sig av som utvecklare, speciellt i projekt där man utvecklar flera personer tillsammans. Versionshanteringssystemets främsta uppgift är att se till så att olika utvecklare inte förstör varandras ändringar. Det finns flera olika system för versionshantering och det är givetvis en fördel att känna till många av dem. Exempel på andra system är: Git, Subversion, Perfoce, Team Foundation Server/source safe och CVS. Ibland länkas versionshanterinssystemet ihop med med system för projektdokumentation/hantering, t.ex. en wiki, issue-hantering, planeringsverktyg etc.

Ditt projekt (kod och annan implementation och dokumentation) skall i denna kurs versionshanteras på tjänsten GitHub. GitHub bygger på versionshanteringssystemet Git. Har du inte använt Git tidigare så finns det en [introduktion till Git och GitHub](https://coursepress.lnu.se/info/manual/kom-igang-med-github/) att börja med.

Du kommer att bli tilldelad ett repositorie i början av kursen. Detta kommer att vara ett privat repro på [organizationen "1dv403"](https://github.com/1dv430) på GitHub. Du, kursledningen och din handledningsgrupp kommer att kunna se detta repo.

Vad ska versionshanteras?

Det korta svaret är ALLT du själv producerar! Ett lite längre svar är: alla filer som man själv editerar manuellt eller som behövs för att kunna leverera systemet. T.ex.

* Dokument som t.ex. projektplan, iterationsplan, risklista, kravspec, etc. etc. Detta versionshanteras via wikin som hör till ditt GitHub-repo.

* Implementation som källkod och grafik som t.ex. asp, php, psd filer.
* Innehåll till systemet som t.ex. bilder i orginalutförande som behövs (.psd filer).
* Manuellt genererat innehåll som t.ex. bilder som behövs fast i leveransformat (.jpg, .gif, .png)
Projekt/IDE specifika filer som kan underlätta arbetet t.ex. Visual Studio Solution filer (.sln)

Vad ska inte versionshanteras?
* **API-nycklar, lösenord etc.**: Dock så händer detta hela tiden. Var noga med att skilja dina nycklar/lösenord från din kod genom t.ex. "miljövariabler". 
* Externa libs. Om din miljö är beroende av externa bibliotek etc. så bör dessa inte versionshanteras utan detta lämnar vi till de som underhåller den koden att sköta. Exempel på detta är jQuery, npm-bibliotek, ruby-gems etc.
* **Din bygda kod.** Detta kan diskuteras. Det kan finnas vissa tillfällen då det är bra att även minifierad/uglyfied-kod kan vara bra att ha i versionshanteringen tillsammans med en fullt körbar version av din kod. 

Versionshanteringen ska hjälpa projektdeltagarna att vara up to date med projektdokumentationen, kunna arbeta på systemet, samt att kunna leverera systemet snabbt och enkelt.

Man ska alltså undvika att versionshantera sådant som genereras automatiskt, t.ex. av en kompilator då frekventa ändringar av denna typ av filer ofta skapar konflikter mellan olika versioner. Det gäller att känna till sin utvecklingsmiljö så bra som möjligt. Se till att direkt lägga in en .gitignore-fil och hela tiden använda `git status` för att säkerhetställa att du inte lägger till kod till versionshanteringen som inte ska vara där. En bra regel kan vara att alltid lägga till alla filer explicit med `git add {FILENAME}` och undvika `git add -A`.
