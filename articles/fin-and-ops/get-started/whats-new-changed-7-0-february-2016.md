---
title: Hva er nytt eller endret i Dynamics AX 7.0 (februar 2016)
description: "Denne artikkelen beskriver funksjoner som enten er nye eller har blitt endret i Microsoft Dynamics AX 7.0. Denne versjonen inneholder både plattformen og programfunksjoner og ble utgitt i februar 2016."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 91243
ms.assetid: 515bc6e7-a85d-4995-95c6-6cab6c8aa0f9
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 57b4f0c0b76445a333ad3eecb2fccddd8619613c
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="whats-new-or-changed-in-dynamics-ax-70-february-2016"></a>Hva er nytt eller endret i Dynamics AX 7.0 (februar 2016)

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver funksjoner som enten er nye eller har blitt endret i Microsoft Dynamics AX 7.0. Denne versjonen inneholder både plattformen og programfunksjoner og ble utgitt i februar 2016.

<a name="cost-management"></a>Kostnadsstyring
---------------

<table>

<tbody>
<tr class="odd">
<td><strong>Hva kan du gjøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er dette viktig?</strong></td>
</tr>
<tr class="even">
<td>Få et raskt overblikk over lagerbalansen, lagerbalansen for varer i arbeid (VIA) og hva lagerinnflyt og -utflyt har vært for det valgte regnskapsåret.</td>
<td>Gjelder ikke her</td>
<td><strong>Kostnadsadministrasjon</strong>-arbeidsområdet inneholder en inndeling der aktivabeholdningsutdrag eller VIA-beholdningsoppgaven vises for den valgte regnskapsperioden. Beholdningsoppgaven er basert på en datasettbuffer som oppdateres hvert døgn som standard. Hurtigbufferen for datasett kan konfigureres slik at brukere kan oppdatere den manuelt for sanntidsrapportering. <strong>Kortet for status for oppdatering av data</strong> i arbeidsområdet <strong>Kostnadsadministrasjon</strong>, viser når hurtigbufferen sist ble oppdatert.</td>
<td>Kostnadskontrollere er interessert i å vite om utdragsbalansen for beholdning eller VIA-lager økes eller reduseres over tid. Ved å klassifisere operative hendelsene i utdraget kan kontrolløren få en oversikt over flyten i beholdningen. Hvis beholdningen eller VIA-lager evalueres etter standardkostnader, kan samlede avvik også sees.</td>
</tr>
<tr class="odd">
<td>Bruk modulen <strong>Kostnadsstyring</strong>.</td>
<td>Gjelder ikke her</td>
<td>Kostnadsstyring introduseres som et domeneområde. Kostnadsrelatert konfigurasjon og innsikt ble spredt over hele Lagerstyring, Produksjonskontroll og Leverandører.</td>
<td>Fordi alle oppgavene som er knyttet til kostnadsadministrasjon, er sentralisert i én modul, er det enklere for kostnadskontrollere å vedlikeholde systemet.</td>
</tr>
<tr class="even">
<td>Posteringstypene som er knyttet til lagerregnskap og produksjonsregnskap har blitt oppdatert.</td>
<td>Etikettene i <strong>InventPosting</strong>-, <strong>Ressurs</strong>-, <strong>ResourceGroup</strong>- og <strong>ProductionGroup</strong>-skjemaene er ikke alltid justert etter <strong>LedgerPostingType</strong>-etikettene som faktisk er brukt. Det er ikke lett å forstå terminologien som brukes i etikettene.</td>
<td>Etikettene er oppdatert slik at etikettene på <strong>InventPosting</strong>-, <strong>Ressurs</strong>-, <strong>ResourceGroup</strong>- og <strong>ProductionGroup</strong>-sidene samsvarer med de faktiske <strong>LedgerPostingType</strong>-etikettene. Alle etikettene har også fått nye navn slik at de samsvarer med de operative hendelsene. Legg merke til at den faktiske posteringslogikken ikke er endret.</td>
<td>Det er enklere å konfigurere systemet, fordi de nye etikettene er knyttet til de operative hendelsene som bruker denne posteringstypen.</td>
</tr>
<tr class="odd">
<td>Import/eksport av kjøpspris, kostnad eller salgspris fra Microsoft Excel til eller fra en kostnadsversjon.</td>
<td>Du kan ikke importere priser eller kostnader riktig i en etterkalkuleringsversjon, fordi datamodellen krever en InventDim-ID.</td>
<td>Innføringen av dataenheter gjør det mulig å implementere en funksjon for import og eksport. Med denne funksjonen kan brukere importere/eksportere priser eller kostnader i en kostnadsversjon.
<ul>
<li>Importer en fullstendig liste over innkjøpspriser for neste år som er hentet fra innkjøpsavdelingen.</li>
<li>Overfør kostnader og standard salgspriser fra hovedkontor til én eller flere salgsselskaper i én operasjon.</li>
</ul></td>
<td>Det kan spare kontrollerne betydelig tid når de vedlikeholder systemet, spesielt når de må vedlikeholde forhåndsbestemte kostnader for det neste regnskapsåret.</td>
</tr>
<tr class="even">
<td>Få et raskt overblikk over lagerbalansen og gjennomsnittlig enhetskostnad for et kostnadsobjekt.</td>
<td>Brukeren må åpne beholdningskjemaet og velge lagerdimensjonene som gjenspeiler kostnadsobjektet. Brukeren må derfor vite hvilke lagerdimensjoner som er merket for økonomisk lager for det bestemte produktet.</td>
<td>En ny <strong>Kostnadsobjekt</strong>-side introduseres. Som standard viser denne siden alle kostnadsobjekter som er knyttet til produktet. Siden viser gjeldende lagerantall, verdi og gjennomsnittlig enhetskostnad per kostnadsobjekt.</td>
<td>Den fjerner noe av kompleksiteten og gjør det enklere å være en kostnadskontroller.</td>
</tr>
<tr class="odd">
<td>Bruk den nye <strong>Kostnadsoppføringer</strong>-siden under lagerstyring.</td>
<td>Det kan være vanskelig å utføre lagerkontroll på registrerte lagertransaksjoner og relaterte utligninger, fordi de samme transaksjonene kan være fysiske eller økonomiske.</td>
<td><strong>Kostnadsoppføringer</strong>-siden gir en ny måte å vise lagertransaksjoner på.
<ul>
<li>Transaksjoner vises i kronologisk rekkefølge.</li>
<li>Bare transaksjoner som bidrar til kostnader, er inkludert.</li>
<li>Det finnes ingen angivelse av fysiske kostnader eller økonomisk kostnad.</li>
<li>Det finnes ingen angivelse av fysisk antall eller økonomisk antall.</li>
<li>Kostnadene legges til trinnvis.</li>
</ul></td>
<td>Det kan spare kostnadskontrollørene for mye tid når de må utføre lagerkontroll på transaksjonsnivå.</td>
</tr>
<tr class="even">
<td>Bruk den nye dialogboksen <strong>VIA-produksjonsoppgave</strong> for å vise en samlet visning av akkumulerte kostnader for et bestemt produkt.</td>
<td>Gjelder ikke her</td>
<td>VIA-oppgaven viser en samlet VIA-saldo for den aktuelle produksjonsordren, gruppert i riktige kostnadsklassifiseringer. Et diagram viser, i kronologisk rekkefølge, hvordan operative posteringer har påvirket VIA-balansen.</td>
<td>Den kan spare kostnadskontrollørene for mye tid når de trenger å vite hva den gjeldende VIA-balanse er på en bestemt produksjonsordre eller hvor mye materiale som er brukt på ordren.</td>
</tr>
<tr class="odd">
<td>Bruk Vis kostnadssammenligning-funksjonen som er introdusert på produksjonsordrer. Funksjonen gjør det enklere å sammenligne kostnader som er knyttet til en produksjonsordre.</td>
<td>Brukeren kan bare sammenligne estimerte kostnader og realiserte kostnader. Sammenligningen kan gjøres på det laveste nivået.</td>
<td>Funksjonen for kostnadssammenligning lar kostnadskontrollører sammenligne følgende data:
<ul>
<li>Aktiv kostnad i forhold til Estimert kost = Planleggingsavvik</li>
<li>Estimert kost i forhold til Realisert kostnad = Produksjonsavvik</li>
<li>Planleggingsavvik + Produksjonsavvik = Totalt avvik</li>
</ul>
Denne funksjonen fungerer uavhengig av etterkalkuleringsmetoder som er tilordnet den produserte varen. Som standard viser et diagram kostnadssammenligningen etter kostgruppetype. Diagrammet lar brukerne gå nedover i mer detaljert nivå.</td>
<td>Kostnadskontrollører eller produksjonssjefer kan analysere hvor produksjonsavvikene kommer fra, og hva som forårsaker dem.</td>
</tr>
</tbody>
</table>

