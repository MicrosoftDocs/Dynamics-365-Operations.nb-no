---
title: Topptekstmodul
description: Dette emnet dekker topptekstmoduler og beskriver hvordan du oppretter sideoverskrifter i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261450"
---
# <a name="header-module"></a>Topptekstmodul


[!include [banner](includes/banner.md)]

Dette emnet dekker topptekstmoduler og beskriver hvordan du oppretter sideoverskrifter i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

I Dynamics 365 Commerce omfatter en sideoverskrift flere moduler, for eksempel modul for topptekst, navigasjonsmeny, søk, kampanjebanner og samtykke til informasjonskapsler. 

Topptekstmodulen inneholder en områdelogo, koblinger til navigasjonshierarkiet, koblinger til andre sider på området, et kurvsymbol, et ønskelistesymbol, påloggingsalternativer og søkefelt. En topptekstmodul optimaliseres automatisk for enheten som området vises på (altså for en skrivebordsenhet eller mobilenhet). På en mobilenhet er for eksempel navigasjonsfeltet skjult i en **Meny**-knapp (som også kalles en *hamburgermeny*).

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

1. Opprett et fragment kalt **Topptekstfragment**, og legg til en containermodul i den.
1. I egenskapsruten for containermodulen setter du **Bredde**-egenskapen til **Fyll container**.
1. Legg til moduler for kampanjebanner og samtykke til informasjonskapsler i containermodulen.
1. Legg til en ny containermodul i fragmentet, og sett **Bredde**-egenskapen til **Fyll container**.
1. Legg til en topptekstmodul i den andre containermodulen.
1. Legg til en navigasjonsmenymodul i **Navigasjonsmeny**-sporet i topptekstmodulen. 
1. Konfigurer egenskapene for navigasjonsmenymodulen i egenskapsruten for navigasjonsmenymodulen.
1. Legg til en søkemodul i **Søk**-sporet i topptekstmodulen. 
1. Konfigurer egenskapene for søkemodulen i egenskapsruten for søkemodulen. 
1. I sporet **Kortikon** i topptekstmodulen legger du til en handlekurvikonmodul. 
1. Konfigurer egenskapene for handlekurvikonmodulen i egenskapsruten for handlekurvikonmodulen. Hvis du vil at handlekurvikonet skal vise en minikurv ved peking over, velger du **Sann** for **Vis minikurv**.
1. Lagre sidefragmentet, fullfør redigeringen, og publiser det. 


For å sikre at det vises en topptekst på hver side, kan du følge denne fremgangsmåten på hver sidemal som opprettes for området.

1. I **Hoved**-sporet på standardsiden legger du til topptekstsidefragmentet som inneholder topptekstmodulen, i toppteksten.
1. Lagre malen, fullfør redigeringen, og publiser den.

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
