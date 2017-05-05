---
title: Karanteneordrer
description: "Denne artikkelen beskriver hvordan karanteneordrer brukes til å blokkere beholdning."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 394276e6908f2c1f6bc72eea061facc3afe701e9
ms.lasthandoff: 03/31/2017


---

# <a name="quarantine-orders"></a>Karanteneordrer

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan karanteneordrer brukes til å blokkere beholdning. 

Karanteneordrer kan brukes til å blokkere lager. Du kan for eksempel sette varer i karantene av kvalitetskontrollgrunner. Beholdning som har blitt satt i karantene overføres til et karantenelager. **Obs!** Hvis du bruker avanserte lagerstyringsprosesser (i Lagerstyring), brukes behandling av karanteneordrer bare for retur av salgsordrer.

## <a name="quarantine-onhand-inventory-items"></a>Sette lagerbeholdningsvarer i karantene
Når du setter varer i karantene, kan du opprette karanteneordrene manuelt eller konfigurere systemet til å opprette karanteneordrene automatisk under innkommende behandling. Du kan opprette karanteneordrer automatisk ved å velge **Karantenestyring** i kategorien **Beholdningspolicyer** på siden **Varemodellgrupper**. Du må også angi et standard karantenelager i feltet **Karantenelager** for de mottakende lagrene. Når den fysiske lagerbeholdningen er registrert i en bestilling eller produksjonsordre, flyttes varer i karantene automatisk til et karantenelager i Microsoft Dynamics 365 for Operations. Denne bevegelsen oppstår fordi statusen for karanteneordren er endret til **Startet**. Når du opprette karanteneordrer manuelt, trenger ikke den gjeldende varen være definert for karantenestyring i den tilknyttede varemodellgruppen. For denne prosessen må du angi lagerbeholdningen som skal være satt i karantene, og karantenelageret som skal brukes. Du kan bruke karanteneordrestatusene til å planlegge prosessen.

## <a name="quarantine-order-statuses"></a>Statuser for karanteneordrer
Karanteneordrer kan ha følgende statuser:

-   Opprettet
-   Startet
-   Ferdigmeldt
-   Avsluttet

### <a name="created"></a>Opprettet

Når en karanteneordre er opprettet manuelt, men varen ennå ikke er plassert i karantenelageret, har karanteneordren statusen **Opprettet**. Det genereres to lagertransaksjoner. Den ene transaksjonen er en avgangstransaksjon som kan ha statusene **I ordre**, **Fysisk reservert** eller **Plukket**. Den andre transaksjonen er en mottakstransaksjon som kan ha statusene **Bestilt** eller** Registrert** i karantenelageret. Du kan reservere, plukke og registrere oppdateringer i beholdningen ved hjelp av de vanlige prosessene.

### <a name="started"></a>Startet

Når en karanteneordre har statusen **Startet**, blir beholdningen overført fra det vanlige lageret til karantenelageret, og to lagertransaksjoner blir generert. Én transaksjon har statusen **Fratrukket**, og den andre transaksjonen har statusen **Mottatt**. Samtidig blir to lagertransaksjoner opprettet for å håndtere returoverføringen. Disse transaksjonene er ikke datert. Én transaksjon har statusen **Fysisk reservert**, og den andre transaksjonen har statusen **Bestilt**.

### <a name="reported-as-finished"></a>Ferdigmeldt

Ved å klikke **Rapporter som fullført** kan du rapportere en startet karanteneordre som fullført. Varen frigis fra karantenen, men flyttes ikke ennå tilbake til det vanlige lageret. Flyttingen tilbake til det vanlige lageret kan behandles via en vareankomstjournal som kan startes under ferdigmeldingsprosessen.

### <a name="ended"></a>Avsluttet

Når en karanteneordre blir ferdig, flyttes varen fra karantenelageret tilbake til det vanlige lageret. Statusen for varetransaksjonen settes til **Solgt** i karantenelageret og **Kjøpt** i det vanlige lageret.

## <a name="quarantine-order-scrap"></a>Karanteneordresvinn
Du kan kassere beholdning som en del av karantenebestillingsprosessen. Når du behandler svinn, blir statusen for beholdningen angitt til **Solgt** av en avgangstransaksjon fra karantenelageret.

<a name="see-also"></a>Se også
--------

[Lagerblokkering](inventory-blocking.md)



