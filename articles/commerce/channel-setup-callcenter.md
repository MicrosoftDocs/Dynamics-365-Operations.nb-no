---
title: Definere en telefonsenterkanal
description: Dette emnet beskriver hvordan du oppretter en ny telefonsenterkanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6ec42ab920868f541eeac54556f4f24cb1efaa3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002456"
---
# <a name="set-up-a-call-center-channel"></a>Definere en telefonsenterkanal


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du oppretter en ny telefonsenterkanal i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

I Dynamics 365 Commerce er et telefonsenter en type detaljhandelskanal som kan defineres i programmet. Ved å definere en kanal for telefonsenterenheter kan systemet knytte bestemte data og ordrebehandlingsstandarder til salgsordrer. Et firma kan definere flere telefonsenterkanaler i Commerce. 

Før du oppretter en ny telefonsenterkanal, må du kontrollere at du har oppfylt [Forutsetninger for kanaloppsett](channels-prerequisites.md).

## <a name="create-and-configure-a-new-call-center-channel"></a>Opprette og konfigurere en ny telefonsenterkanal

Hvis du vil opprette og konfigurere en ny telefonsenterkanal, gjør du følgende:

1. I navigasjonsruten går du til **Moduler \> Kanaler \> Telefonsentre \> Alle telefonsentre**.
1. I handlingsruten velger du **Ny**.
1. I **Navn**-feltet oppgir du et navn for den nye kanalen.
1. Velg den aktuelle **juridiske enheten** fra rullegardinlisten.
1. Velg det aktuelle **lagerstedet** fra rullegardinlisten.
1. Angi en gyldig standardkunde i feltet **Standardkunde**.
1. I feltet **Profil for e-postvarsling** oppgir du en gyldig profil for e-postvarsling.
1. Angi en infokode for **Prisoverstyring**. Merk at du kanskje må opprette en informasjonskode for dette først.
1. Oppgi en infokode for **Sperrekode**. Merk at du kanskje må opprette en informasjonskode for dette først.
1. Angi en infokode for **Kreditt**. Merk at du kanskje må opprette en informasjonskode for dette først.
1. Velg **Lagre**.

Bildet nedenfor viser opprettelsen av en ny telefonsenterkanal.

![Ny telefonsenterkanal](media/channel-setup-callcenter-1.png)

Bildet nedenfor viser et eksempel på en telefonsenterkanal.

![Eksempel på telefonsenterkanal](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Ekstra kanaloppsett

Andre oppgaver som kreves for oppsett av telefonsenterkanal, omfatter definere betalingsmåter og leveringsmåter.

Bildet nedenfor viser oppsettsalternativene **Leveringsmåter** og **Betalingsmåter** i kategorien **Oppsett**.

![Ekstra konfigurasjonshandlinger for telefonsenterkanal](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Definere betalingsmåter

Hvis du vil definere betalingsmåter, følger du disse trinnene for hver betalingstype som støttes på denne kanalen.

1. I handlingsruten velger du kategorien **Oppsett** og deretter **Betalingsmåter**.
1. I handlingsruten velger du **Ny**.
1. Velg en ønsket betalingsmåte i navigasjonsruten.
1. I delen **Generelt** angir du et **operasjonsnavn** og konfigurerer eventuelle andre ønskede innstillinger.
1. Konfigurer eventuelle tilleggsinnstillinger som kreves for betalingstypen.
1. Velg **Lagre** i handlingsruten.

Bildet nedenfor viser et eksempel på en kontantbetalingsmåte.

![Eksempel på betalingsmåter](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Definer leveringsmåter

Du kan se de konfigurerte leveringsmåtene ved å velge **Leveringsmåter** fra kategorien **Oppsett** i **handlingsruten**.  

Hvis du vil endre eller legge til en leveringsmåte, følger du disse trinnene.

1. I navigasjonsruten går du til **Moduler \> Lagerstyring \> Leveringsmåter**.
1. Velg **Ny** i handlingsruten for å opprette en ny leveringsmåte, eller velg en eksisterende måte.
1. I delen **Detaljhandelskanaler** velger du **Legg til linje** for å legge til kanalen. Legge til kanaler ved hjelp av organisasjonsnoder i stedet for å legge til hver kanal for seg, kan effektivisere tillegg av kanaler

Bildet nedenfor viser et eksempel på en leveringsmåte.

![Definer leveringsmåter](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Forutsetninger for kanaloppsett](channels-prerequisites.md)

[Salgsfunksjonalitet for telefonsenter](call-center-functionality.md)

[Definere ordrebehandlingsalternativer for telefonsenter](set-up-order-processing-options.md)

[Telefonsenterkataloger](call-center-catalogs.md)

[Definere og arbeide med svindelvarsler](set-up-fraud-alerts.md)

[Definere kontinuitetsprogrammer for telefonsentre](set-up-continuity-program.md)
