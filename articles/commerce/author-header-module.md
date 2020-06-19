---
title: Topptekstmodul
description: Dette emnet dekker topptekstmoduler og beskriver hvordan du oppretter sideoverskrifter i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a5f7ad7d9c5ff63c3c3a8fe38275eec0d138891d
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411226"
---
# <a name="header-module"></a>Topptekstmodul

[!include [banner](includes/banner.md)]

Dette emnet dekker topptekstmoduler og beskriver hvordan du oppretter sideoverskrifter i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

I Dynamics 365 Commerce omfatter en sideoverskrift flere moduler, for eksempel modul for topptekst, navigasjonsmeny, søk, kampanjebanner og samtykke til informasjonskapsler. 

Topptekstmodulen inneholder en områdelogo, koblinger til navigasjonshierarkiet, koblinger til andre sider på området, et kurvsymbol, et ønskelistesymbol, påloggingsalternativer og søkefelt. En topptekstmodul optimaliseres automatisk for enheten som området vises på (altså for en skrivebordsenhet eller mobilenhet). På en mobilenhet er for eksempel navigasjonsfeltet skjult i en **Meny**-knapp (som også kalles en *hamburgermeny*).

Bildet nedenfor viser et eksempel på en topptekstmodul på en hjemmeside.

![Eksempel på en topptekstmodul](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Egenskaper for en topptekstmodul

En topptekstmodul støtter **Logobilde**, **Logokobling** og egenskaper for **Min konto-koblinger**. 

**Logobilde**- og **Logokobling**-egenskapene brukes til å definere en logo på siden. Hvis du vil ha mer informasjon, kan du se [Legge til en logo](add-logo.md). 

Egenskapen **Min konto-koblinger** kan brukes til å definere kontosider som områdeeieren ønsker å vise hurtigkoblinger for i toppteksten.

## <a name="modules-that-are-available-in-a-header-module"></a>Moduler som er tilgjengelige i en overskriftsmodul

Følgende moduler kan brukes i en topptekstmodul:

- **Navigasjonsmeny** – Navigasjonsmenyen representerer kanalnavigasjonshierarkiet og andre statiske navigasjonskoblinger. Kanalnavigeringshierarkiet kan konfigureres i Dynamics 365 Commerce. Navigasjonsmenyen har egenskapen **Navigasjonskilde** som brukes til å angi navigasjonsmenyelementer og statiske menyelementer for Retail Server som en kilde. Hvis statiske menyelementer angis som en kilde, kan relative koblinger til andre sider på området angis. Konfigurerte varer vises deretter som topptekstnavigasjon. 

- **Søk** – Med søkemodulen kan brukere angi søkeord for å søke etter produkter. URL-adressen til standard søkeside og parameterne for søkespørringen må angis under **Områdeinnstillinger \> Utvidelser**. Søkemodulen har egenskaper som lar deg skjule søkeknappen eller etiketten etter behov. Søkemodulen støtter også alternativer for automatiske forslag, for eksempel søkeresultater for produkt, nøkkelord og kategori.

- **Handlekurvikon** – Handlekurvikonmodulen representerer handlekurvikonet, som viser antall varer i handlekurven på et gitt tidspunkt. Hvis du vil ha mer informasjon, se [Handlekurvikonmodulen](cart-icon-module.md).

## <a name="create-a-header-module-for-a-page"></a>Opprette en topptekstmodul for en side

Hvis du vil opprette en topptekstmodul, følger du trinnene nedenfor.

1. Gå til **Sidefragmenter**, og velg **Ny** for å opprette et nytt sidefragment.
1. I dialogboksen **Nytt sidefragment** velger du **Beholder**-modulen, skriver inn et navn på sidefragmentet og velger **OK**.
1. Velg **Standardbeholder**-sporet. Deretter går du til egenskapsfanen på høyre side og angir egenskapen for **Bredde** til **Fyll beholder**.
1. I **Standard beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du modulene **Kampanjebanner** og **Samtykke til informasjonskapsler**, og deretter velger du **OK**.
1. I **Standard beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. Velg **Beholder**-sporet. Deretter går du til egenskapsfanen på høyre side og angir egenskapen for **Bredde** til **Fyll beholder**.
1. I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Topptekst**-modulen, og deretter velger du **OK**.
1. I **Navigasjonsmeny**-sporet i topptekstmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Navigasjonsmeny**-modulen, og deretter velger du **OK**.
1. Konfigurer egenskapene for navigasjonsmeny-modulen i egenskapsruten etter behov.
1. I **Søk**-sporet i topptekstmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Søk**-modulen, og deretter velger du **OK**.
1. Konfigurer egenskapene for søkemodulen i egenskapsruten etter behov.
1. I **Handlevogn**-sporet i topptekstmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Handlevognikon**-modulen, og deretter velger du **OK**.
1. Konfigurer egenskapene for handlevognikon-modulen i egenskapsruten etter behov. Hvis du vil at handlekurvikonet skal vise et sammendrag av handlekurven (også kjent som en minikurv) når brukerne holder pekeren over den, velger du **Vis minikurv**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.

For å sikre at det vises en topptekst på hver side, kan du følge denne fremgangsmåten på hver sidemal som opprettes for området.

1. I **Topptekst**-sporet på **Standardside**-modulen legger du til bunntekstfragmentet du opprettet.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kjøpsboksmodul](add-buy-box.md)

[Handlekurvmodul](add-cart-module.md)

[Handlekurvikonmodul](cart-icon-module.md)

[Kassemodul](add-checkout-module.md)

[Ordrebekreftelsesmodul](order-confirmation-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)
