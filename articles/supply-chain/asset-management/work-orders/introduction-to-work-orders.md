---
title: Innføring i arbeidsordrer
description: Denne artikkelen gir en oversikt over arbeidsordrer i Aktivastyring.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderLineNote, EntAssetWorkOrderTable, EntAssetWorkOrderActive, EntAssetWorkOrderHoursInfoPart, EntAssetWorkOrderLineListPage, EntAssetWorkOrderAddObjectBOMItem, EntAssetWorkOrderTablePoolAdd, EntAssetWorkOrderPurchReqListPagePreviewPane, EntAssetWorkOrderPoolReferenceAdd, EntAssetWorkOrderWorkspace, EntAssetWorkOrderTableAdjust, EntAssetWorkOrderGantt, EntAssetWorkOrderNotes, EntAssetWorkOrderActivePart, EntAssetWorkOrderTableInfoPart, EntAssetWorkOrderLineListPagePreviewPane, EntAssetWorkOrderTool, EntAssetMobileWorkOrderLineDetails, EntAssetMobileWorkOrderLineList, EntAssetMobileWorkOrderDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5eb911ec4ba9655c4ecaea3bf9a4f8736fa036c2
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016717"
---
# <a name="introduction-to-work-orders"></a>Innføring i arbeidsordrer

[!include [banner](../../includes/banner.md)]



Arbeidsordrer brukes til å administrere vedlikeholdsoppgaver, angi nødvendig informasjon om oppgavene og registrere forbruk for dem. Hver arbeidsordre kan inneholde én eller flere arbeidsordrejobber, og ett eller flere aktiva kan knyttes til hver arbeidsordre. Hver arbeidsordrejobb definerer en vedlikeholdsjobb som er planlagt for aktivumet.

Arbeidsordrer kan opprettes på følgende måter:

- Automatisk ved hjelp av [Planlegg vedlikeholdsplaner](../preventive-and-reactive-maintenance/schedule-maintenance-plans.md) for kalenderbaserte vedlikeholdsplaner satt til "Opprett automatisk".

- Automatisk ved hjelp av [Planlegg vedlikeholdsrunder](../preventive-and-reactive-maintenance/maintenance-rounds.md) for vedlikeholdsrunder satt til "Opprett automatisk".

- Fra [Vedlikeholdsplan](../preventive-and-reactive-maintenance/maintenance-schedule.md) for forebyggende vedlikeholdsjobber eller meldinger.

- Manuelt

- Fra siden **Alle meldinger**, **Aktive meldinger** eller **Mine meldinger for funksjonslokasjon**.

>[!NOTE]
>Arbeidsordrejobber som er knyttet til samme aktivum, er knyttet til samme prosjekt-ID.

## <a name="all-work-orders"></a>Alle arbeidsordrer

Velg **Aktivastyring** > **Arbeidsordrer** > **Alle arbeidsordrer** for å åpne listesiden **Alle arbeidsordrer**. Denne siden viser alle arbeidsordrer og noe av informasjonen som er relatert til hver av dem.

Illustrasjonen nedenfor viser et eksempel på listesiden **Alle arbeidsordrer**.

![Figur 1.](media/01-work-orders.png)

Velg **Aktivastyring** > **Arbeidsordrer** > **Aktive arbeidsordrer** for å se en liste over bare aktive arbeidsordrer. 

Hvis du vil se en liste over arbeidsordrejobber som inneholder aktiva som er installert på funksjonslokasjoner du er knyttet til som arbeider, velger du **Aktivastyring** > **Arbeidsordrer** > **Mine arbeidsordrelinjer for funksjonslokasjon**. (Forholdet mellom arbeidere og funksjonssteder er definert på **Arbeidere**-siden. Hvis du vil ha mer informasjon, se [Vedlikeholdspersoner og arbeidergrupper](../setup-for-objects/workers-and-worker-groups.md).)

Her er noen måter du kan bruke siden **Alle arbeidsordrer** på:

- I rutenettvisningen velger du en kobling i kolonnen **Arbeidsordre** til å vise detaljvisningen for den valgte posten. Deretter kan du velge **Rediger** for å åpne posten for redigering.

- I detaljvisningen kan du se detaljert informasjon knyttet til arbeidsordren.  

- I detaljvisningen velger du **Linjer**-fanen for å se detaljer om arbeidsordrejobben eller **Hode**-fanen for å se detaljer om arbeidsordren.  

- Utvid ruten **Beslektet informasjon** til høyre for siden for å vise tilleggsinformasjon som er knyttet til den valgte arbeidsordren.

Illustrasjonen nedenfor viser et eksempel på detaljvisningen **Alle arbeidsordrer**.

![Figur 2.](media/02-work-orders.png)


Knappene i handlingsruten er ordnet i kategorier. Følgende tabell beskriver kort hvilke knapper som er knyttet til Aktivastyring:



