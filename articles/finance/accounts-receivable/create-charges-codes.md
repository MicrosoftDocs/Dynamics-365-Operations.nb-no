---
title: Opprett tilleggskoder
description: Denne artikkelen beskriver hvordan du konfigurerer tilleggskoder for både leverandører og kunder.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MarkupTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d65952cb989672e4eac2dd6101ee9c7c9424daed
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866090"
---
# <a name="create-charges-codes"></a>Opprett tilleggskoder

Denne artikkelen beskriver hvordan du konfigurerer tilleggskoder for både leverandører og kunder. Hvis organisasjonen krever at salgs- eller innkjøpsbeløp skal spores i tillegg til linjevarer på en salgsordre eller bestilling, kan du bruke tilleggskoder til dette formålet. Du betaler for eksempel frakt og forsikring på en bestilling, og disse beløpene er spesifisert separat på bestillingen. I dette tilfellet kan du angi om beløpene skal posteres til utgiftskontoer eller legges til kostnadene for varene.

## <a name="set-up-charges-codes-for-accounts-receivable"></a>Definer tilleggskoder for kunder

Følg denne fremgangsmåten for å opprette tilleggskoder for kunder.

1. Gå til **Kunder** &gt; **Oppsett for tillegg** &gt; **Tilleggskode**.
2. Velg **Ny**.
3. Angi en kode for tillegget i **Tilleggskode**-feltet.
3. I **Beskrivelse**-feltet skriver du inn en beskrivelse av tillegget.
4. Valgfritt: Velg en mva-gruppe i feltet **Varens mva-gruppe**.
5. Angi hvordan tillegget skal debiteres og krediteres automatisk, på hurtigfanen **Postering**.
6. Hvis du valgte **Finanskonto** som debettype eller kredittype, angir du en posteringstype i **Postering**-feltene og angir hovedkontoen i **Konto**-feltene.

### <a name="example"></a>Eksempel

Kunden betaler gebyret. Derfor legges det til i salgsordretotalene. Du må angi følgende posteringsinformasjon:

- I **Type**-feltet i **Debet**-delen velger du **Kunde/leverandør** for å legge til fakturatillegget på kundens konto.
- I **Type**-feltet, i **Kredit**-delen velger du **Finanskonto**. Deretter, i **Konto**-feltet, velger du hovedkontoen for inntekt fra fakturatilegg.

> [!NOTE]
> Hvis debettypen eller kredittypen for den valgte koden er **Finanskonto** eller **Vare**, kan du angi en annen valuta for tilleggstransaksjonen.

Du kan skrive ut teksten for tillegg på språket som er angitt for kunden. Hvis du vil angi teksten for tilleggskoden på andre språk, velger du **Oversettelser**.

## <a name="set-up-charges-codes-for-accounts-payable"></a>Definer tilleggskoder for leverandører

Følg denne fremgangsmåten for å opprette tilleggskoder for leverandører.

1. Følg ett av disse trinnene:

    - Gå til **Leverandører** &gt; **Oppsett for** **tillegg** &gt; **Tilleggskode**.
    - Gå til **Innkjøp og leverandører** &gt; **Oppsett** &gt; **Tillegg** &gt; **Tilleggskode**.

2. Velg **Ny**.
3. Angi en kode for tillegget i **Tilleggskode**-feltet.
3. I **Beskrivelse**-feltet skriver du inn en beskrivelse av tillegget.
4. Valgfritt: Velg en mva-gruppe i feltet **Varens mva-gruppe**.
5. Valgfritt: I **Maksimumsbeløp**-feltet angir du maksimumsbeløpet som er tillatt for tilleggskoden.

    Dette feltet brukes til å validere gebyrer for leverandørfakturaer. Hvis du vil aktivere validering av tillegg, merker du av for **Aktiver validering av fakturakontroll** på fanen **Fakturavalidering** på siden **Leverandørparametere**.

    > [!IMPORTANT]
    > Hvis du vil validere tillegg for fakturaer, må du også opprette en forekomst av en policyregeltype som er basert på tillegg for den bestemte leverandørfakturapolicyen.

6. Angi hvordan tillegget skal debiteres og krediteres automatisk, på hurtigfanen **Postering**.
7. Hvis du valgte **Finanskonto** som debettype eller kredittype, angir du en posteringstype i feltene **Debetpostering** og **Kreditpostering** og angir hovedkontoen i feltene **Debetkonto** og **Kreditkonto**.
8. Hvis du vil aktivere sammenligningen av tilleggsverdier for en faktura som inneholder tilleggene fra tilsvarende bestillingshode eller -linjer, merker du av for **Sammenlign bestillings- og fakturaverdi**.

### <a name="example"></a>Eksempel

Du kan registrere tillegget som en utgift, som en del av totalen for bestillingen eller leverandørfakturaen. Følg disse trinnene for å konfigurere posteringsinformasjon. 

- I **Type**-feltet i **Kredit**-delen velger du **Kunde/leverandør** for å legge til fakturatillegget på leverandørens konto.
- I **Type**-feltet, i **Debet**-delen velger du **Finanskonto**. Deretter, i **Konto**-feltet, velger du hovedkontoen for utgifter fra fakturatilegg.

Følg denne fremgangsmåten for å konfigurere posteringsinformasjon, slik at enhetstillegget legges til i varekosten.

- I **Type**-feltet i **Kredit**-delen velger du **Kunde/leverandør** for å legge til fakturatillegget på leverandørens konto.
- I **Type**-feltet i **Debet**-delen velger du **Vare** for å legge til tillegget i varekostnaden.

> [!NOTE]
> Du ønsker kanskje å bruke en annen valuta enn valutaen som er angitt på bestillingen eller fakturaen. Du kan angi en annen valuta hvis debettypen eller kredittypen for den valgte tilleggskoden er satt til **Finanskonto** eller **Vare**.

Du kan skrive ut teksten for tillegg på språket som er angitt for kunden. Hvis du vil angi teksten for tilleggskoden på andre språk, velger du **Oversettelser**.
