---
title: Refunderingsbehandling i telefonsentre
description: Denne artikkelen beskriver hvordan betalingsrefusjoner genereres via telefonsentre når returer opprettes, eller når ordrer eller ordrelinjer annulleres.
author: hhainesms
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 330674a31dc59e99ffedb82d0896c64214562eb3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880120"
---
# <a name="refund-payment-processing-in-call-centers"></a>Refunderingsbehandling i telefonsentre

Denne artikkelen beskriver hvordan betalingsrefusjoner genereres via telefonsentre når returer opprettes, eller når ordrer eller ordrelinjer annulleres.

En bruker som oppretter en returordre for en kunde som telefonsenterbruker i Microsoft Dynamics 365 Commerce Headquarters, bruker siden **Returordre** til å opprette det første autorisasjonsreturnummeret (RMA). RMA definerer produktene som kunden vil returnere eller bytte, og det oppretter en koblet retursalgsordre som har ordretypen **Returordre**. Denne koblede returnerte ordren brukes til å spore posteringen av det returnerte lageret og eventuelle kreditnotaer eller betalingsrefusjoner som er postert.

Hvis alternativet **Aktiver ordreklarering** er satt til **Ja** for telefonsenterkanalen, må telefonsenterbrukeren som oppretter produksjonsreturen, kjøre arbeidsflyten for fullføring av ordren ved å velge **Fullfør** på **Returordre**-siden. Funksjonen **Fullført** gir et beregnet retursammendrag som viser det forfalte refunderingsbeløpet. Når den er riktig konfigurert, oppretter den dessuten en refunderingsbetalingslinje mot returordren når den er riktig konfigurert.

Telefonsenterlogikken bestemmer betalingsmåten for betalingslinjen for refusjon basert på betalingsmåten som ble brukt for den opprinnelige ordren. Hvis returordren som opprettes, ikke er knyttet til en original ordre, brukes det en standard betalingsmåte fra en systemparameter.

## <a name="how-a-call-center-determines-which-payment-method-to-apply-to-a-return-order"></a>Hvordan et telefonsenter avgjør hvilken betalingsmåte som skal brukes på en returordre

Telefonsenteret bruker betalingsmåten til den opprinnelige ordren for å bestemme betalingsmåten som skal brukes på en returordre. Her ser du hvordan denne prosessen fungerer for følgende opprinnelige betalingsmåter:

- **Vanlig** (kontant) eller **Sjekk** – Når en returordre som opprettes, refererer til en original ordre som ble betalt ved hjelp av den vanlig (kontant) betalingstype eller sjekkbetalingstypen, refererer samtalesenterprogrammet til konfigurasjoner på siden **Refunderingsmetoder for telefonsenter**. På denne siden kan organisasjoner definere, i ordrevalutaen, hvordan refusjoner utstedes til kunder for ordrer som opprinnelig ble betalt ved hjelp av vanlig betalingstype eller sjekk. Ved hjelp av siden **Refunderingsmetoder for telefonsenter** kan også organisasjoner velge om det skal sendes en systemgenerert refunderingskontroll til kunden. I disse scenarioene refererer samtalesenterlogikken til valutaen til returordren, og deretter brukes verdien for **betalingsmåte for detaljhandel** for den valutaen for å opprette en refunderingsbetalingslinje på retursalgsordren. Senere kobles en kundebetalingsjournal for kunder (AR) som bruker den tilordnede AR-betalingsmetoden, til valutaen.

    Illustrasjonen nedenfor viser konfigurasjonen for et scenario der en kunde returnerer produkter fra en salgsordre som er koblet til valutaen USD, og som opprinnelig ble betalt for ved hjelp av betalingstypen vanlig eller sjekk. I dette scenariet vil en refusjon bli utstedt til kunden via en systemgenerert refunderingskontroll. AR-betalingsmåten **REF-CHK** er konfigurert som en betalingstype for refundering av sjekk.

    ![Konfigurasjon av tilbakebetalingsmetoder for telefonsenter for opprinnelige betalinger for vanlig betaling og sjekkbetaling.](media/callcenterrefundmethods.png)

    > [!NOTE]
    > Kundekontoer støttes ikke som refunderingsmetode for kontant- eller sjekkbetalinger.

