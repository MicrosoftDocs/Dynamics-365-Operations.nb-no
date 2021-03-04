---
title: Oversikt over bestilling
description: Denne artikkelen inneholder generell informasjon om bestillinger og koblinger til flere artikler som er knyttet til de ulike stadiene som en bestilling går gjennom.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder, PurchConfirmationRequestJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 93083
ms.assetid: e9b7bc5b-1d7e-4ec2-97be-d655274b0613
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cfb35d6db74f965911329dbd6215d1108149fa6c
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434843"
---
# <a name="purchase-order-overview"></a>Oversikt over bestilling

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder generell informasjon om bestillinger og koblinger til flere artikler som er knyttet til de ulike stadiene som en bestilling går gjennom.

En bestilling er et dokument som representerer en avtale med en leverandør om å kjøpe varer eller tjenester. Dokumentet bidrar også til å holde oversikt over produktkvitteringer som er gjort mot ordren og, senere, regnskap for leverandørfakturaer som leverandøren veksler mot ordren.  

Siden **Bestillinger** inneholder en oversikt over ordrene som er tilgjengelige og lar deg endre disse ordrene. Når du åpner en bestilling, kan du velge **Topptekst**-visningen, som inneholder informasjon som er angitt bare én gang for hver bestilling, for eksempel leverandørdetaljer. Du kan også velge **Linjer**-visningen, der du kan endre ordrelinjer. Vanligvis kan du bytte mellom disse to visningene når du endrer bestillinger. Tillegg vises ikke direkte på siden **Bestillinger**, men de er tilgjengelige via menyer i ordrehodet og -linjene.  

Det finnes mange rapporter der du kan vise informasjon om bestillinger, produktkvitteringer og leverandørfakturaer. Disse rapportene er finnes i modulene **Innkjøp og leverandører** og **Leverandører**.  

Arbeidsområdene **Bestillingsklargjøring** og **Bestillingsmottak og oppfølging** lar deg vise lister over bestillinger i de ulike stadiene som de har kommet til. De gir også et sammendrag av handlinger som må utføres. Arbeidsområdet **Bestillingsklargjøring** fokuserer på oppretting av bestilling og gjennomgang, behandling av ordren til godkjenning og bekreftelse med leverandøren. Arbeidsområdet **Bestillingsmottak og oppfølging** fokuserer på behandling av mottak av varer eller tjenester mot bestillinger. Det inneholder lister som gir innsikt i mottak som er forfalt, eller som snart forfaller for levering av leverandøren. Disse arbeidsområdene brukes ikke til å utføre de relaterte mottaksaktivitetene som gjøres på lageret. Disse aktivitetene utføres ved hjelp av sider i modulene **Beholdningsstyring** og **Lagerstyring**. Behandling av leverandørfakturaer skal gjøres ved hjelp av arbeidsområdet **Leverandørfakturaregistrering**, og betalinger skal gjøres ved hjelp av arbeidsområdet **Leverandørbetalinger**.  

Artiklene nedenfor inneholder en oversikt over de ulike stadiene som en bestilling går gjennom:

-   [Opprette bestillinger](purchase-order-creation.md)
-   [Godkjenne og bekrefte bestillinger](purchase-order-approval-confirmation.md)
-   [Mottaksseddel mot bestillinger](product-receipt-against-purchase-orders.md)
-   [Oversikt over leverandørfakturaer](../../financials/accounts-payable/vendor-invoices-overview.md)

## <a name="types-of-purchase-orders"></a>Bestillingstyper
Det finnes tre bestillingstyper: Når du oppretter en bestilling, må du angi type. Du kan definere en standard ordretype for nye bestillinger på siden **Parametere for innkjøp og leverandører**.

