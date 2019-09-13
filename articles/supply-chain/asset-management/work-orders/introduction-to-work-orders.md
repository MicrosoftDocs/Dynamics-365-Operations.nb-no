---
title: Innføring i arbeidsordrer
description: Dette emnet gir en oversikt over arbeidsordrer i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9483c50a15fca566b1f5e089297795bbbe09c042
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875827"
---
# <a name="introduction-to-work-orders"></a>Innføring i arbeidsordrer

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Arbeidsordrer brukes til å administrere, angi nødvendig informasjon for og registrere forbruk for vedlikeholdsjobber. En arbeidsordre kan inneholde én eller flere arbeidsordrejobber, og ett eller flere aktiva kan knyttes til en arbeidsordre. Hver arbeidsordrelinje definerer en vedlikeholdsjobb som er planlagt for aktivaet.

Arbeidsordrer kan opprettes automatisk eller manuelt:

- Automatisk ved hjelp av skjemaet **Planlegg vedlikeholdsplaner** for kalenderbaserte vedlikeholdsplaner satt til Opprett automatisk.  

- Automatisk ved hjelp av skjemaet **Planlegg vedlikeholdsrunder** for vedlikeholdsrunder satt til Opprett automatisk.  

- Opprett fra vedlikeholdsplan, som kan være forebyggende vedlikeholdsjobber eller vedlikeholdsforespørsler.  

- Opprett en arbeidsordre manuelt.  

- Opprett en arbeidsordre fra **Alle vedlikeholdsforespørsler** eller **Aktive vedlikeholdsforespørsler** eller **Mine vedlikeholdsforespørsler for arbeidssted**.

>[!NOTE]
>Arbeidsordrejobber knyttet til samme aktivum er knyttet til samme prosjekt-ID.

## <a name="all-work-orders"></a>Alle arbeidsordrer

Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** for å åpne listen. **Alle arbeidsordrer** inneholder en liste over alle arbeidsordrene og viser noe av informasjonen som er knyttet til en arbeidsordre.

![Figur 1](media/01-work-orders.png)

- Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Aktive arbeidsordrer** for å se en liste over aktive arbeidsordrer.

- Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Mine vedlikeholdsjobber for arbeidsordre for arbeidssted** hvis du vil se en liste over arbeidsordrejobber som inneholder aktiva som finnes på arbeidssteder du er knyttet til som arbeider (definert i [Vedlikeholdsarbeidere og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md)).

- I listen **Alle arbeidsordrer** (rutenettvisning) klikker du på en kobling i kolonnen **Arbeidsordre** for å vise detaljene for den valgte posten. Klikk på **Rediger**-knappen for å åpne for redigering.  

- I detaljvisningen kan du se detaljert informasjon knyttet til arbeidsordren.  

- I detaljvisningen velger du **Linjer**-koblingen for å se arbeidsordrejobbdetaljer, eller velger **Hode**-koblingen for å se arbeidsordredetaljer.  

- Den loddrette ruten **Relatert informasjon** til høyre på skjermen inneholder ekstra arbeidsordrerelatert informasjon. Utvid ruten for å se den tilknyttede informasjonen for den valgte arbeidsordren.  


![Figur 2](media/02-work-orders.png)


Handlingsruteknappene er ordnet i kategorier på handlingsruten. Her er en kort beskrivelse av knappene knyttet til Enterprise Asset Management:



