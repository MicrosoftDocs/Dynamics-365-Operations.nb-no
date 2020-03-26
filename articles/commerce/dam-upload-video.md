---
title: Laste opp videoer
description: Dette emnet beskriver hvordan du laster opp videoer i områdebygger for Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 98cb4f9049509dd700cf38a5d176447f86e9c824
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097063"
---
# <a name="upload-videos"></a>Laste opp videoer

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du laster opp videoer i områdebygger for Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Med mediebiblioteket for Commerce-områdebygger kan du laste opp videoer. Du bør alltid laste opp den versjonen av en video med den høyeste bithastigheten og oppløsningen, fordi videoen automatisk vil bli konvertert til å passe for forskjellige visningsporter og deres stoppunkter.

### <a name="video-information-specified-during-upload"></a>Videoinformasjon som angis under opplasting

Når du laster opp en video, kan følgende informasjon angis.

- **Tittel, beskrivelse, nøkkelord**: metadata for videoen.
- **Generer undertekster automatisk**: angir om teksting for hørselshemmede skal genereres automatisk for videoen.
- **Teksting for hørselshemmede**: angir hvilken teksting for hørselshemmede som skal brukes.
- **Vanlig lyd**: angir det vanlige lydsporet som skal brukes.
- **Miniatyrbilde**: angir miniatyrbildet for videoen. Bildet blir generert automatisk hvis det ikke angis.
- **Beskrivende lyd**: angir det beskrivende lydsporet som skal brukes.

## <a name="upload-a-video"></a>Laste opp en video

Hvis du vil laste opp en video i områdebygger, gjør du følgende:

1. Velg **Mediebibliotek** i navigasjonsruten til venstre.
1. Velg **Last opp \> Last opp medieelementer** på kommandolinjen.
1. I Filutforsker-vinduet går du til og velger én eller flere videofiler du vil laste opp, og velger deretter **Åpne**.
1. I dialogboksen **Last opp medieelement** angir du nødvendig tittel og alt-tekst.
1. Angi en valgfri beskrivelse og nøkkelord, og velg en kategori hvis ønskelig. 
1. Hvis du vil publisere bilder like etter opplastingen, merker du av for **Publiser medieelementer etter opplasting**.
1. Velg **OK**.

Hvis du laster opp flere typer aktiva samtidig (for eksempel bilder og videoer), vil du i dialogboksen **Last opp medieelement** bare kunne angi nøkkelord, om filene skal publiseres umiddelbart etter opplastingen, og om teksting for hørselshemmede skal genereres automatisk for videofiler. Alle anleggsmidlene vil dele de samme nøkkelordene.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over digital anleggsmiddelbehandling](dam-overview.md)

[Laste opp bilder](dam-upload-images.md)

[Laste opp filer](dam-upload-files.md)

[Beskjære bilder](dam-crop-images.md)

[Tilpasse bildefokuspunkter](dam-custom-focal-point.md)
