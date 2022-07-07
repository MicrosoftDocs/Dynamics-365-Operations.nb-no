---
title: Typer funksjonslokasjoner
description: Denne artikkelen beskriver hvordan du oppretter funksjonslokasjonstyper i Aktivastyring.
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
ms.openlocfilehash: 0c44e503900bd157d7f0159cdf2b2d0c1fb3393f
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015790"
---
# <a name="functional-location-types"></a>Typer funksjonslokasjoner

[!include [banner](../../includes/banner.md)]

 

Denne artikkelen beskriver hvordan du oppretter funksjonslokasjonstyper i Aktivastyring. Funksjonslokasjonstyper brukes til å administrere krav til funksjonslokasjoner, inkludert hvordan aktiva installeres på en funksjonslokasjon. Du kan definere aktivatyper, vedlikeholdsplaner, funksjonslokasjonsattributter og krav til aktivaattributter som skal brukes på en funksjonslokasjon som bruker den bestemte funksjonslokasjonstypen. Når du oppretter en funksjonslokasjon, er funksjonslokasjonstypen obligatorisk.

>[!NOTE] 
>Hvis du vil arbeide med funksjonslokasjoner, må du opprette en standard funksjonslokasjon som bare skal brukes til å opprette nye aktiva. For denne standard funksjonslokasjonen bør du opprette en standard funksjonslokasjonstype som er svært enkel, og tillater at flere aktiva installeres på standard funksjonslokasjon. Se [Opprette funksjonslokasjoner](../functional-locations/create-functional-locations.md) hvis du vil ha mer informasjon om hvordan du definerer funksjonslokasjoner.

## <a name="create-a-default-functional-location-type"></a>Opprette en standard funksjonslokasjonstype

Denne fremgangsmåten viser hvordan du oppretter en standard funksjonslokasjonstype som skal brukes for en standard funksjonslokasjon.

1. Velg **Aktivastyring** > **Oppsett** > **Funksjonslokasjoner** > **Funksjonslokasjonstyper**.
2. Velg **Ny** for å opprette en funksjonslokasjonstype.
3. Sett inn en type-ID for funksjonslokasjonen i feltet **Funksjonslokasjonstype**, for eksempel "Standard", og et navn i **Navn**-feltet.
4. Velg en livssyklusmodell i feltet **Livssyklusmodell for funksjonslokasjon**.
5. Velg Ja på knappen **Flere aktiva** for å tillate at flere aktiva kan installeres på en funksjonslokasjon (standard funksjonslokasjon) som bruker denne typen.

Nå opprettes standard funksjonslokasjonstype, som bare skal brukes på en standard funksjonslokasjon. Du bør ikke legge til flere krav eller begrensninger for denne standard funksjonslokasjonstypen.


## <a name="create-functional-location-types"></a>Opprette funksjonslokasjonstyper

1. Velg **Aktivastyring** > **Oppsett** > **Funksjonslokasjoner** > **Funksjonslokasjonstyper**.
2. Velg **Ny** for å opprette en funksjonslokasjonstype.
3. Sett inn en type-ID for funksjonslokasjonen i feltet **Funksjonslokasjonstype** og et navn i **Navn**-feltet.
4. Velg en livssyklusmodell i feltet **Livssyklusmodell for funksjonslokasjon**. Se [Livssyklustilstander for funksjonslokasjoner](../setup-for-functional-locations/functional-location-stages.md) for mer informasjon om livssyklustilstander for funksjonslokasjoner og livssyklusmodeller.
5. Velg Ja på knappen **Flere aktiva** hvis det skal være mulig å installere flere aktiva på et som bruker denne funksjonslokasjonstypen. Hvis du velger Nei, kan du bare installere *ett* aktivum på en funksjonslokasjon ved hjelp av denne funksjonslokasjonstypen.
6. Velg Ja på knappen **Oppdater aktivadimensjon** hvis du vil at aktiva installert på en funksjonslokasjon av denne typen automatisk skal bruke finansdimensjonene som er knyttet til funksjonslokasjonen. Dette betyr at hvis du endrer finansdimensjoner i skjemaet [Opprette funksjonslokasjoner](../functional-locations/create-functional-locations.md) og funksjonslokasjonen bruker en funksjonslokasjonstype med denne veksleknappen satt til "Ja", oppdateres finansdimensjoner automatisk på alle aktiva installert på denne funksjonslokasjonen.
7. Feltet **Aktivatype** brukes hvis du vil opprette *ett* aktivum automatisk for funksjonslokasjonen med samme ID og navn som funksjonslokasjonen du oppretter. Dette kan for eksempel være relevant hvis du oppretter en statisk funksjonslokasjon, for eksempel en bygning eller en rørledning. I så fall velger du aktivatypen du vil bruke for det automatisk opprettede aktivumet. Husk at hvis du velger noe i dette feltet, må knappen for **Flere aktiva** være satt til Nei.
8. I hurtigfanen **Aktivatyper** velger du aktivatypene som skal relateres til funksjonslokasjonstypen. Velg **Legg til linje**, og velg aktivatypene. Hvis du legger til aktivatyper her, kan bare aktiva som bruker disse aktivatypene, installeres på en funksjonslokasjon med denne funksjonslokasjonstypen. Hvis ingen aktivatyper er valgt på hurtigfanen **Aktivatyper**, kan alle aktivatyper installeres.
9. I hurtigfanen **Vedlikeholdsplaner** velger du vedlikeholdsplanene som automatisk skal defineres på nye funksjonslokasjoner ved hjelp av denne funksjonslokasjonstypen. Velg **Legg til linje**, og velg vedlikeholdsplanene. Hvis du legger til vedlikeholdsplaner her, kan bare disse planene brukes på en funksjonslokasjon ved hjelp av denne funksjonslokasjonstypen.
10. I hurtigfanen **Attributtkrav for aktiva** definerer du aktivaattributtene som automatisk skal defineres på nye funksjonslokasjoner ved hjelp av denne funksjonslokasjonstypen. Velg **Legg til linje**, og velg attributtet. Disse attributtkravene fungerer som retningslinjer. De valideres ikke mot attributter som er definert for et aktivum (**Aktivastyring** > **Aktiva** > **Alle aktiva** > velg aktivum på listesiden > **Generelt**-fanen > **Attributter**-knappen). Kravene til attributtet vises når du installerer aktiva på funksjonslokasjoner.
11. I hurtigfanen **Tillatte typer** velger du funksjonslokasjonstypene som skal være gyldige for underordnede funksjonslokasjonstyper som er relatert til en overordnet funksjonslokasjonstype, som bruker den valgte funksjonslokasjonstypen.
12. I hurtigfanen **Attributter** velger du funksjonslokasjonsattributtene som automatisk skal defineres på funksjonslokasjoner ved hjelp av denne funksjonslokasjonstypen. Velg **Legg til linje**, og velg attributtet.


>[!NOTE] 
>På hurtigfanen **Generelt** kan du få en oversikt over antall aktivatyper, vedlikeholdsplaner, krav til aktivaattributter, tillatte typer, attributter og funksjonslokasjoner som er definert for funksjonslokasjonstypen. Feltet **Funksjonslokasjoner** viser antall funksjonslokasjoner som bruker funksjonslokasjonstypen. Du kan bruke **Kopier**-knappen til å kopiere innstillinger fra en funksjonslokasjonstype til den valgte funksjonslokasjonstypen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]