## <a name="developer"></a>Utvikler
|                                                                                                              |                                                                                                                                                                                                    |                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hva kan du gjøre?**                                                                                         | **Dynamics AX 2012**                                                                                                                                                                               | **Dynamics AX 7.0**                                                                                                                                                                                                            | **Hvorfor er dette viktig?**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Opprett webbaserte løsninger i nettskyen som er tilgjengelige på mange enheter.                                 | Ikke tilgjengelig                                                                                                                                                                                      | Den gjeldende versjonen av Dynamics AX baseres på en ny webbasert klient og klientrammeverk.                                                                                                                                    | Du kan levere løsninger for neste generasjon til sluttbrukerne.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Bruk Microsoft Visual Studio til å utvikle dine løsninger.                                                       | Microsoft MorphX er primært utviklingsmiljø, men noe utvikling skjer i Visual Studio.                                                                                                | Visual Studio er det eneste utviklingsmiljøet.                                                                                                                                                                             | Det har kjente Dynamics AX 2012-begreper og tilpasser dem sømløst til Visual Studio-rammeverket og paradigmer. Det gjør det mulig med standard interoperabilitet med andre .NET-språk og -prosjekter.                                                                                                                                                                                                                                                                                                                                                                                                   |
| Kompiler Common Intermediate Language (CIL) for alle funksjoner.                                                 | X ++ er kompilert til p-kode.                                                                                                                                                                         | Helt ny X ++-kompilator genererer CIL for alle funksjoner. CIL er det samme midlertidige språket som brukes av andre. NET-baserte språk.                                                                                   | CIL går raskere og kan effektivt referere til klasser i administrerte biblioteker for dynamiske koblinger (DLL-er), og kan kjøres på en stor verktøybase på .NET-verktøy.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Bygg inn BI-rapporter (forretningsintelligens) og visualiseringer i Microsoft Dynamics AX-klienten.             | Ikke tilgjengelig                                                                                                                                                                                      | Opprett svært intuitive og flytende visualiseringer.                                                                                                                                                                              | Den gjør det mulig å ta beslutninger på grunnlag av innsikt som er basert på BI.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Integrer med Microsoft Office.                                                                             | Ikke tilgjengelig                                                                                                                                                                                      | Nye funksjoner inkluderer Excel-datatilkoblingsappen, **Arbeidsbokutforming**-siden, Eksporter API og Dokumentstyring.                                                                                                        | Du kan opprette produktivitetsløsninger for sluttbrukerne.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Automatiser bygging, testing og distribusjon.                                                                            | Delvis tilgjengelig                                                                                                                                                                                | Distribuere utviklertopologien ved hjelp av Utvikler og Bygg VM. Automatisk konfigurasjon av Bygg VM for å finne, bygge moduler fra Visual Studio Online (VSO) og kjør tester. Kompilering av C\# og X++-modulen og referanser støttes. | Det øker produktiviteten til utviklere ved å redusere kostnader og arbeid for testing og valideringer.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Tilpass med overlag og utvidelser.                                                                  | Utvidelser er ikke tilgjengelige.                                                                                                                                                                       | Den gjeldende versjonen av Dynamics AX har en ny modell for tilpasning.                                                                                                                                                              | Du kan tilpasse kildekoden og metadata for modellelementer som er levert av Microsoft eller tredjeparts Microsoft-partnere.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Lag nye kontroller og grensesnittelementer ved hjelp av X++ og et moderne webrammeverk.                                  | Egendefinerte kontroller er avhengige av eksterne rammeverk som for eksempel Microsoft ActiveX og Windows Presentation Foundation (WPF).                                                                                   | Det er enklere å bygge kontroller i den gjeldende versjonen. X++-rammeverket kan brukes til virkemåte- og forretningslogikk i programmet, og en HTML/JavaScript-basert klient tillater moderne visualiseringer.                         | Kontrollene kan utformes til å se ut og fungere på samme måte som de medfølgende kontrollene i Dynamics AX.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Evaluer og juster ytelsen ved hjelp av nye verktøy.                                                            | PerfSDK, verktøysett for datautvidelse, Trace Parser Web-app og PerfTimer er ikke tilgjengelig.                                                                                                             | PerfSDK, verktøysett for datautvidelse, Trace Parser Web-app og PerfTimer er nye.                                                                                                                                                  | I Software Development Kit (SDK) kan du teste og validere alle viktige forretningsprosesser for ytelse i en enkeltbrukertestkjøring og eventuelt i en flerbrukertestkjøring. Med verktøysettet for datautvidelse kan du utvide alle ytelsestester der hoveddata og transaksjonsdata må utvides på riktig måte. Ved hjelp av Trace Parser kan du validere en enkeltbrukerytelsestest eller en flerbrukerkjøring. Med PerfTimer kan du se om en spørring eller et bestemt metodekall forårsaker et ytelsesproblem. Derfor trenger du ikke ta en sporing og analysere alt i detalj. |
| Vis oppdaterbar visning ved å bruke OData.                                                                        | Ikke tilgjengelig                                                                                                                                                                                      | Den gjeldende versjonen av Dynamics AX introduserer et offentlig OData-tjenesteendepunkt som gir tilgang til Dynamics AX-data på en konsekvent måte på tvers av mange klienter.                                                     | Dine løsninger kan fungere sammen med RESTful-tjenester, dele data på en synlig måte og aktivere omfattende integrering ved hjelp av HTTP-stakkprotokollen.                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Dra nytte av Business Connector for å redigere forretningslogikk og støtte integreringsscenarioer.         | Business connector er tilgjengelig for kalle inn i X++-kode fra forvaltet kode. Vi anbefaler at du bruker Business Connector bare for å redigere forretningslogikk i C\#, ikke for integreringsscenarier. | Business Connector støttes ikke lenger. Redigeringskravet kommer fra det faktum at X++ er kompilert til behandlet kode. Derfor er interoperabilitet enklere. Integreringsscenarioene oppfylles ved hjelp av OData.       | Du kan ikke bruke Business Connector fremover.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Velg skala (det vil si antall desimaler) på reelle databasefelt og utvidede datatyper (EDT-er). | Skala 16 er standardskalaen og kan ikke endres av utvikleren.                                                                                                                               | EDT-er og felt har nå en skalaegenskap som kan brukes på de enkelte felt og EDT. Standarden er 6, ikke 16.                                                                                                | Ytelse med NCCI-tabeller (minneintern støtte i SQL) er raskere ved ordrer med stor størrelse når en mindre skala brukes. Endre skalaen i henhold til hva din bruk av de enkelte feltene krever.                                                                                                                                                                                                                                                                                                                                                                                                               |
## <a name="financial-management"></a>Økonomistyring
<table>






<tbody>
<tr class="odd">
<td><strong>Hva kan du gjøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er dette viktig?</strong></td>
</tr>
<tr class="even">
<td>Eksporter kontostrukturer til Microsoft Excel.</td>
<td>Ikke tilgjengelig</td>
<td>Nå kan du velge en kontostruktur og eksportere den til Excel.</td>
<td>Mange kunder har bedt om muligheten til å eksportere kontostrukturer til Excel for å filtrere enklere.</td>
</tr>
<tr class="odd">
<td>Vis finans og avanserte regelstrukturer som er knyttet til en kontostruktur på én side.</td>
<td> Brukeren må navigere til flere skjemaer for å se finans og kontostrukturen som brukes. </td>
<td>Faktabokser er lagt til på siden for kontostruktur.</td>
<td>Det er enklere å få tilgang til viktig informasjon når kontostrukturer er definert og redigeres.</td>
</tr>
<tr class="even">
<td>Vis finans som er knyttet til en kontoplan på én side.</td>
<td>Brukeren må gå til hvert firma og åpne finansskjemaet for å se kontoplanen som er tilordnet til finans.</td>
<td>Faktabokser er lagt til på **Kontoplan**-siden.</td>
<td> Det er enklere å få tilgang til viktig informasjon når en kontoplan er definert og tilordnet.</td>
</tr>
<tr class="odd">
<td>Vis lukkingen av arkjusteringer og transaksjoner i separate kolonner på **Råbalanse**-listesiden. </td>
<td>Brukeren ser begge typer transaksjoner i en enkelt kolonne.</td>
<td>En ekstra parameter er lagt til på **Råbalanse**-listesiden.</td>
<td>Den gjør det mulig for enklere analyse av data og kreves også for forskriftsmessig rapportering i enkelte land/regioner. </td>
</tr>
<tr class="even">
<td>Bruk den nye siden **Global økonomijournal**.</td>
<td>Ikke tilgjengelig </td>
<td>Ny **Global økonomijournal**-side for å angi økonomijournaler. Rettigheter for denne siden legges til i **Regnskapsfører**-rollen.</td>
<td>Gjør det mulig for en regnskapsfører for delte tjenester å angi økonomijournaler på tvers av firmaer uten å gå ut av skjemaet, eller bytte firmakontekst.</td>
</tr> 
<tr class="odd">
<td>Bruk den nye siden **Regnskapskildeutforsker**.</td>
<td>Tilgjengelig fra Dynamics AX 2012 R3 CU10.</td>
<td>Ny **Regnskapskildeutforsker**-siden og handlinger for å navigere der fra listesiden **Råbalanse** og siden **Bilagstransaksjoner**.</td>
<td>Gjør det mulig å vise den mest detaljerte informasjonen om kilden for en råbalanse eller en regnskapsoppføring i økonomimodulen, eller for ad hoc-analyse.</td>
</tr>
<tr class="even">
<td>Legg til ekstra posteringslag.</td>
<td>Tillegging av ekstra posteringslag var en utvikleropplevelse.</td>
<td>Ti posteringslag er nå tilgjengelig.</td>
<td>De fleste kunder legge til ekstra posteringslag.</td>
</tr>
<tr class="odd">
<td>Bruk alternativet Beslektet bilag.</td>
<td>Ikke tilgjengelig</td>
<td>Alternativet Beslektet bilag er tilgjengelig for brukerne for å vise bilaget i motregningsfirma ved postering av konserninterne transaksjoner. Fra de relaterte bilagene kan brukere klikker på detaljene og raskt hoppe til bilaget for motkontofirmaet.</td>
<td>Ved postering av konserninterne transaksjoner, hadde brukere ingen synlighet eller sporing til bilaget som ble postert i motregningsfirma.</td>
</tr>
<tr class="even">
<td>Masseavslutning for regnskapsperiode</td>
<td>Ikke tilgjengelig</td>
<td>Brukere kan oppdatere modultilgangen og endre periodestatusen for flere firmaer samtidig.</td>
<td>Før denne funksjonen måtte brukere endre hvilket firma de logget på, gå til økonomikalenderskjemaet og manuelt oppdatere modultilgangen og periodestatusen.</td>
</tr>
<tr class="odd">
<td>Få valutakurser fra Oanda.</td>
<td>Konfigurering av valutakursleverandøren for å importere kurser fra Oanda, var en utvikleropplevelse. </td>
<td>Hvis brukere har en nøkkel for Oanda, kan de angi den når de konfigurerer valutakursleverandøren.</td>
<td>Brukere kan dra nytte av den innebygde funksjonaliteten ved å få valutakurser fra Oanda importert basert på en tidsplan.</td>
</tr>
<tr class="even">
<td>Filtrer finansrapporter (Management Reporter) basert på dimensjoner, attributter, datoer og scenarier. </td>
<td> All filtrering av Administrasjonsreporter-rapporter håndteres gjennom utforming av rapporten. Hvis en bruker som for eksempel har visningsrettigheter, vil vise en rapport for en annen dato, må en rapportutformer gjøre endringen. </td>
<td>Rapportalternativer er lagt til slik at ulike filtre kan brukes når en bruker viser en rapport. En ny rapport blir deretter generert basert på disse filtrene.</td>
<td>Forbrukere av økonomiske rapporter kan bruke forskjellige filtre for dimensjoner, datoer, attributter og scenarioer uten at det kreves oppdateringer i rapportutforminger.</td>
</tr>
<tr class="odd">
<td>Vis finansrapporter (Management Reporter) i Microsoft Dynamics AX-klienten.</td>
<td>En egen webklient ble brukt til å vise Administrasjonsreporter-rapporter.</td>
<td>Alle økonomiske rapporter er tilgjengelige i Dynamics AX-klienten. Brukeren velger en rapport som skal vises, og rapporten vises i klienten.</td>
<td>Du kan nå vise økonomiske rapporter uten å åpne andre klienter/applikasjoner.</td>
</tr>
<tr class="even">
<td>Skriv ut finansrapporter (Management Reporter) fra Microsoft Dynamics AX-klienten.</td>
<td>Utskrift av en rapport bruker nettleserens utskriftsalternativer for utskrift og skriver bare ut det brukeren kan se på skjermen. </td>
<td>Brukeren kan velge detaljnivået og sideoppsettet for en rapport ved hjelp av alternativet Skriv ut i finansrapporten i Dynamics AX-klienten.</td>
<td>Utskrevne rapporter skrives ut slik brukerne forventer i stedet for å skrive ut en webside.</td>
</tr><tr class="odd">
<td>Analyser økonomiske data ved hjelp av "Overvåk økonomiske resultater"-innholdet for Power BI.</td>
<td>Ikke tilgjengelig</td>
<td>I PowerBI.com velg **Hent data**, og velg deretter **Dynamics AX – Finansresultater**-innholdspakken. Angi URL-adressen for sluttpunktet i Dynamics AX for å vise dataene i instrumentbordet.</td>
<td>Med tre til fire klikk kan organisasjoner distribuere et Power BI-instrumentbord som inneholder viktige økonomiske data. Innholdet kan tilpasses av organisasjonen.</td>
</tr>
<tr class="even">
<td>Spor avslutningsprosess i regnskapsperiode.</td>
<td>Ikke tilgjengelig </td>
<td>Lukking av maler og planer kan utføres ved hjelp av konfigurasjonen for Regnskapsperiodeavslutning. Bruk **Regnskapsperiodeavslutning**-arbeidsområdet til å spore fremdriften for lukking av tidsplaner på tvers av flere firmaer.</td>
<td>Arbeidsområdet eliminerer manuelle systemer for å definere, planlegge og kommunisere aktiviteter for lukking. Derfor er antall dager til avslutning redusert.</td>
</tr>
<tr class="odd">
<td>Overvåk budsjett kontra faktiske, og lag prognoser for finans ved hjelp av **Finansbudsjetter og prognoser**-arbeidsområdet og andre spørringsskjemaer.</td>
<td>Ikke tilgjengelig</td>
<td> Arbeidsområdet kan nås via instrumentbordet Dynamics AX. Det inneholder koblinger til flere nye forespørselssider: **Sammendrag av faktiske kontra budsjett**, **Sammendrag av statistikk for budsjettkontroll**, **Budsjettregisteroppføringer** og **Budsjettplaner**.</td>
<td>Nye forespørselssider gir lett tilgang til budsjettinformasjon. Arbeidsområdet kombinerer all budsjettvedlikeholds- og overvåkingsoppgaver på ett sted som er lett for budsjettledere eller regnskapssjefer å bruke.</td>
</tr>
<tr class="even">
<td>Lag oppsett for budsjettplaner og prognoser.</td>
<td>**Budsjettplan**-dokumentet vises som en liste med linjer som har effektive datoer og beløp for kombinasjoner av finansdimensjoner. Brukeren må opprette og bruke Excel-maler for å vise budsjettplandata i en pivottabell.</td>
<td>Et ubegrenset antall oppsett er tilgjengelig for budsjettplaner og prognoser. Du kan kombinere valgte finansdimensjoner, brukerdefinerte kolonner og andre radattributter (for eksempel kommentarer, prosjekter og aktiva) i oppsettet. Brukere kan bytte oppsettet for budsjettplandokumentet direkte og redigere data ved hjelp av et hvilket som helst valgt oppsett. Konfigurasjonen av budsjettplanlegging er forenklet ved å fjerne scenariobegrensninger og ved hjelp av oppsett for å definere hvilke data som kan vises og redigeres i hvert trinn av budsjettplandokumentet.</td>
<td>Den gir fleksibilitet til å opprette og redigere budsjettplaner ved hjelp av både Excel og Dynamics AX-klienten. Maler for Excel-arbeidsbøker kan genereres ved hjelp av konfigurasjon av budsjettplanoppsettet.</td>
</tr>
<tr class="odd">
<td>Skriv ut **Leverandørfakturatransaksjoner**-rapporten ved hjelp av informasjon fra **Detaljert forfallsdatoliste**-rapporten, som omfatter dager over fristen. </td>
<td>Du må skrive ut to forskjellige rapporter: **Detaljert forfallsdatoliste** og **Leverandørfakturatransaksjoner**.</td>
<td>Informasjonen i de to rapportene er konsolidert i **Leverandørfakturatransaksjoner**-rapporten. **Detaljert forfallsdatoliste**-rapporten ble avskrevet. </td>
<td>Den eliminerer behovet for å skrive ut to atskilte, men beslektede rapporter.</td>
</tr>
<tr class="even">
<td>Generer forskriftsmessige rapporter direkte i PDF-format.</td>
<td>Du må først generere en forskriftsmessig rapport i ett format og deretter eksportere den til PDF-format.</td>
<td>PDF-formatet er standardformatet for forskriftsmessige rapporter.</td>
<td>Den gir en enhetlig visningsopplevelse både skjermen og en utskrevet kopi.</td>
</tr>
<tr class="odd">
<td>Kjør mva-utligningsprosessen som en partiprosess. </td>
<td>Ikke tilgjengelig</td>
<td>På **Mva-utligningsperiode**-siden kan du angi at utligningsprosessen bør kjøres i satsvis modus.</td>
<td>For perioder som har mange mva-transaksjoner, kan utligningsprosessen ta lang tid, og det kan være bedre å kjøre prosessen i bakgrunnen som en partiprosess.</td>
</tr>
</tbody>
</table>





