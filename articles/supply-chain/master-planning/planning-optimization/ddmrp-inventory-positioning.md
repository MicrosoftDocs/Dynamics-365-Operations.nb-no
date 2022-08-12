---
title: Lagerplassering
description: Denne artikkelen inneholder informasjon om strategisk lagerplassering, som omfatter identifisering av utkoblingspunkter i forsyningskjeden, der du kan bygge opp lagerbeholdning for å komprimere leveringstidene og absorbere forstyrrelser i forsyningskjeden.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ReqGroup, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: bec36b5b51b937782afdb78d7009a58dcd0942f0
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186738"
---
# <a name="inventory-positioning"></a>Lagerplassering

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Strategisk lagerplassering innebærer identifisering av utkoblingspunkt i forsyningskjeden, der du kan bygge opp lagerbeholdning. Denne fremgangsmåten brukes hovedsakelig til å komprimere leveringstiden og absorbere forstyrrelser i forsyningskjeden. På denne måten kan du redusere innvirkningen av "piskesnerteffekten", fordi etterspørselsavvik ikke har passert helt ned i forsyningskjeden. (*Piskesnerteffekten* refererer til hvor små variasjoner i etterspørselen på detaljhandelsnivået som kan forårsake gradvis større variasjoner i etterspørselen på grossist-, distributør-, produsent- og råvareleverandørnivå.)

Lagerplassering er det første trinnet i DDMRP (Demand Driven Materials Resource Planning – behovsdrevet planlegging av materialressurser).

## <a name="inventory-positioning-for-manufacturing"></a>Lagerplassering for produksjon

I denne delen finner du et eksempel som viser hvordan du tar avgjørelser om lagerplassering hvis du produserer et typisk puteprodukt. Puten har en stykkliste på flere nivåer, som vist i illustrasjonen nedenfor.

![Eksempel på stykkliste på flere nivåer for et puteprodukt.](media/ddmrp-bom-example.png "Eksempel på stykkliste på flere nivåer for et puteprodukt")

### <a name="choose-your-decoupling-points"></a>Velg utkoblingspunktene

Når du velger hvor du vil plassere utkoblingspunktene, bør du vurdere alle de følgende aspektene ved hver vare i stykklisten som kriterier:

- Ekstern variasjon
- Lagerutnyttelse og fleksibilitet
- Kritisk operasjonsbeskyttelse
- Kundens toleransetid
- Synlighetshorisont for salgsordrer
- Potensiell leveringstid på markedet

I eksemplet med puten kan du sette ditt første utkoblingspunkt til *skumbarrene* av følgende årsaker:

- Det er vanskelig å angi kilde for materialene som brukes til å lage skumbarrer, og tilgjengeligheten er flyktig. Derfor er kriteriet *ekstern variasjon* oppfylt.
- Skumbarrene kan kuttes i mange forskjellige former og størrelser for å lage skuminnfatninger for andre produkter som du produserer, i tillegg til puten. Derfor er kriteriet *lagerutnyttelse og fleksibilitet* oppfylt.

Deretter kan du sette det neste utkoblingspunktet til *stoffsettet*, som er det forhåndskuttede putestoffet. Du kan velge dette punktet fordi du bare har én maskin til å skjære stoff. Derfor er kriteriet *kritisk operasjonsbeskyttelse* oppfylt.

Til slutt kan du plassere det siste avkoblingspunktet på den ferdige putevaren. Du kan velge dette punktet fordi du har en svært kort *kundetoleransetid* på salg, og fordi *synlighetshorisonten for salgsordrer* er forholdsvis kort. Derfor må du sørge for at du har nok lagerbeholdning til å oppfylle innkommende ordrer. Du kan også angi en høyere pris ved å beholde leveringstiden så kort, og det er dette kriteriet *potensiell leveringstid på markedet* refererer til.

Basert på denne analysen viser illustrasjonen nedenfor hvordan stykklisten for puten vil se ut. Gule lagersymboler fremhever utkoblingspunktene.

![Eksempel på stykkliste med utkoblingspunkter uthevet.](media/ddmrp-bom-decoupling-example.png "Eksempel på stykkliste med utkoblingspunkter uthevet")

### <a name="calculate-your-decoupled-lead-time"></a>Beregn utkoblet leveringstid

Denne delen viser hvordan du beregner de nye leveringstidene etter at du har innført utkoblingspunkter.

I illustrasjonen nedenfor for puteeksemplet som ble startet i den forrige delen, vises leveringstidene i grå bokser øverst til venstre for hver stykklistekomponent. Bokser som har en rød kontur, angir varer som driver den kumulative leveringstiden (summen av den lengste leveringstiden på hvert nivå i stykklisten). Denne leveringstiden er 21 dager når du starter fra begynnelsen.

![Eksempel på stykkliste med leveringstider.](media/ddmrp-bom-lead-times-example.png "Eksempel på stykkliste med leveringstider")

