---
title: Delvis levering av en transportlast
description: Dette emnet forklarer hvordan du kan delvis levere en last og utsette planleggingen av kapasitet for lasten.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: e92a15cf4e2694eba1804184a02a7fd13159799e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434290"
---
# <a name="partial-shipment-of-a-transport-load"></a>Delvis levering av en transportlast

[!include[banner](../includes/banner.md)]

Ved å sette opp delvis levering av laster, kan du håndtere laster der kapasiteten ikke kan fastslås før alle salgslinjene er lagt til en last. Prosessen kan deretter fullføres når det nøyaktige pallantallet er kjent. Du trenger derfor ikke avgjøre hvilke paller som skal tilordnes til hvilken transport før tidspunktet når en transport fysisk lastes ut av lageret.

Denne funksjonen gir et alternativ til en mer fast struktur der du må bestemme hvilke paller som skal tilordnes til hvilken transport før plukkearbeidet eller lastearbeidet kan opprettes. I stedet kan brukere konfigurere individuelle laster for en delleveringsbekreftelse. Transportlasteprosessene for disse lastene kan deretter utføres. Derfor kan transportplanleggingsavdelingen planlegge laster uten å måtte vurdere kapasiteten til individuelle transporter.

Når lastingen utføres, kan medarbeidere definere en ny transportlast som en pall kan lastes til. De kan også identifisere en eksisterende transportlast. Disse dataene kan registreres via en mobilenhet. Derfor kan flere lagermedarbeidere laste beholdning fra de samme lastene eller ulike laster til samme lastebil. Lastene kan deretter helt eller delvis leveres.

> [!NOTE] 
> Hvis du vil laste beholdning fra en last til en bestemt transportlast og delvis sende lasten, må arbeid genereres ved hjelp av en lasteklasse i en arbeidsmal. Vanlig plukkarbeid av typen **Plukking** kan ikke lastes til en transportlast som en lastebil.

## <a name="set-up-transport-loads-for-partial-shipment"></a>Definere transportlaster for delvis forsendelse

Oppsettet for delvis forsendelse av laster består av følgende to fremgangsmåter.

### <a name="set-the-loading-strategy"></a>Angi lastestrategien

Du må aktivere delvis lasting ved å angi lastestrategien. Du kan angi lastestrategien når du har opprettet en last.

1. Velg **Lagerstyring** \> **Laster** \> **Alle laster**.
2. Velg en last, og klikk deretter **Hode**.
3. I **Lastestrategi**-feltet velger du **Levering med delvis last tillatt**.

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a>Opprette et menyelement for lasting av transportlaster

Du må opprette et nytt menyelement som gjør at transportlaster kan lastes. En transportlast lar deg gruppere arbeidslinjer fra en last til flere laster. Alt som er lagt til transportlasten, kan deretter sendes ved hjelp av en mobil skanner.

1. Velg **Lagerstyring** \> **Oppsett** \> **Mobilenhet** \> **Menyelementer på mobilenheten**.
2. Velg **Ny**, og deretter i **Modus**-feltet, velg **Arbeid**.
3. Angi alternativet **Bruk eksisterende arbeid** til **Ja**.
4. Gå til kategorien **Generelt**, og velg **Transportlasting** i feltet **Styrt av**.
5. Hvis du vil aktivere forsendelsesbekreftelse på en mobil skanner, velger **Transportlast** i **Tillatt type forsendelsesbekreftelse**-feltet.

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a>Bekrefte foresendelse av en transportlast fra klienten

I dette oppsettet kan du bekrefte en transportlast som inkluderer en full last eller en delvis lastet last som skal sendes.

1. Velg **Lagerstyring** \> **Laster** \> **Transportlaster**.
2. Velg **Transport** i **Send og motta**-kategorien i **Bekreft**-gruppen.
