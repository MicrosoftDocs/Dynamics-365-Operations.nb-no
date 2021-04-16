---
title: Synkronisere dato og klokkeslett i importjobber
description: Bruk UTC-tidssoner i importjobber for å unngå problemer med tidssonekonvertering.
author: Sunil-Garg
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c0ec805a20a525989e0133e5dffb29ce3fed39
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748675"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>Synkronisere dato og klokkeslett i importjobber

[!include [banner](../includes/banner.md)]

Det er viktig å angi tidssonen UTC (Coordinated Universal Time) for importjobben. Du får kanskje uventede datoer og klokkeslett i de importerte dataene hvis du bruker en annen innstilling. Uten riktig innstilling konverterer importprosessen UTC-datoen til det lokale formatet, og deretter konverterer systeminnstillingene den på nytt.

Denne doble konverteringen gjør at datoer endres mellom programmer. Den doble konverteringen kan for eksempel gjøre at startdatoen for en ansatt, blir forskjellige i Dynamics 365 Human Resources og Dynamics 365 Finance på grunn av forskjeller i lokale tidssoner. Du løser dette problemet ved å angi UTC for importjobben.

1. Velg **Databehandling** i Dynamics 365 Finance and Operations.

2. Velg **Importer prosjekter**, og velg deretter prosjektet.

3. Velg **CSV-Unicode** under **Kildedatoformat**.

   [![Endre kildedatoformatet til UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. Endre **Tidssone** til **Coordinated Universal Timezone**, og endre **Språk** til **En-US**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]