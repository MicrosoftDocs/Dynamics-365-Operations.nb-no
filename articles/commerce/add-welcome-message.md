---
title: Legge til en velkomstmelding
description: Dette emnet beskriver hvordan du legger til en velkomstmelding i Microsoft Dynamics 365 Commerce-webområdet.
author: psimolin
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ca10b01268b5dcd4c6fe448d90cd0ebd65a2673b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001260"
---
# <a name="add-a-welcome-message"></a>Legge til en velkomstmelding


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du legger til en velkomstmelding i Microsoft Dynamics 365 Commerce-webområdet.

## <a name="overview"></a>Oversikt

En velkomstmelding på webområdet for e-handel kan informere besøkende om pågående salg, områdeoppdateringer eller tilgjengelighet for sesongsamlinger. Velkomstmeldingen angis ved hjelp av varselmodulen.

Varselmodulen skal legges til i sporet for **Feilmeldinger/Informasjonsmeldinger** i topptekstfragmentet. Ved hjelp av varselmodulen kan du angi teksten som vises, tekstfargen og justeringen. Du kan også angi om gjester på området kan ignorere meldingen.

Når en velkomstmelding blir lagt til i et delt topptekstfragment, vises den på hver side som bruker malen der det delte topptekstfragmentet brukes.

Følg denne fremgangsmåten for å legge til en velkomstmelding på området.

1. I Dynamics 365 Commerce går du til området ditt.
1. Velg **Fragmenter**.
1. Velg topptekstfragmentet du vil legge til meldingen i.
1. Utvid **Feilmeldinger/Informasjonsmeldinger** i disposisjonstreet.
1. Velg varselmodulen.

    Hvis det ennå ikke finnes en varselmodul, velger du ellipseknappen (**...**) ved siden **Feilmeldinger/Informasjonsmeldinger**, og deretter velger du **Legg til modul**. Velg varselmodulen, og velg deretter **OK**.

1. I egenskapsruten til høyre, i kategorien **Data**, velger du **Legg til datakilde**, og deretter velger du **Innhold**.
1. I feltet **Inndatatekst** skriver du inn teksten i velkomstmeldingen.
1. Lagre topptekstfragmentet, sjekk det inn, og publiser det.

Velkomstmeldingen vil nå vises øverst på alle områdesider som bruker det valgte topptekstfragmentet.

## <a name="additional-resources"></a>Tilleggsressurser

[Legge til en logo](add-logo.md)

[Velge et områdetema](select-site-theme.md)

[Arbeide med CSS-overstyringsfiler](css-override-files.md)

[Legge til et favorittikon](add-favicon.md)

[Legge til en opphavsrettserklæring](add-copyright-notice.md)

[Legge til språk på området](add-languages-to-site.md)

[Legge til skript kode i områdes ID-er for å støtte telemetri](add-telemetry.md)

