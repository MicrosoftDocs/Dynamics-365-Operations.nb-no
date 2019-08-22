---
title: Introduksjon til aktiva
description: Dette emnet gir en oversikt over aktiva i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84609106fc3daafbbfed6f947df4524160bd7450
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783488"
---
# <a name="introduction-to-assets"></a>Introduksjon til aktiva

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Dette emnet gir en oversikt over aktiva i Aktivastyring. Et *aktivum* er enhver type utstyr, for eksempel en maskin eller en maskindel, som krever vedlikehold, service eller reparasjon.

Et aktivum oppdateres automatisk med relatert informasjon. Denne informasjonen kan for eksempel være nye eller oppdaterte arbeidsordrer. Du kan opprette aktiva via menyelementet **Alle aktiva** eller menyelementetet **Ventende aktiva**. Dette emnet beskriver hvordan du oppretter aktiva via menyelementet **Alle aktiva**. Hvis du vil ha informasjon om hvordan du oppretter aktiva via menyalementet **Ventende aktiva**, kan du se [Opprette aktiva basert på bestillinger](../objects/create-objects-based-on-purchase-orders.md).

## <a name="all-assets"></a>Alle anleggsmidler

Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva**. Listesiden **Alle aktiva** viser alle aktiva og noe av informasjonen som er knyttet til dem. Hvis du bare vil vise aktive aktiva, velger du **Aktive aktiva**. Hvis du bare vil vise aktiva som er installert på arbeidsstedene du er knyttet til som en vedlikeholdsperson, velger du **Mine aktive aktiva**. (Denne relasjonen er definert på **Arbeidere**-siden. Hvis du vil ha mer informasjon, se [Vedlikeholdspersoner og arbeidergrupper](../setup-for-objects/workers-and-worker-groups.md).)

I rutenettvisningen **Alle aktiva** velger du en kobling i kolonnen **Aktivum** for å vise detaljene for den valgte posten. Hvis du vil redigere posten, velger du **Rediger**-knappen. Detaljvisningen viser detaljert informasjon som er knyttet til aktivumet. En **Beslektet informasjon**-rute til høyre inneholder mer aktiva-relatert informasjon. Utvid ruten for å vise den tilknyttede informasjonen for det valgte aktivumet.

Knappene i handlingsruten er ordnet i kategorier. Følgende tabell beskriver kort hvilke knapper som er knyttet til Aktivastyring.

| Navn på knapp          | Beskrivelse                                                                                                                                                       |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rediger                 | Rediger det valgte aktivumet.                                                                                                                                         |
| Nye                  | Opprett et nytt aktivum.                                                                                                                                                |
| Slett               | Slett der valgte aktivumet.                                                                                                                                       |
| Flytt aktivum           | Flytt aktiva til en annen aktivastruktur eller et annen sted i den samme aktivastrukturen.                                                                                         |
| Erstatt aktivum        | Erstatt ett underordnet aktivum i et aktivahierarki med et annet aktivum.                                                                                                  |
| Installer aktivum        | Installer et aktivum på et arbeidssted.                                                                                                                          |
| Kopier aktivum           | Kopier et aktivumhierarki til et annet aktivum.                                                                                                                          |
| Forespørsler             | Åpne listesiden **Aktive forespørsler**, der du kan vise vedlikeholdsforespørsler som er opprettet for det valgte aktivumet.                                                                         |
| Hendelseshistorikk        | Vis en oversikt over de ulike registreringene som er gjort på aktivumet.                                                                                                         |
| Stykkliste for aktiva            | Vis en liste over alle varer (reservedeler og andre varer) som brukes på et aktivum.                                                                                  |
| Arbeidsordrer          | Åpne listesiden **Aktive arbeidsordrer**, der du kan vise arbeidsordrer for aktivumet.                                                                                        |
| Sjekkliste            | Vis en oversikt over kontrollister for vedlikehold og målinger som er registrert på aktivumet.                                                                                                 |
| Nedetid ved vedlikehold | Opprett eller vis registreringer av nedetid ved vedlikehold på aktivumet.                                                                                                       |
| Prosjekttransaksjoner | Vis alle posterte transaksjoner som er knyttet til arbeidsordrer som er opprettet for aktivumet.                                                                                       |
| Aktivummål       | Opprett eller vis aktivummål på aktivumet.                                                                                                               |
| Vedlikeholdsplan | Åpne listesiden **Åpne vedlikeholdsplan**, der du kan vise vedlikeholdsplaner, vedlikeholdsforespørsler og vedlikeholdsrunder som er knyttet til aktivumet, og som har statusen **Opprettet**. |
| Oppdater tilstand for aktivum   | Oppdatere livsløpstilstanden for aktivumet. Du kan velge flere aktiva på listesiden **Alle aktiva** og deretter oppdatere livsløpstilstanden for alle aktivaene samtidig.              |
| Logg for livsløpstilstand  | Åpne en logg som viser livsløpstilstandene til det valgte aktivumet.                                                                                                                 |
| Aktivadokumenter      | Vis en liste over dokumentene som er knyttet til et aktivum. Disse dokumentene er definert i **Aktivastyring** \> **Oppsett** \> **Aktivadokumenter**.                 |
| Attributter           | Opprett eller vis aktivaattributter.                                                                                                                             |
| Bilde                | Velg et bilde for aktivumet.                                                                                                                                   |
| Overordnede aktiva        | Vis loggen over overordnede objekter for det valgte aktivumet.                                                                                                                |
| Arbeidssteder | Vis loggen over arbeidssteder for det valgte aktivumet.                                                                                                          |
| Betingelsesvurdering | Registrer betingelsesvurderingsmålinger for aktivumet.                                                                                                         |
| Feil               | Åpne listesiden **Aktivafeil**, der du kan vise feil som er registrert på aktivumet.                                                                                             |
| Kostkontroll         | Sammenligne budsjettkostnader og faktiske kostnader for aktivumet.                                                                                                              |
| Timekontroll         | Sammenligne prognosetimer og faktiske timer på aktivumet.                                                                                                              |
| KPI-er for aktivum           | Beregn og vis KPI-er for aktivumet.                                                                                              |
| Jobbtyper            | Vis en oversikt over de gjeldende standardjobbtypene for aktivumet.                                                                                                            |
| Type kritisk aktivitet    | Vis eller oppdater typer kritisk aktivitet for aktivumet.                                                                                                                              |
| Reservedeler          | Vis en liste over godkjente og alternative reservedeler som kan brukes for aktivumet.                                                                               |
| Aktivumforbruk    | Skriv ut en rapport som viser forbruksregistreringer for aktivumet.                                                                                                |
| Aktivumfeil          | Skriv ut en rapport som viser feilregistreringer for aktivumet.                                                                                                      |