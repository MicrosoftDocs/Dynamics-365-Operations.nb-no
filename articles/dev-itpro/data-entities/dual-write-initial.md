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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797304"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a>Utføringsordre for innledende synkronisering av Finance and Operations og Common Data Service

Før du bruker dataintegrering, må du opprette de første dataene som kreves for kunder, leverandører og kontakter. Hvis du for eksempel vil opprette en ny **Leverandørgruppe**-vare og angi **betalingsbetingelsene** som **Net30**, før du prøver å opprette **Leverandørgruppe**-varen, må du kontrollere at **Net30** finnes både i Finance and Operations og Common Data Service. (I fremtiden vil vi gi ut en dobbel skrive plattform funksjonalitet kalt **Initial Sync**. Det vil gjøre en éngangs datasynkronisering mellom Finance and Operations og Common Data Service som en del av dual-Write-oppsettet.)

Tips: Vi lanserer et dual-Write-kart for alle referansedata inkludert **betalingsbetingelser**. Hvis du allerede har de opprinnelige dataene i ett system, kan en liten oppdateringsoperasjon på en oppføring utløse dobbel skriving på denne oppføringen. 

Du må følge følgende prioritetsrekkefølge og kontrollere at de opprinnelige dataene er tilgjengelige både i Finance and Operations og Common Data Service.   

## <a name="vendor"></a>Leverandør

Rekkefølgen for utførelse av leverandør er:

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a>Kunde (organisasjon)

Rekkefølgen for utførelse av kunde er:

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a>Kontakt (person)

Rekkefølgen for utførelse av kontakt er:

```
Customer
Vendor               
```