| Navn på knapp                     | Beskrivelse                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rediger                            | Rediger den valgte arbeidsordren.                                                                                                                                                                                                                                           |
| Nye                             | Opprett ny arbeidsordre.                                                                                                                                                                                                                                                  |
| Slett                          | Slett den valgte arbeidsordren.                                                                                                                                                                                                                                         |
| Arbeidsordresamling                 | Legg til valgt arbeidsordre i en arbeidsordresamling, eller fjern fra arbeidsordresamling.                                                                                                                                                                                           |
| Juster                          | Juster informasjon om forventet start og slutt, servicenivå, ansvarlig vedlikeholdsperson eller ansvarlig vedlikeholdspersongruppe i valgte arbeidsordrer.                                                                                                                                     |
| Relatert arbeidsordre              | Opprett en ny arbeidsordre knyttet til den valgte arbeidsordrejobben. Dette er nyttig hvis du vil registrere primære og sekundære arbeidsordrer.                                                                                                                              |
| Kopier arbeidsordre                 | Opprett en ny arbeidsordre basert på en eksisterende arbeidsordre.                                                                                                                                                                                                                |
| Hendelseshistorikk                   | Se registreringslogg i arbeidsordren.                                                                                                                                                                                                                |
| Merknader for vedlikeholdsjobb for arbeidsordre                           | Lag en beskrivelse eller sett inn merknader eller kommentarer i en arbeidsordre. Start ved å klikke på knappen **Legg til tidsstempel** for å legge til brukernavnet og et tidsstempel i merknaden. Merknader vises i **Arbeidsordre**-skjemaet > **Linjedetaljer**-hurtigfanen > **Beskrivelse**-kategorien. |
| Verktøy                           | Opprett en liste over nødvendige verktøy i en arbeidsordre. Verktøy defineres som ressurser i **Organisasjonsstyring** > **Felles** > **Ressurser** > **Ressurser**.                                                                                                      |
| Sjekkliste for vedlikehold           | Vis sjekkliste for aktivaet som er knyttet til arbeidsordren.                                                                                                                                                                                                              |
| Aktivumfeil                     | Vis eller registrer feilinformasjon for et aktiva som skal brukes til feilbehandling.                                                                                                                                                                                        |
| Nedetid ved vedlikehold            | Angi nedetid for vedlikehold for en arbeidsordre.                                                                                                                                                                                                                               |
| Betingelsesvurdering            | Registrer betingelsesvurderingsmålinger for en arbeidsordre.                                                                                                                                                                                                             |
| Aktivatellere                 | Opprett eller vis tellerregistreringer på aktivumet.                                                                                                                                                                                                                     |
| Prognose                        | Vis eller opprett prognoser i en arbeidsordre.                                                                                                                                                                                                                               |
| Journaler                        | Vis eller opprett arbeidsordrejournaler. Journallinjer kan kopieres fra prognoser.                                                                                                                                                                                         |
| Prosjekttransaksjoner            | Vis alle posterte transaksjoner relatert til arbeidsordrer som er opprettet for aktivaet.                                                                                                                                                                                             |
| Oppdater tilstand for arbeidsordre                | Oppdater tilstand for arbeidsordrelivssyklus.                                                                                                                                                                                                                                                |
| Logg for livsløpstilstand                       | Logg som viser livssyklustilstanden til den valgte arbeidsordren.                                                                                                                                                                                                                   |
| Aktivadokumenter                | Vis liste over dokumenter knyttet til aktiva som er knyttet til en arbeidsordre. Disse dokumentene er definert i **Aktivastyring** > **Oppsett** > **Aktivadokumenter**.                                                                                                 |
| Planlegg                        | Planlegg de valgte arbeidsordrene.                                                                                                                                                                                                                                      |
| Fordeling            | Planlegg den valgte arbeidsordren for én arbeider.                                                                                                                                                                                                                        |
| Slett tidsplan                 | Slett planlegging for den valgte arbeidsordren.                                                                                                                                                                                                                          |
| Planlagte vedlikeholdsjobber for arbeidsordre             | Åpne listesiden **Planlagte vedlikeholdsjobber for arbeidsordre**.                                                                                                                                                                                                                             |
| Innkjøpsrekvisisjon for arbeidsordre | Åpne listesiden **Innkjøpsrekvisisjon for arbeidsordre**.                                                                                                                                                                                                                 |
| Innkjøp for arbeidsordre             | Åpne listesiden **Arbeidsordrekjøp**.                                                                                                                                                                                                                             |
| Kostkontroll                    | Sammenligne budsjettkostnader og faktiske kostnader i arbeidsordren.                                                                                                                                                                                                                |
| Timekontroll                    | Sammenligne prognosetimer og faktiske timer i arbeidsordren.                                                                                                                                                                                                                |
| Arbeidsordrerapport               | Skriv ut arbeidsordrerapport.                                                                                                                                                                                                                                                |
| Arbeidsordreforbruk          | Skriv ut forbruksrapport.                                                                                                                                                                                                                                               |


Knappene i kategorien **Arbeidsordre** > **Prosjekt**-gruppen er relatert til funksjonalitet i **Prosjektstyring og regnskap**-modulen som gjelder prognoser, journaler og fakturering.

>[!NOTE]
>Prognoser som er opprettet i en arbeidsordre, kan inkluderes ved kjøring av hovedplanlegging ved hjelp av prognosemodellen som er valgt i skjemaet **Aktivabehandlingsparametere**.

