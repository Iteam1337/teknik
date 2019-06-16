# Svelte 3

[https://svelte.dev/](https://svelte.dev/)

Svelte är ett ramverk som flyttar kraften till kompileringen istället för i browsern som React och Vue.
Svelte 2 kom 2018 och nästan på dagen ett år senare (22 april 2019) släpptes Svelte 3. Syntaxet är väldigt
likt Vue och några mindre likheter med React.

## Fördelar

- Ramverket "försvinner" vid bygge till skillnad från React och Vue, dvs. koden kompileras till vanilla JS
- Inbyggd hjälp för accessibility (a11y)
- Finns SSR-paket likt t.ex. Next.js, [Sapper](https://sapper.svelte.dev/)
- Snabbt och enkelt att komma igång med likt Vue

## Nackdelar

- Är inte backat av något stort företag
- Likt Vue så är det gärna muterande state, vilket kan leda till svårföljd kod i en större app
- Oklart hur globalt state sköts
- Saknar dev tools
- Inget stöd för typning med t.ex. TypeScript än [#1639](https://github.com/sveltejs/svelte/issues/1639)
- Native-stöd finns, men är fortfarande litet [Svelte Native](https://svelte-native.technology/)

| **Kriterium**     | **Poäng (0-5)** | **Kommentar**                                                                      |
| ----------------- | --------------- | ---------------------------------------------------------------------------------- |
| Community         | 2               | Låg användning jämfört med de stora ramverken                                      |
| Tekniska fördelar | 1               | Snabbare än React och Vue om superhög performance är definitivt måste, annars lite |
| Dokumentation     | 4               | Likt Vue så har det bra och utförlig [dokumentation](https://svelte.dev/docs)      |
| Testad            | 0               | Har inte testats i något projekt av större storlek, bara småtest och tutorials     |
| Integration       | 1               | Stor skillnad mot tänket i det stora ramverken gör det svårt att lätt byta         |
| Införande         | 4               | Lätt att införa då det är likt Vue                                                 |

**Summa poäng (0-30):** 12
**Rekommendation:** Det skulle kunna fungera bra för en snabb PoC
**Kategori:** Inte än
**Utvärderat av:** [Rickard Laurin](https://github.com/believer)