| Navn på knapp                     | Beskrivelse                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rediger                            | Rediger den valgte arbeidsordren.                                                                                                                                                                                                                                           |
| Nye                             | Opprett ny arbeidsordre.                                                                                                                                                                                                                                                  |
| Delete                          | Slett den valgte arbeidsordren.                                                                                                                                                                                                                                         |
| Arbeidsordresamling                 | Legg til den valgte arbeidsordren i en arbeidsordresamling, eller fjern den fra arbeidsordresamling.                                                                                                                                                                                           |
| Juster                          | Juster informasjon om forventet start og slutt, servicenivå, ansvarlig vedlikeholdsperson eller ansvarlig vedlikeholdspersongruppe i valgte arbeidsordrer.                                                                                                                                     |
| Relatert arbeidsordre              | Opprett en ny arbeidsordre knyttet til den valgte arbeidsordrejobben. Dette er nyttig hvis du vil registrere primære og sekundære arbeidsordrer.                                                                                                                              |
| Kopier arbeidsordre                 | Opprett en ny arbeidsordre som er basert på en eksisterende arbeidsordren.                                                                                                                                                                                                               |
| Hendelseshistorikk                   | Vis registreringslogg for arbeidsordren.                                                                                                                                                                                                                |
| Merknader for vedlikeholdsjobb for arbeidsordre                           | Lag en beskrivelse for en arbeidsordren, eller sett inn merknader eller kommentarer om den. Først velger du **Legg til tidsstempel** for å legge til brukernavnet og et tidsstempel i merknaden. Merknader vises i fanen **Beskrivelse** i hurtigfanen **Linjedetaljer** på siden **Arbeidsordre**.         |
| Verktøy                           | Opprett en liste over nødvendige verktøy i en arbeidsordre. Verktøy defineres som ressurser i **Organisasjonsstyring** > **Ressurser** > **Ressurser**.                                                                                                      |
| Sjekkliste for vedlikehold           | Vis sjekklisten for aktivumet som er knyttet til arbeidsordren.                                                                                                                                                                                                              |
| Aktivumfeil                     | Vis eller registrer feilinformasjon for et aktivum. Denne informasjonen er for feilstyring.                                                                                                                                                                                      |
| Nedetid ved vedlikehold            | Angi nedetid for vedlikehold for en arbeidsordre.                                                                                                                                                                                                                               |
| Betingelsesvurdering            | Registrer betingelsesvurderingsmålinger for en arbeidsordre.                                                                                                                                                                                                             |
| Aktivatellere                 | Opprett eller vis tellerregistreringer på aktivumet.                                                                                                                                                                                                                     |
| Prognose                        | Vis eller opprett prognoser i en arbeidsordre.                                                                                                                                                                                                                               |
| Journaler                        | Vis eller opprett arbeidsordrejournaler. Journallinjer kan kopieres fra prognoser.                                                                                                                                                                                         |
| Prosjekttransaksjoner            | Vis alle posterte transaksjoner som er relatert til arbeidsordrer som er opprettet for aktivumet.                                                                                                                                                                                             |
| Oppdater tilstand for arbeidsordre           | Oppdater tilstanden for arbeidsordrelivssyklusen.                                                                                                                                                                                                                                                |
| Logg for livssyklustilstand                      | Vis en logg som viser livssyklustilstandene til den valgte arbeidsordren.                                                                                                                                                                                                                   |
| Aktivadokumenter                | Vis listen over dokumenter knyttet til aktiva som er knyttet til en arbeidsordre. Disse dokumentene er definert i **Aktivastyring** > **Oppsett** > **Aktivadokumenter**.                                                                                                 |
| Planlegg                        | Planlegg de valgte arbeidsordrene.                                                                                                                                                                                                                                      |
| Fordeling            | Planlegg den valgte arbeidsordren for én arbeider.                                                                                                                                                                                                                        |
| Slett tidsplan                 | Slett planleggingen for den valgte arbeidsordren.                                                                                                                                                                                                                          |
| Planlagte vedlikeholdsjobber for arbeidsordre             | Åpne listesiden **Planlagte vedlikeholdsjobber for arbeidsordre**.                                                                                                                                                                                                                             |
| Innkjøpsrekvisisjon for arbeidsordre | Åpne listesiden **Innkjøpsrekvisisjon for arbeidsordre**.                                                                                                                                                                                                                 |
| Innkjøp for arbeidsordre             | Åpne listesiden **Arbeidsordrekjøp**.                                                                                                                                                                                                                             |
| Kostkontroll                    | Sammenligne budsjettkostnader og faktiske kostnader i arbeidsordren.                                                                                                                                                                                                                |
| Timekontroll                    | Sammenligne prognosetimer og faktiske timer i arbeidsordren.                                                                                                                                                                                                                |
| Arbeidsordrerapport               | Skriv ut en arbeidsordrerapport.                                                                                                                                                                                                                                                |
| Arbeidsordreforbruk          | Skriv ut en forbruksrapport.                                                                                                                                                                                                                                               |


Knappene i gruppen **Prosjekt** i fanen **Arbeidsordre** i handlingsruten er relatert til funksjonaliteten for prognoser, journaler og fakturering i modulen **Prosjektstyring og regnskap**.

>[!NOTE]
>For å inkludere prognoser som er opprettet i en arbeidsordre når du kjører hovedplanlegging, bruker du prognosemodellen som er valgt på siden **Aktivabehandlingsparametere**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]