---
title: Bruke det mobile arbeidsområdet Aktivastyring
description: Denne artikkelen inneholder informasjon om det mobile arbeidsområdet Aktivastyring.
author: johanhoffmann
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: 8f215d5f6758f222a9dc6b382b172009836547ec
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067009"
---
# <a name="use-the-asset-management-mobile-workspace"></a>Bruke det mobile arbeidsområdet Aktivastyring

[!include [banner](../../includes/banner.md)]
[!include [mobile app deprecated](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Denne artikkelen inneholder informasjon om det mobile arbeidsområdet **Aktivastyring**. Dette arbeidsområdet lar brukere vise og opprette vedlikeholdsforespørsler og arbeidsordrer. Brukere kan også vise tilordnede arbeidsordrejobber i en kalender- eller listevisning. Du kan også vise og søke etter aktiva og arbeidssteder.

## <a name="overview"></a>Oversikt

Aktivastyring er en avansert modul for håndtering av aktiva og arbeidsordrejobber i Dynamics 365 Supply Chain Management. Det mobile arbeidsområdet **Aktivastyring** lar brukere raskt vise tilordnede arbeidsordrejobber på den valgte mobilenheten. Brukere kan også opprette og administrere vedlikeholdsforespørsler, oppdatere livssyklustilstand og vise detaljer for arbeidssted ved hjelp av mobilenheten.

Det mobile arbeidsområdet for **Aktivastyring** lar brukere utføre disse oppgavene:

- Opprette, vise og rediger vedlikeholdsforespørsler, ta et bilde eller legger ved et eksisterende bilde i vedlikeholdsforespørselen, endre livssyklustilstanden for vedlikeholdsforespørselen. 
- Opprette, vise og rediger arbeidsordrer, ta et bilde eller legger ved et eksisterende bilde i arbeidsordren, endre livssyklustilstanden for arbeidsordren, vise arbeidsordrejobber.
- Vise tilordnet arbeidsordrejobber i en kalender visning.
- Opprette, vise og redigere arbeidsordrejobb, oppdater anleggsmiddeltellere, vise sjekkliste for vedlikehold, vise og rediger merknader for arbeidsordrejobb, vise verktøyene som kreves for arbeidsordrejobben.
- Vise eller søke etter et bestemt anleggsmiddel eller arbeidssted.

## <a name="prerequisites"></a>Forutsetninger

Før du kan bruke det mobile arbeidsområdet **Aktivastyring**, må administratoren konfigurere den nødvendige brukeren og arbeiderkontoene og publisere arbeidsområdet. Hvis du vil ha mer informasjon, kan du se [Konfigurere det mobile arbeidsområdet Aktivastyring](set-up-asset-management-mobile.md).

## <a name="download-and-install-the-mobile-app"></a>Laste ned og installere mobilappen

Last ned og installer økonomi- og driftsmobilappen (Dynamics 365):

- [For Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
- [For iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logge på mobilappen

1. Start appen på mobilenheten.

1. Skriv inn URL-adressen for Dynamics 365.

1. Første gang du logger deg på, blir du bedt om brukernavn og passord. Angi legitimasjon.

1. Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet. Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.

    ![Velge et arbeidsområde.](media/am-mobile-01.png "Velge et arbeidsområde")

## <a name="view-assigned-work-order-jobs-in-calendar-view"></a>Vise tilordnet arbeidsordrejobber i en kalender visning

1. Åpne arbeidsområdet **Aktivastyring** på mobilenheten.

1. Velg **Min kalender for arbeidsordrejobber**.

1. Velg datoen du vil vise arbeidsordrejobber for. I listen vises ID for anleggsmiddel og arbeidssted for hver arbeidsordrejobb.

1. Velg en arbeidsordrejobb i listen for å se jobbdetaljer: Detaljer om anleggsmiddel og arbeidssted, samt andre navigasjonskoblinger for å vise **Vedlegg**, **Kontrollister**, **Verktøy**, **Anleggsmiddeltellere**, **Merknader** og **Journaler**.

    ![Vise tilordnet arbeidsordrejobber i en kalender visning.](media/am-mobile-02.png "Vise tilordnet arbeidsordrejobber i en kalender visning")

## <a name="create-a-work-order-job"></a>Opprette en arbeidsordrejobb

1. Åpne arbeidsområdet **Aktivastyring** på mobilenheten.

1. Velg **Alle arbeidsordrer for vedlikehold**.

1. Velg arbeidsordren du vil opprette en ny arbeidsordrejobb for.

1. Velg **Legg til linje**.

1. Velg **anleggsmiddelet** du vil opprette en arbeidsordrejobb for.

1. Velg **Vedlikeholdsjobbtype**, **Variant av vedlikeholdsjobbtype** og **Handel**.

1. Velg **Ferdig**.

    ![Skjermen Legg til linje.](media/am-mobile-03.png "Skjermen Legg til linje")


## <a name="add-attachment-to-a-work-order-job"></a>Legge til vedlegg i en arbeidsordrejobb

1. Åpne arbeidsområdet **Aktivastyring** på mobilenheten.

1. Velg **Alle arbeidsordrer for vedlikehold**.

1. Velg arbeidsordren > arbeidsordrejobben du vil legge til et vedlegg i.
    - Du kan også velge **Min kalender for arbeidsordrejobber** eller **Min liste for arbeidsordrejobber** på startsiden for å gå til siden **Detaljer for arbeidsordrejobb**.

1. Velg **Vedlegg** på siden **Detaljer for arbeidsordrejobb**.

1. Du vil se eksisterende vedlegg i arbeidsordrejobben. Velg **Legg til vedlegg**.

1. Angi **Navn** og **Merknader** for vedlegget.

1. Velg **Velg bilde** for å velge et bilde fra mobilgalleriet, eller **Ta bilde** for å ta et bilde.

1. Velg **Ferdig**.

    ![Vise og legge til vedlegg for en arbeidsordrejobb.](media/am-mobile-04.png "Vise og legge til vedlegg for en arbeidsordrejobb")

## <a name="view-maintenance-checklist-on-a-work-order-job"></a>Vise kontrolliste for vedlikehold på en arbeidsordrejobb

1. Åpne arbeidsområdet **Aktivastyring** på mobilenheten.

1. Velg **Alle arbeidsordrer for vedlikehold**.

1. Velg arbeidsordren > arbeidsordrejobben du vil vise kontrollister for.
    - Du kan også velge **Min kalender for arbeidsordrejobber** eller **Min liste for arbeidsordrejobber** på startsiden for å gå til siden **Detaljer for arbeidsordrejobb**.

1. Velg **Kontrolliste** på siden **Detaljer for arbeidsordrejobb**.

1. Det vises en liste over kontrollistelinjer som er knyttet til arbeidsordrejobben. Velg en kontrollistelinje for å vise **Instruksjoner** og legge til **Merknader**.

1. Velg Tilbake-knappen (**<**) for å gå tilbake til forrige side.

    ![Sjekkliste for vedlikehold og linjedetaljer.](media/am-mobile-05.png "Sjekkliste for vedlikehold og linjedetaljer")

## <a name="view-and-update-asset-counters-on-a-work-order-job"></a>Vise og oppdatere anleggsmiddeltellere i en arbeidsordrejobb

1. Åpne arbeidsområdet **Aktivastyring** på mobilenheten.

1. Velg **Alle arbeidsordrer for vedlikehold**.

1. Velg arbeidsordren > arbeidsordrejobben du vil vise anleggsmiddeltellere for.
    - Du kan også velge **Min kalender for arbeidsordrejobber** eller **Min liste for arbeidsordrejobber** på startsiden for å gå til siden **Detaljer for arbeidsordrejobb**.

1. Velg **Anleggsmiddeltellere** på siden **Detaljer for arbeidsordrejobb**.

1. Det vises en liste over anleggsmiddeltellere som er knyttet til arbeidsordrejobben. Velg blyantikonet på en anleggsmiddeltellerlinje for å oppdatere tellerverdien.

1. Angi en ny tellerverdi, og velg **Fullført**.

    ![Vis og oppdater aktivatellere.](media/am-mobile-06.png "Vis og oppdater aktivatellere")

## <a name="register-consumption-on-a-work-order-job"></a>Registrere forbruk i en arbeidsordrejobb

1. Åpne arbeidsområdet **Aktivastyring** på mobilenheten.

1. Velg **Alle arbeidsordrer for vedlikehold**.

1. Velg arbeidsordren > arbeidsordrejobben du vil legge til forbruksregistreringer for.
    - Du kan også velge **Min kalender for arbeidsordrejobber** eller **Min liste for arbeidsordrejobber** på startsiden for å gå til siden **Detaljer for arbeidsordrejobb**.

1. Velg **Journaler** på siden **Detaljer for arbeidsordrejobb**.

1. Velg **Legg til timer** for å opprette arbeidstimeregistreringer.
    1. Velg **Kategori** fra oppslaget.
    1. I **Timer**-feltet angir du antallet arbeidstimer som er brukt på arbeidsordrejobben.
    1. Velg aktuell **Linjeegenskap**.
    1. Velg **Ferdig**.

1. Velg **Legg til varer** for å opprette vareregistreringer.
    1. Velg **Varenummer** fra oppslaget.
    1. Velg **Område** fra oppslaget.
    1. Angi **Antall** varer som skal forbrukes.
    1. Velg **Ferdig**.

1. Velg **Legg til utgift** for å opprette utgiftsregistreringer.
    1. Velg **Kategori** fra oppslaget.
    1. Angi antallet for utgiftsregistreringen.
    1. Velg **Salgsvaluta** fra oppslaget.
    1. Angi **Kostpris** for utgiftsregistreringen.
    1. Velg **Ferdig**.

    ![Oppdatere en arbeidsordrejournal.](media/am-mobile-07.png "Oppdatere en arbeidsordrejournal")

## <a name="update-lifecycle-state-on-a-work-order"></a>Oppdatere livssyklustilstand på en arbeidsordre

1. Åpne arbeidsområdet **Aktivastyring** på mobilenheten.

1. Velg **Alle arbeidsordrer for vedlikehold**.

1. Velg arbeidsordren du vil oppdatere livssyklustilstand for.

1. Velg **Oppdater tilstand**-knappen nederst på skjermen.

1. Velg en ny livssyklustilstand fra listen.

1. Velg **Ferdig**.

    ![Oppdatere livssyklustilstand på en arbeidsordre.](media/am-mobile-08.png "Oppdatere livssyklustilstand på en arbeidsordre")

## <a name="create-a-maintenance-request"></a>Opprette en vedlikeholdsanmodning

1. Åpne arbeidsområdet **Aktivastyring** på mobilenheten.

1. Velg **Alle vedlikeholdsforespørsler**.

1. Velg **Handlinger** nederst på skjermen, og velg deretter **Opprett vedlikeholdsforespørsel**.

1. Hvis nummerserie er aktivert for vedlikeholdsforespørsler i **Aktivastyring**, skjules feltet **Vedlikeholdsforespørsel** fordi det fylles ut automatisk. Hvis feltet **Vedlikeholdsforespørsel** vises, angir du en ID for vedlikeholdsforespørsel.

1. Velg **Type vedlikeholdsforespørsel**.

1. Angi en **Beskrivelse** vedlikeholdsforespørselen.

1. Velg **Anleggsmiddel** du vil opprette forespørselen for.

1. Velg **Servicenivå** for vedlikeholdsforespørselen.

1. Velg **Ferdig**.

    ![Opprette en melding.](media/am-mobile-09.png "Opprette en melding")

## <a name="add-attachment-to-a-maintenance-request"></a>Legge til vedlegg i en vedlikeholdsforespørsel

1. Åpne arbeidsområdet **Aktivastyring** på mobilenheten.

1. Velg **Alle vedlikeholdsforespørsler**.

1. Velg vedlikeholdsforespørselen du vil legge til et vedlegg i.

1. Velg **Vedlegg** nederst på skjermen.

1. Velg **Legg til vedlegg**.

1. Angi **Navn** og **Merknader** for vedlegget.

1. Velg **Velg bilde** for å velge et bilde fra mobilgalleriet, eller **Ta bilde** for å ta et bilde.

1. Velg **Ferdig**.

    ![Legge til et vedlegg i en vedlikeholdsforespørsel.](media/am-mobile-10.png "Legge til et vedlegg i en vedlikeholdsforespørsel")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

