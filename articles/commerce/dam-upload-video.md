---
title: Laste opp videoer
description: Denne artikkelen beskriver hvordan du laster opp videoer i områdebyggeren for Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 06/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 3f6c426984c84e657e99b12e9522080c3042db4a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278550"
---
# <a name="upload-videos"></a>Laste opp videoer

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du laster opp videoer i områdebyggeren for Microsoft Dynamics 365 Commerce.

Med mediebiblioteket for Commerce-områdebygger kan du laste opp videoer. Du bør alltid laste opp den versjonen av en video med den høyeste bithastigheten og oppløsningen, fordi videoen automatisk vil bli konvertert til å passe for forskjellige visningsporter og deres stoppunkter.

### <a name="video-information-specified-during-upload"></a>Videoinformasjon som angis under opplasting

Når du laster opp en video, kan følgende informasjon angis.

- **Tittel, beskrivelse, nøkkelord**: metadata for videoen.
- **Generer teksting for hørselshemmede automatisk**: angir om teksting for hørselshemmede skal genereres automatisk for videoen (bare engelsk støttes). 
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

[Last opp og betjen statiske filer](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
