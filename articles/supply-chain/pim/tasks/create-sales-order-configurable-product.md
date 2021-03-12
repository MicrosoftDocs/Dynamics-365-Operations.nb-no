---
title: Opprette en salgsordre for et konfigurerbart produkt
description: Denne prosedyren viser hvordan du bruker en konfigurasjonsmal for et produkt på en salgsordre.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77404694b3426f9ef051721191b607f91c908cc4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992326"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Opprette en salgsordre for et konfigurerbart produkt

[!include [banner](../../includes/banner.md)]

Denne prosedyren viser hvordan du bruker en konfigurasjonsmal for et produkt på en salgsordre. Dette eksemplet bruker høyttalermodellen D0006 i demonstrasjonsdatafirmaet USMF. En salgsordrebehandler bruker vanligvis denne prosedyren.


## <a name="create-a-sales-order"></a>Opprette en salgsordre
1. Klikk på Salgsordrebehandling og -spørring.
2. Klikk på Ny.
3. Klikk på Salgsordre.
4. Velg US-001 i Kundekonto-feltet. 
5. Klikk på OK.
6. Velg D0006 i feltet Varenummer.
    * Du må velge et konfigurerbart produkt for denne oppgaven.  
7. Klikk på Produkt og forsyning.
8. Klikk på Konfigurer linje.
    * Vær oppmerksom på at prisen er endret, basert på konfigurasjonen som ble valgt, og at feltet for å ta med kabel er satt til sann.  
    * Vær oppmerksom på standardprisen og innstillingene som er valgt for kabelen.  
9. Klikk på Last inn mal.
    * Dette eksemplet viser hvordan du kan bruke en mal for å velge en forhåndsdefinert konfigurasjon. Hvis du bruker denne prosedyren som en oppgaveveiledning og ønsker å se andre attributtverdier som er tilgjengelige, må du klikke Lås opp-knappen.  
10. Klikk på OK.
11. Klikk på OK.
12. Vis seksjonen Linjedetaljer.
13. Klikk på fanen Produkt.
    * Konfigurasjonen for varen er nå oppført under produktdimensjonene.  
14. Lukk siden.

## <a name="select-the-product-configuration"></a>Velge produktkonfigurasjonen

