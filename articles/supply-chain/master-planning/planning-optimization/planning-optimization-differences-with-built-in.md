---
title: Forskjeller mellom innebygd hovedplanlegging og planleggingsoptimalisering
description: Dette emnet viser funksjoner som Planleggingsoptimalisering ennå ikke støtter, og som ikke er oppført på siden Analyse for tilpasning av planleggingsoptimalisering.
author: t-benebo
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: c73587015d6714c409819ab19ad68685aaa71cf7
ms.sourcegitcommit: 70289a33b0a6ff3f9418d91a928db452cfd815bd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2022
ms.locfileid: "8618267"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Forskjeller mellom innebygd hovedplanlegging og planleggingsoptimalisering

[!include [banner](../../includes/banner.md)]

Resultatet av planleggingsoptimalisering kan være forskjellig fra den innebygde hovedplanleggingsmotoren. Forskjellen kan også skyldes ventende funksjoner. Dette emnet viser funksjoner som Planleggingsoptimalisering ennå ikke støtter, og som ikke er oppført på siden **[Analyse for tilpasning av planleggingsoptimalisering](planning-optimization-fit-analysis.md)**.

| Funksjon | Gjeldende virkemåte i Planleggingsoptimalisering |
|---|---|
| Produkter med faktisk vekt | Produkter med faktisk vekt betraktes som vanlige produkter.|
| Utvidbare dimensjoner | Utvidbare dimensjoner er tomme i planlagte bestillinger selv om det er merket av for **Dekningsplanlegg etter dimensjon** på siden **Lagringsdimensjonsgrupper** eller **Sporingsdimensjonsgrupper**. |
| Filtrerte produksjonsutkjøringer | Hvis du vil ha mer informasjon, kan du se [Produksjonsplanlegging – filtre](production-planning.md#filters). |
| Prognoseplanlegging | Prognoseplanlegging støttes ikke. Vi anbefaler at du bruker hovedplanlegging der en prognosemodell er tilordnet hovedplanen. |
| Nummersekvenser for planlagte ordrer | Nummerserier for planlagte ordrer støttes ikke. Planlagte bestillingsnumre genereres på servicesiden. Det planlagte bestillingsnummeret vises vanligvis med ti sifre, men rekkefølgen bygges faktisk på 20 tegn, med ti sifre tilordnet for planleggingskjøringen, og de ti andre sifrene for de planlagte bestillingene teller. |
| Planlegg kopiering, sletting av plan og opprydding av planversjon | <p>Følgende elementer er deaktivert under **Hovedplanlegging \> Hovedplanlegging \> Vedlikehold planer** i navigasjonsruten:</p><ul><li>Planlegg kopi</li><li>Slett plan</li><li>Planlegg versjonsopprydding</li></ul> |
| Returordrer | Returordrer tas ikke hensyn til. |
| Planleggingsrelaterte funksjoner | Hvis du vil ha mer informasjon, kan du se [Planlegging med uendelig kapasitet](infinite-capacity-planning.md#limitations). |
| Fullføring av sikkerhetslager | Planleggingsoptimalisering bruker alltid *Dagens dato + leveringstid* for feltet **Fyll opp minimum** på siden **Varedekning**. Dette hindrer uønskede planlagte ordrer og andre problemer fordi hvis leveringstiden ikke er inkludert for sikkerhetslager, vil planlagte bestillinger som opprettes for den gjeldende lagerbeholdningen, alltid bli forsinket på grunn av leveringstiden. |
| Utligning av sikkerhetslager og nettobehov | Kravtypen *Sikkerhetslager* er ikke inkludert og vises ikke på siden **Nettobehov**. Sikkerhetslager representerer ikke etterspørsel og har ikke en tilknyttet behovsdato. I stedet definerer det en begrensning for hvor mye lager som må finnes til enhver tid. Det tas imidlertid fremdeles hensyn til **Minimum**-feltverdien ved beregning av planlagte bestillinger under hovedplanleggingen. Vi foreslår at du undersøker kolonnen **Akkumulert antall** på **Nettobehov**-siden for å se at denne verdien ble tatt hensyn til. |
| Transportkalendere | Verdien i kolonnen **Transportkalender** på siden **Leveringsmåter** ignoreres. |
| Minimum/maksimum dekningskode uten verdier| Med den innebygde planleggingsmotoren når du bruker en minimums- eller maksimumskode der ingen minimums- eller maksimumsverdier er angitt, behandler planleggingsmotoren dekningskoden som et krav, og oppretter én ordre for hvert behov. Med planleggingsoptimalisering oppretter systemet én ordre per dag for å dekke hele beløpet for den dagen.  |
| Nettobehov og manuelt opprettede planlagte ordrer | Med den innebygde planleggingsmotoren vises manuelt opprettede forsyningsordrer for en vare blant nettobehovene for denne varen. Når du for eksempel oppretter en bestilling fra en salgsordre, vises bestillingen på **Nettobehov**-siden uten at det kreves noe forutgående handlinger. Dette skjer fordi den innebygde planleggingsmotoren logger lagertransaksjoner i `inventLogTTS`-tabellen og viser endringer på **Nettobehov**-siden for dynamiske planer. Med planleggingsoptimalisering vises imidlertid ikke ordrer som er opprettet manuelt blant nettobehovene til en vare før planleggingsoptimaliseringen kjøres (ved hjelp av en plan som inkluderer varen), eller til du velger **Oppdater \> Hovedplanlegging** i handlingsruten på **Nettobehov**-siden, som vil kjøre hovedplanlegging for varen. Hvis du vil ha mer informasjon om hvordan du arbeider med **Nettobehov**-siden, kan du se [Nettobehov og utligningsinformasjon med planleggingsoptimalisering](net-requirements.md). |

## <a name="additional-resources"></a>Tilleggsressurser

- [Analyse for tilpasning av planleggingsoptimalisering](planning-optimization-fit-analysis.md)
- [Parametere som ikke brukes av planleggingsoptimalisering](not-used-parameters.md)
- [Parametere for dato og klokkeslett som brukes av planleggingsoptimalisering](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
