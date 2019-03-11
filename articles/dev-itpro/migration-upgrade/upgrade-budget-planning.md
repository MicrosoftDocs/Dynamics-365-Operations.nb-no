---
title: Oppgradere budsjettplanlegging
description: Det er store forskjeller i budsjettplanlegging mellom Microsoft Dynamics AX 2012 og Microsoft Dynamics 365 for Finance and Operations. Noen funksjoner ble ikke oppgradert og krever derfor ny konfigurasjon. Dette emnet beskriver hva som må konfigureres på nytt og beskriver også nye funksjoner som må vurderes etter at oppgraderingen er fullført.
author: ryansandness
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.custom: 272923
ms.assetid: 17cdfe74-bdfd-466a-9bdd-c12583f250c7
ms.search.region: Global
ms.author: ryansand
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 3d57419ca5c59be185c87b869302b41bef05a3c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "342966"
---
# <a name="upgrade-budget-planning"></a>Oppgradere budsjettplanlegging

[!include [banner](../includes/banner.md)]

Det er store forskjeller i budsjettplanlegging mellom Microsoft Dynamics AX 2012 og Microsoft Dynamics 365 for Finance and Operations. Noen funksjoner ble ikke oppgradert og krever derfor ny konfigurasjon. Dette emnet beskriver hva som må konfigureres på nytt og beskriver også nye funksjoner som må vurderes etter at oppgraderingen er fullført.  

Budsjettplanlegging i Microsoft Dynamics 365 for Finance and Operations har mange forbedringer som ikke var tilgjengelige i Microsoft Dynamics AX 2012. Dette emnet beskriver endringene som må utføres av kunder som oppgraderer. Det beskriver også de nye funksjonene som må vurderes under oppgraderingen. På grunn av omfanget av endringene, kan ikke eventuelle eksisterende budsjettplaner åpnes før det gjøres endringer som er beskrevet i dette emnet. Rapporter skal imidlertid fortsatt fungere og krever ikke flere endringer.

## <a name="overview-of-changes"></a>Oversikt over endringer
Mange store endringer er gjort i budsjettering for Finande and Operations. Disse endringene er ment å gjøre budsjettplanleggingen enklere å konfigurere og bruke på nytt, for å redusere årlig vedlikehold og oppsett. Følgende områder i AX 2012 finnes ikke lenger i Finance and Operations:

-   Budsjettplanmaler (budsjettplanleggingskonfigurasjon)
-   Budsjettplanmapper (budsjettplanleggingskonfigurasjon)
-   Scenariobegrensninger (budsjettplanleggingskonfigurasjon)
-   Maler for Stadieregler og maler for budsjettplanlegging (budsjettplanleggingsprosess)
-   Matrisefelt for regnearkmaler
-   Veiviser for Microsoft Excel-mal for budsjettplan

Enkelte nye konsepter kan ikke oppgraderes direkte fra den tidligere funksjonaliteten. Derfor må du fullføre en ny konfigurasjon for å ta hensyn til disse nye begrepene. Avsnittene nedenfor beskriver begrepene som har erstattet elementene i listen ovenfor.

### <a name="columns"></a>Kolonner

Kolonner er et nytt begrep som erstatter deler av Excel-malen og også matrisefelt. Kolonner kan representere periode, måned, kvartal, år eller all tid. Tidsreferansen er dynamisk. Den peker til en relativ periode eller år med hensyn til budsjettprosessen. Kolonnen **Januar foregående år** refererer for eksempel til regnskapsperiode 1 for år -1. En kolonne er spesifikk for et budsjettplanscenario, for eksempel faktiske eller budsjettforespørsler.

### <a name="layouts"></a>Oppsett

Oppsett er et nytt begrep som erstatter Excel-malen. Oppsett inneholder kolonnene som definerer hvilke budsjett eller faktiske data og perioder som skal vises. Oppsett deles også mellom klienten og Excel-tillegget. Når du angir eller viser data i Finance and Operations-klienten, er brukeropplevelsen derfor bedre enn brukeropplevelsen i AX 2012. Hvis du vil skrive inn data i Finance and Operations-klienten, er du ikke lenger begrenset til visning og registrering av ett enkelt scenario i en transaksjonsvisning. I stedet lar en sammenligning deg enkelt vise og angi beløp for flere perioder og or kontoer samtidig. Oppsett kan også defineres, slik at du kan angi og Vis valuta, kommentarer og andre valgfrie data. Oppsett lar deg også definere hvilke finansdimensjoner og dimensjonsbeskrivelser som skal vises. Oppsett omfatter også scenariebegrensninger for å definere hvilke kolonner i en mal som kan redigeres, og hvilke kolonner som skal være tilgjengelige i Excel. Når du har definert et oppsett, genereres en mal for den. Denne malen oppretter igjen den tilsvarende Excel-malen. Deretter kan du redigere Excel-malen for å legge til flere formler og formatering og deretter laste den opp på nytt. Oppsett tilordnes deretter til hver stadieregel på siden **Budsjettplanleggingsprosess**. Derfor erstatter oppsettene maler som var tilordnet og brukes på lignende måte.

