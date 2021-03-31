---
title: Integrering av budsjettplanlegging med andre moduler
description: Budsjettplaner kan genereres fra flere ulike ressurser. De grunnleggende elementene i den periodiske prosessen er den samme for alle ressurser.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.custom: 64443
ms.assetid: f9a94db5-906c-404a-9ca5-91528d67c490
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d94e95c921d8237d8f69f793dbf48f1f40632964
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210343"
---
# <a name="budget-planning-integration-with-other-modules"></a>Integrering av budsjettplanlegging med andre moduler

[!include [banner](../includes/banner.md)]

 Budsjettplaner kan genereres fra flere, ulike ressurser. De grunnleggende elementene i den periodiske prosessen er den samme for alle ressurser. 



<a name="periodic-processes-for-generating-budget-plans"></a>Periodiske prosesser for å generere budsjettplaner
----------------------------------------------

Budsjettplaner kan genereres fra følgende ressurser:

-   Økonomimodultransaksjoner
-   Anleggsmidler
-   Prognosestillinger
-   Prosjektprognoser
-   Forsyningsprognoser
-   Behovsprognoser
-   Budsjettregisteroppføringer
-   Andre budsjettplaner

De grunnleggende elementene i den periodiske prosessen er den samme for alle prosesser. Kategorier lar deg definere kilden til dataene, målattributter (budsjettplanen) og alternativer for å kjøre prosessen i bakgrunnen som en partiprosess. Senere deler i denne artikkelen beskriver varer som kanskje ikke er synlige i hver prosess.

### <a name="actions"></a>Handlinger

Det finnes tre handlinger for hver generasjonsprosess:

-   **Opprett en ny budsjettplan** oppretter en ny plan som har attributtene som er valgt i **Mål**-delen. Disse attributtene trenger ikke å være unike. To planer kan derfor ha samme navn og andre verdier.
-   **Erstatt eksisterende budsjettplanscenario** sletter alle data i målbudsjettplanen i det valgte budsjettplanscenarioet og oppretter nye linjer som bruker de valgte kildedataene.
-   **Oppdater eksisterende budsjettplanscenario, og tilføy nye data** oppdaterer eksisterende linjer i målplanen som samsvarer med kildelinjene, og legger til nye linjer for nye data. Samsvaret er basert på finanskontoen, dato, budsjettklasse og diverse andre felt. Når du for eksempel genererer budsjettplaner fra prognosestillinger, er stillingsnummeret et viktig felt. Alle linjer som har et stillingsnummer som samsvarer med kildestillingsnummeret, erstattes med de nye linjene fra kilden.

### <a name="source"></a>Kilde

For alle prosesser kan du bruke **Kilde**-kategorien til å filtrere data ved hjelp av **Filter**-knappen. Som standard legges bestemte felt til i filteret for hver prosess. For prosessen **Generer budsjettplan fra økonomimodul** er for eksempel kategoriene **Finanskonto** og **Hovedkonto** tilgjengelige, og de vises på siden for generering. Alle felt som du legger til i filteret, legges også til på siden, sammen med eventuelle kriterier du legger til.

### <a name="target"></a>Mål

Alternativet **Historisk** i kategorien **Mål** lar deg bruke datoene fra kildedataene som den gyldige datoen i budsjettplanen. Vanligvis må den gyldige datoen må være innenfor planens budsjettsyklus. Når du angir alternativet **Historisk** som **Ja**, brukes datoen for kilden (også året), slik at du kan bruke tidligere data som basis for sammenligning. Du kan ikke endre historiske data i budsjettplanen, og planen settes til en godkjent arbeidsflytstatus. Du kan imidlertid tilbakestille statusen hvis andre scenarier i planen krever endringer.

Feltet **Aggreger total etter** øverst på siden bestemmer også datoen som skal brukes. Dette feltet summerer beløpene, og angir valgfritt den gyldige datoen til den første dagen i regnskapsåret eller regnskapsperioden. 

Mange av feltene i kategorien <strong>Mål</strong> blir redigerbare eller skrivebeskyttet, avhengig av handlingen du har valgt. Når du endrer fra å opprette en ny budsjettplan for å oppdatere en eksisterende plan, blir feltet **Navn på budsjettplan** utilgjengelig, og feltene som er knyttet til å velge en eksisterende plan, blir tilgjengelige. I både kategoriene **Mål** og **Kilde** er feltet **Finans** alltid utilgjengelig, fordi verdien bestemmes av den valgte budsjettplanleggingsprosessen. 

Feltet **Budsjettklasse** lar deg angi budsjettplanlinjene som utgiftstransaksjoner eller inntektstransaksjoner. Vanligvis er inntektstransaksjoner krediteringer til en finanskonto og lagres derfor som negative beløp. Vanligvis vises disse transaksjonene også som negative beløp i budsjettplanen. Ved å sette inn budsjettklassen som et felt i planoppsettet, kan du imidlertid aktivere at inntekter skal vises som positive beløp.

