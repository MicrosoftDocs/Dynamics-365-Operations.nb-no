---
title: Mobilt arbeidsområde for aktivum
description: Dette emnet inneholder informasjon om mobilt arbeidsområde for aktivum
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: 525f21d076027f1bf339e59fd0e346706044839c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216511"
---
# <a name="asset-management-mobile-workspace"></a>Mobilt arbeidsområde for aktivum

[!include [banner](../../includes/banner.md)]


Dette emnet inneholder informasjon om mobilt arbeidsområde for aktivum Dette arbeidsområdet lar brukere vise og opprette vedlikeholdsforespørsler og arbeidsordrer. Brukere kan også vise tilordnede arbeidsordrejobber i en kalender- eller listevisning. Du kan også vise og søke etter aktiva og arbeidssteder.


## <a name="overview"></a>Oversikt

Aktivastyring er en avansert modul for håndtering av aktiva og arbeidsordrejobber i Dynamics 365 Supply Chain Management. Det mobile arbeidsområdet **Aktivabehandling** lar brukere raskt vise tilordnede arbeidsordrejobber på den valgte mobilenheten. Brukere kan også opprette og administrere vedlikeholdsforespørsler, oppdatere livsløpstilstand og vise detaljer for arbeidssted ved hjelp av mobilenheten.

Det mobile arbeidsområdet for **Aktivastyring** lar brukere utføre disse oppgavene:

- Opprette, vise og rediger vedlikeholdsforespørsler, ta et bilde eller legger ved et eksisterende bilde i vedlikeholdsforespørselen, endre livsløpstilstanden for vedlikeholdsforespørselen. 
- Opprette, vise og rediger arbeidsordrer, ta et bilde eller legger ved et eksisterende bilde i arbeidsordren, endre livsløpstilstanden for arbeidsordren, vise arbeidsordrejobber.
- Vise tilordnet arbeidsordrejobber i en kalender visning.
- Opprette, vise og redigere arbeidsordrejobb, oppdater anleggsmiddeltellere, vise sjekkliste for vedlikehold, vise og rediger merknader for arbeidsordrejobb, vise verktøyene som kreves for arbeidsordrejobben.
- Vise eller søke etter et bestemt anleggsmiddel eller arbeidssted.


## <a name="prerequisites"></a>Forutsetninger