### <a name="budget-planning-processes"></a>Budsjettplanleggingsprosesser

Budsjettplanleggingsprosesser er stort sett de samme som i AX 2012. De viktigste endringene er erstatning av maler med oppsett. Hvis prosesser tidligere ble fullført i AX 2012, oppdateres prosessene til statusen pågår, slik at du kan utføre endringer. Du må tilordne oppsett du trenger for hver stadieregel for å angi hvilke scenarier og tidsperioder som vises når planen åpnes i klienten. Oppsettene bestemmer også hvilken Excel-mal som åpnes utenfor Dynamic 365 for Finance and Operations, slik at du kan vise budsjettet. **Standard kontostruktur** er et nytt obligatorisk felt for budsjettplanleggingsprosessen. Tilordne den primære kontostrukturen som skal brukes for budsjettering, for hver budsjettplanleggingsprosess.

### <a name="attachments"></a>Vedlegg

I AX 2012 ble justeringsdokumenter lagret i en vedleggsmappe. Ingen tidligere justeringsdokumenter blir oppgradert. Justeringsdokumenter lagres nå i databasen. Hvis denne informasjonen skal lagres i den oppgraderte versjonen, kan du laste opp de endelige justeringsdokumentene for hver plan som et vedlegg, ved hjelp av **Justering** -knappen i handlingsruten. I AX 2012 ble Excel-regneark for hver budsjettplanen opprettet basert på malen. I Finance and Operations åpner alle planer en kopi av oppsettet. Imidlertid blir ingen endringer i Excel-filen lagret. Formler eller støtteinformasjon som ble brukt per plan, må legges til via kommentarer, et justeringsdokumentet eller en annen tilleggsprosess.

## <a name="configuring-an-upgraded-environment-from-ax-2012"></a>Konfigurere et oppgradert miljø fra AX 2012
I eksemplet nedenfor brukes en oppgradert budsjettprosess fra AX 2012-demodata for å finne ut hvordan du konfigurerer det oppgraderte systemet. Standard konfigurasjonsdata for kolonner ble opprettet for å bidra med oppgraderingsprosessen. Du kan oppdatere eller slette disse standarddataene hvis de ikke oppfyller dine krav til konfigurasjon. **Obs!** De er nye obligatoriske felt som ikke angis i systemet. Hvis du står fast på en side, for eksempel siden **Budsjettplanleggingskonfigurasjon**, og kan ikke forlate den, kan du lukke nettleseren og åpne den til en annen side for å registrere informasjon i riktig rekkefølge. Det er obligatoriske felt som ikke er angitt ennå. Derfor kan det oppstå problemer før alt er konfigurert og alle nødvendige felt er angitt. Dette emnet beskriver hvordan du angir disse feltene etter behov. Her er noen av disse obligatoriske feltene:

-   Siden **Budsjettplanleggingsprosess**: Feltet **Standard kontostruktur**
-   Siden **Budsjettplanleggingsprosess**: **Oppsett**-feltet i hurtigfanen **Stadiumsregler og oppsett for budsjettplanlegging**

### <a name="define-columns-and-layouts"></a>Definere kolonner og oppsett

