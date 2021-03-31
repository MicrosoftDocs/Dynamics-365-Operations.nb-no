---
title: Opprette en bestilling for en engangsleverandør
description: Denne fremgangsmåten viser hvordan du oppretter en bestilling manuelt for en engangsleverandør.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1abd942da608bc221a7a66e03b5269fa30e2c20
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212036"
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