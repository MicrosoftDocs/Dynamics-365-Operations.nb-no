---
title: Innkjøpsrekvisisjoner
description: Dette emnet beskriver hvordan innkjøpsrekvisisjoner støttes i planleggingsoptimalisering.
author: ChristianRytt
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 20b4012e054a25d7d21c6f017d8ebcf18f6ee28d
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501084"
---
# <a name="purchase-requisitions"></a>Innkjøpsrekvisisjoner

Hovedplanlegging kan etterfylle godkjente innkjøpsrekvisisjoner. Brukere trenger derfor ikke å bruke en arbeidsflyt til å opprette bestillinger for å dekke innkjøpsrekvisisjoner. Innkjøpsrekvisisjoner kan i stedet dekkes av hovedplanlegging. På grunn av denne funksjonaliteten kan en innkjøpsrekvisisjon produsere en bestilling, en overføringsordre eller en produksjonsordre, avhengig av verdien for **Type planlagt bestilling** som er angitt for det tilknyttede produktet.

## <a name="enable-master-plans-to-include-requisitions"></a>Aktivere hovedplaner for å inkludere rekvisisjoner

Følg denne fremgangsmåten for å inkludere rekvisisjoner under dekningsberegningen for en hovedplan.

1. Gå til **Hovedplanlegging** \> **Oppsett** \> **Planer** \> **Hovedplaner**.
1. Opprett eller velg en hovedplan.
1. I hurtigfanen **Generelt** angir du *Ja* for alternativet **Inkluder rekvisisjoner**.
1. Gjenta trinn 2 og 3 for hver ytterligere hovedplan der du vil ta med rekvisisjoner.

## <a name="approved-requisitions-time-fence"></a>Horisont for godkjente rekvisisjoner

*Horisonten for godkjente rekvisisjoner* fastsetter hvor langt tilbake (i dager) en hovedplan skal ta med behov fra godkjente etterfyllingsrekvisisjoner. Du kan angi en horisont for godkjente rekvisisjoner både på dekningsgruppenivået og hovedplannivået.

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a>Angi horisonten for godkjente rekvisisjoner for en dekningsgruppe

1. Gå til **Hovedplanlegging** \> **Oppsett** \> **Dekning** \> **Dekningsgrupper**.
1. Opprett eller velg en dekningsgruppe.
1. Angi antallet dager som skal tas med i horisonten, i feltet **Godkjente rekvisisjoner - horisont (dager)** i hurtigfanen **Annet**.
1. Gjenta trinn 2 og 3 for hver ytterligere dekningsgruppe der du vil angi en horisont for godkjente rekvisisjoner.

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a>Angi horisonten for godkjente rekvisisjoner for individuelle hovedplaner

Når du angir en horisont for godkjente rekvisisjoner for en individuell hovedplan, overstyrer innstillingen horisontinnstillingen for enhver gjeldende dekningsgruppe.

1. Gå til **Hovedplanlegging** \> **Oppsett** \> **Planer** \> **Hovedplaner**.
1. Opprett eller velg en hovedplan.
1. Angi antallet dager som skal tas med i horisonten, i feltet **Godkjente rekvisisjoner - horisont (dager)** i hurtigfanen **Horisonter i dager**.
1. Gjenta trinn 2 og 3 for hver ytterligere hovedplan der du vil angi en horisont for godkjente rekvisisjoner.

> [!IMPORTANT]
> **Kommer snart:** Horisonter for godkjente rekvisisjoner støttes ikke ennå for planleggingsoptimalisering. Før de støttes, ignoreres alle verdier du angir i feltet **Godkjente rekvisisjoner - horisont (dager)**.

## <a name="independent-supply-regardless-of-coverage-code"></a>Uavhengig forsyning, uavhengig av dekningskode

Innkjøpsrekvisisjoner dekkes alltid av uavhengige planlagte bestillinger, uavhengig av dekningskode. Denne virkemåten sikrer klar sporbarhet og klare arbeidsflyter mellom innkjøpsrekvisisjoner og etterfyllingsordrer.

### <a name="example-1"></a>Eksempel 1

Et produkt er konfigurert slik at det har **Dekningskode**-verdien *Min./maks.* Det har følgende statuser for beholdning og rekvisisjon:

- Lagerbeholdningsantall = 10.
- Minimumslagerantall = 15.
- Maksimumslagerantall = 20.
- Det finnes en innkjøpsrekvisisjon for ett stykk. Ønsket dato for den er i dag.

Når hovedplanlegging kjører, opprettes det to planlagte bestillinger: én for 10 stykker for å etterfylle beholdningen til maksimumsantallet, og én for ett stykk for å etterfylle innkjøpsrekvisisjonen.

### <a name="example-2"></a>Eksempel 2

Et produkt er konfigurert slik at det har **Dekningskode**-verdien *Min./maks.* Det har følgende statuser for beholdning og rekvisisjon:

- Lagerbeholdningsantall = 17.
- Minimumslagerantall = 15.
- Maksimumslagerantall = 20.
- Det finnes en innkjøpsrekvisisjon for ett stykk. Ønsket dato for den er i dag.

Når hovedplanleggingen kjører, opprettes det én planlagt bestilling for ett stykk for å etterfylle innkjøpsrekvisisjonen.

### <a name="example-3"></a>Eksempel 3

Et produkt er konfigurert slik at det har **Dekningskode**-verdien *Periode* og en periodelengde på sju dager. Det har følgende statuser for beholdning, salgsordre og rekvisisjon:

- Lagerbeholdningsantall = 0.
- Det finnes en salgsordre for fem stykker. Forventet forsendelsesdato er i dag pluss én dag.
- Det finnes en innkjøpsrekvisisjon for tre stykker. Ønsket dato for den er i dag pluss tre dager.

Når hovedplanlegging kjører, opprettes det to planlagte bestillinger: én for tre stykker for å etterfylle innkjøpsrekvisisjonen, og én for fem stykker for å etterfylle salgsordrebehovet.

> [!NOTE]
> Når en planlagt bestilling som er utlignet mot en innkjøpsrekvisisjon, autoriseres, beholder planleggingsmotoren utligningen mot innkjøpsrekvisisjonen. Hvis den autoriserte bestillingen senere mangler noe av antallet som kreves for å oppfylle innkjøpsrekvisisjonen, oppretter systemet en ny planlagt bestilling for differansen.

Hvis du vil ha mer informasjon om innkjøpsrekvisisjoner, kan du se [Oversikt over innkjøpsrekvisisjon](../../procurement/purchase-requisitions-overview.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]