### <a name="generation-rules"></a>Regler for generering

Tre felt tilbyr ekstra funksjonalitet: **Faktor**, **Minimum** og **Avrundings** **regel**. 

Verdien i feltet **Faktor** multipliseres med kildebeløpet for å angi beløpet i budsjettplanen. Du kan deretter gjøre justeringer når du oppretter budsjettplanlinjer. Du kan for eksempel angi **1,03** for en 3-prosents økning. Faktoren må være et positivt tall. 

**Minimum** feltet lar deg angi terskelbeløpet for å opprette en budsjettplanlinje. Hvis kildebeløpet er mindre enn dette tallet, blir ikke budsjettplanlinjen opprettet. En verdi på **0,00** tillater alle beløp, men begrenser ikke linjer til positive beløp. (Ingen verdi begrenser linjer til positive beløp. Negative beløp er alltid inkludert, og representerer vanligvis kreditposter.)

Feltet **Avrundingsregel** lar deg angi presisjonen for budsjettplanlinjene som er opprettet. Du kan runde av beløp til den nærmeste 1,00 10,00, 100,00 og så videre, i valuta.

## <a name="notes-for-specific-processes"></a>Merknader for bestemte prosesser
### <a name="generate-budget-plan-from-general-ledger"></a>Generer budsjettplan fra økonomimodul

Når du oppretter en budsjettplan fra økonomimoduldata, må du angi feltet **Aggreger total etter** som **Regnskapsår** hvis alternativet **Historisk** er satt til **Nei**. Periodene og datoene i kilden samsvarer kanskje ikke med periodene i datoer i målet. Fordi prosessen ikke har noen pålitelig måte å tilordne disse verdiene på må du begrense prosessen til først i året. 

I målet settes feltet **Budsjettklasse** til enten **Utgift** eller **Omsetning**. Denne innstillingen brukes til å velge **Budsjettype** attributtet for linjer som opprettes, når hovedkontoen på en linje som ikke er av typen **Omsetning** eller **Utgift**.

### <a name="generate-budget-plan-from-fixed-assets"></a>Generer budsjettplan fra anleggsmidler

Prosessen **Generer budsjettplan fra anleggsmidler** har ikke noe alternativ for å aggregere etter periode eller dag. Det finnes heller ingen alternativer for å angi planen som historisk. Du kan bruke denne periodiske prosessen til å ta med forventede transaksjoner for anleggsmidler i budsjettplanleggingen.

### <a name="generate-budget-plan-from-forecast-positions"></a>Generer budsjettplanlinjer fra prognosestillinger

Prosessen **Generer budsjettplan fra prognosestillinger** tilordner kildeprognosestillingen til budsjettplanlinjen. Du kan vise stillingen ved å legge til prognosestillingen som en rad i budsjettplanoppsettet eller bruke forespørselen **Budsjettplanlinjer**. Hvis du ikke vil at prognosestillingen skal tilordnes til budsjettplanlinjer, setter du alternativet **Inkluder stilling i budsjettplanlinje** til **Nei**.

Linjer i budsjettplanen samles etter finanskonto og posisjon. Du kan imidlertid utelate posisjonsnummeret, slik at linjene bare samles etter finanskonto. På kategorien **Mål** angir du **Inkluder stilling i budsjettplan** som **Nei**.

I feltet **FTE-scenario for budsjettplan** kan du velge et scenario for å inkludere antall fulltidsekvivalenter (heltidsansatte) i budsjettplanen. Dette feltet er begrenset til antallstypescenarier som er inkludert i oppsettet for målbudsjettplanen. Hvis du velger et FTE-scenario, må du også velge en FTE-hovedkonto. Denne kontoen brukes til å opprette budsjettplanlinjene for antall. 

Budsjettplanleggingsprosessen og budsjettplanscenarioet som er valgt i kilden, angir budsjettplanleggingsprosessen og budsjettplanscenarioet for målscenarioet. Fordi disse attributtene er tilordnet til prognosestillinger må de være samsvar med budsjettplanen. Disse attributtene kan derfor ikke endres på målet.

### <a name="generate-budget-plan-from-project-forecasts"></a>Generer budsjettplan fra prosjektprognoser

Prosessen **Generer budsjettplan fra prosjektprognoser** har som prosessen **Generer budsjettplan fra prognosestillinger** et alternativ for å inkludere prosjektantall (timer, utgifter og varer) i et scenario for antall. De to prosessene har også lignende filtre for kolonnene i budsjettplanoppsettet. 