Forutsetningene varierer avhengig av hvilken versjon av Dynamics 365 Supply Chain Management som er distribuert i organisasjonen.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-supply-chain-management"></a>Forutsetninger hvis du bruker Microsoft Dynamics 365 Supply Chain Management 
Hvis Microsoft Dynamics 365 Supply Chain Management har blitt innført i organisasjonen din, må systemadministrator publisere det mobile arbeidsområdet **Aktivabehandling**. Hvis du vil ha instruksjoner, kan du se [Publisere et mobilt arbeidsområde](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

## <a name="download-and-install-the-mobile-app"></a>Laste ned og installere mobilappen
Last ned og installer mobilappen Dynamics 365 for Unified Operations:

- [For Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
- [For iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logge på mobilappen
1. Start appen på mobilenheten.

2. Skriv inn URL-adressen for Dynamics 365.

3. Første gang du logger deg på, blir du bedt om brukernavn og passord. Angi legitimasjon.

4. Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet. Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.

![Figur 1](media/am-mobile-01.png)


## <a name="view-assigned-work-order-jobs-in-calendar-view"></a>Vise tilordnet arbeidsordrejobber i en kalender visning

1. Åpne arbeidsområdet **Aktivabehandling** på mobilenheten.

2. Velg **Min kalender for arbeidsordrejobber**.

3. Velg datoen du vil vise arbeidsordrejobber for. I listen vises ID for anleggsmiddel og arbeidssted for hver arbeidsordrejobb.

4. Velg en arbeidsordrejobb i listen for å se jobbdetaljer: Detaljer om anleggsmiddel og arbeidssted, samt andre navigasjonskoblinger for å vise **Vedlegg**, **Kontrollister**, **Verktøy**, **Anleggsmiddeltellere**, **Merknader** og **Journaler**.

![Figur 2](media/am-mobile-02.png)


## <a name="create-a-work-order-job"></a>Opprette en arbeidsordrejobb

1. Åpne arbeidsområdet **Aktivabehandling** på mobilenheten.

2. Velg **Alle arbeidsordrer for vedlikehold**.

3. Velg arbeidsordren du vil opprette en ny arbeidsordrejobb for.

4. Velg **Legg til linje**.

5. Velg **anleggsmiddelet** du vil opprette en arbeidsordrejobb for.

6. Velg **Vedlikeholdsjobbtype**, **Variant av vedlikeholdsjobbtype** og **Handel**.

7. Velg **Ferdig**.

![Figur 3](media/am-mobile-03.png)


## <a name="add-attachment-to-a-work-order-job"></a>Legge til vedlegg i en arbeidsordrejobb

1. Åpne arbeidsområdet **Aktivabehandling** på mobilenheten.

2. Velg **Alle arbeidsordrer for vedlikehold**.

3. Velg arbeidsordren > arbeidsordrejobben du vil legge til et vedlegg i.
    - Du kan også velge **Min kalender for arbeidsordrejobber** eller **Min liste for arbeidsordrejobber** på startsiden for å gå til siden **Detaljer for arbeidsordrejobb**.

4. Velg **Vedlegg** på siden **Detaljer for arbeidsordrejobb**.

5. Du vil se eksisterende vedlegg i arbeidsordrejobben. Velg **Legg til vedlegg**.

6. Angi **Navn** og **Merknader** for vedlegget.

7. Velg **Velg bilde** for å velge et bilde fra mobilgalleriet, eller **Ta bilde** for å ta et bilde.

8. Velg **Ferdig**.

![Figur 4](media/am-mobile-04.png)


## <a name="view-maintenance-checklist-on-a-work-order-job"></a>Vise kontrolliste for vedlikehold på en arbeidsordrejobb

1. Åpne arbeidsområdet **Aktivabehandling** på mobilenheten.

2. Velg **Alle arbeidsordrer for vedlikehold**.

3. Velg arbeidsordren > arbeidsordrejobben du vil vise kontrollister for.
    - Du kan også velge **Min kalender for arbeidsordrejobber** eller **Min liste for arbeidsordrejobber** på startsiden for å gå til siden **Detaljer for arbeidsordrejobb**.

4. Velg **Kontrolliste** på siden **Detaljer for arbeidsordrejobb**.

5. Det vises en liste over kontrollistelinjer som er knyttet til arbeidsordrejobben. Velg en kontrollistelinje for å vise **Instruksjoner** og legge til **Merknader**.

6. Velg Tilbake-knappen (**<**) for å gå tilbake til forrige side.

![Figur 5](media/am-mobile-05.png)


## <a name="view-and-update-asset-counters-on-a-work-order-job"></a>Vise og oppdatere anleggsmiddeltellere i en arbeidsordrejobb

1. Åpne arbeidsområdet **Aktivabehandling** på mobilenheten.

2. Velg **Alle arbeidsordrer for vedlikehold**.

3. Velg arbeidsordren > arbeidsordrejobben du vil vise anleggsmiddeltellere for.
    - Du kan også velge **Min kalender for arbeidsordrejobber** eller **Min liste for arbeidsordrejobber** på startsiden for å gå til siden **Detaljer for arbeidsordrejobb**.

4. Velg **Anleggsmiddeltellere** på siden **Detaljer for arbeidsordrejobb**.

5. Det vises en liste over anleggsmiddeltellere som er knyttet til arbeidsordrejobben. Velg blyantikonet på en anleggsmiddeltellerlinje for å oppdatere tellerverdien.

6. Angi en ny tellerverdi, og velg **Fullført**.

![Figur 6](media/am-mobile-06.png)


## <a name="register-consumption-on-a-work-order-job"></a>Registrere forbruk i en arbeidsordrejobb

1. Åpne arbeidsområdet **Aktivabehandling** på mobilenheten.

2. Velg **Alle arbeidsordrer for vedlikehold**.

3. Velg arbeidsordren > arbeidsordrejobben du vil legge til forbruksregistreringer for.
    - Du kan også velge **Min kalender for arbeidsordrejobber** eller **Min liste for arbeidsordrejobber** på startsiden for å gå til siden **Detaljer for arbeidsordrejobb**.

4. Velg **Journaler** på siden **Detaljer for arbeidsordrejobb**.

5. Velg **Legg til timer** for å opprette arbeidstimeregistreringer.
    1. Velg **Kategori** fra oppslaget.
    2. I **Timer**-feltet angir du antallet arbeidstimer som er brukt på arbeidsordrejobben.
    3. Velg aktuell **Linjeegenskap**.
    4. Velg **Ferdig**.

6. Velg **Legg til varer** for å opprette vareregistreringer.
    1. Velg **Varenummer** fra oppslaget.
    2. Velg **Område** fra oppslaget.
    3. Angi **Antall** varer som skal forbrukes.
    4. Velg **Ferdig**.

7. Velg **Legg til utgift** for å opprette utgiftsregistreringer.
    1. Velg **Kategori** fra oppslaget.
    2. Angi antallet for utgiftsregistreringen.
    3. Velg **Salgsvaluta** fra oppslaget.
    4. Angi **Kostpris** for utgiftsregistreringen.
    5. Velg **Ferdig**.

![Figur 7](media/am-mobile-07.png)


## <a name="update-lifecycle-state-on-a-work-order"></a>Oppdatere livsløpstilstand på en arbeidsordre

1. Åpne arbeidsområdet **Aktivabehandling** på mobilenheten.

2. Velg **Alle arbeidsordrer for vedlikehold**.

3. Velg arbeidsordren du vil oppdatere livsløpstilstand for.

4. Velg **Oppdater tilstand**-knappen nederst på skjermen.

5. Velg en ny livsløpstilstand fra listen.

6. Velg **Ferdig**.

![Figur 8](media/am-mobile-08.png)


## <a name="create-a-maintenance-request"></a>Opprette en vedlikeholdsanmodning

1. Åpne arbeidsområdet **Aktivabehandling** på mobilenheten.

2. Velg **Alle vedlikeholdsforespørsler**.

3. Velg **Handlinger** nederst på skjermen, og velg deretter **Opprett vedlikeholdsforespørsel**.

4. Hvis nummerserie er aktivert for vedlikeholdsforespørsler i **Aktivastyring**, skjules feltet **Vedlikeholdsforespørsel** fordi det fylles ut automatisk. Hvis feltet **Vedlikeholdsforespørsel** vises, angir du en ID for vedlikeholdsforespørsel.

5. Velg **Type vedlikeholdsforespørsel**.

6. Angi en **Beskrivelse** vedlikeholdsforespørselen.

7. Velg **Anleggsmiddel** du vil opprette forespørselen for.

8. Velg **Servicenivå** for vedlikeholdsforespørselen.

9. Velg **Ferdig**.

![Figur 9](media/am-mobile-09.png)


## <a name="add-attachment-to-a-maintenance-request"></a>Legge til vedlegg i en vedlikeholdsforespørsel

1. Åpne arbeidsområdet **Aktivabehandling** på mobilenheten.

2. Velg **Alle vedlikeholdsforespørsler**.

3. Velg vedlikeholdsforespørselen du vil legge til et vedlegg i.

4. Velg **Vedlegg** nederst på skjermen.

5. Velg **Legg til vedlegg**.

6. Angi **Navn** og **Merknader** for vedlegget.

7. Velg **Velg bilde** for å velge et bilde fra mobilgalleriet, eller **Ta bilde** for å ta et bilde.

8. Velg **Ferdig**.

![Figur 10](media/am-mobile-10.png)

