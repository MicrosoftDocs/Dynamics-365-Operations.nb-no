---
title: Opprett meldinger
description: Denne artikkelen forklarer hvordan du oppretter en melding i Aktivastyring.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 92f3a2bc3d2a4d5d1c3be0c6dda2674dc3e7d0bb
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016833"
---
# <a name="create-maintenance-requests"></a>Opprette meldinger

[!include [banner](../../includes/banner.md)]

 

Meldinger kan brukes hvis vedlikeholdspersoner eller produksjonsarbeidere oppdager at utstyr krever reparasjon, men reparasjonsjobben kan ikke utføres med en gang.

**Eksempel:** Mens en vedlikeholdsperson foretar en reparasjon, oppdager vedkommende at et annet aktivum på samme lokasjon må ha service. Vedlikeholdspersonen har imidlertid ikke tid eller nødvendige reservedeler til å utføre reparasjonsjobben. Derfor oppretter vedkommende en melding på aktivumet og angir en kort beskrivelse av problemet.

Delen **Aktive meldinger** i ruten **Relatert informasjon** til høyre for **Alle aktiva** eller **Aktive aktiva**-siden (**Aktivastyring** \> **Aktiva** \> **Alle aktiva** eller **Aktive aktiva**) viser meldingene som er knyttet til det valgte aktivumet.

1. Velg **Aktivastyring** \> **Meldinger** \> **Alle meldinger** eller **Aktive meldinger**.
2. Velg **Ny**.
3. I dialogboksen **Opprett forespørsel** i feltet **Type melding** velger du typen melding. En standardtype foreslås.
4. I **Beskrivelse**-feltet skriver du inn et navn eller en tittel som kort beskriver meldingen.
5. I feltene **Funksjonslokasjon** og **Aktivum** velger du en funksjonslokasjon eller et aktivum eller en kombinasjon av begge deler, alt etter behov. Du kan opprette en melding uten å velge et aktivum, og aktivumet kan legges til i meldingen senere. Hvis vedlikeholdspersonen som er logget på er knyttet til en ressurs som er knyttet til et aktivum, angis **Aktivum**-feltet automatisk.

    Hvis en melding allerede er knyttet til det valgte aktivumet, vises en meldingslinje øverst i dialogboksen **Opprett forespørsel** for å varsle deg om ID-en for den eksisterende meldingen. En meldingslinje varsler deg også hvis aktivumet dekkes av en garantiavtale.

6. I feltet **Servicenivå** velger du et servicenivå som angir viktigheten av forespørselen.
7. Hvis du valgte et aktivum i trinn 5, kan du bruke feltene **Feilsymptom**, **Feilområde** og **Feiltype** til å opprette en feilregistrering.
8. Hvis meldingen har forårsaket nedetid for vedlikehold, angir du startdatoen og klokkeslettet for nedetiden.

    Feltet **Startet av** blir automatisk satt til ditt navn.

10. **Faktisk start**-feltet settes automatisk til gjeldende dato og klokkeslett. Du kan imidlertid endre verdien etter behov.
11. Angi eventuelle tilleggsmerknader i feltet **Notater**.
12. Velg **OK**.

![Opprett melding.](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a>Påfølgende behandling av meldinger

Når en melding er opprettet, men før den konverteres til en arbeidsordre, bør diverse informasjon oppdateres på den. Vanligvis fullfører en planlegger eller en annen administrativ ansatt denne oppgaven.

- På siden **Alle meldinger** eller **Aktive meldinger** velger du forespørselen du vil arbeide med, og deretter velger du **Rediger**.

I detaljvisningen kan du oppdatere forskjellig informasjon. Her er noen eksempler:

- Velg og kontroller aktivumet. Hvis du må velge et annet aktivum senere, kan du sette alternativet **Aktivum bekreftet** til **Nei**.
- Velg en ansvarlig vedlikeholdspersongruppe og/eller en ansvarlig vedlikeholdsperson. Hvis du vil ha mer informasjon om nødvendig oppsett, kan du se [Ansvarlige vedlikeholdspersoner](../setup-for-maintenance-requests/responsible-workers.md).
- Velg en vedlikeholdsjobbtype og, hvis denne informasjonen er relevant, en relatert vedlikeholdsjobbvariant og et jobbfag.
- Angi geografiske koordinater i feltene **Breddegrad** og **Lengdegrad**. Alle koordinater som legges til i en melding, overføres automatisk til en relatert arbeidsordre. 

![Oppdatere melding.](media/04-manage-maintenance-requests.png)

> [!NOTE]
> Hvis du velger et aktivum når du oppretter en melding, kan du legge til én feil i aktivumet. Etter at meldingen er opprettet, kan du legge til flere feil, etter behov. Hvis du vil legge til feil, velger du **Aktivafeil** på siden **Alle meldinger**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]