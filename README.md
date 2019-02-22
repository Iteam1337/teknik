# Teknikval på Iteam
Iteams process för att välja tekniker i projekt.

## Process

Utvärderingskriterierna poängsätts för varje specifik teknik med betyg mellan 0 och 5. När poängsättningen är klar summeras poängen och en rekommendation sammanfattas av den eller de som utvärderar. Varje ny utvärdering skapas som en Pull Request som godkänns av teknikvalsgruppen som ansvarar för att kontroller att alla delar av utvärderingen har fyllts i.

## Utvärderingskriterier

 - **Community** - stars och forks på github, pull requests, aktivitet på SOME, nedladdningar på npm (där så är relevant), aktiv community, positiv trend
 - **Tekniska fördelar** - ger tekniken fördelar, löser unika problem?
 - **Dokumentation** - är dokumentationen bra, finns en tydlig roadmap, finns källkod?
 - **Testad** - har vi själva testat den? Har vi labbat på den?
 - **Integration** - hur väl passar tekniken ihop med våra andra tekniker? Finns det ett sätt att backa ur beslutet om tekniken inte håller? Finns ett ekosystem? Är tekniken stabil?
 - **Införande** - hur lätt är tekniken att inför i ett projekt? Lätt att komma igång med, användbar i många projekt, rimlig svårighetsgrad för juniora utvecklare, skulle ett skeptiskt team ändå kunna tänka sig att testa?

## Rekommendation

Rekommendationen består av en fritext + en kategori som den nya tekniken placeras i.

### Kategorier

- **Rekommenderad** - kan och bör införas snarast i projekt där den ger tekniska fördelar
- **Potential men riskfylld** - intressant, men bör införas med försiktighet, t.ex. i projekt med tydligt innovationsfokus
- **Inte än** - tekniken är lovande men innehåller för många risker just nu, håll koll på den och gör ny utvärdering senare
- **Behöver mer utvärdering** - utvärderingen ger inte tillräckliga svar i nuläget, beskriv vilka aktiviteter som behövs
- **Nej** - denna teknik passar inte i våra projekt (motivera varför).

