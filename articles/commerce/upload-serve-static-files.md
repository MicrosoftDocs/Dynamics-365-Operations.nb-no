---
title: Laste opp og betjene statiske filer
description: Dette emnet beskriver hvordan du laster opp en statisk fil til områdebyggeren for Microsoft Dynamics 365 Commerce, og hvordan du oppretter en egendefinert nettadresse og et filnavn som kan brukes til å be om denne filen.
author: StuHarg
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 389d33189644241dcf98da0c7f3b841e82a4430ac459dc8027284cecc299b4b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714689"
---
# <a name="upload-and-serve-static-files"></a>Laste opp og betjene statiske filer

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du laster opp en statisk fil til områdebyggeren for Microsoft Dynamics 365 Commerce, og hvordan du oppretter en egendefinert nettadresse og et filnavn som kan brukes til å be om denne filen.

Noen tredjepartskontakter krever at en fil blir lagret og betjent fra e-handelsområdet. Disse koblingene forventer at filen blir returnert ved forespørsler til en bestemt URL-bane for tilbakeringing og et filnavn. Dette emnet beskriver derfor hvordan du laster opp og betjener en statisk fil med en brukerdefinert URL-adresse og et filnavn på et Dynamics 365 Commerce-e-handelsområde.

## <a name="create-a-site-url-that-returns-a-static-file"></a>Opprett en URL-adresse for område som returnerer en statisk fil

Følg denne fremgangsmåten for å opprette en URL-adresse for område som returnerer en statisk fil i Commerce-områdebygger.

1. Gå til mediebiblioteket for området, og last opp filen som skal betjenes av forespørsler til URL-adressen du vil definere. Hvis du allerede har lastet opp filen, kan du hoppe over dette trinnet.
1. Gå til **URL-adresser** for området.
1. Velg **Ny \> Ny URL-adresse**.
1. Velg **Mediebibliotekressurs** i dialogboksen **Ny URL-adresse**.
1. I feltet **URL-bane** angir du URL-banen. Inkluder filnavnet i banen.
1. Velg **Neste**. Mediebiblioteket åpnes, og alle medieressursene for **dokumenttypen** som er lastet opp, vises.
1. Velg filen som skal betjenes for forespørsler til URL-adressen du definerte i trinn 5.
1. Velg **Lagre**.

På dette tidspunktet er URL-adressen du opprettet, i utkasttilstand. Filen som URL-adressen peker til, returneres ikke før du publiserer URL-adressen. Før du publiserer URL-adressen, kan du validere at den returnerer de riktige dataene.

## <a name="validate-and-publish-a-url"></a>Validere og publiser en URL

Hvis du vil validere en URL før du publiserer, følger du denne fremgangsmåten.

1. Gå til **URL-adresser** for området, og velg URL-adressen du vil forhåndsvise.
2. I egenskaperruten til høyre, under **Rediger**-knappen velger du den riktige URL-koblingen. Et nytt nettleservindu åpnes, og du får en 404-feilmelding.
3. Legg til **?preview=inprogress**-spørringsstrengen til URL-adressen (for eksempel `https://yoursite.com/callback.html?preview=inprogress`), og last inn siden på nytt. Filen du lastet opp til mediebiblioteket, skal returneres i svaret.

Når du har validert URL-adressen, kan du publisere den.

1. Gå til **URL-adresser** for området, og velg URL-adressen.
2. Velg **Publiser** på kommandolinjen.

## <a name="update-the-file-that-a-url-points-to"></a>Oppdater filen som en URL-adresse peker til

Når en URL-adresse er publisert, kan du oppdatere den slik at den peker til en annen fil. Du kan også oppdatere URL-adressen slik at den peker mot en annen ressurstype, som beskrevet i neste del. Du kan for eksempel peke URL-adressen til en intern side eller en omadressering.

Følg denne fremgangsmåten for å oppdatere filen som en URL-adresse peker til.

1. Gå til **URL-adresser** for området, og velg URL-adressen du vil oppdatere.
1. Velg **Rediger** i egenskapsruten til høyre.
1. Under **URL-tilordning** velger du **Trinn 2**-boksen og deretter velger du et nytt dokument fra mediebiblioteket.
1. Velg **Bruk**.

## <a name="update-the-asset-type-that-a-url-points-to"></a>Oppdater ressurstypen som en URL-adresse peker til

Du kan også oppdatere en URL-adresse slik at den peker på en annen aktivumtype (ressurs), for eksempel en intern side eller en omadressering.

Følg denne aktivumtypen for å oppdatere filen som en URL-adresse peker til.

1. Gå til **URL-adresser** for området, og velg URL-adressen du vil oppdatere.
1. Velg **Rediger** i egenskapsruten til høyre.
1. Under **URL-tilordning** under **Trinn 1** velger du en annen aktivumtype.
1. Velg **Trinn 2**-boksen, og velg deretter den nye ressursen.
1. Velg **Bruk**.

## <a name="change-the-url-path"></a>Endre URL-banen

Når en URL-adresse er opprettet, kan ikke banen endres. Hvis du må endre URL-banen som betjener en fil eller en annen ressurstype, må du opprette en ny URL-adresse, tilordne den til den eksisterende filen eller en annen ressurs, og deretter oppheve publiseringen og slette den gamle URL-adressen.

Hvis du vil endre URL-banen, følger du denne fremgangsmåten.

1. Hvis du vil opprette en ny URL-adresse og tilordne den til den eksisterende filen eller en annen ressurs, følger du instruksjonene i delen [Opprett en URL-adressen for område som returnerer en statisk fil](#create-a-site-url-that-returns-a-static-file) tidligere i dette emnet.
1. Velg den nye URL-adressen, og velg **Publiser** på kommandolinjen. Den nye URL-adressen publiseres.
1. Hvis du vil oppheve publiseringen av den gamle URL-adressen, merker du den og velger **Opphev publisering** på kommandolinjen. Du kan nå slette den gamle URL-adressen hvis du vil det.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over behandling av digitale aktiva](dam-overview.md)

[Laste opp bilder](dam-upload-images.md)

[Laste opp videoer](dam-upload-video.md)

[Laste opp andre filer enn bilder og videoer](dam-upload-files.md)

[Beskjære bilder](dam-crop-images.md)

[Tilpasse bildefokuspunkter](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]