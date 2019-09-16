# Elm

Elm är ett starkt typat språk vars första version kom 2012. Det byggs i stort sett av en person, [Evan Czaplicki](https://github.com/evancz), och används för webbprojekt som kompileras till JavaScript. De säger själva att det **aldrig** kommer förekomma några runtime exceptions då alla potentiella fel fångas i kompileringen. Elm är snabbt och kompileras till små filer då det inte inkluderar lika mycket ramverk som de tre stora (React, Angular och Vue). Eftersom det har en hel del likheter med ReasonML så kommer jag jämföra med det.

## Projekt som använder tekniken

- [NoRedInk](https://www.noredink.com/) - App för engelsklärare med över 250k (2018)[<sup>1</sup>](https://elmtown.simplecast.fm/upgrading-to-elm-019-luke-westby-richard-feldman) rader Elm, Evan Czaplicki är anställd här fulltid för att jobba med Elm
- [Volvo M](https://m.co/se/sv-SE/) - Volvos Car Sharing service
- [Culture Amp](https://www.cultureamp.com/) - Liknar Officevibe för att bygga bättre kultur i företag

## Fördelar

- Starkt typat med inferens, men det är standard att skriva typerna för funktioner i toppnivå
- Oftast är felmeddelanden ännu tydligare än i ReasonML
- En ingående [guide](https://guide.elm-lang.org/) för att komma igång
- Eget paketbibliotek som tvingar till att använda SemVer genom att automatiskt upptäcka API-ändringar
- Kompilerar snabbt i 0.19[<sup>2</sup>](https://discourse.elm-lang.org/t/our-experience-upgrading-to-0-19-at-humio/3258) [<sup>3</sup>](https://discourse.elm-lang.org/t/how-are-0-19-compile-times-for-50k-loc-projects/3680/7) och har automatisk dead code elimination[<sup>4</sup>](https://elm-lang.org/news/small-assets-without-the-headache)

## Nackdelar

- Uppdateras väldigt sällan. Mellan version 0.18 och 0.19 tog det 1 år och 9 månader (645 dagar). 0.19 släpptes 12 augusti 2018 så det har gått över ett år sen en ny version när denna utvärdering skrivs
- Indentering är superviktigt, likt t.ex. Python, men det hanteras inte automatiskt av `elm-format` så blir ofta fel när man är van att formatteraren ska hantera det
- Interop med JavaScript är inte lika "enkelt" som ReasonML[<sup>5</sup>](https://guide.elm-lang.org/interop/ports.html)
- Eget paketbibliotek innebär ett mindre utbud även om det mesta finns
- Bussfaktor med en huvudutvecklare
- Jag hade ett fall där jag tog bort en funktion från `exposing`, dvs. exporterad, men kompileringen klagade inte förrän jag sparade filen som försökte importera den. Vet inte om det bara var `create-elm-app` som spökade

| **Kriterium**     | **Poäng (0-5)** | **Kommentar**                                                                                                                                     |
| ----------------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| Community         | 3               | Har inte själv deltagit aktivt i communityn, men andra har haft dåliga erfarenheter[<sup>6</sup>](https://dev.to/kspeakman/elm-019-broke-us--khn) |
| Tekniska fördelar | 4               | Snabbt, typat                                                                                                                                     |
| Dokumentation     | 3               | Bra guider och dokumentation av bibliotek, men inte alltid uppdaterade exempel                                                                    |
| Testad            | 4               | Testat i personligt projekt [WOD](https://github.com/believer/wod-elm)                                                                            |
| Integration       | 3               | Går att integrera i befintliga appar stegvis                                                                                                      |
| Införande         | 2               | Liknar ReasonML till vissa delar, men det mesta är helt eget och nytt att lära sig _The Elm Architecture_                                         |

- **Summa poäng (0-30):** 19
- **Rekommendation:** Typningen känns säker, kompileringen är hjälpsam och det finns tydlig dokumentation. Det som gör mig osäker är uppdateringstakten och att communityn omkring inte verkar så trevlig mot förslag som ogillas av [BDFL](https://en.wikipedia.org/wiki/Benevolent_dictator_for_life) Evan.
- **Kategori:** Potential med riskfylld
- **Utvärderat av:** [Rickard Laurin](https://github.com/believer)

## Noter

- <sup>1. - [Elm Town 37 - Upgrading to Elm 0.19 with Luke Westby & Richard Feldman](https://elmtown.simplecast.fm/upgrading-to-elm-019-luke-westby-richard-feldman)</sup>
- <sup>2. - [Our Experience upgrading to 0.19 at Humio](https://discourse.elm-lang.org/t/our-experience-upgrading-to-0-19-at-humio/3258)</sup>
- <sup>3. - [How are 0.19 compile times for 50k+ LOC projects?](https://discourse.elm-lang.org/t/how-are-0-19-compile-times-for-50k-loc-projects/3680/7)</sup>
- <sup>4. - [Small Assets without the Headache](https://elm-lang.org/news/small-assets-without-the-headache)</sup>
- <sup>5. - [Elm ports](https://guide.elm-lang.org/interop/ports.html)</sup>
- <sup>6. - [Elm 0.19 Broke Us 💔](https://dev.to/kspeakman/elm-019-broke-us--khn)</sup>
