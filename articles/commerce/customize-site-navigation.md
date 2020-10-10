---
title: Tilpasse områdenavigering
description: Dette emnet beskriver hvordan du oppretter et tilpasset elektronisk navigasjonshierarki for å organisere produktene for weblesing på Microsoft Dynamics 365 Commerce-området.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2b6a7a3b35873e80be391c627d0397fd6398a99
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817236"
---
# <a name="customize-site-navigation"></a>Tilpasse områdenavigering


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du oppretter et tilpasset elektronisk navigasjonshierarki for å organisere produktene for weblesing på Microsoft Dynamics 365 Commerce-området.

## <a name="overview"></a>Oversikt

Nettbutikkfasader lar vanligvis kunder oppdage og bla gjennom produkter ved å navigere gjennom produktkategorier. Denne funksjonen finnes vanligvis ved hjelp av kategorier øverst på siden eller ved hjelp av et navigasjonsfelt på venstre side. I Dynamics 365 Commerce kan du opprette og behandle hierarkistrukturen for kategorinavigasjonen og produktene som er inkludert i de ulike kategoriene.

## <a name="create-a-channel-navigation-hierarchy"></a>Opprette et kanalnavigasjonshierarki

Følg denne fremgangsmåten for å opprette et kanalnavigasjonshierarki.

1. Gå til **Detaljhandel og handel \> Produkter og kategorier \> Kategori- og produktadministrering**.
1. Velg **Kategorihierarkier**, og velg deretter **Ny**.
1. Gi hierarkiet et navn.

    > [!NOTE]
    > Den øverste kategorien som du oppretter, er rotkategorinoden. Den vises ikke på området. Hvis du vil opprette et kategorihierarki der en enkelt node på øverste nivå vises på området, oppretter og navngir du kategorien som et underordnet objekt av rotkategorien.

1. Velg **Ny kategorinode**, og gi kategorien et navn.
1. Fortsett å opprette likestilte og underordnede kategorier etter behov.

Du kan nå tilordne produkter til hver kategori du opprettet under kategorien på toppnivå.

## <a name="customize-the-order-of-categories"></a>Tilpasse rekkefølgen på kategorier

Som standard vises kategoriene du definerer, i alfabetisk rekkefølge på området. Du kan imidlertid også tilpasse visningsrekkefølgen for kategorier.

## <a name="assign-a-category-hierarchy-type"></a>Tilordne en kategorihierarkitype

1. Gå til **Detaljhandel og handel \> Produkter og kategorier \> Kategori- og produktadministrering**.
1. Velg **Kategorihierarkier**.
1. I handlingsruten, i kategorien **Kategorihierarki** i gruppen **Oppsett** velger du **Tilknytt hierarkitype**.
1. Velg **Ny**.
1. I feltet **Kategorihierarkitype** velger du **Kanalnavigasjonshierarki**.
1. I feltet **Kategorihierarki** velger du kanalnavigeringshierarkiet du opprettet tidligere.

## <a name="publish-new-or-updated-navigation-hierarchies"></a>Publisere nye eller oppdaterte navigasjonshierarkier

Følg denne fremgangsmåten for å gjøre navigasjonshierarkiet tilgjengelig for nettbutikkfasaden.

1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Kanalkategorier og produktattributter**.
1. Velg nettbutikken i treet til venstre.
1. Velg **Publiser kanaloppdateringer**.
1. Gå til **Detaljhandel og handel \> IT for detaljhandel og handel \> Distribusjonsplan**.
1. Finn og velg **Jobb 1040** i listen.
1. Velg **Kjør nå**.
1. Gjenta trinn 5 og 6 for jobbene 1070 og 1150.

## <a name="show-categories-on-your-site"></a>Vise kategorier på området

Hvis du vil vise kategorihierarkiet i nettbutikkfasaden, må du legge til navigasjonsmenymodulen på riktig sted i en mal eller et fragment. Navigasjonsmenymodulen vil deretter vise navigasjonshierarkiet, forutsatt at du har publisert navigasjonshierarkiet til kanalen som området er bundet til.

> [!NOTE]
> Navigasjonsmenymodulen som er inkludert i modulbiblioteket, gjør at brukere bare kan navigere til kategorier som ikke har underkategorier. Hvis kundene skal kunne navigere til kategorier som har underkategorier, må du tilpasse navigasjonsmenymodulen.

## <a name="add-custom-navigation-options"></a>Legge til egendefinerte navigasjonsalternativer

Du kan legge til navigasjonsalternativer som ikke er en del av produktkategorihierarkiet, på navigasjonsmenyen. På slutten av listen over produktkategorier kan du for eksempel legge til en **Kontakt oss**-vare som peker til en kontaktside som du har bygget for området.

Hvis du vil legge til egendefinerte navigasjonsalternativer i navigasjonsmenyen, følger du disse trinnene.

1. I malen eller fragmentet som du vil tilpasse, velger du navigasjonsmenymodulen.
1. I egenskapsruten i kategorien **Data** velger **Legg til vare** for å opprette et nytt navigasjonselement for innholdsbehandlingssystem (CMS).
1. Angi koblingstekst og en URL-adresse.
1. Gjenta trinn 2 og 3 for å legge til flere egendefinerte navigasjonsalternativer.
1. Når du er ferdig, velger du **Lagre** for å lagre malen eller fragmentet, og velg deretter **Fullfør redigering** for å sjekke den inn.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over maler og oppsett](templates-layouts-overview.md)

[Arbeide med maler](work-with-templates.md)

[Arbeide med forhåndsinnstilte oppsett](work-with-layouts.md)

[Arbeide med fragmenter](work-with-fragments.md)

[Arbeide med moduler](work-with-modules.md)

[Opprette en URL-adresse for side](create-page-url.md)

[Arbeide med publiseringsgrupper](publish-groups.md)
