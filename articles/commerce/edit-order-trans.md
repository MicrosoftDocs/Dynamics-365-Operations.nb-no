---
title: Redigere og overvåke nettordretransaksjoner og asynkrone kundeordretransaksjoner
description: Dette emnet beskriver hvordan du redigerer og overvåker nettordretransaksjoner og asynkrone kundeordretransaksjoner i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5113f7ac0d308076ebaa9daeca0929eb537e94ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792687"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a>Redigere og overvåke nettordretransaksjoner og asynkrone kundeordretransaksjoner

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du redigerer og overvåker nettordretransaksjoner og asynkrone kundeordretransaksjoner i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Mellom Commerce-versjon 10.0.5 og 10.0.6 ble støtte lagt til for redigering av hentesalgstransaksjoner (for eksempel salg og returer) og kassastyringstransaksjoner (for eksempel flytregistrering og fjerning av betalingsmiddel). I Commerce-versjon 10.0.7 ble støtte lagt til for redigering av nettordretransaksjoner og asynkrone kundeordretransaksjoner.

## <a name="edit-and-audit-order-transactions"></a>Redigere og overvåke ordretransaksjoner

Følg denne fremgangsmåten for å redigere og overvåke transaksjoner i Commerce Headquarters.

1. Installer [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. På siden **Detaljhandelsparametere** i fanen **Kundeordrer** angir du en sperrekode i hurtigfanen **Ordre** for **Sperrekode for ordresynkroniseringsfeil**.
1. Åpne arbeidsområdet **Finans for handelsbutikk**. Flisene **Synkroniseringsfeil for nettordre** og **Synkroniseringsfeil for kundeordre** inneholder en forhåndsfiltrert visning av siden Detaljhandelstransaksjon. Hver side viser transaksjonspostene som ikke ble synkronisert for tilsvarende ordretype.
1. Åpne siden **Synkroniseringsfeil for nettordre** eller **Synkroniseringsfeil for kundeordre**. Velg en post for å vise detaljer om synkroniseringsfeil. Hurtigfanen **Synkroniseringsstatus** inneholder følgende feildetaljer:

    - Status for ventende ordre
    - Detaljer om ordrefeil
    - Endringsdato og -klokkeslett
    - Antall nye forsøk

1. Hvis feildetaljene indikerer at posten må repareres, velger du **Office-tillegg**, og deretter velger du **Rediger valgt transaksjon**. Det åpnes en Excel-fil som viser detaljene for den valgte transaksjonen.

    - Hvis transaksjonen som skal redigeres, er en nettordretransaksjon, inneholder Excel-filen følgende regneark:

        - **Transaksjon** – Dette regnearket har hodedetaljene for transaksjonen.
        - **Salgstransaksjon** – Dette regnearket har linjedetaljene for transaksjonen.
        - **Betalingstransaksjoner** – Dette regnearket har detaljene for betalingslinjene for transaksjonen.
        - **Rabattransaksjoner** – Dette regnearket har rabattrelaterte detaljer for transaksjonen.
        - **Avgiftstransaksjoner** – Dette regnearket har avgiftsrelaterte detaljer for transaksjonen.
        - **Gebyrtransaksjoner** – Dette regnearket har gebyrrelaterte data for transaksjonen.

    - Hvis transaksjonen som skal redigeres, er en asynkron kundeordretransaksjon, inneholder Excel-filen følgende regneark:

        - **Linjer** – Dette regnearket har hode- og linjedetaljene for transaksjonen.
        - **Betalinger** – Dette regnearket har detaljene for betalingslinjene for transaksjonen.
        - **Rabatter** – Dette regnearket har rabattrelaterte detaljer for transaksjonen.
        - **Avgifter** – Dette regnearket har avgiftsrelaterte detaljer for transaksjonen.
        - **Gebyrer** – Dette regnearket har gebyrrelaterte data for transaksjonen.

1. Velg **Redigering** I feltet **Status for ventende ordre** I Excel-filen, og publiser deretter endringen. På denne måten hindrer du at jobben **Synkroniseringsordre** som kjører i satsvis modus, hopper over denne posten under behandling.
1. I Excel-filen endrer du de aktuelle feltene, og deretter laster du opp dataene tilbake til Commerce Headquarters ved hjelp av publiseringsfunksjonen i Dynamics Excel-tillegget. Etter at dataene er publisert, vil endringene gjenspeiles i systemet. Under publiseringen utføres det ingen validering for endringer som brukerne gjør.
1. Du kan vise et fullstendig overvåkingsspor for endringene ved å velge **Vis overvåkingsspor** i hodet for **Detaljhandelstransaksjon** for endringer på hodenivå, og i den relevante delen og posten på den riktige transaksjonssiden. Alle endringer som er knyttet til salgslinjer, vises for eksempel på siden **Salgstransaksjoner**, og alle endringer som er relatert til betalinger, vises på siden **Betalingstransaksjoner**. Følgende overvåkingsdetaljer beholdes for endringene:

    - Endringsdato og -klokkeslett
    - Felt
    - Gammel verdi
    - Ny verdi
    - Endret av

1. Etter at du har utført og publisert endringene, velger du **Synkroniser ordre** for å starte synkroniseringsprosessen umiddelbart. Du kan også vente på at synkroniseringsprosessen som kjører i satsvis modus, skal behandle transaksjonen.

Når ordrene er synkronisert, settes de som standard i en sperrestatus basert på sperrekoden som er definert i Commerce-parameterne. Sperringen av ordrene må fjernes før ordrene kan behandles videre for oppfylling eller andre operasjoner.

## <a name="additional-resources"></a>Tilleggsressurser

[Redigere og overvåke hentesalgs- og kassastyringstransaksjoner](edit-cash-trans.md)

[Redigere finansdimensjoner for detaljhandelstransaksjoner](edit-financial-dim.md)

[Opprette en Excel-arbeidsbok for å redigere detaljhandelstransaksjoner](create-excel-edit.md)

[Legge til felt i en Excel-arbeidsbok for å redigere detaljhandelstransaksjoner](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]