## <a name="foundation"></a>Stiftelse
<table>






<tbody>
<tr class="odd">
<td><strong>Hva kan du gjøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er dette viktig?</strong></td>
</tr>
<tr class="even">
<td>Få tilgang til klienten når som helst og hvor som helst. </td>
<td>Dynamics AX 2012-skrivebordsklienten inneholder et fullstendig sett av skjemaer, men den kan kjøres bare på datamaskiner som kjører Microsoft Windows, og krever installasjon. Terminalserveren brukes ofte med skrivebordsklienten til å aktivere tilgang via et regionnett (WAN). Webklienten Enterprise Portal gir et redusert sett med skjemaer.</td>
<td>De to klientene for AX 2012 har blitt erstattet av én standardbasert webklient som gir hele settet med funksjonalitet til skrivebordsklienten sammen med rekkevidden til Enterprise Portal-klienten.</td>
<td>Den hindrer at utviklingstiltak blir delt mellom to grensesnittplattformer. Ved hjelp av standard webgrensesnitt elimineres behovet for Terminal Server.</td>
</tr>
<tr class="odd">
<td>Vær produktiv ved å bruke den nye Oppgaveregistrering.</td>
<td>AX 2012 Oppgaveregistrering krever direkte tilgang til en datamaskin med Application Object Server (AOS) og utvidede rettigheter, og har ingen redigeringsalternativer.</td>
<td>Den nye Oppgaveregistrering kan brukes direkte fra webklienten. Tilgang til Oppgaveregistrering krever ikke administratorrettigheter. Registrerte trinn kan vises direkte mens du registrerer, nye redigeringsalternativer er introdusert, og Oppgaveregistrering støtter flere scenarioer i tillegg til eksisterende Forretningsprosessmodelerer-scenarioer.</td>
<td>Den nye Oppgaveregistrering gir en strømlinjeformet opplevelse og driver nye funksjoner i Dynamics AX. Noen av disse funksjonene er tilgjengelige nå, og flere følger i fremtiden.</td>
</tr>
<tr class="even">
<td>Hjelp brukerne med å forstå bedre det kommende arbeidet med arbeidsområder.</td>
<td>Rollesentre gir en oversikt over informasjon som gjelder brukerens jobbfunksjon i bedriften eller organisasjonen.</td>
<td>Arbeidsområder er et nytt konsept i Dynamics AX som er ment å erstatte rollesentre som den primære måten å navigere til oppgaver og bestemte sider. De gir en énsides oversikt over en forretningsaktivitet og hjelper brukerne med å forstå gjeldende status, kommende arbeidsbelastning og ytelse til prosess eller bruker. Arbeidsområder er mer sammensatte enn AX 2012-rollesentre, og en bruker kan ha tilgang til flere arbeidsområder.</td>
<td>Arbeidsområder er ment å øke brukerproduktiviteten. Utviklere må opprette et arbeidsområde for alle viktige "aktiviteter" som støttes i produktet. Et eldre rollesenter fra AX 2012 vil vanligvis erstattes av flere arbeidsområder i gjeldende versjon av Dynamics AX.</td>
</tr>
<tr class="odd">
<td>Gjør at skjemaer reagerer på nettleserstørrelse eller enhetsstørrelse.</td>
<td>I AX 2012 ble skjemainnhold strengt satt opp ved hjelp av kolonner, og den generelle skjemaet høyden/bredden ble stort sett fastslått basert på kontrollene i skjemaet.</td>
<td>Med vridningen mot nettet i den nyeste Dynamics AX-versjonen, er nå dimensjonene for et skjema basert på nettleseren visningsstørrelse eller enhet. Kontroller og parametere for oppsett er endret eller lagt til for å svare bedre på endringer av visningsstørrelse.</td>
<td>Skjemainnhold må være raskere for å bruke optimalt den tilgjengelig høyden/bredden for nettleseren eller enheten. Det krever endringer i måten et skjema er modellert for å oppnå bedre hastighet.</td>
</tr>
<tr class="even">
<td>Bruk mønstre for en forbedret skjemautviklingsopplevelse.</td>
<td>Skjemamaler var tilgjengelige som utgangspunkt for skjemautvikling i AX 2012 basert på en skjemastil. Skjemastilkontrollen, et valgfritt tillegg, ga informasjon om hvordan et skjema avveket fra den tilsvarende malen.</td>
<td>Skjemamønstre er introdusert i gjeldende versjon av Dynamics AX. Skjemamønstrene representerer en kombinasjon av skjemamaler og skjemastilkontrollen tett integrert i utviklingsopplevelsen. Mønstre er definert på skjemanivå (som AX 2012) med flere tilgjengelige undermønstre på sidenivå for gruppe og kategori.</td>
<td>Skjemaer som overholder mønstre har mange fordeler, blant annet et mer konsekvent brukergrensesnitt, en enklere utviklingsopplevelse, enklere oppgraderingsbane for skjemaet og økt tillit til respons for skjemaoppsett.</td>
</tr>
</tbody>
</table>

## <a name="help"></a>Hjelp
<table>






<tbody>
<tr class="odd">
<td><strong>Hva kan du gjøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er dette viktig?</strong></td>
</tr>
<tr class="even">
<td>Tilgang til veiledet prosedyremessig hjelp (oppgaveveiledning) og fremgangsmåter ved å klikke **Hjelp**.</td>
<td>Hjelpesystemet for AX 2012 peker til HTML-emner som er lagret på en lokal webserver. Kunder og partnere kan opprette sin egen hjelp.</td>
<td>Hjelpesystemet i den gjeldende versjonen av Dynamics AX viser oppgaveveiledninger som er lagret i Microsoft Dynamics Lifecycle Services (LCS) BPM. Hjelpesystemet viser også emner fra Microsofts nettsted for dokumenter. Hvis du vil ha mer informasjon, kan du se [Hjelp for Dynamics AX – Komme i gang](help-overview.md) og [Nye oppgaveveiledninger tilgjengelige (februar 2016)](new-task-guides-available-february-2016.md).</td>
<td>Oppgaveveiledninger gir en veiledet, interaktiv opplevelse som leder deg gjennom trinnene for en aktivitet eller forretningsprosess. Du kan laste ned og tilpasse oppgaveveiledningene som Microsoft tilbyr. Emnet gir en raskere og mer fleksibel måte å opprette, levere og oppdatere produktdokumentasjonen. Derfor garanterer det at du har tilgang til den nyeste tekniske informasjonen.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Forvaltning av menneskelig kapital
<table>