1. På siden **Budsjettplanleggingsprosess**, klikk **Kolonner**-kategorien. Som del av oppgraderingen vil nye kolonner automatisk opprettes basert på dine budsjettplanlinjer. Kolonner bruker nå dynamiske datoer, der klokkeslett og år forskyves fra regnskapsåret som er definert i budsjettplanleggingsprosessen. **Obs!** Av ytelseshensyn under oppgraderingen antas det at alle budsjettsykluser representerer kalenderår, ikke regnskapsår. Hvis du bruker regnskapsår, må du redigere for riktig tilordning av kolonner til regnskapsåret. Disse elementene finnes for eksempel i AX 2012:
   -   Budsjettplanscenarioer: Faktisk, Grunnverdi, Budsjettforespørsel, Budsjett godkjent
   -   Budsjettplanlinjer for alle scenarier i 2017 og faktiske data for både 2017 og 2016

   Følgende kolonner vil bli opprettet i Finance and Operations:

   | Kolonnenavn    | Budsjettplanscenario | Tidsperiode for kolonne | Årsforskyvning |
   |----------------|----------------------|--------------------|-------------|
   | Jan scenario 1 | Faktiske beløp              | 1                  | 0           |
   | Jan scenario 2 | Grunnlinje             | 1                  | 0           |
   | Jan scenario 3 | Budsjettforespørsel       | 1                  | 0           |
   | Jan scenario 4 | Budsjett godkjent      | 1                  | 0           |
   | Jan scenario 5 | Faktiske beløp              | 1                  | -1          |
   | Feb scenario 1 | Faktiske beløp              | 1                  | 0           |
   | ...            | ...                  | ...                | ...         |

   I dette eksemplet opprettes en kolonne med navnet **Jan scenario 1** for de siste transaksjonsdataene for budsjettplanen som finnes der det finnes transaksjoner i januar. Det opprettes en lignende kolonne for hvert scenario som inneholder data. Når det finnes kolonner for alle perioder i dette året, opprettes det kolonner for tidligere år.
2. Endre kolonnenavn, beskrivelser og eventuelt andre detaljer, enten manuelt i klienten eller ved å gjøre masseoppdateringer ved hjelp av Excel-tillegget som peker til dataenheten for budsjettplankolonner. Filtre som tidligere er angitt for matrisefelt er nå angitt i kolonnene.
3. Opprett et nytt budsjettplanoppsett. Et oppsett peker til flere kolonner for å definere visningen som vises i Excel og klienten. Oppsettet krever først at du angir en finansdimensjon angitt for å fastslå hvilke finansdimensjoner som kan angis. Når du angir dimensjonssettet, klikker du på **Beskrivelse** for å velge dimensjonsbeskrivelser som skal tas med i oppsettet.
4. I hurtigfanen **Oppsettelementer** klikker du på **Legg til** for å legge til metadata for hver rad, for eksempel en valuta, en merknad eller en budsjettklasse, som bestemmer omsetnings- kontra utgiftsrader. Deretter legger du til kolonner for tidsperioden, og scenarier som gjelder denne budsjettsyklusen og dette stadiet. Du kan gjøre disse endringene manuelt i klienten eller ved hjelp av Excel-tillegget som peker til dataenheten for oppsettelementer for budsjettplanen.
5. For hvert element i oppsettet velger du om kolonnen kan redigeres og om kolonnen også skal vises i Excel-arbeidsboken for dette oppsettet. **Obs!** Du bør vurdere et oppsett med tolv månedlige kolonner for alle budsjettplanscenarioer for denne prosessen for våre historiske planer.

### <a name="update-budget-planning-processes-to-use-the-appropriate-layout-for-each-budget-stage"></a>Oppdatere budsjettplanleggingsprosesser til å bruke det passende oppsettet for hver budsjettstadium

1.  På siden **Budsjettplanleggingsprosess** velger du prosessen som skal konfigureres.
2.  Klikk på **Rediger** i handlingsruten.
3.  Angi standard kontostruktur for denne budsjettprosessen. **Standard kontostruktur** er et nytt obligatorisk felt som må angis.
4.  I hurtigfanen **Stadiumsregler og oppsett for budsjettplanlegging** i **Oppsett**-feltet, velger du et oppsett som tidligere ble konfigurert og som passer for dette stadiet.
5.  Fortsett å velge samme eller andre oppsett for de ulike budsjettplanleggingsstadiene, og lagre deretter endringene.

## <a name="additional-features-to-consider-in-your-budgeting-process"></a>Flere funksjoner som bør vurderes i budsjetteringsprosessen
### <a name="budget-planning-workspace"></a>Arbeidsområde for budsjettplanlegging

Dette arbeidsområdet er utformet for både budsjetteier og individuelle budsjettbidragsytere. Det inneholder koblinger til budsjettdokumenter som krever din oppmerksomhet. Det har også rapporter og nøkkelytelsesindikatorer (KPI-er) for budsjettprosessen. Budsjettadministrator kan angi gjeldende budsjettplanleggingsprosess for alle brukere på siden **Budsjetteringsparametere**. I kategorien **Innstillinger for arbeidsområde** inneholder hurtigfanen **Budsjettplanlegging** et felt der du kan velge budsjettplanleggingsprosessen.

### <a name="alternate-layouts"></a>Alternative oppsett

