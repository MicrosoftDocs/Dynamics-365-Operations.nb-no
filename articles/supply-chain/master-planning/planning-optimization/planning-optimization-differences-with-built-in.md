---
title: Forskjeller mellom planleggingsoptimalisering og den avskrevne hovedplanleggingsmotoren
description: Denne artikkelen viser funksjoner som Planleggingsoptimalisering ennå ikke støtter, og som ikke er oppført på siden Analyse for tilpasning av planleggingsoptimalisering.
author: t-benebo
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 6e1671a508b85a94ac9687af15e898d885ea94c1
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745368"
---
# <a name="differences-between-planning-optimization-and-the-deprecated-master-planning-engine"></a>Forskjeller mellom planleggingsoptimalisering og den avskrevne hovedplanleggingsmotoren

[!include [banner](../../includes/banner.md)]

Resultatet av planleggingsoptimalisering kan være forskjellig fra den avskrevne hovedplanleggingsmotoren. Forskjellen kan også skyldes ventende funksjoner. Denne artikkelen viser funksjoner som Planleggingsoptimalisering ennå ikke støtter, og som ikke er oppført på siden **[Analyse for tilpasning av planleggingsoptimalisering](planning-optimization-fit-analysis.md)**.

| Funksjon | Gjeldende virkemåte i Planleggingsoptimalisering |
|---|---|
| Produkter med faktisk vekt | Produkter med faktisk vekt betraktes som vanlige produkter.|
| Utvidbare dimensjoner | Utvidbare dimensjoner støttes ikke av Planleggingsoptimalisering. Når du bruker Planleggingsoptimalisering, er utvidbare dimensjoner tomme i planlagte bestillinger selv om det er merket av for **Dekningsplanlegg etter dimensjon** på siden **Lagringsdimensjonsgrupper** eller **Sporingsdimensjonsgrupper**. |
| Filtrerte produksjonsutkjøringer | Hvis du vil ha mer informasjon, kan du se [Produksjonsplanlegging – filtre](production-planning.md#filters). |
| Prognoseplanlegging | Prognoseplanlegging støttes ikke. Vi anbefaler at du bruker hovedplanlegging der en prognosemodell er tilordnet hovedplanen. |
| Nummersekvenser for planlagte ordrer | Nummerserier for planlagte ordrer støttes ikke. Planlagte bestillingsnumre genereres på servicesiden. Det planlagte bestillingsnummeret vises vanligvis med ti sifre, men rekkefølgen bygges faktisk på 20 tegn, med ti sifre tilordnet for planleggingskjøringen, og de ti andre sifrene for de planlagte bestillingene teller. |
| Planlegg kopiering, sletting av plan og opprydding av planversjon | <p>Følgende elementer er deaktivert under **Hovedplanlegging \> Hovedplanlegging \> Vedlikehold planer** i navigasjonsruten:</p><ul><li>Planlegg kopi</li><li>Slett plan</li><li>Planlegg versjonsopprydding</li></ul> |
| Returordrer | Returordrer tas ikke hensyn til. |
| Planleggingsrelaterte funksjoner | Hvis du vil ha mer informasjon, kan du se [Planlegging med uendelig kapasitet](infinite-capacity-planning.md#limitations). |
| Fullføring av sikkerhetslager | Planleggingsoptimalisering bruker alltid *Dagens dato + leveringstid* for feltet **Fyll opp minimum** på siden **Varedekning**. Dette hindrer uønskede planlagte ordrer og andre problemer fordi hvis leveringstiden ikke er inkludert for sikkerhetslager, vil planlagte bestillinger som opprettes for den gjeldende lagerbeholdningen, alltid bli forsinket på grunn av leveringstiden. |
| Utligning av sikkerhetslager og nettobehov | Kravtypen *Sikkerhetslager* er ikke inkludert og vises ikke på siden **Nettobehov**. Sikkerhetslager representerer ikke etterspørsel og har ikke en tilknyttet behovsdato. I stedet definerer det en begrensning for hvor mye lager som må finnes til enhver tid. Det tas imidlertid fremdeles hensyn til **Minimum**-feltverdien ved beregning av planlagte bestillinger under hovedplanleggingen. Vi foreslår at du undersøker kolonnen **Akkumulert antall** på **Nettobehov**-siden for å se at denne verdien ble tatt hensyn til. Siden utligningen er forskjellig, kan ulike handlinger foreslås. |
| Transportkalendere | Verdien i kolonnen **Transportkalender** på siden **Leveringsmåter** ignoreres. |
| Minimum/maksimum dekningskode uten verdier| Med den avskrevne hovedplanleggingsmotoren når du bruker en minimums- eller maksimumskode der ingen minimums- eller maksimumsverdier er angitt, behandler planleggingsmotoren dekningskoden som et krav, og oppretter én ordre for hvert behov. Med planleggingsoptimalisering oppretter systemet én ordre per dag for å dekke hele beløpet for den dagen.  |
| Nettobehov og manuelt opprettede planlagte ordrer | Med den avskrevne hovedplanleggingsmotoren vises manuelt opprettede forsyningsordrer for en vare blant nettobehovene for denne varen. Når du for eksempel oppretter en bestilling fra en salgsordre, vises bestillingen på **Nettobehov**-siden uten at det kreves noe forutgående handlinger. Dette skjer fordi den avskrevne hovedplanleggingsmotoren logger lagertransaksjoner i `inventLogTTS`-tabellen og viser endringer på **Nettobehov**-siden for dynamiske planer. Med planleggingsoptimalisering vises imidlertid ikke ordrer som er opprettet manuelt blant nettobehovene til en vare før planleggingsoptimaliseringen kjøres (ved hjelp av en plan som inkluderer varen), eller til du velger **Oppdater \> Hovedplanlegging** i handlingsruten på **Nettobehov**-siden, som vil kjøre hovedplanlegging for varen. Hvis du vil ha mer informasjon om hvordan du arbeider med **Nettobehov**-siden, kan du se [Nettobehov og utligningsinformasjon](net-requirements.md). |
| Ressurstilordning | Når du arbeider med ubegrenset kapasitet, tilordner den avskrevne hovedplanleggingsmotoren alle planlagte bestillinger til den samme ressursen på en angitt ressursgruppe. Planleggingsoptimalisering forbedrer dette ved å velge ressurser i tilfeldig rekkefølge, slik at ulike produksjonsordrer kan bruke forskjellige ressurser. Hvis du vil bruke den samme ressursen for alle planlagte bestillinger, må du angi denne ressursen i ruten. |
| Utvidede datatyper (EDTs) | Planleggingsoptimalisering støtter ikke endringer i presisjonen i utvidede datatyper. Det betyr at denne prosessen ikke støttes offisielt og kanskje ikke fungerer. |
| Fullføring av sikkerhetslager | Planleggingsoptimalisering bruker alltid *Dagens dato + leveringstid* for **Fyll opp minimum**. Dette forbereder systemet til bruk av et forenklet planleggingsoppsett i fremtiden, og gir et gjennomførbart resultat. Hvis leveringstiden ikke er inkludert for sikkerhetslager, vil planlagte bestillinger som opprettes for liten lagerbeholdning, alltid bli forsinket på grunn av leveringstiden. Denne virkemåten kan føre til betydelig støy og uønskede planlagte bestillinger. Den anbefalte fremgangsmåten er å endre innstillingen slik at *Dagens dato + leveringstid* brukes. Oppdater hoveddata for å unngå advarsler. |
| Kopier statisk til dynamisk plan | Planleggingsoptimalisering kopierer ikke statiske planer til dynamiske planer, uavhengig av innstillingen på siden **Parametere for hovedplanlegging**. Denne operasjonen er generelt mindre relevant på grunn av hastigheten og fullføringsregenereringen som gis av planleggingsoptimaliseringen. Hvis det brukes to eller flere planer, bør hovedplanlegging utløses for hver plan. |

## <a name="additional-resources"></a>Tilleggsressurser

- [Analyse for tilpasning av planleggingsoptimalisering](planning-optimization-fit-analysis.md)
- [Parametere som ikke brukes av planleggingsoptimalisering](not-used-parameters.md)
- [Parametere for dato og klokkeslett som brukes av planleggingsoptimalisering](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
