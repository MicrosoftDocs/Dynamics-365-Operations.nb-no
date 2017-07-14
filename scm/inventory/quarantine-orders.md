---
title: Karanteneordrer
description: "Denne artikkelen beskriver hvordan karanteneordrer brukes til å blokkere beholdning."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: ec3d54e8e08850cd81891e7058b2b787e08b0fb9
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017


---

# Karanteneordrer
<a id="quarantine-orders" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan karanteneordrer brukes til å blokkere beholdning. 

Karanteneordrer kan brukes til å blokkere lager. Du kan for eksempel sette varer i karantene av kvalitetskontrollgrunner. Beholdning som har blitt satt i karantene overføres til et karantenelager. **Obs!** Hvis du bruker avanserte lagerstyringsprosesser (i Lagerstyring), brukes behandling av karanteneordrer bare for retur av salgsordrer.

## Sette lagerbeholdningsvarer i karantene
<a id="quarantine-onhand-inventory-items" class="xliff"></a>
Når du setter varer i karantene, kan du opprette karanteneordrene manuelt eller konfigurere systemet til å opprette karanteneordrene automatisk under innkommende behandling. Du kan opprette karanteneordrer automatisk ved å velge **Karantenestyring** i kategorien **Beholdningspolicyer** på siden **Varemodellgrupper**. Du må også angi et standard karantenelager i feltet **Karantenelager** for de mottakende lagrene. Når den fysiske lagerbeholdningen er registrert i en bestilling eller produksjonsordre, flyttes varer i karantene automatisk til et karantenelager i Microsoft Dynamics 365 for Finance and Operations. Denne bevegelsen oppstår fordi statusen for karanteneordren er endret til **Startet**. Når du opprette karanteneordrer manuelt, trenger ikke den gjeldende varen være definert for karantenestyring i den tilknyttede varemodellgruppen. For denne prosessen må du angi lagerbeholdningen som skal være satt i karantene, og karantenelageret som skal brukes. Du kan bruke karanteneordrestatusene til å planlegge prosessen.

## Statuser for karanteneordrer
<a id="quarantine-order-statuses" class="xliff"></a>
Karanteneordrer kan ha følgende statuser:

-   Opprettet
-   Startet
-   Ferdigmeldt
-   Avsluttet

### Opprettet
<a id="created" class="xliff"></a>

Når en karanteneordre er opprettet manuelt, men varen ennå ikke er plassert i karantenelageret, har karanteneordren statusen **Opprettet**. Det genereres to lagertransaksjoner. Den ene transaksjonen er en avgangstransaksjon som kan ha statusene **I ordre**, **Fysisk reservert** eller **Plukket**. Den andre transaksjonen er en mottakstransaksjon som kan ha statusene **Bestilt** eller **Registrert** i karantenelageret. Du kan reservere, plukke og registrere oppdateringer i beholdningen ved hjelp av de vanlige prosessene.

### Startet
<a id="started" class="xliff"></a>

Når en karanteneordre har statusen **Startet**, blir beholdningen overført fra det vanlige lageret til karantenelageret, og to lagertransaksjoner blir generert. Én transaksjon har statusen **Fratrukket**, og den andre transaksjonen har statusen **Mottatt**. Samtidig blir to lagertransaksjoner opprettet for å håndtere returoverføringen. Disse transaksjonene er ikke datert. Én transaksjon har statusen **Fysisk reservert**, og den andre transaksjonen har statusen **Bestilt**.

### Ferdigmeldt
<a id="reported-as-finished" class="xliff"></a>

Ved å klikke **Rapporter som fullført** kan du rapportere en startet karanteneordre som fullført. Varen frigis fra karantenen, men flyttes ikke ennå tilbake til det vanlige lageret. Flyttingen tilbake til det vanlige lageret kan behandles via en vareankomstjournal som kan startes under ferdigmeldingsprosessen.

### Avsluttet
<a id="ended" class="xliff"></a>

Når en karanteneordre blir ferdig, flyttes varen fra karantenelageret tilbake til det vanlige lageret. Statusen for varetransaksjonen settes til **Solgt** i karantenelageret og **Kjøpt** i det vanlige lageret.

## Karanteneordresvinn
<a id="quarantine-order-scrap" class="xliff"></a>
Du kan kassere beholdning som en del av karantenebestillingsprosessen. Når du behandler svinn, blir statusen for beholdningen angitt til **Solgt** av en avgangstransaksjon fra karantenelageret.

Se også
<a id="see-also" class="xliff"></a>
--------

[Lagerblokkering](inventory-blocking.md)




