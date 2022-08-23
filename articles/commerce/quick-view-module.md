---
title: Hurtigvisningsmodul
description: Denne artikkelen dekker hurtigvisningsmoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 16f4b0aad803434f10a1c0ab8375552772ee534a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286871"
---
# <a name="quick-view-module"></a>Hurtigvisningsmodul

[!include [banner](includes/banner.md)]

Denne artikkelen dekker hurtigvisningsmoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.

Med hurtigvisningsmodulen kan brukere raskt vise produktinformasjon når de blar gjennom produkter på en listeside og legger til én eller flere produkter i handlekurven fra listesiden, uten å måtte gå til produktdetaljersiden (PDP). Modulen for hurtigvisning gir en oversikt over produktinformasjonen som brukerne trenger for å ta en avgjørelse om å legge til i handlekurv. Den inneholder også en kobling til PDP-en, slik at brukere kan vise flere produktdetaljer og innkjøpsalternativer.

Modulen for hurtigvisning støttes av modulene for [produktsamling](product-collection-module-overview.md) og [søkeresultater](search-result-module.md).

> [!IMPORTANT]
> Hurtigvisningsmodulen er tilgjengelig fra Commerce versjon 10.0.17-versjonen.

Illustrasjonen nedenfor viser et eksempel på en hurtigvisningsmodul på en produktlisteside.

![Eksempel på en hurtigvisningsmodul på en produktlisteside.](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a>Modulegenskaper

Modulen for hurtigvisning støtter noen av de samme funksjonene som kjøpsboksmodulen. Derfor ligner egenskapene til en hurtigvisningsmodul egenskapene til en kjøpsboksmodul.

| Egenskap | Verdier | beskrivelse |
|----------------|--------|-------------|
| Overskriftsetikett | **H1**, **H2**, **H3**, **H4**, **H5** eller **H6** | Denne egenskapen definerer overskriftsetiketten for produkttittelen. Hvis hurtigvisningsmodulen er øverst på siden, bør denne egenskapen settes til **H1** for å oppfylle tilgjengelighetsstandardene. |
| Tillat egendefinert pris | **Sann** eller **Usann** | Hvis denne egenskapen er satt til **Sann**, kan brukeren angi en egendefinert pris. |
| Minstepris | Heltall | Denne egenskapen gjelder bare hvis egenskapen **Tillat egendefinert pris** er satt til **Sann**. Den definerer minimumsprisen som brukeren kan angi (for eksempel USD 1). |
| Maksimumspris | Heltall | Denne egenskapen gjelder bare hvis egenskapen **Tillat egendefinert pris** er satt til **Sann**. Den definerer maksimumsprisen som brukeren kan angi (for eksempel USD 1 000). |

## <a name="commerce-site-builder-settings"></a>Innstillinger for Commerce-områdebygger

På samme måte som kjøpsboksmodulen overholder hurtigvisningsmodulen innstillingene i **Områdeinnstillinger \> Tillegg \> Legg til produkt i handlekurv**. Innstillingen **Naviger til handlekurvside** ignoreres imidlertid fordi den er inkonsekvent med formålet med hurtigvisningsmodulen, som er å gjøre det mulig for brukere å bla gjennom flere produkter på en listeside og legge dem til i handlekurven uten å gå bort fra listesiden.

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a>Legge til en hurtigvisningsmodul på en produktsamlingsmodul

En hurtigvisningsmodul kan legges til produktsamlings- og søkeresultatmodulene.

Følg denne fremgangsmåten for å legge til en hurtigvisningmodul i en produktsamlingsmodul i Commerce-områdebyggeren.

1. Gå til **Sider**, og velg hjemmesiden for Fabrikam-området.
1. Gå til en **Produktsamling**-modul på hjemmesiden, velg ellipsen (**...**), og velg deretter **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Hurtigvisning**-modulen, og deretter velger du **OK**.
1. I overskriftsruten i modulen **Hurtigvisning** velger du **Overskrift**. I dialogboksen **Overskrift** angir du **Overskriftsnivå**-feltet til **H2**, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Kjøpsboksmodul](add-buy-box.md)

[Produktsamlingsmodul](product-collection-module-overview.md)

[Søkeresultatmodul](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