<tbody>
<tr class="odd">
<td><strong>Hva kan du gjøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er dette viktig?</strong></td>
</tr>
<tr class="even">
<td>Overfør kompetanse og sertifikater til klassedeltakere etter fullføring av kurs.</td>
<td>Dette er en manuell prosess.</td>
<td>Når et kurs er fullført, blir et nytt alternativ tilgjengelig for å oppdatere en deltakers poster med nye ferdigheter og sertifikater.</td>
<td>Det gir en ny og effektiv måte å oppdatere poster for ansatte.</td>
</tr>
<tr class="odd">
<td>Bekreft ansettelse raskt.</td>
<td>Dette er en manuell prosess.</td>
<td>Personalavdelingen kan raskt kontrollere ansettelse ved hjelp av et arbeidsområde eller ansattsiden.</td>
<td>Personalavdelingen trenger ikke lenger åpne flere sider for å kontrollere startdato, leder, måneder i stillingen og kompensasjonsdata.</td>
</tr>
<tr class="even">
<td>La ansatte vise, oppdatere og slette informasjon i systemet.</td>
<td>Tilgjengelig, men med begrenset funksjonalitet for visning og oppdatering.</td>
<td>Denne funksjonen er aktivert og gjør at ansatte og oppdragstakere kan vise en rekke personlige data. En arbeidsflyt kan eventuelt brukes når informasjon opprettes, oppdateres eller slettes.</td>
<td>Den lar ansatte få kontroll over sin informasjon, for eksempel oppdatering av adresse- eller kontaktinformasjon, søking på en jobb, utfylling av et spørreskjema eller oppdatering av bildet sitt. Når en arbeidsflyt er aktivert, kan informasjonen kontrolleres av en godkjenner eller godkjennes automatisk basert på forretningsprosessene dine.</td>
</tr>
<tr class="odd">
<td>La ledere vise eller redigere ansattinformasjon.</td>
<td>Tilgjengelig, men med begrenset funksjonalitet for visning og oppdatering.</td>
<td>Avhengig av konfigurasjonsinnstillinger og sikkerhet kan ledere vise eller redigere informasjon om ansatte.</td>
<td>Den lar ledere få tilgang til viktige ansattdata slik at de kan ta bedre avgjørelser om rekruttering, ytelse og ansattutvikling.</td>
</tr>
<tr class="even">
<td>Dra nytte av funksjon for å administrere selvbetjening.</td>
<td>Ikke tilgjengelig</td>
<td>Ledere kan nå sende forespørsler om nye ansettelser (ansatte og kontraktører), overføringer og oppsigelse (avslutte ansettelse). Ledere kan også be om en ny stilling, utvide stillingsvarighet eller be om stillingsendringer.</td>
<td>Disse scenariene var tidligere bare tilgjengelige for personaladministrasjonen. Aktivering av disse scenariene gir kraftige verktøy for ledere i en organisasjon. Valgfrie arbeidsflyter kan aktiveres for å angi riktig nivå for gjennomgang og godkjenning.</td>
</tr>
<tr class="odd">
<td>Få tilgang til resultater av kompensasjonsprosessen.</td>
<td>Resultater er tilgjengelige bare på tidspunktet for behandling.</td>
<td>Resultater for kompensasjon er nå tilgjengelige når som helst etter at prosessen er kjørt.</td>
<td>Det gir en utmerket kontroll av prosessen og resultatet av prosessen. Det gir også en omfattende visning av dataene før ansattposter blir oppdaterte.</td>
</tr>
<tr class="even">
<td>Få tilgang til resultater av fordelsprosessen.</td>
<td>Resultater er tilgjengelige bare på tidspunktet for behandling.</td>
<td>Resultater av fordeler er nå tilgjengelige når som helst etter at prosessen er kjørt.</td>
<td>Det gir en omfattende visning av dataene som er oppdatert av fordelsregistrering og kostnadsendringer.</td>
</tr>
<tr class="odd">
<td>Vis endringer på "Gyldig dato"-tidslinjen.</td>
<td>Ikke tilgjengelig</td>
<td>Dette sammenligningsverktøyet er tilgjengelig for ansatte, stillinger og jobber. Det gir en omfattende oversikt over endringer fra én versjon av en post til en annen.</td>
<td>Du sparer tid når du viser endringer som har oppstått over tid, for ansatte, stillinger og jobbposter. Du kan raskt sammenligne to versjoner av en post, eller alle postene, over tid.</td>
</tr>
<tr class="even">
<td>Vis ansatte etter firma.</td>
<td>Dette er en manuell prosess som utføres med filtrering.</td>
<td>Ansatt- og oppdragstakerlister blir automatisk filtrert av firmaet du er logget på.</td>
<td>Det gir en filtrert visning av ansatte som er ansatt i firmaet som er logget på. Arbeiderlisten er fremdeles tilgjengelig for en ufiltrert visning av alle ansatte og oppdragstakere. I den gjeldende versjonen av Dynamics AX endrer ikke systemet firmaet basert på den ansatte som er valgt i listen.</td>
</tr>
<tr class="odd">
<td>Oppdater kursdeltakerlisten.</td>
<td>Ikke tilgjengelig</td>
<td>Kursdeltakere kan fjernes fra listen over deltakere.</td>
<td>Det gjør det enkelt å oppdatere kursdeltakere som er registrert ved en feiltakelse.</td>
</tr>
<tr class="even">
<td>Behandle kompensasjonshendelser i en gruppe.</td>
<td>Ikke tilgjengelig</td>
<td>Denne funksjonen forenkler behandlingen av kompensasjonsendringer for ansatte.</td>
<td>Den gir en enkel strømlinjeformet prosess for å oppdatere ansattposter gjennom kompensasjonsarbeidsområdet og relaterte sider.</td>
</tr>
</tbody>
</table>

## <a name="inventory-management"></a>Lagerstyring
Ingen nye funksjoner er lagt til.

## <a name="localization"></a>Lokalisering
<table>






<tbody>
<tr class="odd">
<td><strong>Hva kan du gjøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er dette viktig?</strong></td>
</tr>
<tr class="even">
<td>Konfigurer og generer elektroniske dokumenter for å oppfylle de juridiske kravene i ulike land/regioner.</td>
<td>Elektroniske dokumenter er hardkodet i X++ eller som XSLT (Extensible Stylesheet Language Transformations). Formatjusteringer krever utviklingstiltak. Tilgang til data og formatering er ikke isolert. En justert formatdistribusjon krever en ny hurtigreparasjonspakke for Microsoft Dynamics AX som overstyrer det eksisterende formatet. Egendefinerte endringer av hvert format må overføres manuelt til kildekoden til en ny hurtigreparasjonspakke for Microsoft Dynamics AX.</td>
<td>Elektronisk rapportering (ER) er et nytt verktøy for å konfigurere og generere elektroniske dokumenter som er rettet mot forretningsvirksomhet i stedet for en utvikler. ER lar deg konfigurere datamodeller som er domenespesifikke og uavhengige av Microsoft Dynamics AX-databasen som datakilder for dokumentformater. En firmabruker kan konfigurere formatene basert på disse domenespesifikke datamodellene (for eksempel for betalinger, Intrastat-rapporter eller mva-rapporter). Brukeren konfigurerer formatene ved å bruke enkle, visuelle verktøy som ligner på Excel. ER støtter for øyeblikket generering av elektroniske dokumenter i tekst-, XML- og Excel-formater. Disse dokumentene kan genereres samtidig og pakkes til zip-filer. Datamodeller og formater støtter versjonskontroll. Formatversjoner kan ha gyldighetsperioder. Hver datamodell eller formatversjon lagres i en egen konfigurasjon og distribueres til partnere og kunder via LCS. Partnere og kunder kan tilpasse Microsoft-datamodeller og -formater eller opprette egne. ER lagrer partner- og kundekonfigurasjonsendringer som delta for Microsoft-konfigurasjoner, som gjør det enklere å oppgradere til nyere versjoner av Microsoft-konfigurasjoner. Ved hjelp av LCS kan partnere også dele sine datamodell- og formatkonfigurasjoner med andre partnere og kunder, som kan tilpasse og dele dem. Deltatilpasning og enkel oppgradering støttes gjennom hele tilpasningskjeden.</td>
<td>ER forenkler oppretting, vedlikehold og oppgradering av elektroniske dokumentformater slik at de oppfyller juridiske krav i forskjellige land/regioner. ER gjør prosessen med å opprette eller endre elektroniske dokumentformater raskere og enklere. Disse endringene gjøres av bedriftsbrukere i stedet for utviklere. ER gjør det raskere og enklere for partnere og kunder å oppgradere sine formattilpassinger til nyere versjoner av formatene som utgis av Microsoft eller andre partnere. ER har én vanlig måte (via LCS) for Microsoft og partnere til å distribuere elektroniske dokumentkonfigurasjoner til andre partnere og kunder. ER gjør det også enklere for partnere og kunder å tilpasse, oppgradere og distribuere elektroniske dokumentformater til sine spesifikke forretningsbehov.</td>
</tr>
<tr class="odd">
<td>(MEX) Generer forskriftsmessige meksikanske merverdiavgiftsrapporter (mva).</td>
<td>Du må generere rapporter for **Mva for salg og innkjøp** ved å bruke funksjonaliteten for urealisert mva slik at brukere kan identifisere transaksjoner som tilhører de realiserte og urealiserte delene basert på statusen.</td>
<td>**Mva for salg og innkjøp**-rapporter er endret og tar bare hensyn til funksjonen for betinget mva ved å bruke bestemte utligningsperioder for definering av ikke-realiserte og realiserte mva-koder.</td>
<td>Endringer i konfigurasjonen av mva-koder er påkrevd før brukere kan generere disse rapportene på riktig måte. En funksjon for betinget mva er obligatorisk, og brukeren må konfigurere separate utligningsperioder, urealiserte og realiserte, for å identifisere transaksjonene i de relaterte deler-områdene.</td>
</tr>
<tr class="even">
<td>(JPN) Behandle deklarasjonsdokumentet for hurtigere avskriving av japanske anleggsmidler.</td>
<td>Ikke tilgjengelig</td>
<td>Viktig deklarasjonsinformasjon er lagret sentralt i ett dokument for bedre vedlikehold.</td>
<td>Dokumentetsamsvar og enkel administrasjon bidrar til å redusere problemer under revisjoner og andre gjennomganger.</td>
</tr>
<tr class="odd">
<td>(JPN) Kontroller JBA-tegn på bankkontoen.</td>
<td>Ikke tilgjengelig</td>
<td>Du kan kontrollere at kana-felt inneholder bare tegnene som tillates av JBA-bankformatet.</td>
<td>Det reduserer avbrudd for brukere under generering av betalingsfilen på grunn av ugyldige tegn.</td>
</tr>
<tr class="even">
<td>(JPN) Samle opp Japan øredifferanse for anleggsmidler på slutten av regnskapsåret.</td>
<td>Ikke tilgjengelig</td>
<td>På siden **Parametere for anleggsmidler** kan du velge å samle opp på slutten av regnskapsperioden eller regnskapsåret.</td>
<td>Det gir større fleksibilitet i forhold til samsvar med lokal praksis.</td>
</tr>
<tr class="odd">
<td>(JPN) Generer japansk selskapsskatt vedlagt tabell 16-serien med et summert beløp for hovedtype for anleggsmiddel.</td>
<td>Ikke tilgjengelig</td>
<td>På verdimodellene for et anleggsmiddel kan du velge å summere etter hovedtypen. Som standard brukes denne funksjonaliteten for nyopprettede anleggsmidler.</td>
<td>For store selskaper som har tusenvis av anleggsmidler, reduserer de summerte rapportene størrelsen på rapporten som genereres, betydelig.</td>
</tr>
<tr class="even">
<td>(JPN) Start å tildele særskilt avskrivningsreserve fra neste regnskapsår for japanske anleggsmidler.</td>
<td>Ikke tilgjengelig</td>
<td>På verdimodellene for et anleggsmiddel som har en passende ekstraordinær avskrivningsprofil, kan du velge å starte tildelingen fra neste regnskapsperiode eller det neste regnskapsåret.</td>
<td>Det gir større fleksibilitet i forhold til samsvar med lokal praksis.</td>
</tr>
<tr class="odd">
<td>(JPN) Generer en japansk forbruksavgiftsrapport som inneholder de endrede mva-satsene.</td>
<td>Forbruksavgiftsrapporten er tilgjengelig for en mva-sats på 5 prosent.</td>
<td>Forbruksavgiftsrapporten inneholder en del for den endrede mva-satsen (for eksempel 8 prosent).</td>
<td>Oppsettet ble nylig annonsert av myndighetene.</td>
</tr>
<tr class="even">
<td>(EU) Konfigurere innstillinger for avrunding for EU-salgslisten.</td>
<td>Innstillinger for avrunding for rapportering av EU-salgslisten for forskjellige land/områder er hardkodet i X++ eller XSLT-filer (Extensible Stylesheet Language Transformations).</td>
<td>Innstillinger for avrunding blir lagt til Utenrikshandelsparametere. Du kan konfigurere avrundingspresisjon, avrundingsmetode, utdatapresisjon og virkemåten for beløp som er mindre enn avrundingspresisjonen.</td>
<td>Dette forener og forenkler konfigureringen av rapporteringen av EU-salgslister. Justering av innstillinger for avrunding krever ikke lenger utviklingstiltak.</td>
</tr>
<tr class="odd">
<td>(EU) Konfigurere gyldighetsregler for snudd avregning.</td>
<td>Gyldighetsregler for snudd avregning er hardkodet for scenariet for innenlands snudd avregning. Terskelen for gyldighet kan defineres per varegruppe. Denne funksjonen er bare tilgjengelig for Storbritannia.</td>
<td>Du kan konfigurere gyldighetsregler for snudd avregning per dokumenttype (bestilling/salgsordre, leverandørfaktura, fritekstfaktura og så videre), og en gruppe for snudd avregning som kombinerer varer, varegrupper og kategorier for kjøp/salg. Gyldighetsreglene har gyldighet fra en dato. Du kan også merke individuelle mva-koder i mva-grupper som gjelder for snudd avregning. Salgsfakturarapporten justeres for å representere detaljene for utlignet snudd avregning. Funksjonaliteten er tilgjengelig for alle europeiske land/områder.</td>
<td>Denne endringen forener konfigurasjonen av gyldighetsregler for snudd avregning, og støtter bruk av innenlandske avregningsbestemmelser i europeiske land/områder.</td>
</tr>
<tr class="even">
<td>(DE) Generer den tyske revisjonsfilen – GDPdUGoBD</td>
<td>Brukere kan definere definisjon av tabeller som inneholder økonomiske data som skal eksporteres til et format som er godkjent av tyske revisorer og myndigheter.</td>
<td>Funksjonen er implementert som en elektronisk rapporteringskonfigurasjon. Denne funksjonen er tilgjengelig for Tyskland og Australia.</td>
<td>Denne endringen gir brukere mange flere muligheter med hensyn til dataformatering og transformasjoner, og gir også alle fordelene som kommer fra administrasjon av livssyklus for elektronisk rapporteringskonfigurasjon, som enkel konfigurasjonsutveksling, versjonskontroll og så videre.</td>
</tr>
<tr class="odd">
<td>(FR) Saldoliste med rapport om gruppetotalkontoer</td>
<td>Saldoliste med rapport om gruppetotalkontoer er implementert som SSRS-rapport (LedgerAccountSum\_FR).</td>
<td>Saldoliste med rapport om gruppetotalkontoer er implementert som Management Reporter-rapporten som er tilgjengelig i mappen for lokaliserte finansrapporter i LCS-aktivabiblioteket.</td>
<td>Dette lar brukere få alle fordelene med og friheten ved tilpassinger ved hjelp av finansrapporter i Management Reporter.</td>
</tr>
<tr class="even">
<td>(EU) Betalingsmelding, deltakernotat og kontrollrapporter for betalinger.</td>
<td>Alle disse rapportene og SSRS-rapporter er implementert.</td>
<td>Disse rapportene er implementert som Open XML-maler som skal brukes i Microsoft Excel.</td>
<td>Elektroniske betalingskonfigurasjoner inneholder oppsett og maler for betalingsfilformat. Dette lar brukere få alle fordelene med og friheten ved rapporttilpassinger ved hjelp elektronisk rapportering.</td>
</tr>
<tr class="odd">
<td>(EU) Konfigurere innstillinger for avrunding for Intrastat.</td>
<td>Innstillinger for avrunding for Intrastat-rapportering for forskjellige land/områder er hardkodet i X++ eller XSLT-filer (Extensible Stylesheet Language Transformations).</td>
<td>Innstillinger for avrunding blir lagt til utenrikshandelsparametere. Du kan konfigurere avrundingspresisjon, avrundingsmetode, utdatapresisjon og virkemåten for beløp som er mindre enn avrundingspresisjonen.</td>
<td>Dette forener og forenkler konfigureringen av Intrastat-rapporteringen. Justering av innstillinger for avrunding krever ikke lenger utviklingstiltak.</td>
</tr>
<tr class="even">
<td>(EU) Definere Intrastat-artikkelkoder i kategorihierarkier.</td>
<td>Intrastat-artikkelkoder er en egen liste. Selv om det finnes et kategorihierarki av typen Artikkelkode, kan disse artikkelkodene angis som standard i Detaljhandel HK og salgkategorier.</td>
<td>Egen liste over Intrastat-artikkelkoder er slått sammen med produkthierarki av typen Artikkelkode.</td>
<td>Dette forener tilnærmingen med til å tilordne artikkelkoder til frigitte produkter og kategorier i salgs- og kjøpsdokumenter.</td>
</tr>
<tr class="odd">
<td>(EU) Rapportantall i tilleggsenheter for Intrastat ved hjelp av innstillingen for konvertering av enhet.</td>
<td>Intrastat-artikkelkoden har et tekstfelt for å identifisere flere enheter, og **Produkt**-kortet har et felt for å identifisere antall tilleggsenheter angitt i kilo.</td>
<td>Tilleggsenheter for Intrastat-artikkelkoden som er valgt fra listen over enheter. Antall tilleggsenheter beregnes gjennom innstillingene for konvertering av enhet.</td>
<td>Det forener tilnærmingen for omberegning fra enheter av transaksjon til tilleggsenheter.</td>
</tr>
<tr class="even">
<td>(EU) Tilordne standard transportmåte til leveringsmåte.</td>
<td>Ikke tilgjengelig</td>
<td>Et felt for standard transportmåte er lagt til leveringsmåten.</td>
<td>Dette forenkler klargjøringen av Intrastat-rapportering.</td>
</tr>
<tr class="odd">
<td>(EU) Marker at frigitt produkt ikke skal rapporteres i Intrastat.</td>
<td>Ikke tilgjengelig</td>
<td>Et alternativ for å utelate varen fra Intrastat-rapportering er lagt til frigitt produkt.</td>
<td>Dette forenkler klargjøringen av Intrastat-rapportering.</td>
</tr>
</tbody>
</table>