Alternative oppsett er en ny funksjon som lar deg vise planer i ulike oppsett. Ett eller flere oppsett kan angis som alternativer. Du kan deretter vise en budsjettplan i et månedlig eller kvartalsvis oppsett. Du definerer alternative oppsett i hurtigfanen **Stadiumsregler og oppsett for budsjettplanlegging** på siden **Budsjettplanleggingsprosess**.

### <a name="budget-milestones"></a>Milepæler for budsjett

Som en del av budsjettprosessen er det viktig at du forstår viktige datoer og tidsfrister. Du kan nå konfigurere datoer slik at de har beskrivelser. Budsjettbrukerne ser disse beskrivelsene når de åpner budsjetter for å redigere eller vise alt som er tilordnet dem.

### <a name="copy-from-budget-plan-allocation"></a>Kopiere fra budsjettplantildeling

En ny tildelingsmetode lar deg distribuere fra en overordnet plan til en underordnet plan uten å måtte gå gjennom en mellomnivå i hierarkiet. Denne metoden er spesielt nyttig for kunder som tidligere har opprettet finansdimensjon for budsjettdistribusjon og godkjenninger.

### <a name="generating-budget-plans-from-new-budget-sources"></a>Generere budsjettplaner fra nye budsjettkilder

Alternativene nedenfor ble lagt til som periodisk prosesser. Disse alternativene lar deg generere en budsjettplan ved hjelp av eksisterende data fra en annen modul som startpunkt:

-   Generere budsjettplan fra behovsprognose
-   Generere budsjettplan fra forsyningsprognose
-   Generere budsjettplan fra prosjekt
-   Generere budsjettplan fra budsjettregister

### <a name="more-complete-tracking-of-amounts"></a>Mer fullstendig sporing av beløp

I AX 2012 hadde budsjettplanlegging et beløp for én plan som ble lagret for hver verdi. I Finance and Operations er datamodellen utvidet. Det er nå beløp for regnskapsvaluta, transaksjonsvaluta og rapporteringsvaluta for hver verdi. Under oppgraderingen fylles disse nye kolonnene ut automatisk for eksisterende data.

### <a name="do-not-convert-currency-in-aggregation"></a>Ikke konverter valuta i aggregering

Når en underordnet plan aggregeres til et overordnet nivå, blir beløpene vanligvis automatisk konvertert fra transaksjonsvalutaen til regnskapsvalutaen for organisasjonen. Når du setter alternativt **Ikke konverter valuta i aggregering** til **Nei**, forblir de aggregerte beløpene i den opprinnelige valutaen. Dette alternativet gir derfor for mer nøyaktige justeringer som påvirkes av fluktueringer i vekslingskurs.

### <a name="looking-back-from-a-budget-plan-to-other-modules-that-contributed-to-the-budget"></a>Se tilbake fra en budsjettplan til andre moduler som bidrar til budsjettet

Budsjettplaner kan genereres fra behov, forsyningsprognoser, prosjekt og andre områder. Forespørselen Budsjettplaner etter dimensjonssett inneholder flere alternativer som lar deg kjøre spørringer for å identifisere dataene som var kilden til budsjettplanen.

### <a name="overwrite-or-append-to-plan-for-allocation-schedules"></a>Overskrive eller tilføye i plan for tildelingsplaner

Hvis det finnes flere kilder for beløpene som må distribueres, kan du angi at beløpene skal være additive. I så fall overskriver ikke beløpene eventuelle eksisterende beløp. I stedet legges de til de eksisterende beløpene.

### <a name="default-financial-dimension-set-for-budget-planning-configuration"></a>Standard finansdimensjon som er angitt for budsjettplanleggingskonfigurasjon

Siden **Budsjettplanleggingskonfigurasjon** inneholder nå et felt der du kan angi standard finansdimensjonssett. Selv om dette feltet er et valgfritt felt, kan det være nødvendig for enkelte forespørsler. Det kan være nødvendig hvis du vil gruppere eller filtrere rapportgruppering etter dimensjonssett.

### <a name="data-entities"></a>Dataenheter

Flere dataenheter er lagt til for å muliggjøre rask implementering av budsjettplanlegging. Enhetene lar deg også gjøre mange endringer til Excel. Du trenger derfor ikke opprette ett element om gangen i klienten. Her er en liste over nye dataoppføringer:

-   Entitynavn
-   Budsjettparametere
-   Budsjettplanparameter
-   Budsjettplanscenarioer
-   Stadier for budsjettplan
-   Arbeidsflytstadium for budsjettplan
-   Fordelingsplaner for budsjettplan
-   Fordelinger for budsjettplanstadium
-   Budsjettplanprioriteter
-   Budsjettplankolonner
-   Elementer for budsjettplanoppsett




