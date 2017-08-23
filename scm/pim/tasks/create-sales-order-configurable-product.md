--- 
title: Opprette en salgsordre for et konfigurerbart produkt
description: "Denne prosedyren viser hvordan du bruker en konfigurasjonsmal for et produkt på en salgsordre."
author: BibiSp
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6546d504a2fda255cb5183408dfe84a3074543ab
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Opprette en salgsordre for et konfigurerbart produkt

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren viser hvordan du bruker en konfigurasjonsmal for et produkt på en salgsordre. Dette eksemplet bruker høyttalermodellen D0006 i demonstrasjonsdatafirmaet USMF. En salgsordrebehandler bruker vanligvis denne prosedyren.


## <a name="create-a-sales-order"></a>Opprette en salgsordre
1. Klikk Salgsordrebehandling og -spørring.
2. Klikk Ny.
3. Klikk Salgsordre.
4. Velg US-001 i Kundekonto-feltet. 
5. Klikk OK.
6. Velg D0006 i feltet Varenummer.
    * Du må velge et konfigurerbart produkt for denne oppgaven.  
7. Klikk Produkt og forsyning.
8. Klikk Konfigurer linje.
    * Vær oppmerksom på at prisen er endret, basert på konfigurasjonen som ble valgt, og at feltet for å ta med kabel er satt til sann.  
    * Vær oppmerksom på standardprisen og innstillingene som er valgt for kabelen.  
9. Klikk Last inn mal.
    * Dette eksemplet viser hvordan du kan bruke en mal for å velge en forhåndsdefinert konfigurasjon. Hvis du bruker denne prosedyren som en oppgaveveiledning og ønsker å se andre attributtverdier som er tilgjengelige, må du klikke Lås opp-knappen.  
10. Klikk OK.
11. Klikk OK.
12. Vis seksjonen Linjedetaljer.
13. Klikk kategorien Produkt.
    * Konfigurasjonen for varen er nå oppført under produktdimensjonene.  
14. Lukk siden.

## <a name="select-the-product-configuration"></a>Velge produktkonfigurasjonen