## <a name="manufacturing"></a>Produksjon
|                                                                                                                                                      |                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hva kan du gjøre?**                                                                                                                                 | **Dynamics AX 2012**                                                                                                             | **Dynamics AX 7.0**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | **Hvorfor er dette viktig?**                                                                                                                                                                                                                                            |
| Utfør en kontroll av materialtilgjengelighet for produksjonsordrer på en egen side som åpnes fra **Produksjonsstyring**-arbeidsområdet. | Ikke tilgjengelig                                                                                                                    | Produksjonsansvarlig kan kontrollere om materialer for planlagte produksjonsordrer er tilgjengelige på påkrevd dato. I arbeidsområdet kan produksjonsansvarlig se hvor mange produksjonsordrer som har planlagt-status og venter på frigivelse. Basert på den dynamiske hovedplanen oppdateres informasjonen om materialtilgjengelighet hvis materialbehovet oppfylles av lagerbeholdning for faktisk bestillinger eller planlagte bestillinger. Basert på informasjonen om materialtilgjengelighet kan arbeidslederen frigi ordrene på **Materialtilgjengelighet**-siden.                                                                                                                                                                                                                                                                                                                        | Det hjelper produksjonsansvarlig med å ta riktige avgjørelser om tildelingen av materialer til ordrer når produksjonsordrer frigis til shop floor.                                                                                                       |
| Start og rapporter fremdrift for produksjonsjobber ved hjelp av den nye **Jobbkortenhet**-siden.                                                              | **Jobbregistrering**-skjemaer er først og fremst målrettet til store terminalskjermer, og brukergrensesnittet er vanligvis tilgjengelig via museklikk. | Selv om den nye **Jobbkortenhet**-siden er utviklet med tanke på enkelhet, er den også utformet for berøring. Siden passer bra på mobilenheter, for eksempel nettbrett og telefoner. Ansatte i shop floor vil oppleve mindre informasjonsoverbelastning og mer brukervennlighet. Arbeideren kan utføre vanlige oppgaver, for eksempel start, slutt og rapportering av fremdriften på en jobb. I tillegg til å arbeide med den faktiske jobben eller logge av og stemple ut kan arbeiden se vedlegg, lunsjpause og utføre andre aktiviteter. Jobber legges i kø til arbeider i en planlagt sekvens, men de kan også plukkes av arbeideren. Siden er først og fremst rettet mot stykkproduksjonoperasjoner, der materialer klargjøres for produksjon. For scenarioer som er relatert til rapportering av koprodukter og biprodukter, og materialplukking etter sporingsdimensjoner, kan du bruke **Jobbregistrering**-siden. | Ved å introdusere et alternativt grensesnitt som er utformet for berøring og er tilgjengelig fra alle typer enheter, for eksempel terminalskjermer og mobilenheter, kan denne funksjonen redusere implementeringskostnadene for en vanlig distribusjon av shop floor-registreringer. |

## <a name="master-planning-and-forecasting"></a>Hovedplanlegging og prognostisering
|                                                                                                                            |                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hva kan du gjøre?**                                                                                                       | **Dynamics AX 2012**                                                                                                                                                                                                                                                                          | **Dynamics AX 7.0**                                                                                                                                                                                                                                                                                                                                               | **Hvorfor er dette viktig?**                                                                                                                              |
| Advare brukeren hvis en salgsordre eller produksjonsordre er ikke klar for levering innen planlagt dato.                         | Advarsler som er opprettet av hovedplanlegging, kalles *terminmeldinger*. *Termin* er en kontrakt mellom to parter om å kjøpe eller selge aktiva til en pris som er avtalt i dag (*terminpris*), selv om leveringen og betalingen utføres på et tidspunkt i fremtiden (*leveringsdatoen)*. | Navnet på *terminmeldinger* og *termindatoer* er endret til henholdsvis *beregnede forsinkelser* og *forsinkede datoer*.                                                                                                                                                                                                                                                   | Terminologien som ble brukt i AX 2012, var feil og førte til feil oversettelser.                                                               |
| Få raskt innblikk i statusen for en hovedplanleggingskjøring, planlagte ordrer som haster, og planlagte ordrer som forårsaker forsinkelser. | Informasjonen er tilgjengelig, men den er spredt i flere skjemaer.                                                                                                                                                                                                                       | **Hovedplanlegging**-arbeidsområdet inneholder raskt informasjon om når den siste hovedplanleggingskjøring ble fullført, om eventuelle feil oppstod, hva de planlagte bestillingene er, og hvilke planlagte bestillinger som forårsaker forsinkelser.                                                                                                                                   | Du har nytte av oversikten arbeidsområdet gir. Relevant informasjon er satt sammen for å veilede med hovedplanlegging og forbedre produktiviteten. |
| Bruk Excel til å oppdatere behovsprognoser.                                                                                      | Ikke tilgjengelig                                                                                                                                                                                                                                                                                 | Du kan dra nytte av sømløs integrasjon med Microsoft Excel når du angir behovsprognoser, oppdaterer og sletter behovsprognoser.                                                                                                                                                                                                                             | Det bidrar til å øke effektiviteten og produktiviteten.                                                                                                          |
| Beregne fremtidig behov og opprette behovsprognoser basert på historiske transaksjonsdata.                                  | I Microsoft Dynamics AX 2012 R3 brukes prognosemodeller i Microsoft SQL Server Analysis Service til å opprette behovsprognoseforutsigelser.                                                                                                                                                | Beregn fremtidig behov ved hjelp av kraften og utvidelsesmulighetene i Microsoft Azure Machine Learning-skytjenesten. Det er enkelt å bruke og utvide prognosemodellene i Machine Learning for å oppfylle kundekrav. Tjenesten velger modell i henhold til hvilken som passer best, og tilbyr nøkkelytelsesindikatorer (KPI-er) som kan brukes til å beregne prognosenøyaktighet. | Generer mer nøyaktige prognoser ved hjelp av Machine Learning-teknikker.                                                                              |
| Optimaliser ordredatoen og -antallet basert på en visuell oversikt over relaterte handlinger fra hovedplanleggingskjøringen.          | Oversikten over handlingsdiagrammet er tilgjengelig, men viser alle de relaterte handlingene. Når handlinger brukes, forsvinner de øyeblikkelig fra visningen.                                                                                                                                             | Handlingsdiagrammet gir en bedre oversikt. Det inneholder alternativer som lar deg vise bare brukte handlinger og direkte tilknyttede handlinger. Når handlinger brukes, vil de vises nedtonet, men vil fortsatt vises. Derfor er oversikten beholdt. Tilleggsinformasjon er lagt til handlingsdiagrammet for å vise dataene på én side.                               | Du drar nytte av forbedring av produktivitet fordi du fokuserer bare på de relevante handlingene.                                                              |

