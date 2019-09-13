---
title: Motta varer i bestilling fra varebehov
description: Dette emnet forklarer hvordan du mottar varer på en bestilling fra et varebehov.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7afdae65c5ae7e3196c6b9f142dd87aec39b5ea3
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867301"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Motta varer i bestilling fra varebehov

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emnet forklarer hvordan du mottar varer på en bestilling fra et varebehov.

Når du bruker et varebehov i stedet for en varetransaksjon, kan du planlegge levering like før varen faktisk brukes, opprette en bestilling, inkludere varen i rammeverket for forretningsavtalen, og inkludere varebehovet i produksjonsplanlegging. 

Denne oppgaven bruker USSI-datasettet.

1. Gå til **Moduler > Prosjektstyring og regnskap > Prosjekter > Alle prosjekter** i navigasjonsruten.
2. Velg koblingen i den ønskede raden i listen.
3. Velg **Plan** i handlingsruten.
4. Velg **Varebehov**.
5. Velg **Ny**.
6. Angi eller velg en verdi i feltet **Varenummer** i den nye raden.
7. Angi et tall i **Antall**-feltet.
8. Velg **Lagre**.
9. Velg **Administrer** på handlingsruten.
10. Velg **Funksjoner**.
11. Velg **Opprett bestilling**.
12. Merk av for **Inkluder alt**.
13. Angi eller velg en verdi i **Leverandørkonto**-feltet.
14. Velg **OK**.
15. I navigasjonsruten går du til **Moduler > Leverandører > Bestillinger > Alle bestillinger**.
16. Velg koblingen i den ønskede raden i listen.
17. Klikk **Innkjøp** i handlingsruten.
18. Velg **Bekreft**.
19. Klikk på **Mottak** i handlingsruten.
20. Velg **Produktkvittering**.
21. Skriv inn en verdi i feltet **Produktkvittering**.
22. Velg **OK**.

