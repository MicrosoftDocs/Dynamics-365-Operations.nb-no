---
title: Vis versjonshistorikk for å tilbakestill sider og fragmenter
description: Denne artikkelen beskriver hvordan du kan vise versjonshistorikken for en side eller et fragment og gå tilbake til en eldre versjon i Microsoft Dynamics 365 Commerce-områdebyggeren.
author: phinneyridge
ms.date: 06/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: fa2ecdd9d9bc7e60b279d850573b5caa6df2c659
ms.sourcegitcommit: 9cfccb5c260ce56a3457f9ea12e80f54ea55a3b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183679"
---
# <a name="view-version-history-to-revert-pages-and-fragments"></a>Vis versjonshistorikk for å tilbakestill sider og fragmenter

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Denne artikkelen beskriver hvordan du kan vise versjonshistorikken for en side eller et fragment og gå tilbake til en eldre versjon i Microsoft Dynamics 365 Commerce-områdebyggeren.

Ved hjelp av Commerce-områdebyggeren kan du vise versjonshistorikken til en side eller et fragment og gå tilbake til en bestemt tidligere versjon av et dokument om nødvendig. Når et dokument er åpent, kan du velge **Vis logg** på kommandolinjen for å åpne dialogboksen **Versjonslogg**, der **Versjon**-fanen viser historikken til alle versjoner og lagrer aktiviteter for siden eller fragmentet. Du kan deretter velge en tidligere versjon av dokumentet i listen, forhåndsvise det og gjenopprette det som gjeldende versjon. **Aktivitet**-fanen i dialogboksen viser hele aktivitetshistorikken for dokumentet, inkludert alle lagrede, publisere og upubliserte hendelser.

> [!NOTE]
> Det opprettes en ny versjon av et dokument hver gang en områdeforfatter gjør endringer, og deretter velger **Fullført redigering** for dokumentet. 

Følg denne fremgangsmåten for å vise versjonshistorikken for en side eller et fragment og gå tilbake til en tidligere versjon.

1. I områdebyggeren åpner du siden ellerfragmentet du vil vise versjonshistorikken for.
1. På kommandolinjen velger du **Vis logg**.

    ![Vis logg-knappen.](./media/version-history-1.png)

1. I dialogboksen **Versjonslogg**, på **Versjon**-fanen, velger du en tidligere versjon av dokumentet. Egenskapsruten til høyre viser en forhåndsvisning av den valgte versjonen, og informasjon om hvem som endret den og når.

    ![Listevisning av versjonshistorikk.](./media/version-history-2.png)

1. Hvis du vil vise en fullstendig gjengitt forhåndsvisning av den valgte versjonen av dokumentet, velger du **Forhåndsvisning**. Hvis du vil lukke forhåndsvisningen og gå tilbake til dialogboksen **Versjonshistorikk**, velger du **Avslutt forhåndsvisning**.
1. Hvis du vil gjenopprette en tidligere versjon av et dokument, velger du det i listen på **Versjon**-fanen og velger deretter **Gjenopprett**. Meldingsboksen **Gjenopprett versjon \<version number\>** vises og ber deg om å bekrefte gjenopprettingshandlingen. 

    ![Gjenopprett-knappen og boksen med bekreftelsesmeldingen.](./media/version-history-3.png)

1. Velg **Gjenopprett** for å fortsette med gjenopprettingshandlingen. Områdebyggeren oppdateres og viser den gjenopprettede versjonen av siden ellerfragmentet.
1. Hvis du vil publisere den gjenopprettede versjonen, velger du **Fullfør redigering** og deretter **Publiser**.
