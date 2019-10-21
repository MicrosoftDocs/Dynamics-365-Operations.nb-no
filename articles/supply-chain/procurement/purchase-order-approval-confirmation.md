---
title: Godkjenne og bekrefte bestillinger
description: Dette emnet beskriver statusene som en bestilling går gjennom når den er opprettet, og effekten av å aktivere endringsadministrasjon på bestillinger.
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.search.industry: ''
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58ff596314d348a465ba6ee23369f09e74d580eb
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248886"
---
# <a name="approve-and-confirm-purchase-orders"></a>Godkjenne og bekrefte bestillinger

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Dette emnet beskriver statusene som en bestilling går gjennom når den er opprettet, og effekten av å aktivere endringsadministrasjon på bestillinger.

Når du har opprettet en bestilling, må den kanskje går gjennom en godkjenningsprosess. Når leverandøren har godtatt ordren, settes bestillingen til statusen **Bekreftet**.

## <a name="approval-of-purchase-orders"></a>Godkjenne bestillinger
Bestillinger som ikke bruker endringsadministrasjon har statusen **Godkjent** så snart de er opprettet, mens bestillinger som bruker endringsadministrasjon har statusen **Utkast** når de opprettes. En bestilling som er opprettet ved å autorisere en planlagt bestilling fra hovedplanlegging, settes alltid til statusen **Godkjent**, uavhengig av innstillingene for endringsadministrasjon. En bestilling oppretter bare lagertransaksjoner når den får statusen **Godkjent**. Derfor vises ikke denne beholdningen som tilgjengelige for reservasjon eller merking før ordren er godtatt.  

Du aktiverer endringsadministrasjon for bestillinger ved å angi alternativet **Aktiver endringsadministrasjon** på siden **Parametere for innkjøp og leverandører**. Når endringsadministrasjon er aktivert, må bestillinger gå gjennom en arbeidsflyt for godkjenning etter at de er fullført. Supply Chain Management har et redigeringsprogram for arbeidsflytprosess der du kan definere en arbeidsflyt til å representere din godkjenningsprosess. Denne arbeidsflyten kan inneholde regler for automatisk godkjenning, regler som bestemmer hvem som skal tilordnes til godkjenning av bestemte bestillinger og regler for eskalering av en arbeidsflyt som har ventet godkjenning i lang tid. For alle aktivere prosessen for endringsadministrasjon for alle eller bestemte leverandører. Du kan også definere prosessen slik at den kan overstyres for individuelle bestillinger.  

Når endringsadministrasjon er aktivert, går bestillinger gjennom seks godkjenningsstatuser, fra **Utkast** til **Sluttført**. Når en ordre er godkjent, må brukere som vil endre den bruke handlingen **Be om endring**.

| Godkjenningsstatus | Beskrivelse                                                                      | Be om endring er aktivert |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Utkast           | Bestillingen er et utkast, og er ikke sendt til godkjenning i arbeidsflyten for bestilling.     | Antall                        |
| Til vurdering       | Bestillingen ble sendt til godkjenning i arbeidsflyten for bestilling. Venter på godkjenning.       | Antall                        |
| Avslått        | Bestillingen ble avvist under godkjenningsprosessen.                                 | Antall                        |
| Godkjent        | Bestillingen ble godkjent.                                                             | Ja                       |
| Bekreftet       | Bestillingen ble bekreftet. En bestilling kan ikke bekreftes før den er godkjent.        | Ja                       |
| Sluttført       | Bestillingen ble gjort endelig. Den er nå økonomisk lukket og kan ikke lenger endres. | Antall                        |

## <a name="confirming-purchase-orders"></a>Bekrefte bestillinger
Bestillinger som har godkjenningsstatusen **Godkjent** kan gå gjennom flere trinn før de er bekreftet. Det kan hende du for eksempel må sende en forespørsel om innkjøp til leverandøren for å spørre om priser, rabatter og leveringsdatoer. I så fall kan du sette bestillingen til statusen **Til eksterne vurdering** ved hjelp av handlingen **Innkjøpsforespørsel**.  