## <a name="procurement-and-sourcing"></a>Innkjøp og leverandører
|                                                                                                                                                         |                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hva kan du gjøre?**                                                                                                                                    | **Dynamics AX 2012** | **Dynamics AX 7.0**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | **Hvorfor er dette viktig?**                                                                                                                                                                                                               |
| Bruk **Bestillingsklargjøring**-arbeidsområdet til å få raskt innblikk i statusen for bestillinger som klargjøres.                      | Støttes ikke        | **Bestillingsklargjøring**-arbeidsområdet gir en oversikt over ordrer fra tidspunktet når de opprettes som en kladd og spores, via statusene for arbeidsflytgodkjenning og videre til bekreftelse.                                                                                                                                                                                                                                                                                                                      | Innkjøpsavdelingen din trenger ikke lenger søke etter informasjon på flere sider, men har nå fordeler av oversikten fra arbeidsområdet.                                                                                         |
| Bruk **Bestillingsmottak og oppfølging**-arbeidsområdet for å få rask innsikt i bestillinger som venter på bekreftelse, for å hjelpe deg med oppfølging. | Støttes ikke        | **Bestillingsmottak og oppfølging** -arbeidsområdet gir en oversikt over bekreftede bestillinger som har ventende mottak eller forsendelser. Arbeidsområdet inneholder lister over forfalte mottak og ventende mottak som hjelper med proaktiv vurdering og oppfølging av leverandøren. Arbeidsområdet viser også bestillinger som det har oppstått ankomstregistreringen for på lageret, for å garantere at mottaket er bokført. Bestillingsreturer som ennå ikke er levert, er også tilgjengelige for gjennomgang. | Innkjøpsavdelingen din har fordel av oversikten som arbeidsområdet gir. Relevant informasjon er satt sammen for å veilede med oppfølging og forbedre produktiviteten.                                                                |
| Send bestillinger til bekreftelse hos en leverandørportal som er lagret i Dynamics AX-klienten. La leverandøren bekrefte eller avvise.                            | Støttes ikke        | Ved hjelp av leverandørportalgrensesnittet kan leverandører motta bestillinger som skal bekreftes eller avvises. Det gir også leverandøren en oversikt over alle bekreftede bestillinger for en konto. Innkjøpsagenten kan sende en bestilling med forespørsel om en bekreftelse fra leverandøren. Leverandøren må være en registrert Microsoft Azure Active Directory-bruker (Azure AS) i Dynamics AX, en kontaktperson for leverandøren og ha en dedikert sikkerhetsrolle.                                                     | Din innkjøpsavdelingen har nytte av redusert papirarbeid og manuelt å holde oversikt over svar på bestillinger, som flyten direkte til systemet. Én sannhetskilde reduserer misforståelser mellom kunde og leverandør. |

## <a name="projects"></a>Prosjekter
|                                        |                                                                                         |                                                                                                                                              |                                                          |
|----------------------------------------|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| **Hva kan du gjøre?**                   | **Dynamics AX 2012**                                                                    | **Dynamics AX 7.0**                                                                                                                          | **Hvorfor er dette viktig?**                               |
| Reserver arbeidere som ressurser i prosjekter. | I likhet med ressurser reseveres arbeidere direkte på prosjekter i tillegg til ressursene. | Arbeidssentertabellen der ressurser for produksjon og fremstilling lagres, kan nå brukes til å reservere arbeidere som ressurser i et prosjekt. | Når du legger inn prosjekter, trenger du bare å reservere ressurser. |

## <a name="retail-sales-marketing-and-customer-service"></a>Detaljhandelsalg, markedsføring og kundeservice
### <a name="retail-hq"></a>Detaljhandel HK

Detaljhandel HK driftet av Microsoft Azure gir sentralisert behandling av og fullstendig oversikt over alle aspekter av handelsoperasjoner via en webklient.

<table>






<tbody>
<tr class="odd">
<td><strong>Hva kan du gjøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er dette viktig?</strong></td>
</tr>
<tr class="even">
<td>Utfør varehandelsoperasjoner.</td>
<td>Brukere må få tilgang til flere skjemaer for å behandle disse dataene:
<ul>
<li>Kategoriadministrasjon</li>
<li>Produktstyring</li>
<li>Kanalproduktattributter</li>
<li>Assortement</li>
<li>Katalogadministrasjon</li>
<li>Sett</li>
<li>Priser og rabatter</li>
</ul></td>
<td><strong>Kategori- og produktstyring</strong>-arbeidsområdet muliggjør følgende funksjonalitet:
<ul>
<li>Sortimentstyring.</li>
<li>Sporing av sortimentlivssyklus.</li>
<li>Styring av frigitte produkter.</li>
</ul>
<strong>Arbeidsområdet for pris- og rabattstyring</strong> muliggjør følgende funksjonalitet:
<ul>
<li>Pris- og rabattstyring for en bestemt kanal og kategori.</li>
<li>Kategoriprisregelbehandling.</li>
<li>Pris- og rabattprioritet, som lar du tilordne prioritet til prisgrupper og rabatter, slik at du kan kontrollere rekkefølgen som de brukes i.</li>
<li>Ansettelses- og katalograbattbehandling.</li>
</ul>
<strong>Katalogadministrasjon</strong>-arbeidsområdet muliggjør følgende funksjonalitet:
<ul>
<li>Sammendrag av aktive kataloger.</li>
<li>Kataloglivssyklussporing på ett sted.</li>
</ul></td>
<td><ul>
<li>Arbeidsområder forbedrer effektiviteten og produktiviteten til ansatte ved at de sentralt kan administrere sine aktiviteter og handlinger som er knyttet til varehandelsrollen.</li>
<li>Funksjonen pris- og rabattprioritet gir kundene bedre kontroll over hvordan priser og rabatter brukes. Funksjonen gir også nye scenarier der høyere butikkpriser gjelder over standardpriser.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Administrer handelskanaldistribusjoner og -operasjoner.</td>
<td>Brukeren må åpne flere skjemaer for å utføre følgende oppgaver:
<ul>
<li>Opprette og konfigurere nye kanaler og relaterte enheter.</li>
<li>Behandle daglige aktiviteter for butikken.</li>
<li>Behandle handelstransaksjoner i Microsoft Dynamics AX, generere detaljhandelsutdrag og oppdatere Microsoft Dynamics AX-lager og -finans.</li>
</ul>
 </td>
<td>Med <strong>Kanaldistribusjon</strong>-arbeidsområdet kan du utføre følgende oppgaver:
<ul>
<li>Opprette nye kanaler og relaterte enheter.</li>
<li>Spore fremdriften for detaljhandelbutikkkonfigurasjonen.</li>
<li>Ta de nødvendige trinnene for å fullføre en aktivitet eller angi informasjon for å fullføre oppgaven.</li>
<li>Spore status for enheter og direkte validere og laste ned programinstallasjonen Retail Modern POS (MPOS) i butikker.</li>
<li>Få tilgang til alle relaterte sider.</li>
</ul>Med 
<strong>Administrasjon av detaljhandelsbutikk</strong>-arbeidsområdet kan du utføre følgende oppgaver:
<ul>
<li>Administrere arbeidere og arbeidernes salgsstedstillatelser (POS).</li>
<li>Spore skiftstatusen for en gitt butikk eller butikkgrupp.</li>
<li>Validere direkte og laste ned programinstallasjonen MPOS i butikker.</li>
<li>Skrive ut rapporter og få tilgang til relaterte sider.</li>
</ul>Med 
<strong>Finans for detaljhandelsbutikk</strong>-arbeidsområdet kan du utføre følgende oppgaver:
<ul>
<li>Opprette, beregne og postere utdrag for en bestemt kanal.</li>
<li>Planlegge satsvise jobber for å oppdatere beholdningen og beregne og postere utdrag.</li>
<li>Spore åpne utdrag.</li>
<li>Spore skiftstatusen for en gitt butikk eller butikkgrupp.</li>
<li>Skrive ut rapporter og få rask tilgang til alle relaterte sider.</li>
</ul></td>
<td>Arbeidsområder forbedrer effektiviteten og produktiviteten til ansatte ved at de sentralt kan administrere de fleste aktivitetene og handlingene som er knyttet til kanaldistribusjon, detaljhandelsbutikk og finans.</td>
</tr>
<tr class="even">
<td>Administrere operasjoner for IT for detaljhandel.</td>
<td>Brukeren må åpne flere skjemaer.</td>
<td><strong>IT for detaljhandel</strong>-arbeidsområdet muliggjør forespørsler om Commerce Data Exchange på ett sted for en bestemt kanal, slik at du kan utføre følgende oppgaver:
<ul>
<li>Nedlastingsøkter.</li>
<li>Opplastingsøkter.</li>
<li>Spore mislykkede økter og starte og kjøre dem på nytt.</li>
<li>Vise eller kjøre kommende jobber.</li>
</ul></td>
<td>Arbeidsområder forbedrer effektiviteten og produktiviteten til ansatte ved at de sentralt kan administrere sine aktiviteter og handlinger som er knyttet til operasjoner for IT for detaljhandel.</td>
</tr>
<tr class="odd">
<td>Import/eksport av data ved hjelp av dataenheter.</td>
<td>AX 2012 støtter enkel Microsoft Dynamics Retail Management System-migrasjon (RMS) ved hjelp av rammeverket for import og eksport av data.</td>
<td>Detaljhandelsdataenheter har blitt utvidet for å støtte alle hoved- og referansedata som er knyttet til handel. Det finnes også forbedret støtte for dataenheter på tvers av hele Dynamics AX-løsningen.</td>
<td>Dataenheter lar kunder utføre metadatadreven import og eksport av data. OData-enheter lar også kunder integrere Dynamics AX med tredjepartsprogrammer.</td>
</tr>
<tr class="even">
<td>Utfør intelligent analyse ved hjelp av BI-rapporter fra Dynamics Microsoft AX og POS-klienten.</td>
<td>Mer enn 25 back office-rapporter og fem kanalsiderapporter er tilgjengelige.</td>
<td>Mer enn 30 back office-rapporter og 10 kanalsiderapporter er tilgjengelige.</td>
<td>Med disse rapportene kan kunder ha mer BI til å forutse trender, avdekke innsikt og operere med kontinuerlig toppytelse.</td>
</tr>
<tr class="odd">
<td>Analyser salgsdata for handelskanal ved å bruke "Overvåk resultat for detaljhandelskanal"-innhold for Power BI.</td>
<td>Ikke tilgjengelig</td>
<td>I PowerBI.com velg <strong>Hent data</strong>, og velg deretter <strong>Dynamics AX – Resultat for detaljhandelskanal</strong>-innholdspakken. Angi URL-adressen for sluttpunktet i Dynamics AX for å vise dataene i instrumentbordet.</td>
<td>Med tre til fire klikk kan organisasjoner distribuere et Power BI-instrumentbord som inneholder viktige økonomiske data. Innholdet kan tilpasses av organisasjonen. I tillegg kan brukere bygge inn Power BI-instrumentbordfliser i sine personlige arbeidsområder i Dynamics AX slik at de raskt kan se analytisk informasjon.</td>
</tr>
<tr class="even">
<td>Konfigurer forbrukertillatelser.</td>
<td>Ikke tilgjengelig</td>
<td>Kunder kan velge om POS-operasjoner skal være tilgjengelige for forbrukere. Detaljhandelsserver bruker tillatelser til API-kall (application programming interface).</td>
<td>Det gir mulighet for å konfigurere tillatelser på forbrukernivå.</td>
</tr>
<tr class="odd">
<td>Behandle og godkjenne enhetskonfigurasjoner.</td>
<td>Ikke tilgjengelig</td>
<td>Funksjonen for konfigurasjonsbehandling og validering gir følgende funksjonalitet:
<ul>
<li>Masseopplasting av konfigurasjonsdata</li>
<li>Forretningsenhetsvalidering</li>
</ul></td>
<td>Det gir mulighet til starte konfigurasjonen med oppstartsprogram og til å validere statusen og om konfigurasjonen er fullført for de ulike elementene i konfigurasjonen.</td>
</tr>
</tbody>
</table>

### <a name="retail-hardware-station"></a>Maskinvarestasjon for detaljhandel

|                                                                                                  |                                                                         |                                                                                                                                                                                                                                                                                                                                                               |                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **Hva kan du gjøre?**                                                                             | **Dynamics AX 2012**                                                    | **Dynamics AX 7.0**                                                                                                                                                                                                                                                                                                                                           | **Hvorfor er dette viktig?**                                                                                                        |
| Aktiver POS-enheter for å koble til enheter som skrivere, kassaskuffer eller betalingsenheter. | Maskinvareprofilen MPOS brukes til å angi enhetene som skal brukes. | En ekstra maskinvareprofil støtter flere typer maskinvare fra én stasjon til neste. En ny maskinvarestasjonprofil støtter en unik terminal-ID for hver maskinvarestasjon når EFT-transaksjoner (elektronisk pengeoverføring) behandles. EFT-støtte er slått sammen med maskinvarestasjon for å redusere involveringen av MPOS i EFT-betalingsbehandling. | Den gir større fleksibilitet for implementeringer. I tillegg gir den bedre sikkerhet og redusert eksponering for kredittkortdata. |

