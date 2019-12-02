# Elixir

Elixir är ett språk skapat (2011) ovanpå Erlang/OTP (skapat av Ericsson 1986). Erlang har använts till Ericssons telecom-produkter sedan skapandet och används fortfarande i en stor utsträckning i många system-kritiska produkter. Att Elixir är byggt ovanpå Erlang gör att Elixir kan använda alla Erlang-bibliotek, däremot kan inte Elixir-bibliotek användas av Erlang. Elixir används främst som backend men på senare tid har det även skapats initiativ för att använda det i frontend-sammanhang, [Scenic](https://github.com/boydm/scenic) som är tilltänkt till "Fixed screen IoT devices", [Lumen](https://github.com/lumen/lumen) som är skapat för att kompileras till WebAssembly och därför ska Elixir gå att köra i browsern istället för javascript, till sist även [Phoenix Live View](https://github.com/phoenixframework/phoenix_live_view). Phoenix är ett web-ramverk med vissa likheter till Ruby on Rails och levererar därför server-side renderade html-templates, tillsammans med Live View håller den vyerna "realtids-updaterade" genom att endast beräkna differentieringen på servern och skicka det som är ändrat i DOM-trädet över en Websocket.

Elixir är drivet och skapat av ett community, men viss hjälp från medelstora spelare så som [DockYard](https://dockyard.com/).
## Projekt som använder tekniken

Erlang har större utbredning och används i många produkter idag; RabbitMQ, Facebook messenger, What's app, CouchDB, och såklart hos Ericsson.

Elixir:

- [Discord](https://blog.discordapp.com/using-rust-to-scale-elixir-for-11-million-concurrent-users-c6f19fc029d3) för att hantera många samtidiga röst/chat-användare
- [Pinterest](https://www.nytimes.com/2018/09/09/technology/pinterest-growth.html) för att hantera sina notifikationer och virtuella "pinboards"
- [Financial Times](https://github.com/Financial-Times?utf8=%E2%9C%93&q=&type=source&language=elixir) för att driva sitt GraphQL api, med hjälp av [absinthe](https://github.com/absinthe-graphql/absinthe)

## Fördelar

- Funktionell, tydlig och lättläslig syntax
- Inte helt olikt från funktionella delar i javascript 
- Har ett stort och användbart och väldokumenterat standard-bibliotek
- Bygger på stabilitet från många år av Erlang-utveckling
- Har ett välutvecklat testbibliotek som är inkluderat
- Mycket stöd för bra och lättskapad dokumentation, inkl. exDoc som automatiskt producerar HTML från modul/funktions-dokumentation
- Reducerad kod. Företag som har bytt kodbas från andra språk har rapporterat om att mängden kod kunnat reduceras vässentligt (2-10 gånger)
- Reducerad hårdvara. Företag som har bytt kodbas från andra språk har rapporterat om att mängden maskiner för att köra deras service kunnat reduceras väsentligt (2-30 gånger) och med lägre responstider
- Stort momentum
- Alla större förändringar i språket är klara och skaparen säger sig inte ha några planer på att införa något som är "breaking", istället kommer mer fokus nu ligga på påbyggnads-bibliotek och att förbättra Erlang
- Tvingar användaren att tänka annorlunda för att skapa tydlig kod
- Inbyggt release med en själv-isolerad mapp med alla onödiga delar avskalat. Kan användas tillsammans med Docker men eftersom Elixir använder supervision-trees blir Docker inte lika nödvändigt.

## Nackdelar

- Dynamiskt typat. Finns stöd för ad-hoc typning, a la Typescript, med [Distillery](https://github.com/bitwalker/distillery), men type-inferensen har förbättringspotential
- Förhållandevis nytt och många projekt är fortfarande i sin uppstartsfas
- Ingen stor spelare med kaptial står bakom språket

| **Kriterium**     | **Poäng (0-5)** | **Kommentar**                                                                                                                                                                                                                                                                                                                                           |
| ----------------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Community         | 4               | [Elixir](https://elixir-slackin.herokuapp.com/) och https://elixirforum.com/, många eldsjälar som hjälper till att svara på frågor. Communityn är inte jättestor för Elixir men växer snabbt och får stor draghjälp av Erlang och andra BEAM-projekt|
| Tekniska fördelar | 5               | Stabilt och "battle-tested", applikationer blir "skalbara per default", immutable, lätt att transformera data, koncept som när de förstås "gör utvecklaren till en bättre utvecklare".                                                                                                                                                                                                                                                                                                                                       |
| Dokumentation     | 5               | Mycket bra dokumentation generellt i communityn, standardbiblioteket är speciellt bra och har mycket doc-tester och utförlig dokumentation som integreras väldigt bra i bl.a VS code.                                                                                                                                                                                                                                                                                               |
| Testad            | 2               | Elixir har testats i ganska hög grad av mig personligen i hobbyprojekt och i diverse "kodutmaningar". Däremot har det inte testats till ett riktigt produktions-projekt.                                                                                                                                                                                       |
| Integration       | 4               | Lätt att skapa microservices och kommunicera med andra tjänster. Passar väl in i vårt tänk om att skapa många utbytbara delar. Finns inget "sätt att backa" om tekniken inte håller, men med tanke på hur stabilt språket/ekosystemet är så är det låg risk.                                                                                                       |
| Införande         | 3.5             | Syntaxen är inte helt olik javascript, däremot finns det nya koncept och det kan vara svårt att tänka "helt funktionellt", och skriva idiomatisk Elixir. Det finns många projekt som skulle ha stor användning av Elixirs simplicitet. 


- **Summa poäng (0-30):** 23.5
- **Rekommendation:** Det funktionella paradigmet exponeras på ett väl avvägt sätt i Elixirs syntax, med utvecklar-glädje i fokus och det finns stora fördelar i kod som är enkel att underhålla samt en plattform som ger skalbarhet på ett enkelt sätt. Ser inga hinder för användning, förutom att utvecklarna ska vara bekväma med det. Så länge momentumet håller i sig väntar en spännande framtid för Elixir och tillägg, och om inte så kommer språket fortsätta vara stabilt.
- **Kategori:** Rekommenderad
- **Utvärderat av:** [Mikael Gråborg](https://github.com/graborg)