Leverandører som er konfigurert til å bruke leverandørportalen, kan se gjennom bestillinger på portalen og godkjenne eller avvise dem. Under denne vurderingsprosessen har bestillingen statusen **Til eksterne vurdering**. Leverandørportalen kan konfigureres slik at en bekreftelse fra leverandøren automatisk bekrefter ordren i Supply Chain Management. Du kan også manuelt bekrefte en bestilling når du mottar bekreftelse fra leverandøren. Hvis en leverandør avviser en bestilling, mottas avvisningen sammen med årsaken til avvisningen og forslag til endringer. I slike tilfeller forblir statusen for bestillingen **Til eksterne vurdering**.  

Det er også et alternativ for å generere en proformabekreftelse for en ordre før den faktiske bekreftelsen er behandlet. Dette alternativet oppretter bare en rapport som du kan dele med leverandøren. Det opprettes ikke journalinformasjon.  

Når leverandøren har godtatt ordren, er neste trinn å registrere bestillingen som igangsatt. Du kan utføre dette trinnet ved å bruke handlingen **Bekreftelse** eller **Bekreft**. Begge disse handlingene setter godkjenningsstatusen for ordren til **Bekreftet**. Bekreftelse av en ordre starter to tilleggsprosesser:

-   Det opprettes en journal for å lagre en nøyaktig kopi i systemet av det som ble bekreftet. Noen ganger kreves det endringer av ordrer, og tilleggsjournaler opprettes etter at den oppdaterte ordren er bekreftet. Disse journalene lar deg vise historikken til de ulike versjonene av ordren som ble bekreftet.
-   Regnskapsdistribusjoner opprettes, og ordre- og budsjettkontroller utføres hvis denne funksjonen er aktivert. Hvis en av kontrollene mislykkes, får du en feilmelding som sier at endringer må gjøres i bestillingen før den kan bekreftes på nytt.

En leverandør kan be om en type forsikring om at betalingen vil utføres for et kjøp. Det finnes ulike metoder for å levere denne garanti innenfor leverandørprosessene. Handlingen **Forskuddsbetaling** reserverer for eksempel midler for bestillingen, og denne forskuddsbetalingen registreres på bestillingen.

## <a name="changing-purchase-orders"></a>Endre bestillinger
I noen tilfeller må du kanskje endre en bestilling når den har får godkjenningsstatusen **Godkjent** eller **Bekreftet**.  

Hvis bestillingen ble opprettet ved hjelp av en prosess for endringsadministrasjon, kan du gjøre endringer ved å tilbakekalle ordren, eller hvis ordren allerede er godkjent, ved hjelp av handlingen **Be om endring**. I så fall endres godkjenningsstatusen tilbake til **Utkast**, og deretter kan du endre ordren. Når du er ferdig med å gjøre endringer, må du kanskje sende bestillingen til ny godkjenning. Du kan konfigurere hvilke typer endringer som krever ny godkjenning ved hjelp en policyregel for **Regel for ny godkjenning for bestillinger** på siden **innkjøpspolicyer**.  

Hvis en del av det bestilte antallet for en bestillingslinje er levert, kan du ikke endre det bestilte antallet. Du kan imidlertid endre antallet **Gjenstående levering** på linjen. Du kan deretter bruke handlingen **Fullfør** til å avbryte linjer og forhindre videre behandling. 

Når en ordre er bekreftet, kan du ikke lenger slette den. Du kan imidlertid avbryte det totale antallet eller eventuelle restantallet i en ordre, forutsatt at antallet ikke er mottatt eller fakturert.

<a name="additional-resources"></a>Tilleggsressurser
--------

[Oversikt over bestilling](purchase-order-overview.md)

[Opprett bestilling](purchase-order-creation.md)

[Mottaksseddel mot bestillinger](product-receipt-against-purchase-orders.md)

[Oversikt over leverandørfakturaer](../../financials/accounts-payable/vendor-invoices-overview.md)



