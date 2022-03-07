---
title: Arbeidsstedstyper
description: Dette emnet beskriver hvordan du oppretter arbeidsstedstyper i Aktivastyring.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 301dc838ed204ebe488dd167df75fc84131f235f64285c6ae99c62ee1188362c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739161"
---
# <a name="functional-location-types"></a>Arbeidsstedstyper

[!include [banner](../../includes/banner.md)]

 

Dette emnet beskriver hvordan du oppretter arbeidsstedstyper i Aktivastyring. Arbeidsstedstyper brukes til å administrere krav til arbeidssteder, inkludert hvordan aktiva installeres på et arbeidssted. Du kan definere aktivatyper, vedlikeholdsplaner, arbeidsstedsattributter og krav til aktivaattributter som skal brukes på et arbeidssted som bruker den bestemte arbeidsstedstypen. Når du oppretter et arbeidssted, er arbeidsstedstypen obligatorisk.

>[!NOTE] 
>Hvis du vil arbeide med arbeidssteder, må du opprette et standard arbeidssted som bare skal brukes til å opprette nye aktiva. For dette standard arbeidsstedet bør du opprette en standard arbeidsstedstype som er svært enkel, og tillater at flere aktiva installeres på standardarbeidsstedet. Se [Opprette arbeidssteder](../functional-locations/create-functional-locations.md) hvis du vil ha mer informasjon om hvordan du definerer arbeidssteder.

## <a name="create-a-default-functional-location-type"></a>Opprette en standard arbeidsstedstype

Denne fremgangsmåten viser hvordan du oppretter en standard arbeidsstedstype som skal brukes for et standard arbeidssted.

1. Velg **Aktivastyring** > **Oppsett** > **Arbeidssteder** > **Arbeidsstedstyper**.
2. Velg **Ny** for å opprette en arbeidsstedstype.
3. Sett inn en type-ID for arbeidsstedet i feltet **Arbeidsstedstype**, for eksempel "Standard", og et navn i **Navn**-feltet.
4. Velg en livssyklusmodell i feltet **Livssyklusmodell for arbeidssted**.
5. Velg Ja på knappen **Flere aktiva** for å tillate at flere aktiva kan installeres på et arbeidssted (standardarbeidsstedet) som bruker denne typen.

Nå opprettes standard arbeidsstedstype, som bare skal brukes på et standard arbeidssted. Du bør ikke legge til flere krav eller begrensninger for denne standard arbeidsstedstypen.


## <a name="create-functional-location-types"></a>Opprette arbeidsstedstyper

1. Velg **Aktivastyring** > **Oppsett** > **Arbeidssteder** > **Arbeidsstedstyper**.
2. Velg **Ny** for å opprette en arbeidsstedstype.
3. Sett inn en type-ID for arbeidsstedet i feltet **Arbeidsstedstype** og et navn i **Navn**-feltet.
4. Velg en livssyklusmodell i feltet **Livssyklusmodell for arbeidssted**. Se [Livssyklustilstander for arbeidssteder](../setup-for-functional-locations/functional-location-stages.md) for mer informasjon om livssyklustilstander for arbeidssteder og livssyklusmodeller.
5. Velg Ja på knappen **Flere aktiva** hvis det skal være mulig å installere flere aktiva på et som bruker denne arbeidsstedstypen. Hvis du velger Nei, kan du bare installere *ett* aktivum på et arbeidssted ved hjelp av denne arbeidsstedstypen.
6. Velg Ja på knappen **Oppdater aktivadimensjon** hvis du vil at aktiva installert på et arbeidssted av denne typen automatisk skal bruke finansdimensjonene som er knyttet til arbeidsstedet. Dette betyr at hvis du endrer finansdimensjoner i skjemaet [Opprette arbeidssteder](../functional-locations/create-functional-locations.md) og arbeidsstedet bruker en arbeidsstedstype med denne veksleknappen satt til "Ja", oppdateres finansdimensjoner automatisk på alle aktiva installert på dette arbeidsstedet.
7. Feltet **Aktivatype** brukes hvis du vil opprette *ett* aktivum automatisk for arbeidsstedet med samme ID og navn som arbeidsstedet du oppretter. Dette kan for eksempel være relevant hvis du oppretter et statisk arbeidssted, for eksempel en bygning eller en rørledning. I så fall velger du aktivatypen du vil bruke for det automatisk opprettede aktivumet. Husk at hvis du velger noe i dette feltet, må knappen for **Flere aktiva** være satt til Nei.
8. I hurtigfanen **Aktivatyper** velger du aktivatypene som skal relateres til arbeidsstedstypen. Velg **Legg til linje**, og velg aktivatypene. Hvis du legger til aktivatyper her, kan bare aktiva som bruker disse aktivatypene, installeres på et arbeidssted med denne arbeidsstedstypen. Hvis ingen aktivatyper er valgt på hurtigfanen **Aktivatyper**, kan alle aktivatyper installeres.
9. I hurtigfanen **Vedlikeholdsplaner** velger du vedlikeholdsplanene som automatisk skal defineres på nye arbeidssteder ved hjelp av denne arbeidsstedstypen. Velg **Legg til linje**, og velg vedlikeholdsplanene. Hvis du legger til vedlikeholdsplaner her, kan bare disse planene brukes på et arbeidssted ved hjelp av denne arbeidsstedstypen.
10. I hurtigfanen **Attributtkrav for aktiva** definerer du aktivaattributtene som automatisk skal defineres på nye arbeidssteder ved hjelp av denne arbeidsstedstypen. Velg **Legg til linje**, og velg attributtet. Disse attributtkravene fungerer som retningslinjer. De er ikke validert mot attributter som er definert på et aktivum (**Aktivastyring** > **Felles** > **Aktiva** > **Alle aktiva** > velg aktivum på listesiden > **Generelt**-fanen > **Attributter**-knappen). Kravene til attributtet vises når du installerer aktiva på arbeidssteder.
11. I hurtigfanen **Tillatte typer** velger du arbeidsstedstypene som skal være gyldige for underordnede arbeidsstedstyper som er relatert til en overordnet arbeidsstedstype, som bruker den valgte arbeidsstedstypen.
12. I hurtigfanen **Attributter** velger du arbeidsstedsattributtene som automatisk skal defineres på arbeidssteder ved hjelp av denne arbeidsstedstypen. Velg **Legg til linje**, og velg attributtet.


>[!NOTE] 
>På hurtigfanen **Generelt** kan du få en oversikt over antall aktivatyper, vedlikeholdsplaner, krav til aktivaattributter, tillatte typer, attributter og arbeidssteder som er definert for arbeidsstedstypen. Feltet **Arbeidssteder** viser antall arbeidssteder som bruker arbeidsstedstypen. Du kan bruke **Kopier**-knappen til å kopiere innstillinger fra en arbeidsstedstype til den valgte arbeidsstedstypen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]