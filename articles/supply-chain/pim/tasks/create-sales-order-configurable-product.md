---
title: Opprette en salgsordre for et konfigurerbart produkt
description: Denne prosedyren viser hvordan du bruker en konfigurasjonsmal for et produkt på en salgsordre.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921295"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Opprette en salgsordre for et konfigurerbart produkt

[!include [banner](../../includes/banner.md)]

Denne prosedyren viser hvordan du bruker en konfigurasjonsmal for et produkt på en salgsordre. Dette eksemplet bruker høyttalermodellen D0006 i demonstrasjonsdatafirmaet USMF. En salgsordrebehandler bruker vanligvis denne prosedyren.

## <a name="create-a-sales-order"></a>Opprette en salgsordre

1. Gå til **Salg og markedsføring \> Arbeidsområder \> Salgsordrebehandling og -spørring**.
1. Velg **Ny**.
1. Velg **Salgsordre**.
1. Velg *US-001* i **Kundekonto**-feltet. 
1. Velg **OK**.
1. Velg *D0006* i feltet **Varenummer**.
    * Du må velge et konfigurerbart produkt for denne oppgaven.  
1. Velg **Produkt og forsyning**.
1. Velg **Konfigurer linje**.
    * Vær oppmerksom på at prisen er endret, basert på konfigurasjonen som ble valgt, og at feltet for å **ta med kabel** er satt til *Sann*.  
    * Vær oppmerksom på standardprisen og innstillingene som er valgt for kabelen.  
1. Velg **Lastmal**.
    * Dette eksemplet viser hvordan du kan bruke en mal for å velge en forhåndsdefinert konfigurasjon. Hvis du bruker denne prosedyren som en oppgaveveiledning og ønsker å se andre attributtverdier som er tilgjengelige, må du velge **Lås opp**-knappen.  
1. Velg **OK**.
1. Velg **OK**.
1. Vis delen **Linjedetaljer**.
1. Velg **Produkt**-fanen.
    * Konfigurasjonen for varen er nå oppført under produktdimensjonene.  
1. Lukk siden.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]