- **Kredittkort** – Når en returordre som opprettes, refererer til original ordre som ble betalt ved hjelp av et kredittkort, bruker samtalesenterlogikken for refusjonsbetalinger samme opprinnelige kredittkort for returordren.
- **Fordelskort** – Når en returordre som opprettes, refererer til en original ordre som ble betalt ved hjelp av et kundefordelskort, bruker samtalesenterlogikken for refusjonsbetalinger refusjonen på samme fordelskort.
- **Gavekort** (internt) – Når en returordre som opprettes, refererer til en opprinnelig ordre som ble betalt ved hjelp av et gavekort som er utstedt fra Dynamics 365 Commerce (intern gavekortfunksjonalitet), bruker samtalesenterlogikken for refusjonsbetalinger refusjonen til det samme opprinnelige gavekortnummeret.
- **Gavekort** (ekstern) – Når en returordre som opprettes, refererer til en original ordre som ble betalt ved hjelp av et eksternt gavekort fra en tredjepart, brukes samtalesenterlogikk for refusjonsbetalinger standard returbetalingsmetode som er definert i kategorien **RMA/retur** på siden **Telefonsenterparametere**.

Hvis betalingstypen for den opprinnelige ordren er ukjent av en hvilken som helst årsak, eller hvis flere betalingsmåter ble brukt til å betale for den opprinnelige ordren, bruker samtalesenterlogikken standard returbetalingsmetode som er definert i kategorien **RMA/retur** på siden **Telefonsenter**.

Illustrasjonen nedenfor viser **Betalingsmåte**-feltet i kategorien **RMA/retur** på siden **Telefonsenterparametere**.

![Betalingsmåte-feltet i kategorien RMA/retur på siden Telefonsenterparametere.](media/callcenterrefundparameters.png)

> [!NOTE]
> Reglene for refunderingsbehandling som beskrevet tidligere, gjelder også for ordrer eller ordrelinjer som en samtalesenterbruker avbryter i Commerce Headquarters. Hvis annullering av en ordre eller bestemte ordrelinjer fører til overbetalinger, blir de samme reglene brukt til å generere refunderingsbetalingslinjer.

En returordre går vanligvis gjennom en standardprosess der lager mottas (eller kasseres), en følgeseddel posteres mot returordren, og deretter kjøres det en fakturaposteringsprosess for retursalgsordren. Retursalgsordren er koblet og systematisk generert som en del av prosessen med å opprette returordren. I vanlige scenarier utstedes ikke betalingsrefusjoner til kunder før fakturaen for retursalgsordren posteres.

### <a name="what-happens-when-an-invoice-is-posted-on-a-return-sales-order"></a>Hva som skjer når en faktura posteres på en retursalgsordre

Følgende scenarioer forklarer hva som skjer når en faktura posteres på en retursalgsordre:

- Hvis refusjonsbetalingen på returordren er for et kredittkort, startes tilleggslogikk når fakturaen posteres. Denne logikken kaller opp betalingsbehandleren for å refundere betaling til kundens kredittkort. Det opprettes også et refunderingskundebetalingsbilag som posteres systematisk mot kundens konto. Denne betalingsjournalen utlignes mot kreditnotabilaget for returordren.
- Hvis refusjonsbetalingen som må utstedes, er for betalingstypen for sjekk, opprettes det et kundebetalingsbilag som bruker AR-betalingsmåten, og det må posteres eller skrives ut manuelt før betalingsbilaget kan posteres mot kundekontoen. Når brukere skal behandle refunderingssjekken, kan de bruke enten siden **Kundebetalingsjournal** i Kunder eller den spesialiserte siden **Behandling av refunderingssjekk** i Retail eller Commerce.
- Hvis refusjonsbetalingen som må utstedes, er for den interne gavekort- eller fordelskortbetalingstypen, opprettes og posteres refunderingsbetalingsbilaget mot kundekontoen når returordren faktureres. Dette faktureringstrinnet legger også til refusjonsbeløpet tilbake til kundens internt sporede gavekortsaldo eller fordelspoengsaldo.
- Hvis en betalingsmåte som bruker **Kunde**-funksjonen (for eksempel en kundekonto), er knyttet til retursalgsordren, blir valideringer av kredittgrensen ignorert når betalingen behandles. Ingen betalingsbilag opprettes eller posteres i denne sammenhengen. Når en kundebetalingstype brukes på en returordre, fungerer kreditnotabilaget som fakturaposteringsprosessen oppretter, som kundekredittbilaget, og angir en refusjon til kundens AR-saldo.