Hvis du imidlertid bruker utkoblingspunktene du valgte tidligere, vil de utkoblede varene alltid være på lager. Derfor har de en leveringstid på 0 (null). Den nye leveringstiden for puten er nå bare fem dager: to dager på å kjøpe tråden og tre dager til produksjon av puten. Denne leveringstiden kalles for *den utkoblede leveringstiden*.

![Eksempel på utkoblet leveringstid.](media/ddmrp-bom-decoupled-lead-time-example.png "Eksempel på utkoblet leveringstid")

## <a name="strategic-inventory-positioning-in-a-retail-model"></a>Strategisk lagerplassering i en detaljhandelsmodell

Siden forhandlere bare lagrer ferdige produkter, er ikke stykklister en sak. Forhandlere kan imidlertid likevel bruke DDMRP ved å angi strategiske lagerplasserings- og buffernivåer basert på lagringslokasjoner i distribusjonsnettverket.

Illustrasjonen nedenfor viser et eksempel på et firma som har et distribusjonssenter i Seattle, og butikker i Boston, Atlanta og Portland.

![Utkoblingspunkter basert på lokasjon i en detaljhandelsmodell.](media/ddmrp-retail-decoupl-points-example.png "Utkoblingspunkter basert på lokasjon i en detaljhandelsmodell")

Du kan bestemme deg for at overføringstiden for å flytte et teppeprodukt mellom distribusjonssenteret og butikkene bryter med *kundetoleransetiden*, fordi kundene forventer at teppet skal være på lager når de besøker dem. I dette tilfellet definerer du et utkoblingspunkt for teppevaren i hver av de tre butikkene. Hver butikk vil ha forskjellige buffernivåer, basert på leveringstider, etterspørselsmønstre og så videre.

## <a name="implement-inventory-positioning-in-dynamics-365-supply-chain-management"></a>Implementer lagerplasseringer i Dynamics 365 Supply Chain Management

Denne delen beskriver hvordan du implementerer lagerplasseringsstrategien i Microsoft Dynamics 365 Supply Chain Management.

### <a name="set-up-item-coverage-groups-that-create-decoupling-points"></a>Definer varedekningsgrupper som oppretter utkoblingspunkter

Varer blir utkoblingspunkter når de tilhører en dekningsgruppe som er konfigurert med **Dekningskode**-verdien *Utkoblingspunkt*. Det første trinnet i prosessen med å konfigurere DDMRP er derfor å bestemme hvilke dekningsgrupper du må implementere for DDMRP-strategien, og deretter opprette dem ved å følge disse trinnene.

1. Gå til **Hovedplanlegging \> Oppsett \> Dekning \> Dekningsgrupper**.
1. I handlingsruten velger du **Ny** for å opprette en dekningsgruppe.
1. Angi informasjonen som identifiserer denne dekningsgruppen, og velg deretter kalenderen du vil bruke.
1. På **Generelt**-fanen angir du **Dekningskode**-feltet til *Utkoblingspunkt*. Denne innstillingen vil føre til at alle varer som tilhører denne dekningsgruppen, behandles som utkoblingspunkter for DDMRP. Det aktiverer også alle DDMRP-innstillinger for denne gruppen, som beskrevet senere i denne prosedyren.
1. Angi følgende obligatoriske felter i delen **DDMRP-parametere** på **Annet**-fanen:

    - **Leveringstidsfaktor** – Angi en faktor (som en desimalverdi mellom 0 og 1) for å kontrollere virkningen som leveringstiden skal ha, når minimum og maksimum lagernivå beregnes for varer i denne dekningsgruppen. Jo lengre leveringstid en vare har, jo lavere skal leveringstidsfaktoren generelt være. En lavere leveringstidsfaktor gir lavere minimum og maksimum lagernivå og fører derfor til mindre og hyppigere ordrer. DDMRP-metoden anbefaler en verdi mellom 0,20 og 0,40 for varer som har lang leveringstid, mellom 0,41 og 0,60 for varer som har middels leveringstid, og mellom 0,61 og 1,00 for varer som har kort leveringstid. Hvis du vil ha mer informasjon, kan du se [Bufferprofil og -nivåer](ddmrp-buffer-profile-and-levels.md).
    - **Variasjonsfaktor** – Angi en faktor (som en desimalverdi mellom 0 og 1) for å kontrollere virkningen som varierende etterspørsel skal ha, når minimum lagernivå beregnes for varer i denne dekningsgruppen. Jo mer variabel en vares etterspørsel er, desto høyere er variasjonsfaktoren generelt for varen. En høyere variasjonsfaktor gir et høyere minimum lagernivå. DDMRP-metoden anbefaler en verdi mellom 0,00 og 0,40 for varer som har lav variasjon, mellom 0,41 og 0,60 for varer som har middels variasjon, og mellom 0,61 og 1,00 for varer som har høy variasjon. Hvis du vil ha mer informasjon, kan du se [Bufferprofil og -nivåer](ddmrp-buffer-profile-and-levels.md).
    - **Periode for min, maks og gjenbestillingspunkt** – Angi hvor ofte bufferverdier skal beregnes (*Daglig* eller *Ukentlig*).

