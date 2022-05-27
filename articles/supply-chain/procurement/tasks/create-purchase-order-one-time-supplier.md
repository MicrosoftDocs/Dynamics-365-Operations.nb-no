---
title: Opprette en bestilling for en engangsleverandør
description: Denne fremgangsmåten viser hvordan du oppretter en bestilling manuelt for en engangsleverandør.
author: GalynaFedorova
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ffb6515d8f24df68efbce265d98ed4e64e8d6b07
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677429"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Opprette en bestilling for en engangsleverandør

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en bestilling manuelt for en engangsleverandør. Leverandøren opprettes automatisk med bestillingen, i stedet for å opprette leverandørkontoen manuelt. Bestillinger opprettes vanligvis av en innkjøpsagent. Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF. Det er en forutsetning at kontoen for engangsleverandør er definert på siden Leverandørparametere.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Opprette en bestilling for en engangsleverandør
1. Gå til Innkjøp og leverandører > Bestillinger > Alle bestillinger.
2. Klikk på Ny.
3. Velg Ja i feltet Engangsleverandør.
    * En leverandørkonto blir automatisk opprettet og tilordnet bestillingen. Leverandørkontoen blir opprettet basert på malen som er angitt i fanen Generelt på siden Leverandørparametere.  
4. I Navn-feltet skriver du inn et unikt navn for leverandøren.
5. Klikk på OK.
    * Bestillingen kan nå fullføres og behandles som hvilken som helst ordre. Det finnes ingen spesielle egenskaper som er relatert til hvordan dette gjøres. Fakturaen registrerer en forfallstransaksjon på leverandørkontoen som ble opprettet med ordren, og deretter behandles betalingen.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]