## <a name="advance-credit"></a>Forskuddskreditt

Når en bruker behandler returordrer som en telefonsenterbruker i et telefonsenter der alternativet **Aktiver ordreklarering** er satt til **Ja**, kan det oppstå et unntak til den tidligere beskrevne prosessen for postering av refunderingsbetaling hvis telefonsenterbrukeren som oppretter returordren, setter alternativet **Forskuddskreditt** til **Ja** i kategorien **RMA/retur** på siden **Telefonsenterparametere** . I dette tilfellet skjer betalingsrefusjonen rett etter at returordren er sendt ved hjelp av **Send**-funksjonen på siden for **Retursammendrag**. Systemet oppretter umiddelbart et kundeforskuddsbetalingsbilag for returverdien, selv om selve retursalgsordren ennå ikke er fakturert. Denne fremgangsmåten kan brukes i situasjoner der en organisasjon må utstede refusjoner til kundene på forhånd på grunn av kundeserviceproblemer, og ikke ønsker å kreve at returnert lager skal mottas før refusjonene utstedes.

## <a name="replacement-orders"></a>Erstatningsordrer

Når en returordre utstedes, kan funksjonen for **Erstatningsordre** brukes til å generere en ny salgsordre for kunden. Denne fremgangsmåten kan brukes i utvekslingsscenarier. Funksjonen **Erstatningsordre** oppretter en annen salgsordre for de nye varene som må sendes, men en kryssreferansekobling i kategorien **RMA/retur** på siden **Samtalesenterparametere** kobler sammen erstatningsordren, RMA-en og den returnerte salgsordren.

Når betalinger på en erstatningsordre behandles, har organisasjoner to alternativer:

- Refundere kunden for returordren basert på den opprinnelige betalingsmåten, og deretter kreve en separat betaling for erstatningsordren. Det kreves ingen ekstra konfigurasjon for å bruke dette alternativet.
- Angi alternativet **Bruk kreditt** til **Ja** i kategorien **RMA/retur** på siden **Telefonsenterparametere** . I dette tilfellet brukes en kundebetalingsmetode systematisk både på returordren og erstatningsordren. Dette alternativet kan forhindre at eksterne refunderingsbetalinger blir utstedt. Det forhindrer også betalingsbehandling på transaksjonen. Det kan være nyttig i situasjoner der det behandles en jevn utveksling, og organisasjonen foretrekker å bruke kredittbilaget som genereres når returordren faktureres for å betale for fakturaen som genereres av erstatningsordren. Når alternativet **Bruk kreditt** er angitt til **Ja**, må organisasjonen utligne kreditnotaen manuelt mot erstatningsordrens faktura etter at begge de økonomiske dokumentene er generert.

Innstillingen **Ja** for alternativet **Bruk kreditt** gjelder bare når returordren skal kobles til en erstatningsordre. I dette tilfellet blir kundebetalingsmåten som skal brukes til å systematisk betale returen og bytteordre, definert av feltet **Bruk kredittbetalingsmetode** i kategorien **RMA/retur** på siden **Telefonsenterparametere**. Bare en betaling av **Kunde**-funksjonsbetalingstypen kan velges i dette feltet.

> [!NOTE]
> For en returordre som ikke har en koblet erstatningsordre, har ikke innstillingen **Ja** for alternativet **Bruk kreditt** noen innvirkning på returordrebetalingslogikken, fordi denne innstillingen bare gjelder for erstatningsordrer.

![Feltet Bruk kredittbetalingsmetode i kategorien RMA/retur på siden Telefonsenterparametere.](media/callcenterrefundparameters1.png)