| Bestillingstype        | Beskrivelse                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Journal        | Bruk denne typen for å opprette en utkastordre. Denne typen har ikke innvirkning på lagerantall eller genererer ikke lagertransaksjoner. Bestillingsjournallinjer tas ikke med i hovedplanlegging.                                                                                                       |
| Bestilling | Bruk denne typen for å opprette bestillinger når ordrer er bekreftet med en leverandør, og når ordrene behandles gjennom tilgang og fakturering før betalingen sendes til leverandøren. Denne typen bestilling er den vanligste.                                                                          |
| Returordre | Bruk denne typen når du returnerer varer til leverandøren. Denne bestillingstypen krever at du angir et autorisasjonsreturnummer (ARM) som leverandøren gir deg. Du angir ARM-nummeret i kategorien **Generelt** i bestillingen. Ordrelinjer må ha negative antall. |

## <a name="purchase-order-statuses"></a>Bestillingsstatuser
Bestillinger inneholder flere statusfelt som viser fremdriften for bestillingen. Disse feltene er synlige i visningen **Topptekst** for ordren, og noen få av dem vises også i rutenettoversikt for alle ordrer. Feltet **Status** viser statusen for et antall på bestillingen. Følgende verdier er tilgjengelige:

-   **Åpen ordre** – Ordre er opprettet, og antall er bestilt.
-   **Mottatt** – Noen av antallene er mottatt, men de er ikke fakturert ennå.
-   **Fakturert** – Hele antallet i ordren er fakturert. **Obs!** Hvis en ordre er *delvis* fakturert, er ikke statusen **Mottatt** eller **Fakturert** riktig. Ordren vil derfor fortsatt ha statusen **Åpen ordre**.
-   **Avbrutt** – En ordre ble bekreftet, men senere avbrutt. Derfor angir denne statusen at det finnes ikke lenger noen åpne antall i bestilling.

Feltet **Dokumentstatus** lar deg raskt se gjennom ordrefremdriften når det gjelder dokumenter som har blitt behandlet. Det viser statusen for det nyeste dokumentet som er fullført for ordren. Følgende verdier er tilgjengelige:

-   **Ingen** – Ingen dokumenter er behandlet for ordren ennå.
-   **Innkjøpsforespørsel** – En innkjøpsforespørsel er generert, og ordren venter på tilbakemelding fra leverandøren.
-   **Bestilling** – Bekreftelse er behandlet på bestillingen.
-   **Produktkvittering** – Produktkvittering er behandlet på ordren.
-   **Faktura** – En faktura er etterberegnet med ordren.

Feltet **Godkjenningsstatus** brukes når en bestilling går gjennom en vurderingsprosess eller arbeidsflyt. Følgende verdier er tilgjengelige:

-   **Utkast**, **Til vurdering** og **Avvist** – Disse statusene brukes bare når en arbeidsflyt for godkjenning brukes for bestillingen.
-   **Godkjent** – Denne statusen blir tilordnet ordrer som har fullført arbeidsflytgodkjenning. Ordrer som er opprettet uten å bruke en arbeidsflyt for godkjenning får statusen **Godkjent** umiddelbart.
-   **Til ekstern vurdering** – Denne statusen brukes i situasjoner der en innkjøpsforespørsel sendes til leverandøren, slik at leverandøren kan bekrefte betingelsene for bestillingen. Denne statusen brukes også i prosessen som startes av handlingen **Forespørsel om bekreftelse**. For denne prosessen blir leverandøren bedt om å bekrefte betingelsene for bestillingen ved å koble til systemet ditt og registrere om ordren bekreftes eller avvises.
-   **Bekreftet** – Denne statusen blir tilordnet når bestillingen er bekreftet. Denne statusen er vanligvis den siste godkjenningsstatusen som tilordnes en ordre.


<a name="additional-resources"></a>Tilleggsressurser
--------

[Opprette bestillinger](purchase-order-creation.md)

[Godkjenne og bekrefte bestillinger](purchase-order-approval-confirmation.md)

[Mottaksseddel mot bestillinger](product-receipt-against-purchase-orders.md)

[Oversikt over leverandørfakturaer](../../financials/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]