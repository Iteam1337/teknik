# ReasonML

ReasonML är ett syntax och toolchain ovanpå OCaml. OCaml har i sin tur funnits sen 1996 och har historiskt sett sin starkaste bas inom den akademiska världen. Det går att använda för frontend, backend och native. ReasonML är skapat av Facebook och en de som står bakom det är Jordan Walke, originalskaparen av React, och därför finns det inbyggt stöd för React genom ReasonReact.

## Projekt som använder tekniken

- [Facebook Messenger](http://messenger.com/) - Facebooks messenger.com[<sup>1</sup>](https://reasonml.github.io/blog/2017/09/08/messenger-50-reason)
- [Sotheby's](https://www.sothebys.com/en/) - Sotheby's auktionsida[<sup>2</sup>](https://www.youtube.com/watch?v=OAtZqdNdC9c)
- [Draftbit](https://draftbit.com/) - Webapp för att bygga React Native-appar och direkt exportera koden[<sup>3</sup>](https://www.youtube.com/watch?v=Hp4t-bMCVe4)

## Fördelar

- Foreign function interface (FFI) som gör det lätt att interagera med JavaScriptkod (så [Sonos Wejay](https://github.com/believer/bs-sonos) pratar med `node-sonos`)
- Syntax som liknar JavaScript - de eftersträvar att övergången ska vara enkel från JS
- Använder `npm` som package manager för JS, `esy`/`dune`/`opam` för native
- Supersnabb kompilering
- Typinferens gör att det ofta är mindre arbete än Flow och TypeScript. Flow är byggt i OCaml, men detta är flera nivåer bättre.
- Breda användningsområden i och med att det kan kompilera till t.ex. [JS](http://bucklescript.github.io/) och bytecode

## Nackdelar

- Inget async/await [än](https://github.com/facebook/reason/issues/1321)
- ~~Inget React Hooks/Context~~ [React Hooks är mergeat](https://github.com/reasonml/reason-react/pull/351)
- Aktivt arbete görs, men det går oftast rätt långsamt. Kan ses som positivt också i och med att API:er är väl genomtänkta.
- Att hantera ren JSON kan vara drygt i och med att fälten behöver typas

| **Kriterium**     | **Poäng (0-5)** | **Kommentar**                                                                                                                                                                                                                                                                                                                                           |
| ----------------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Community         | 4               | [Discord](https://discordapp.com/invite/reasonml) där det alltid ges jättebra hjälp. Communityn är inte jättestor i övrigt än, men det finns bloggposter och det dyker upp på konferenser. [Reason conf](https://www.reason-conf.com/) görs 2019 för andra året i rad. "Vann" Prediction Award i [State of JS 2018](https://2018.stateofjs.com/awards/) |
| Tekniska fördelar | 4               | Snabbt, typat, likt JS                                                                                                                                                                                                                                                                                                                                  |
| Dokumentation     | 2               | Inte alltid den bästa dokumentationen för enklare exempel                                                                                                                                                                                                                                                                                               |
| Testad            | 5               | För JavaScript och React har vi testat det väl - [Sonos Wejay](https://github.com/Iteam1337/sonos-wejay/), två av projekten till IteamCon#1 och personliga projekt                                                                                                                                                                                      |
| Integration       | 4               | Det är relativt enkelt att integrera med befintliga React-appar i Flow och TypeScript, [MED typning över gränsen](https://github.com/cristianoc/genType). API:et är i stort sett stabilt och om det görs ändringar erbjuder de alltid codemods                                                                                                          |
| Införande         | 4               | Borde inte vara någon större tröskel att komma igång med för de med JS-vana                                                                                                                                                                                                                                                                             |

- **Summa poäng (0-30):** 23
- **Rekommendation:** Reason kompilerat till JavaScript har flera fördelar mot Flow och TypeScript som gör det till ett bra alternativ. Framtiden för det ser ljus ut.
- **Kategori:** Rekommenderad
- **Utvärderat av:** [Rickard Laurin](https://github.com/believer)

## Noter

- <sup>1. - [Messenger.com Now 50% Converted to Reason](https://reasonml.github.io/blog/2017/09/08/messenger-50-reason)</sup>
- <sup>2. - [Arnar Þór Sveinsson - Reasoning with Sotheby's | ReasonConf 2019](https://www.youtube.com/watch?v=OAtZqdNdC9c)</sup>
- <sup>3. - [Peter Piekarczyk - How ReasonML has improved our hiring process | ReasonConf 2019](https://www.youtube.com/watch?v=Hp4t-bMCVe4)</sup>
