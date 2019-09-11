---
title: Utføringsordre for innledende synkronisering av Finance and Operations og Common Data Service
description: Dette emnet angir rekkefølgen for synkroniseringen du må følge for å opprette de opprinnelige dataene.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873134"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a>Utføringsordre for innledende synkronisering av Finance and Operations og Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Før du bruker dataintegrering, må du opprette de første dataene som kreves for kunder, leverandører og kontakter. Du vil for eksempel opprette en ny **Leverandørgruppe**-vare og sette **Betalingsvilkår**-verdien til **Net30**. Før du prøver å opprette **Leverandørgruppe**-varen, må du i dette tilfellet kontrollere at **Net30** finnes i både Microsoft Dynamics 365 for Finance and Operations og Common Data Service. (I fremtiden vil Microsoft gi ut en dobbel skrive plattform funksjonalitet kalt Initial Sync. Denne funksjonaliteten vil gjøre en éngangs datasynkronisering mellom Finance and Operations og Common Data Service som en del av dual-Write-oppsettet.)

> [!TIP]
> Microsoft lanserer et dual-Write-kart for alle referansedata, inkludert **betalingsbetingelser**. Hvis du allerede har de opprinnelige dataene i ett system, kan en liten oppdateringsoperasjon på en oppføring utløse dobbel skriving på denne oppføringen.

Du må følge følgende prioritetsrekkefølge og kontrollere at de opprinnelige dataene er tilgjengelige både i Finance and Operations og Common Data Service.

## <a name="vendor"></a>Leverandør

Her er utførelsesrekkefølgen for **Leverandør**-enheten:

1. Leverandørgruppe

    1. Betalingsbetingelser

        1. Betalingsdag og linjer
        2. Betalingsplan

2. Betalingsmåte for leverandør

## <a name="customer-organization"></a>Kunde (organisasjon)

Her er utførelsesrekkefølgen for **Kunde**-enheten:

1. Kundegruppe

    1. Betalingsbetingelser

        1. Betalingsdag og linjer
        2. Betaling 

2. Kundebetalingsmåte

## <a name="contact-person"></a>Kontakt (person)

Her er utførelsesrekkefølgen for **Kontakt**-enheten:

1. Kunde
2. Leverandør
