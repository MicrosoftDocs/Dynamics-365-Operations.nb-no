---
title: Registrere betalinger automatisk for konserninterne kundefakturaer
description: Denne artikkelen forklarer hvordan du registrerer betalinger automatisk for konserninterne kundefakturaer
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4e8f784cd310026f0a647a0f509999e11ab26ce5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878794"
---
# <a name="register-payments-automatically-for-intercompany-customer-invoices"></a>Registrere betalinger automatisk for konserninterne kundefakturaer

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management oppretter en kundetransaksjon når en konsernintern kundefaktura posteres. Denne kundetransaksjonen forblir åpen til den er utlignet, som betyr at den er betalt. Når den tilsvarende konserninterne bestillingen fakturaoppdateres, opprettes det en leverandørtransaksjonen som samsvarer med kundetransaksjonen. Denne leverandørtransaksjonen forblir også åpen til den er utlignet. Hvis du vil redusere risikoen for avvik, kan en betalingsjournal for kunder opprettes og posteres automatisk når betalingsjournalen for kunder posteres.

1. Gå til **Salg og markedsføring \> Kunder \> Alle kunder**.
1. Velg **Konsernintern** i fanen **Generelt** i handlingsruten.
1. Hvis du vil definere konserninterne betalinger for kunder på **Konsernintern**-siden for salgsordrer, velger du koblingen **Salgsordrepolicyer**.
1. I **Betalingsjournal**-feltet velger du betalingsjournalen for kunder du vil registrere konserninterne leverandørbetalinger til. Du kan definere dette på siden **Kundeparametere**.
1. Hvis du vil postere til denne journalen automatisk, merker du av for **Poster journal automatisk**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
