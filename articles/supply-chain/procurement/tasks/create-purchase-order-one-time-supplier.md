---
title: Opprette en bestilling for en engangsleverandør
description: Denne fremgangsmåten viser hvordan du oppretter en bestilling manuelt for en engangsleverandør.
author: Henrikan
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e89a9d1b382efa3b90b8d70e84777321e9595f4a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579550"
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