I kategorien **Kilde** bestemmer tre alternativer i delen **Inkluder oppgave** hvilke budsjettplanlinjer som skal opprettes. Disse alternativene er de samme som alternativene som er tilgjengelige når du oppretter budsjettregisteroppføringer direkte fra prosjektprognoser. Angi alternativet **Resultat** som **Ja** for å opprette linjer for kostnader og inntekter. Angi alternativet **VIA** som **Ja** for å opprette poster for varer i arbeid. Angi alternativet **Lønnsfordeling** som **Ja** for å opprette linjer for motkontoer for lønn for timetransaksjoner. 

Det finnes intet **Budsjettklasse**-felt, fordi budsjettklassen (**Utgift** eller **Omsetning**) bestemmes av kilden. 

Du kan bruke prosjektbudsjetter som en kilde ved å velge prognosemodellen som inneholder prosjektbudsjettbeløpene. Husk at prosjektbudsjetter oppretter prosjektprognoseposter når de blir godkjent.

For å velge bare kostnader eller omsetning for budsjettplanlinjer bruker du bruke filteret for å velge <strong>Budsjettoppdateringer: beløpstype = kostnad</strong>. For å velge bare én type prognose bruker du filteret til å velge <strong>Budsjettoppdateringer: transaksjonstype = *xxx</strong>*. 

Bare én prognosemodell kan brukes til å generere et budsjettplanscenario. Hvis du kjører prosessen for én prognosemodell og deretter foretar en oppdatering og prøver å angi en annen modell, overskrives den første modellen hvis den bruker samme prosjekt- og finanskontoer. Hvis du vil generere et budsjettplanscenario fra mer enn én prognosemodell, genererer du til forskjellige budsjettplanscenarioer og bruker tildelingsalternativer for å legge dem til sammen i et annet scenario. 

Prosessen **Generer budsjettplan fra prosjektprognoser** tilordner også kildeprosjektet til budsjettplanlinjen.

### <a name="generate-budget-plan-from-supply-forecast"></a>Generer budsjettplan fra forsyningsprognose

Kildefilteralternativene i prosessen **Generer budsjettplan fra forsyningsprognose** er modellert etter alternativer i funksjonen **Overfør innkjøpsbudsjett til finans** på grunn av likheter mellom prosessen og funksjonen.

### <a name="generate-budget-plan-from-demand-forecast"></a>Generer budsjettplan fra behovsprognose

For prosessen **Generer budsjettplan fra behovsprognose** kan du angi alternativet **Salgsordre** som **Ja** for å generere inntektslinjer i budsjettplanen, angi **Forbruk** som **Ja** for å opprette utgiftslinjer, eller sette begge alternativene til **Ja**.

### <a name="generate-budget-plan-from-budget-register-entries"></a>Generer budsjettplan fra budsjettregisteroppføringer

For prosessen **Generer budsjettplan fra budsjettregisteroppføringer** må kilden angi en undermodell, én budsjettkode og ett oppføringsnummer. Du kan altså opprette budsjettplanlinjer for bare én budsjettregisteroppføring om gangen. Du kan bruke flere oppføringer i samme budsjettplanen ved å kjøre prosessen én gang for hver kildeoppføring.

### <a name="generate-budget-plan-from-budget-plan"></a>Generer budsjettplan fra budsjettplan

For prosessen **Generer budsjettplan fra budsjettplan** lar et ekstra sett med alternativer i kategorien **Mål** deg tilordne nye finansdimensjoner. Hvis en finansdimensjon er valgt, vil denne verdien brukes for alle budsjettplanlinjene. Derfor kan du bruke én budsjettplan som grunnlag for andre budsjettplaner, men kan også tilordne, for eksempel en annen avdeling eller et annet kostsenter til de nye budsjettplanene.

## <a name="looking-back-from-the-budget-plan"></a>Se tilbake fra budsjettplanen
### <a name="budget-plans-by-dimension-set-inquiry"></a>Forespørsel om budsjettplaner etter dimensjonssett

Forespørselen **Budsjettplaner etter dimensjonssett** inneholder flere alternativer som lar deg kjøre en spørring for å identifisere kilden til budsjettplandataene. 

Velg en linje, og klikk knappen **Budsjettplanlinjer** for å kjøre spørringen **Budsjettplanlinjer**. Resultatene filtreres for dimensjonsverdiene for den valgte linjen. Deretter kan du bruke flere parametere. 

Bruk knappene **Forsyningsprognose** og **Behovsprognose** for å kjøre disse spørringene. I begge tilfeller søker spørringen etter prognoselinjene som kan ha opprettet budsjettplanlinjene. 

Flere rapporter som er tilgjengelige, inkluderer rapporten **Prognosestillinger etter budsjettplan**. Denne rapporten er spesielt nyttig når du vil finne ut om en stilling er riktig fordelt til budsjettplaner.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]