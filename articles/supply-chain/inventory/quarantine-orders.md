---
title: Karanteneordrer
description: Dette emnet beskriver hvordan karanteneordrer brukes til å blokkere beholdning.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956188"
---
# <a name="quarantine-orders"></a>Karanteneordrer

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan karanteneordrer brukes til å blokkere beholdning.

Du kan bruke karanteneordrer til å blokkere beholdning. Du kan for eksempel sette varer i karantene av kvalitetskontrollgrunner. Beholdning som har blitt satt i karantene overføres til et karantenelager.

> [!NOTE]
> Hvis du bruker avanserte lagerstyringsprosesser (i Lagerstyring), brukes behandling av karanteneordrer bare for retur av salgsordrer.

## <a name="quarantine-on-hand-inventory-items"></a>Sette lagerbeholdningsvarer i karantene

Når du setter varer i karantene, kan du opprette karanteneordrene manuelt eller konfigurere systemet til å opprette dem automatisk under innkommende behandling.

Følg denne fremgangsmåten for å sette opp systemet slik at det automatisk genererer karanteneordrer.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Varemodellgrupper**.
1. Velg en relevant modellgruppe i listeruten, eller opprett en ny modellgruppe.
1. Merk av for **Overstyr reservering for vareproduksjon** i hurtigfanen **Karantenestyring**.
1. Lukk siden.
1. Angi et standard karantenelager i feltet **Karantenelager** for de mottakende lagrene.

Når en vare som er registrert som mottatt på lageret, tilhører en modellgruppe der det er merket av for **Karantenestyring**, genererer systemet en karanteneordre for den. Karanteneordren ber arbeiderne om å flytte varen til karantenelageret.

Når du oppretter karanteneordrer manuelt på **Karanteneordrer**-siden, trenger ikke den gjeldende varen være definert for karantenestyring i den tilknyttede varemodellgruppen. For denne prosessen må du angi lagerbeholdningen som skal være satt i karantene, og karantenelageret som skal brukes. Du kan bruke karanteneordrestatusene til å planlegge prosessen.

## <a name="quarantine-order-statuses"></a>Statuser for karanteneordrer

Karanteneordrer kan ha følgende statuser:

- Opprettet
- Startet
- Ferdigmeldt
- Avsluttet

### <a name="created"></a>Opprettet

Når en karanteneordre er opprettet manuelt, men varen ennå ikke er plassert i karantenelageret, har karanteneordren statusen **Opprettet**. Det genereres to lagertransaksjoner. Den ene transaksjonen er en avgangstransaksjon som kan ha statusene **I ordre**, **Fysisk reservert** eller **Plukket**. Den andre transaksjonen er en mottakstransaksjon som kan ha statusene **Bestilt** eller **Registrert** i karantenelageret. Du kan reservere, plukke og registrere oppdateringer i beholdningen ved hjelp av de vanlige prosessene.

### <a name="started"></a>Startet

Når en karanteneordre har statusen **Startet**, blir beholdningen overført fra det vanlige lageret til karantenelageret, og to lagertransaksjoner blir generert. Én transaksjon har statusen **Fratrukket**, og den andre transaksjonen har statusen **Mottatt**. Samtidig blir to lagertransaksjoner opprettet for å håndtere returoverføringen. Disse transaksjonene er ikke datert. Én transaksjon har statusen **Fysisk reservert**, og den andre transaksjonen har statusen **Bestilt**.

### <a name="reported-as-finished"></a>Ferdigmeld

Hvis du vil rapportere en startet karanteneordre som fullført, åpner du ordren og velger **Ferdigmeld** i handlingsruten. Varen frigis fra karantenen, men flyttes ikke ennå tilbake til det vanlige lageret. Flyttingen tilbake til det vanlige lageret kan behandles via en vareankomstjournal som kan startes under ferdigmeldingsprosessen.

### <a name="ended"></a>Avsluttet

Når en karanteneordre blir ferdig, flyttes varen fra karantenelageret tilbake til det vanlige lageret. Statusen for varetransaksjonen settes til *Solgt* i karantenelageret og *Kjøpt* i det vanlige lageret.

## <a name="quarantine-order-scrap"></a>Karanteneordresvinn

Du kan kassere beholdning som en del av karantenebestillingsprosessen. Når du behandler svinn, blir statusen for beholdningen angitt til *Solgt* av en avgangstransaksjon fra karantenelageret.

## <a name="additional-resources"></a>Tilleggsressurser

- [Lagerblokkering](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
