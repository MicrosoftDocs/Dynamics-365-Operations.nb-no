---
title: Opprette vedlikeholdsforespørsler
description: Dette emnet forklarer hvordan du oppretter en vedlikeholdsforespørsel i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 03e090633276cd264ad03f561ddb425a9816357e
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847511"
---
# <a name="create-maintenance-requests"></a>Opprette vedlikeholdsforespørsler

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Vedlikeholdsforespørsler kan brukes hvis vedlikeholdsarbeidere eller produksjonsarbeidere oppdager at utstyr krever reparasjon, men reparasjonsjobben kan ikke utføres med en gang.

**Eksempel:** Mens en vedlikeholdsarbeider foretar en reparasjon, oppdager hun at et annet aktivum på samme lokasjon må ha service. Vedlikeholdsarbeideren har imidlertid ikke tid eller nødvendige reservedeler til å utføre reparasjonsjobben. Derfor oppretter hun en vedlikeholdsforespørsel på aktivumet og angir en kort beskrivelse av problemet.

Delen **Aktive vedlikeholdsforespørsler** i ruten **Relatert informasjon** til høyre for **Alle aktiva** eller **Aktive aktiva**-siden (**Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva** eller **Aktive aktiva**) viser vedlikeholdsforespørslene som er knyttet til det valgte aktivumet.

1. Velg **Aktivastyring** \> **Felles** \> **Vedlikeholdsforespørsler** \> **Alle vedlilkeholdsforespørsler** eller **Aktive vedlikeholdsforespørsler**.
2. Velg **Ny**.
3. I dialogboksen **Opprett forespørsel** i feltet **Type vedlikeholdsforespørsel** velger du typen vedlikeholdsforespørsel. En standardtype foreslås.
4. I **Beskrivelse**-feltet skriver du inn et navn eller en tittel som kort beskriver vedlikeholdsforespørselen.
5. I feltene **Arbeidssted** og **Aktivum** velger du et arbeidssted eller et aktivum eller en kombinasjon av begge deler, alt etter behov. Du kan opprette en vedlikeholdsforespørsel uten å velge et aktivum, og aktivumet kan legges til i vedlikeholdsforespørselen senere. Hvis vedlikeholdspersonen som er logget på Microsoft Dynamics 365 for Finance and Operations, er knyttet til en ressurs som er knyttet til et aktivum, angis **Aktivum**-feltet automatisk.

    Hvis en vedlikeholdsforespørsel allerede er knyttet til det valgte aktivumet, vises en meldingslinje øverst i dialogboksen **Opprett forespørsel** for å varsle deg om ID-en for den eksisterende vedlikeholdsforespørselen. En meldingslinje varsler deg også hvis aktivumet dekkes av en garantiavtale.

6. I feltet **Servicenivå** velger du et servicenivå som angir viktigheten av forespørselen.
7. Hvis du valgte et aktivum i trinn 5, kan du bruke feltene **Feilsymptom**, **Feilområde** og **Feiltype** til å opprette en feilregistrering.
8. Hvis vedlikeholdsforespørselen har forårsaket nedetid for vedlikehold, angir du startdatoen og klokkeslettet for nedetiden.

    Feltet **Startet av** blir automatisk satt til ditt navn.

10. **Faktisk start**-feltet settes automatisk til gjeldende dato og klokkeslett. Du kan imidlertid endre verdien etter behov.
11. Angi eventuelle tilleggsmerknader i feltet **Notater**.
12. Velg **OK**.

![Figur 1](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a>Påfølgende behandling av vedlikeholdsforespørsler

Når en vedlikeholdsforespørsel er opprettet, men før den konverteres til en arbeidsordre, bør diverse informasjon oppdateres på den. Vanligvis fullfører en planlegger eller en annen administrativ ansatt denne oppgaven.

- På siden **Alle vedlikeholdsforespørsler** eller **Aktive vedlikeholdsforespørsler** velger du forespørselen du vil arbeide med, og deretter velger du **Rediger**.

I detaljvisningen kan du oppdatere forskjellig informasjon. Her er noen eksempler:

- Velg og kontroller aktivumet. Hvis du må velge et annet aktivum senere, kan du sette alternativet **Aktivum bekreftet** til **Nei**.
- Velg en ansvarlig vedlikeholdspersongruppe og/eller en ansvarlig vedlikeholdsperson. Hvis du vil ha mer informasjon om nødvendig oppsett, kan du se [Ansvarlige vedlikeholdspersoner](../setup-for-maintenance-requests/responsible-workers.md).
- Velg en vedlikeholdsjobbtype og, hvis denne informasjonen er relevant, en relatert vedlikeholdsjobbvariant og et jobbfag.
- Angi geografiske koordinater i feltene **Breddegrad** og **Lengdegrad**. Alle koordinater som legges til i en vedlikeholdsforespørsel, overføres automatisk til en relatert arbeidsordre. 

![Figur 2](media/04-manage-maintenance-requests.png)

> [!NOTE]
> Hvis du velger et aktivum når du oppretter en vedlikeholdsforespørsel, kan du legge til én feil i aktivumet. Etter at vedlikeholdsforespørselen er opprettet, kan du legge til flere feil, etter behov. Hvis du vil legge til feil, velger du **Aktivafeil** på siden **Alle vedlikeholdsforespørsler**.