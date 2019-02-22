# DynamoDB

**Dokument- och key/value-databas som en service av AWS**

Om ens stack redan existerar i AWS och en dokumentdatabas behövs, kan detta ses<br/>
som ett alternativ. Denna konkurrerar dock inte ut mongodb, utan snarare redis.

Caveats:
 - Icke intuitiva queries
   - Generellt bara key-value queries
   - Finns Sekundära index, men dessa måste defineras vid skapandet av tabellen
 - Sorteringen måste definieras vid skapandet av tabellen
 - Ingen out-of-the-box data-migrering
 - Storleken på datan får inte överstiga 400 kb
 - Det finns JSON-support för datan (om inte väldigt krångligt i skapandet), men inte BSON
 - Ingen schema-validering (enda kravet är att index (+sekundära index) + soteringsnyckel existerar)
 - Luddig prismodell (likt allt som finns i AWS)
 - Den som sätter upp databasen måste veta hur IAM-roller fungerar


| **Kriterium** | **Poäng (0-5)** | **Kommentar** |
|---------------|-----------------|---------------|
| Community | 4 | Enligt [db-engines](https://db-engines.com/en/system/Amazon+DynamoDB) är servicen måttligt populär|
| Tekniska fördelar | 2 | Om stack:en redan existerar i AWS och någon hostad key-value databas krävs är detta helt okej|
| Dokumentation | 4 | Om dokumentation eftersöks finns det [nästan oändigt med detta](https://docs.aws.amazon.com/dynamodb/). Det finns nästan för mycket exempel ... API:et har inte uppdaterats sedan 2012 |
| Testad | 2 | Själv har jag bara använt det i ett _serverless_-projekt för playpilot. Här passade det bra, men lite småstökigt med hantering av sekundära index |
| Integration | 4 | Tekniken är stabil och fungerar väl ihop med systemet om det redan existerar inom AWS |
| Införande | 4 | Konceptet är enkelt, DSL:en inte lika intuitiv. Finns sdk och wrappers för i stort sätt _alla_ språk |

Summa poäng (0-30): 20

Rekommendation (text): Enkel att komma igång med, men finns bättre alterativ. <br/> Kräver att datan är väl genomtänkt vid uppsättningen eftersom det inte finns <br/>
något sätt att migrera tabellen i efterhand.

Kategori: potential men riskfylld

Utvärderat av: Dennis Pettersson