### <a name="retail-server-and-data-management"></a>Detaljhandelsserver og databehandling

Med detaljhandelsserver og databehandling kan kunder og bedrifter opprette en omnikanal for handleopplevelse på online-, butikk- og telefonsenterkanaler.

<table>






<tbody>
<tr class="odd">
<td><strong>Hva kan du gjøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er dette viktig?</strong></td>
</tr>
<tr class="even">
<td>Koble til en database for commerce runtime (CRT) som inneholder forretningsdata for kanalen, ved hjelp av CRT-tjenester.</td>
<td>OData V3 støttes.</td>
<td>OData V4 støttes.</td>
<td>Du hjelper kunden med å holde seg oppdatert med OData-standardene. Det opprettes også en robust omnikanalopplevelse ved å integrere salg på tvers av butikk-, mobil- og onlinekanaler.</td>
</tr>
<tr class="odd">
<td>Støtter detaljhandelstjenester som et tjenestesett som kan være vert.</td>
<td>E-handels-API støttes ikke via detaljhandelsserver.</td>
<td>E-handels-API er nå tilgjengelig via detaljhandelsserver for å støtte online-scenarier.</td>
<td>Den gir vertsbasert og skalerbar e-handelstjenester som kan brukes med tredjeparts nettbutikker.</td>
</tr>
<tr class="even">
<td>Flytt data mellom Microsoft Dynamics AX-underkontoen og -kanalene ved hjelp av Commerce Data Exchange.</td>
<td>Commerce Data Exchange er et system som overfører data mellom Microsoft Dynamics AX og detaljhandelskanaler, for eksempel nettbutikker eller fysiske butikker. Hvis du vil ha mer informasjon, kan du se <a href="https://technet.microsoft.com/en-us/library/dn741440.aspx">Commerce Data Exchange [AX 2012]</a>.</td>
<td>Det finnes funksjonell paritet med Microsoft Dynamics AX 2012 CU8. Vær imidlertid oppmerksom på følgende detaljer:
<ul>
<li>Commerce Data Exchange er rekonstruert for skyen.</li>
<li>Asynkron tjeneste bruker direkte databasetilgang til kanaldatabasen.</li>
<li>Commerce Data Exchange: Real-time Service er lagret som en egendefinert tjeneste for Microsoft Dynamics AX.</li>
<li>MPOS administrerer synkroniseringen mellom frakoblede databaser og detaljhandelsserveren.</li>
</ul></td>
<td>Commerce Data Exchange er rekonstruert for skyplattformen. Den fortsetter å administrere overføringen av data mellom Microsoft Dynamics AX og detaljhandelskanaler, for eksempel nettbutikker eller fysiske butikker.</td>
</tr>
<tr class="odd">
<td>Støtter plug and play, delvis integrert betaling på tvers av kanaler ved hjelp av betalings-SDK-en.</td>
<td>AX 2012 inneholder følgende funksjonalitet:
<ul>
<li>Støtte for alle kanaler: salgssted, e-handel og telefonsenter.</li>
<li>Støtte for funksjon der kort forevises og ikke forevises.</li>
<li>Side for å godta betaling.</li>
<li>Ekstern støtte for LS5300 og MX925 som eksempelkode i SDK for detaljhandel.</li>
</ul></td>
<td>Den gjeldende versjonen av Dynamics AX støtter alle eksisterende Microsoft Dynamics AX for Retail 2012 kreditt-/debetkortfunksjoner og fire nye forbedringer.</td>
<td>Den lar kunden behandle kreditt-/debetkorttransaksjoner for betalinger.</td>
</tr>
<tr class="even">
<td>Aktiver enheter ved hjelp av en Microsoft-konto (Microsoft Azure Active Directory (Azure AD)).</td>
<td>Ikke tilgjengelig</td>
<td>Følgende funksjonalitet finnes:
<ul>
<li>Forbedret sikkerhet ved Azure AD-basert aktivering for skyen.</li>
<li>Utvidet sikkerhet for behandling av token.</li>
<li>Forbedret pålitelighet, feilsøking og feilmeldinger under aktivering</li>
<li>Forenklede IT-administrasjonsoppgaver som er knyttet til aktivering.</li>
<li>Gikk tilbake til trusselmodell og fikset sikkerhetsproblemer.</li>
</ul></td>
<td>Den gir følgende fordeler:
<ul>
<li>Sikkerheten er forbedret gjennom Azure AD og enhetstoken/-ID (RS-kall som bruker token, brukerspesifikk applagring).</li>
<li>Den stopper uautorisert ekstern bruk av MPOS (fysisk enhet).</li>
<li>Den sporer MPOS-enheter for PCI-samsvarsformål.</li>
<li>Den tilordner fysiske enheter til en bransjeenhet (register) ved hjelp av en enhetskode.</li>
<li>Den initialiserer innstillinger for jevn MPOS-funksjonalitet (nummerserier og maskinvareprofiler) som første kontaktpunkt for MPOS.</li>
<li>Den rapporterer enhetsinformasjon fra hovedkontor.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Behandle rikt medieinnhold for redigering og levering via galleriet for medier.</td>
<td>Ikke tilgjengelig</td>
<td><ul>
<li>Støtter bildeopplasting, og visning, behandling og sletting, fra mediegalleriet både for eksternt vertsbaserte bilder og bilder som er vertsbaserte i detaljhandel.</li>
<li>Støtter bildeopplasting og visning fra enhetssider (<strong>Produkter</strong>, <strong>Kataloger</strong> og så videre) ved å koble et bilde fra galleriet og laste opp et bilde fra skrivebordet.</li>
<li>Optimaliser bildene for miniatyrvisning, tilpasset størrelse og original.</li>
<li>Massekoble enheter ved å bruke en mal og bakgrunnsjobber for massetilknytning.</li>
<li>Microsoft Excel-integrasjon overskriver attributtgruppebegrensningen for navnekonvensjoner og forhåndsdefinerte baner.</li>
<li>Støtter frakoblede bilder og sikre bilder for PII-innhold (personlig identifiserbar informasjon), for eksempel ansatt- og kundebilder som er vertsbasert i detaljhandel.</li>
</ul></td>
<td><ul>
<li>Det håndterer utfordringer rundt eksternt vertsbaserte bilder slik at du slipper å gå frem og tilbake og i stedet kan behandle på ett sted.</li>
<li>Det gir omfattende innholdsstyring fra mediegalleriet for opplastede og eksternt vertsbaserte bilder og inneholder også filtrering for å hjelpe deg å finne bilder.</li>
<li>Du kan enkelt opprette bulktilknytninger mellom eksternt vertsbaserte bilder og enheter, for eksempel produkter og kataloger.</li>
<li>Det støtter vertsbasert lagring av bilder i detaljhandel og Excel-integrering for enkle oppdateringer.</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="rich-clientele-experience"></a>Rik kundeopplevelse

Detaljhandel gir dyptgående mobilopplevelse når og hvor som helst og på hvilken som helst enhet. Denne funksjonen gir bedre shopping- og butikkopplevelse på tvers av alle kanaler.

<table>






<tbody>
<tr class="odd">
<td><strong>Hva kan du gjøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er dette viktig?</strong></td>
</tr>
<tr class="even">
<td>Søk, bla gjennom, slå opp eller skann produkter, legg til produkter i en handlekurv, godta betaling og sjekk ut ved hjelp av en intuitiv, berøringsvennlig, rik og dyptgående brukeropplevelse på MPOS.</td>
<td>AX 2012 har følgende funksjoner:
<ul>
<li>Utfør salg, returer og annulleringer.</li>
<li>Opprett, endre og fang opp kundeordrer.</li>
<li>Utfør skift- og skuffoperasjoner.</li>
<li>Plukk og motta ordrer, og utfør lagertellinger.</li>
<li>Vis butikkrapporter.</li>
</ul></td>
<td>Funksjonell paritet med AX 2012 MPOS leveres. Dette omfatter følgende funksjonalitet:
<ul>
<li>Kundeoppslag på tvers av butikker/kanaler.</li>
<li>Muligheten til å opprette kundeordrer uten å bruke sanntidstjeneste.</li>
<li>Forbedret enhetsaktiveringsarbeidsflyter, status og feilmeldinger.</li>
<li>Utvidelsesforbedringer, for eksempel førpostutløsere og aktivitetsstøtte for å forbedre tilpasning.</li>
</ul></td>
<td>Selgere kan behandle salgstransaksjoner og kundeordrer og utføre daglige operasjoner og lagerstyring ved hjelp av mobilenheter hvor som helst i butikken.</td>
</tr>
<tr class="odd">
<td>Start salgssted som en webapp via skysalgssted.</td>
<td>Ikke tilgjengelig</td>
<td>Funksjonell paritet med MPOS leveres. Dette omfatter følgende funksjonalitet:
<ul>
<li>Enhetsaktivering ved hjelp av AAD</li>
<li>Responsiv oppsettdesign</li>
<li>Støtte for Edge-, Internet Explorer- og Chrome-nettlesere.</li>
</ul></td>
<td>Det inneholder et salgssted for webapp med funksjonalitet som er kompatibel med MPOS, og som kan brukes på tvers av plattformer og nettlesere med gratis distribusjon.</td>
</tr>
<tr class="even">
<td>Integrer med systemer for innholdsbehandling for å opprette et nettsted for omnikanal for e-handel.</td>
<td>Microsoft SharePoint- og tredjeparts butikkfasader støttes.</td>
<td>Det finnes en e-handelsplattform som støtter tredjeparts butikkfasader. Plattformen inneholder følgende funksjoner:
<ul>
<li>En rik forbruker-API.</li>
<li>Godkjenningsintegrering med hvilke som helst tredjeparts openID-leverandører.</li>
<li>Betalingsintegrasjon.</li>
</ul></td>
<td>Kunder har nå fleksibilitet til å bruke innholdsbehandlingssystem etter eget valg.</td>
</tr>
<tr class="odd">
<td>Målrett kunder via e-postordrekataloger, og strømlinjeforme operasjoner via rask ordreregistrering, assistert salg og fullføring ved hjelp av telefonsenter.</td>
<td><ul>
<li>Telefonsenterkanal</li>
<li>E-postordrekataloger</li>
<li>Rask ordreregistrering og assistert salg</li>
<li>Forbedret ordrefullføring</li>
<li>Kundestøtte</li>
<li>Integrert prising og kampanjer/rabatter</li>
</ul></td>
<td>Funksjonsparitet med AX 2012-kundesenterløsning er tilgjengelig, med unntak av prisoverstyringer.</td>
<td>Telefonsentre er en type detaljhandelskanal der arbeidere mottar ordrer fra kunder via telefonen og oppretter salgsordrer.</td>
</tr>
</tbody>
</table>

### <a name="commerce-essentials"></a>Grunnleggende om handel

Et detaljhandels- og handelsfokusert konfigurasjonsalternativ bidrar til å strømlinjeforme handelsspesifikke distribusjoner.