1. Angi følgende obligatoriske felter i delen **Gjennomsnittlig daglig bruk** på **Annet**-fanen:

    - **Gjennomsnittlig daglig bruk basert på** – Velg hvilke tidsperioder beregningen av gjennomsnittlig daglig bruk (ADU) skal baseres på. Velg én av følgende verdier:

        - *Tidligere* – Ser bare på tidligere bruk for antallet dager som er angitt i feltet **Tidligere periode (dager)**. ADU beregnes som den totale etterspørselen for en vare i løpet av beregningsperioden (i beholdningsenheter) dividert med antall dager i beregningsperioden.
        - *Senere* – Ser bare på prosjektert fremtidig bruk (inkludert prognoser) for antallet dager som er angitt i feltet **Senere periode (dager)**. ADU beregnes som den totale etterspørselen for en vare i løpet av beregningsperioden (i beholdningsenheter) dividert med antall dager i beregningsperioden. 
        - *Blandet* – Ser på både tidligere og fremtidig bruk. Både innstillinger for feltet **Tidligere periode (dager)**, feltet **Senere periode (dager)** og blandingsalternativer gjelder. 

            *Blandet ADU* = (\[*Tidligere vekting* × *Tidligere ADU*\] + \[*Senere vekting* × *Senere ADU*\]) ÷ (*Tidligere vekting* + *Senere vekting*)

    - **Tidligere periode (dager)** – Angi antall tidligere dager (opptil og inkludert i dag) som systemet skal vurdere når det beregner ADU for varer i denne dekningsgruppen. Denne innstillingen gjelder bare når feltet **Gjennomsnittlig daglig bruk basert på** er satt til *Tidligere* eller *Blandet*.
    - **Senere periode (dager)** – Angi antall fremtidige dager (fra i dag og frem til den angitte dagen) som systemet skal vurdere når det beregner ADU for varer i denne dekningsgruppen. Denne innstillingen gjelder bare når feltet **Gjennomsnittlig daglig bruk basert på** er satt til *Senere* eller *Blandet*.
    - **Relativ vekt av perioden tidligere for blandet gjennomsnittlig daglig bruk** – Angi vektingen (som en prosentverdi) som skal brukes på den tidligere perioden, når blandet ADU beregnes. Denne innstillingen gjelder bare når feltet **Gjennomsnittlig daglig bruk basert på** er satt til *Blandet*.
    - **Relativ vekt av perioden fremover for blandet gjennomsnittlig daglig bruk** – Angi vektingen (som en prosentverdi) som skal brukes på perioden fremover, når blandet ADU beregnes. Denne innstillingen gjelder bare når feltet **Gjennomsnittlig daglig bruk basert på** er satt til *Blandet*.

1. For alle andre faner og felter angir du de detaljerte innstillingene som brukes til å beregne behov for varene som er knyttet til denne dekningsgruppen.

### <a name="set-an-item-as-a-decoupling-point"></a>Angi en vare som et utkoblingspunkt

Følg denne fremgangsmåten for å angi en vare som et utkoblingspunkt.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Finn og velg en frigitt vare som du vil definere for DDMRP.
1. Gå til **Plan**-fanen i handlingsruten, og velg deretter **Varedekning**.
1. På **Varedekning**-siden vises kanskje flere varedekningsposter allerede, der hver vare gjelder for en forskjellig kombinasjon av lagrings- og produktdimensjoner. Du kan velge en eksisterende varedekningspost som gjelder for dimensjonene der du vil opprette et utkoblingspunkt. Du kan også velge **Ny** i handlingsruten for å opprette en ny varedekningspost.
1. Definer varedekningsposten på vanlig måte. Du må som et minimum angi området og lageret der utkoblingspunktet skal gjelde.
1. La den aktuelle posten fortsatt være valgt, og velg **Generelt**-fanen.
1. Merk av for **Bruk spesifikke innstillinger**.
1. Sett **Dekningsgruppe**-feltet til en dekningsgruppe som er konfigurert til å opprette utkoblingspunkter (som beskrevet i forrige del).
1. Varen er nå konfigurert som et utkoblingspunkt. Når du bruker DDMRP, vil du vanligvis også konfigurere innstillinger her som påvirker bufferstørrelser og gjenbestillingsantallet. Du kan imidlertid fullføre denne konfigurasjonen senere. Hvis du vil ha mer informasjon om innstillingene, kan du se [Definer buffere for en vare som har et utkoblingspunkt](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

> [!NOTE]
> Hvis du vil planlegge varer som ikke er utkoblingspunkter, følger du de samme trinnene som når standard planlegging av materialbehov (MRP) brukes.
