---
title: Aktivere "kjøp med lignende beskrivelse"-anbefalinger
description: Dette emnet beskriver hvordan du aktiverer produktanbefalinger av typen "kjøp lignende beskrivelse" i Microsoft Dynamics 365 Commerce.
author: bsokolov
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ce7f249d496a8cf57ad60ac33506fba3cc3dcce40cd89a0cc663ead5263e441a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755860"
---
# <a name="enable-shop-similar-description-recommendations"></a>Aktivere anbefalinger av typen Kjøp lignende beskrivelse

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du aktiverer produktanbefalinger av typen "kjøp lignende beskrivelse" i Microsoft Dynamics 365 Commerce.

Anbefalingsfunksjonen "kjøp med lignende beskrivelse" i Dynamics 365 Commerce bruker kunstig intelligens og maskinlæring (AI og ML) for å levere anbefalinger for produkter med lignende beskrivelser som produktet kunden ser etter. Ved å gjøre anbefalinger av typen "kjøp med lignende beskrivelse" tilgjengelig for alle handelskanaler i Commerce, kan forhandlere hjelpe kunder med å enkelt finner det de ønsker.

Funksjonaliteten til anbefalinger av typen "kjøp med lignende beskrivelse" bruker produktnavnet og -beskrivelsen av utvalgte produkter til å finne og anbefale visuelt lignende produkter i en forhandlers produktkatalog.

Anbefalinger av typen "kjøp med lignende beskrivelse" er tilgjengelige både på salgsstedet og i e-handelsopplevelser.

## <a name="example-scenarios"></a>Eksempelscenarioer

Følgende eksempelscenarier viser anbefalingstypene som funksjonaliteten "kjøp med lignende beskrivelse" kan tilby:

- En kunde ser et par retro hornbriller og mottar anbefalinger for andre briller med lignende utforming i sammenheng med forhandlerens bransje.
- En kunde bruker "kjøp med lignende beskrivelse"-anbefalinger til å oppdage kaffesmaker som ligner på en smak de har kjøpt fra forhandleren tidligere.

## <a name="set-up-shop-similar-description-recommendations"></a>Opprette "kjøp med lignende beskrivelse"-anbefalinger

Produktanbefalinger støttes bare for Commerce-brukere som har migrert beholdningen til Azure Data Lake Storage Gen2.

### <a name="prerequisites"></a>Forutsetninger

Før "kjøp med lignende beskrivelse"-anbefalinger kan vises til kunder, må du fullføre følgende forutsetninger:

- [Aktiver produktanbefalinger](enable-product-recommendations.md) i Commerce Headquarters.
- Kontroller at medieserveren støtter HTTPS-kall.

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a>Aktivere funksjonen for "kjøp med lignende beskrivelse"-anbefalinger

Hvis du vil aktivere anbefalingsfunksjonen "kjøp med lignende beskrivelse" i Commerce Headquarters, følger du denne fremgangsmåten.

1. I listen over tilgjengelige funksjoner i arbeidsområdet for **Funksjonsbehandling** kan du søke etter og velge **kjøp med lignende beskrivelse**.
1. Velg **Aktiver** i høyre rute.

> [!NOTE]
> Når du slår på funksjonen, begynner systemet å generere produktanbefalingslister. Det kan ta opptil en dag for disse listene å bli tilgjengelige og synlige på Internett og salgsstedsterminaler.
>
> Hvis du deaktiverer funksjonen, påvirkes ikke andre typer produktanbefalinger. Hvis du vil ha mer informasjon om produktanbefalinger, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a>Legge til en Kjøp med lignende beskrivelse-knapp på produktdetaljersiden

Når du har aktivert anbefalingsfunksjonen "kjøp med lignende beskrivelse" i Commerce Headquarters, kan du legge til en knapp for **kjøp med lignende beskrivelse** i kjøpeboksen på en side med produktdetaljer (PDP). En kunde som velger denne knappen, blir tatt med til en dedikert **Kjøp med lignende beskrivelse**-side som viser visuelt lignende produkter. Kunden kan deretter bruke velgere til å filtrere varene ytterligere.

Hvis du vil legge til en **Kjøp med lignende beskrivelse**-knapp for en PDP ved å bruke Commerce-områdebygger, gjør du følgende.

1. Åpne en eksisterende områdebyggerside som inneholder en kjøpeboksmodul.
1. Velg produktsamlingsmodulen i den venstre kjøpeboksmodulen.
1. I den høyre ruten merker du av for **Aktiver kobling til kjøp med lignende beskrivelse**.
1. Velg **Lagre**.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den. Etter at siden er publisert, vil PDP inkludere en **Kjøp med lignende beskrivelse**-knapp.

Den følgende illustrasjonen viser avmerkingsboksen **Aktiver kobling til kjøp med lignende beskrivelse** og knappen **Kjøp med lignende beskrivelse** i et eksempel-PDP i områdebyggeren.

![Avmerkingsboksen Aktiver kobling til kjøp med lignende beskrivelse og knappen Kjøp med lignende beskrivelse på en PDP i områdebyggeren.](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over produktanbefalinger](product-recommendations.md)

[Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktiver produktanbefalinger](enable-product-recommendations.md)

[Aktivere Kjøp lignende utseender-anbefalinger](shop-similar-looks.md)

[Justere anbefalingsresultater for AI-ML](modify-product-recommendation-results.md)

[Opprette kuraterte anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Vanlige spørsmål om produktanbefalinger](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]