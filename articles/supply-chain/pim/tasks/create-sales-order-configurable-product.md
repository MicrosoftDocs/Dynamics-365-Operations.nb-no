---
title: Opprette en salgsordre for et konfigurerbart produkt
description: Denne prosedyren viser hvordan du bruker en konfigurasjonsmal for et produkt på en salgsordre.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e42f121d1efa66f85a3dd811606962b907ed177d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570591"
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