> [!IMPORTANT]
> Hvis brukere som oppretter erstatningsordrer, planlegger å bruke alternativet **Bruk kreditt**, bør de ikke kjøre funksjonen **Fullført** på returordren før de angir alternativet **Bruk kreditt** til **Ja**. Når funksjonen **Fullført** er kjørt, beregnes refusjonsbetalingen og brukes på salgsreturordren. Alle forsøk på å sette alternativet **Bruk kreditt** til **Ja** etter at en refusjonsbetaling allerede er beregnet og brukt, vil ikke utløse en omberegning av refusjonsbetalingen, og betalingsmåten som er valgt i feltet **Bruk krediteringsbetaling**, vil ikke bli brukt. Hvis alternativet **Bruk kreditt** må brukes i denne sammenhengen, må brukeren slette erstatningsordren og RMA-en, og deretter starte på nytt og opprette en ny RMA. Denne gangen må brukeren sikre at alternativet **Bruk kreditt** er satt **Ja** før funksjonen **Fullført** kjøres.

## <a name="payment-overrides-for-call-center-returns"></a>Betalingsoverstyringer for telefonsenterreturer

Selv om telefonsenterlogikk systematisk bestemmer betalingsmåten for refundering på den måten som beskrives tidligere i denne artikkelen, kan det hende at brukerne noen ganger ønsker å overstyre disse betalingene. En bruker kan for eksempel redigere eller fjerne eksisterende refunderingsbetalingslinjer og bruke nye betalingslinjer. Systemberegnede refusjonsbetalinger kan bare endres av brukere som har riktige overstyringstillatelser. Disse tillatelsene kan konfigureres på siden **Overstyr tillatelser** i Retail og Commerce. Hvis du vil gjøre en betalingsoverstyring for refusjon, må brukeren være koblet til en sikkerhetsrolle der alternativet **Tillat alternativ betaling** er angitt til **Ja** på siden **Overstyringstillatelser**.

![Tillate alternativt betalingsalternativ på siden Overstyringstillatelser.](media/overridepermissions.png)

En organisasjon kan eventuelt sette alternativet **Tillat betalingsoverstyring** til **Ja** i kategorien **RMA/retur** på siden **Telefonsenterparametere**. I dette tilfellet må en sikkerhetsoverstyringskode velges i feltet **Sikkerhetsoverstyringskode**. Sikkerhetsoverstyringskoden er en alfanumerisk kode som må behandles eksternt, fordi brukere ikke kan vise den i Commerce Headquarters etter at den er angitt. Sikkerhetsoverstyringskoden bør bare være kjent av noen få klarerte nøkkelpersoner i en organisasjon. Når alternativet **Tillat betalingsoverstyring** er satt til **Ja**, har de muligheten til å angi en sikkerhetsoverstyringskode hvis brukere som ikke har de riktige rolletillatelsene, forsøker å endre betalingsmåten på en returordre. Hvis de ikke vet koden, eller hvis en leder eller arbeidsleder ikke kan legge den inn på siden for dem, kan de ikke overstyre returbetalingsmetoden.

> [!NOTE]
> Hvis sikkerhetsoverstyringskoden går tapt eller blir glemt, må organisasjonen tilbakestille den ved å definere en ny sikkerhetsoverstyringskode i feltet **Sikkerhetsoverstyringskode** i kategorien **RMA/retur** på siden **Telefonsenterparameter**.

![Betalingsoverstyringsparametere i kategorien RMA/retur på siden Telefonsenterparametere.](media/overridepaymentparameter.png)

> [!IMPORTANT]
> Før organisasjoner prøver å overstyre refunderingsbetalinger som bruker betalingstyper for kredittkort, bør de kontrollere at kredittkortbehandleren tillater returer som ikke er koblet til. Mange behandlere krever at refusjoner posteres tilbake til det opprinnelige kortet. Alle forsøk på å utstede en refusjon til et kort som ikke har tidligere hentinger, kan forårsake posteringsfeil hos behandleren.

## <a name="additional-resources"></a>Tilleggsressurser

[Betalingsmåter i telefonsentre](work-with-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]