|                                               |                                                                                                             |                                                                                                                                                                               |                                                                                                                                                         |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hva kan du gjøre?**                          | **Dynamics AX 2012**                                                                                        | **Dynamics AX 7.0**                                                                                                                                                           | **Hvorfor er dette viktig?**                                                                                                                              |
| Bruk Grunnleggende om handel-instrumentbordet.        | En områdeside med koblinger til menyelementer er tilgjengelig.                                                         | Grunnleggende om handel-instrumentbordet inneholder koblinger til vanlige oppgaver, inkludert koblinger til arbeidsområder, Power BI-webkontrollen, favoritter, nylige sider og gjeldende arbeidselementer. | Det utvidede instrumentbordet gjør det mulig for arbeidere å jobbe effektivt og gir et fleksibelt utgangspunkt for handelsspesifikke aktiviteter.             |
| Bruk dataenheter til å få tilgang til kontoendringer.  | Kontoendringer eksporteres til en mappe på filsystemet.                                                | Kontoendringer er tilgjengelige gjennom dataenheter.                                                                                                                         | Denne funksjonen gir større fleksibilitet når du flytter data mellom ulike systemer. Denne funksjonen kan bli forbedret gjennom OData-programmer også. |
| Bruk skysalgssted og MPOS.                       | Bare Enterprise POS (EPOS) støttes som standard.                                                     | MPOS og skysalgssted erstatter EPOS-klienten. E-handelskanalen er også lagt til i Grunnleggende om handel som standard.                                                     | Denne funksjonen gir økt standard kanalstøtte med raskt distribuerbare salgsstedsklienter.                                                  |
| Implementere og vedlikeholde tolagsarkitektur. | Rammeverket for dataimport/-eksport gir mulighet for å flytte data mellom AX 2012 og tredjepartssystemer. | Dataenheter opprettet for å forbedre støtten for tolagsarkitektur.                                                                                                           | Dataenheter og OData-programmer gir et abstraksjonslag for å gjøre det enklere å implementere og vedlikeholde tolagsscenarier.                          |
| Forenkle skjemaer.                               | Egendefinert kode kreves for å forenkle brukergrensesnittet.                                                                 | Skjema- og menyutvidelser gir standardisert grensesnittforenkling.                                                                                                              | Denne funksjonen gir en raskere og enklere måte å finjustere skjemaer basert på behovene til forhandleren.                                                             |

### <a name="pos-task-recorder"></a>Oppgaveregistrering for salgssted

<table>






<tbody>
<tr class="odd">
<td><strong>Hva kan du gjøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er dette viktig?</strong></td>
</tr>
<tr class="even">
<td>Opprette og dele aktivitetsveiledninger og dokumenter for moderne salgssted.</td>
<td>Ikke tilgjengelig</td>
<td>MPOS-oppgaveregistrering støtter følgende funksjoner:
<ul>
<li>Opprette oppgaveregistreringer for forskjellige oppgaver som utføres i MPOS.</li>
<li>Generere et dokument som inneholder trinn og skjermbilder og knytte det til en node i forretningsprosessmodellen.</li>
</ul></td>
<td>Partnere og uavhengige programvareleverandører (ISV-er) kan tilpasse MPOS og gi støttedokumenter for å lære opp sine brukere.</td>
</tr>
</tbody>
</table>

### <a name="extensibility"></a>Utvidelsesmuligheter

<table>






<tbody>
<tr class="odd">
<td><strong>Hva kan du gjøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er dette viktig?</strong></td>
</tr>
<tr class="even">
<td>Støtte for komponenter for detaljhandel som er utvidbare og enkle å distribuere på tvers av hovedkontor, telefonsenter, e-handel og salgsstedet.</td>
<td>Komponentene kan utvides ved hjelp av SDK for detaljhandel. Ingen funksjoner for pakking og distribusjon støttes.</td>
<td>Utvidelsesbindinger er forbedret på tvers av de forskjellige komponentene for å gi bedre støtte for kodeisolering og tilgjengelighet. Her er noen av funksjonene som følger med:
<ul>
<li>Arbeidsflyt, aktivitet og operasjon.</li>
<li>Forhåndsutløsere og etterutløsere som gjør det enkelt å utvide en arbeidsflyt.</li>
<li>Program- og operasjonsutløsere.</li>
</ul>
I tillegg finnes det et rammeverk som lar deg lage og pakke disse komponentene ved hjelp av MSBuild og deretter sømløst distribuere tilpassingen ved hjelp av Microsoft Dynamics Lifecycle Services (LCS).</td>
<td>Forhandlere har veldig spesifikke krav basert på vertikaler og områder for operasjonen. Ved hjelp av en enkelt utvidbar plattform kan vi aktivere bruk på tvers av vertikaler og markeder. Fordi detaljhandel også har en svært distribuert arkitektur, kan muligheten til sømløs distribusjon øke produktiviteten betydelig.</td>
</tr>
</tbody>
</table>

### <a name="lifecycle-management"></a>Administrasjon av livssyklus

Lifecycle Services (LCS) gir et sett med tjenester som kunder og partnere kan bruke til å administrere livssyklusen til systemet fra registrering til daglige operasjoner.

<table>






<tbody>
<tr class="odd">
<td><strong>Hva kan du gjøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er dette viktig?</strong></td>
</tr>
<tr class="even">
<td>Behandle programmet via skydistribusjonstjenester.</td>
<td>Ikke tilgjengelig</td>
<td>Følgende topologier kan distribueres til skyen:
<ul>
<li>Detaljhandel prøvetopologi med virtuell maskin med én boks.</li>
<li>Detaljhandel flerbokstopologi med høy tilgjengelighet.</li>
<li>Utviklertopologi med SDK for detaljhandel.</li>
</ul>
Det finnes en forbedret og forenklet klientkomponentinstallasjon via selvbetjeningsinstallasjonen:
<ul>
<li>Moderne salgssted for detaljhandel.</li>
<li>Maskinvarestasjon for detaljhandel</li>
<li>Støtte for opplasting og distribusjon av egendefinerte pakker via selvbetjeningsinstallasjon.</li>
</ul></td>
<td>Skydistribusjonstjenester gir følgende fordeler:
<ul>
<li>Betydelig redusert distribusjonsinnsats og -kompleksitet for Detaljhandel HK-komponenter.</li>
<li>Opprinnelig distribusjon til den offentlige Microsoft Azure-skyen.</li>
<li>Forbedret selvbetjeningsinstallasjon av komponenter i butikken slik at konfigurasjonen blir enklere og mer intuitivt</li>
</ul></td>
</tr>
<tr class="odd">
<td>Overvåke tilstanden til systemet og analysere problemer og feil.</td>
<td>Denne funksjonen krever <a href="http://www.microsoft.com/en-us/download/details.aspx?id=42636">System Center 2012-administrasjonspakken for Microsoft Dynamics AX 2012 R3 CU8 Retail</a>.</td>
<td>Overvåking og diagnose for detaljhandelskomponenter er nå tilgjengelig gjennom <strong>Driftsinnsikt</strong>-instrumentbordet i LCS.</td>
<td><strong>Driftsinnsikt</strong>-instrumentbordet er en skybasert overvåkingsportal som erstatter behovet for å installere SCOM-infrastrukturen (System Center Operations Manager).</td>
</tr>
<tr class="even">
<td>Opprette, konfigurere, laste ned og installere Maskinvarestasjon for detaljhandel og enheter ved hjelp av selvbetjening.</td>
<td>Ved hjelp av Objektinnpakking og Enterprise Portal kan en bruker utføre en automatisert installasjon og konfigurasjon av alle komponenter som kreves i en bestemt datamaskin, basert på en definert topologi.</td>
<td>Fordi det bare er to installasjonspakker, én for MPOS-klienten og den andre for komponenten Maskinvarestasjon for detaljhandel, har selvbetjeningen redusert arbeidsmengden som kreves på alle nivåer for å installere disse klientkomponentene.</td>
<td>Selvbetjening har til hensikt å minimere krav og gjøre det enklere for brukere å utføre en installasjon.</td>
</tr>
</tbody>
</table>

## <a name="sales"></a>Salg
<table>






<tbody>
<tr class="odd">
<td><strong>Hva kan du gjøre?</strong></td>
<td><strong>Dynamics AX 2012</strong></td>
<td><strong>Dynamics AX 7.0</strong></td>
<td><strong>Hvorfor er dette viktig?</strong></td>
</tr>
<tr class="even">
<td>Få et raskt overblikk over leveringsalternativer når du lover ordrer til kunder.</td>
<td>Når det finnes begrensninger for produkttilgjengeligheten, og kundens ønskede leveringsdato for ett eller flere produkter i ordren ikke kan oppfylles, blir ordrebekreftelsesoppgaven vanskelig. Hvis du vil finne alternativer som kan forskyve tilgjengelighets- og leveringsproblemer slik at kundens ønskede dato kan oppfylles, eller hvis du vil gi kundene en leveringsløsning som de kan godta og stole på, kan det hende at ordrebehandleren må åpne flere skjemaer, som hver bare gir et delsett av den nødvendige informasjonen. Mer spesifikt viser ett skjema lagerbeholdningen på tvers av områder, et annet skjema viser lagerbeholdningen i den konserninterne innstillingen, et tredje skjema lar brukere beregne den tidligste tilgjengelige datoen for ett område / én variant om gangen, og et fjerde skjema viser forsyningsordrer. Derfor føler ikke brukere seg sikre på at de har vurdert alle de relevante alternativene i stedet for å bare velge en umiddelbar, men ikke optimal løsning. Brukere føler seg heller ikke effektive fordi mange avbrudd oppstår under ordrebekreftelsesflyten når de åpner og lukker flere sider og kombinerer innsikter og alternativer.</td>
<td>Basert på eksisterende algoritmer for leveringsdatoberegning viser siden <strong>Leveringsalternativer</strong> en ny brukeropplevelse for ordrebekreftelse:
<ul>
<li>Den konsoliderer relevant informasjon fra flere skjemaer på ett område.</li>
<li>Den har "ferdiglagede" alternative leveringpakker, for eksempel en kombinasjon av område/lager/variant/transportmodus basert på vilkåret raskeste levering (tidligste tilgjengelige dato), som brukeren kan velge blant.</li>
<li>Den lar brukeren velge alternativer fra simuleringsgrensesnittet og overføre dem til salgsordrelinjen.</li>
</ul></td>
<td>Firmaer som streber mot å gi høy kundeservice samtidig som de forplikter seg til en beholdningsoptimaliseringsstrategi, må kunne garantere ordrepålitelighet og konkurransedyktige vilkår. Kundenes egne virksomheter krever tross alt at produktene er tilgjengelige innen tidsfristen. <strong>Leveringsalternativer</strong>-oppgavesiden gjør ordrebekreftelsesoppgaven raskere, enklere og mer systematisk ved å identifisere og anbefale de beste alternative ordreleveringsdatoene på ett interaktivt sted.</td>
</tr>
</tbody>
</table>

## <a name="service-management"></a>Servicestyring
Ingen nye funksjoner er lagt til.

## <a name="transportation-management"></a>Transportstyring
Ingen nye funksjoner er lagt til.

## <a name="travel-and-expense"></a>Reiseregninger
Ingen nye funksjoner er lagt til.

## <a name="warehouse-management"></a>Lagerstyring
|                                                                       |                                                                                                                                                                                                              |                                                                                                                                                               |                                                                                                                                                                                      |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hva kan du gjøre?**                                                  | **Dynamics AX 2012**                                                                                                                                                                                         | **Dynamics AX 7.0**                                                                                                                                           | **Hvorfor er dette viktig?**                                                                                                                                                           |
| Laste ned, installere og konfigurere portalen for lagermobilenheter. | Du kan laste ned, installere og konfigurere portalen under installasjonen av Microsoft Dynamics AX via et standardoppsett. Det er utformet for selvdrevet lokal distribusjon og konfigurasjon. | Du kan laste ned et frittstående installasjonsprogram via et menyelement i Lagerstyring. Det er utformet for selvdrevet lokal distribusjon og konfigurasjon. | Når du aktiverer oppsett av funksjonen for mobilenhet, må du installere og konfigurere portalen for lagermobilenheter lokalt og opprette en tilkobling til Dynamics AX i skyen. |



<a name="see-also"></a>Se også
--------

[Hva er nytt eller endret?](whats-new-changed.md)

[Nye oppgaveveiledninger tilgjengelige (februar 2016)](new-task-guides-available-february-2016.md)




