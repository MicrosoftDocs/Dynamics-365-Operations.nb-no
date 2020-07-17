---
title: Administrere robots.txt-filer
description: Dette emnet beskriver hvordan du administrerer robots.txt-filer i Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brishoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4b3856a7a0b4b198e71ce9af6691b1d90362f3e7
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533419"
---
# <a name="manage-robotstxt-files"></a>Administrere robots.txt-filer


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du administrerer robots.txt-filer i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Robotutelukkelsestandarden, eller robots.txt, er en standard som nettsteder bruker for å kommunisere med Web-roboter. Den instruerer Web-roboter om alle områder av et nettsted som ikke bør besøkes. Roboter brukes ofte av søkemotorer til å indeksere nettsteder.

Hvis du vil utelate roboter fra en server, oppretter du en fil på serveren. I denne filen angir du en tilgangspolicy for roboter. Filen må være tilgjengelig via HTTP på den lokale URL-adressen **/robots.txt**. Robots.txt-filen hjelper søkemotorene med å indeksere innholdet på nettstedet ditt.

Dynamics 365 Commerce lar deg laste opp en robots. txt-fil for domenet ditt. For hvert domene i Commerce-miljøet kan du laste opp én robots. txt-fil og knytte den til dette domenet.

Hvis du vil ha mer informasjon om robots.txt-filen, kan du gå til [siden Web-roboter](https://www.robotstxt.org/).

## <a name="upload-a-robotstxt-file"></a>Laste opp en robots.txt-fil

Etter at du har opprettet og redigert robots.txt-filen i henhold til [robotutelukkelsestandarden](https://www.robotstxt.org/orig.html), må du kontrollere at filen er tilgjengelig på datamaskinen der du skal bruke verktøyene for handelsredigering. Filen må hete **robots.txt**. For best resultat må den være i formatet som er notert i standarden. Hver Commerce-kunde er ansvarlig for å validere og vedlikeholde innholdet i robots.txt-filen. Hvis du vil laste opp en robots.txt-fil, må du være logget på Commerce som systemadministrator.

Hvis du vil laste opp en robots.txt-fil i Commerce, gjør du følgende:

1. Logg på Commerce som systemadministrator.
2. I den venstre navigasjonsruten velger **Leierinnstillinger** (ved siden av tannhjulsymbolet) for å utvide den.
3. Velg **robots.txt** under **Leierinnstillinger**. En liste over alle domenene som er knyttet til miljøet ditt, vises i hoveddelen av vinduet.
4. Velg **Administrer** for å laste opp en robots.txt-fil for et domene i miljøet ditt.
5. På menyen til høyre velger du **Last opp**-knappen (pilen som peker oppover) ved siden av domenet som er knyttet til robots.txt-filen. En filleser-dialogboks vises.
6. I dialogboksen blar du til og velger robots.txt-filen du vil laste opp for det tilknyttede domenet, og deretter velger du **Åpne** for å fullføre opplastingen.

> [!NOTE] 
> Under opplasting kontrollerer Commerce at filen er en tekstfil, men den validerer ikke innholdet i filen.

## <a name="download-a-robotstxt-file"></a>Laste ned en robots.txt-fil

Hvis du vil laste ned en robots.txt-fil i Commerce, gjør du følgende:

1. Logg på Commerce som systemadministrator.
2. I den venstre navigasjonsruten velger **Leierinnstillinger** (ved siden av tannhjulsymbolet) for å utvide den.
3. Velg **robots.txt** under **Leierinnstillinger**. En liste over alle domenene som er knyttet til miljøet ditt, vises i hoveddelen av vinduet.
4. Velg **Administrer** for å laste ned en robots.txt-fil for et domene i miljøet ditt.
5. På menyen til høyre velger du **Last ned**-knappen (pilen som peker nedover) ved siden av domenet som er knyttet til robots.txt-filen. En filleser-dialogboks vises.
6. I dialogboksen går du til ønsket plassering på den lokale stasjonen, bekrefter eller skriver inn et filnavn, og deretter velger du **Lagre** for å fullføre nedlastingen.

> [!NOTE]
> Denne fremgangsmåten kan brukes til å laste ned bare robots.txt-filer som tidligere ble lastet opp via redigeringsverktøyene for handel.

## <a name="delete-a-robotstxt-file"></a>Slette en robots.txt-fil

Hvis du vil slette en robots.txt-fil i Commerce, gjør du følgende:

1. Logg på Commerce som systemadministrator.
2. I den venstre navigasjonsruten velger **Leierinnstillinger** (ved siden av tannhjulsymbolet) for å utvide den.
3. Velg **robots.txt** under **Leierinnstillinger**. En liste over alle domenene som er knyttet til miljøet ditt, vises i hoveddelen av vinduet.
4. Velg **Administrer** for å slette en robots.txt-fil for et domene i miljøet ditt.
5. På menyen til høyre velger du **Slett**-knappen (papirkurvsymbolet) ved siden av domenet som er knyttet til robots.txt-filen. Et filleser-vindu vises.
6. I filleser-vinduet blar du til og velger robots.txt-filen du vil slette for domenet, og deretter velger du **Åpne**. En advarselsboks vises.
7. I meldingsboksen velger du **Slett** for å bekrefte slettingen av robots.txt-filen.

> [!NOTE] 
> Denne fremgangsmåten kan brukes til å slette bare robots.txt-filer som tidligere ble lastet opp via redigeringsverktøyene for handel.

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere domenenavnet](configure-your-domain-name.md)

[Distribuere et nytt e-handelsområde](deploy-ecommerce-site.md)

[Opprette et e-handelsområde](create-ecommerce-site.md)

[Knytte et nettområde til en kanal](associate-site-online-store.md)

[Laste opp URL-adresser for omadressering samtidig](upload-bulk-redirects.md)

[Konfigurere en B2C-leier i Commerce](set-up-B2C-tenant.md)

[Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md)

[Konfigurere flere B2C-leiere i et Commerce-miljø](configure-multi-B2C-tenants.md)

[Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md)

[Aktivere stedsbasert butikkregistrering](enable-store-detection.md)
