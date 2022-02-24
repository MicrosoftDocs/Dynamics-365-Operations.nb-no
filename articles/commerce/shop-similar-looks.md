---
title: Aktiver anbefalinger av typen "kjøp lignende utseende"
description: Dette emnet beskriver hvordan du aktiverer produktanbefalinger av typen "kjøp lignende utseende" i Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: da957850072e233a41a042d5857f81ddbf178f7a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414717"
---
# <a name="enable-shop-similar-looks-recommendations"></a>Aktiver anbefalinger av typen "kjøp lignende utseende"

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du aktiverer produktanbefalinger av typen "kjøp lignende utseende" i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Anbefalingsfunksjonen "kjøp lignende utseende" i Dynamics 365 Commerce bruker kraften i kunstig intelligens og maskinlærin (AI og ML) for å levere anbefalinger for visuelt liknende produkter til kunder. Ved å gjøre anbefalinger av typen "kjøp lignende utseende" tilgjengelig for alle handelskanaler i Commerce, kan forhandlere øke kundetilfredsheten ved å bidra til at kundene enkelt finner det de ønsker.

Funksjonaliteten til anbefalinger av typen "kjøp lignende utseende" bruker produktbilder av utvalgte produktvarianter for å finne og anbefale visuelt lignende produkter i en forhandlers produktkatalog. 

Anbefalinger av typen "kjøp lignende utseende" er tilgjengelige både ved salgssted og e-handel.

### <a name="example-scenarios"></a>Eksempelscenarioer

- En kunde ser på en genser med svarte striper og får en anbefaling om en lignende genser i rødt. Kunden velger det anbefalte produktet i stedet for det opprinnelig viste produktet, og mottar deretter anbefalinger for liknende produkter i rødt. 
- En kunde bruker anbefalinger av typen "kjøp lignende utseende" for å finne samsvarende øreringer for en ring som kunden er interessert i å kjøpe.

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a>Aktivere anbefalinger av typen "kjøp lignende utseende" i Commerce Headquarters

Produktanbefalinger støttes bare for Commerce-brukere som har migrert beholdningen til Azure Data Lake Gen2.

### <a name="prerequisites"></a>Forutsetninger

Før forhandlere kan begynne å vise anbefalinger av typen "kjøp lignende utseende" for kunder, er det to nødvendige trinn:

- [Aktiver produktanbefalinger](enable-product-recommendations.md) i Commerce Headquarters.
- Kontroller at medieserveren støtter HTTPS-kall.

For at anbefalingsmotoren kan få tilgang til produktbildene, må forhandlere generere URL-adressene for produktene. Følg denne fremgangsmåten for å generere URL-adresser for produkter i Commerce Headquarters.

1. Gå til **Produktbilder**.
1. Velg **Definer mal for medier** i handlingsruten.
1. I egenskapsruten **Definer mal for medier**, under **URL-adresser for medier**, velger du **Generer URL-adresser**.

> [!NOTE]
> Når du aktiverer anbefalingsfunksjonen "kjøp likt utseende", starter prosessen med å generere produktanbefalingslister. Det kan være nødvendig med opptil én dag før disse listene er tilgjengelige og synlige på Internett og salgsstedsterminaler.

Hvis du vil aktivere anbefalingsfunksjonen "kjøp lignende utseende" i Commerce Headquarters, følger du denne fremgangsmåten.

1. Gå til **Funksjonsbehandling**.
1. I listen over tilgjengelige funksjoner kan du søke etter og velge **Kjøp lignende utseende**.
1. Velg **Aktiver** i høyre rute for å aktivere tjenesten.

Illustrasjonen nedenfor viser funksjonen **Kjøp lignende utseende** på siden **Funksjonsbehandling** i Commerce Headquarters.

![Funksjonen Kjøp lignende utseende på siden Funksjonsbehandling i Commerce Headquarters](./media/enableshopsimilarlooks.png)

Når de foregående oppgavene er fullført, forbedres POS-terminaler automatisk med et kontekstavhengig **Kjøp lignende produkter**-panelet. Ved å velge **Se mer** kan brukere av salgsstedsterminaler tas til en dedikert "kjøp likt utseende"-side som kan filtreres ytterligere.

> [!NOTE]
> Hvis du slår av anbefalingsfunksjonen "kjøp lignende utseende", påvirkes ingen andre typer produktanbefalinger. Hvis du vil ha mer informasjon om produktanbefalinger, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a>Legge til en knapp for kjøp lignende utseende på sider med produktdetaljer ved hjelp av Commerce-områdebygger

Når du har aktivert anbefalingsfunksjonen "kjøp likt utseende" i Commerce Headquarters, kan forhandlere bruke et alternativ i Commerce-områdebygger til å legge til knapp for **kjøp lignende utseende** i kjøpeboksen på en side med produktdetaljer (PDP). En kunde som velger denne knappen, blir tatt med til en dedikert "kjøp likt utseende"-side som returnerer visuelt lignende produkter. Der kan kunden kan bruke velgere til å filtrere varene ytterligere.

Hvis du vil legge til en **Kjøp lignende utseende**-knapp for en PDP ved å bruke Commerce-områdebygger, gjør du følgende.

1. Åpne en eksisterende områdebyggerside som inneholder en kjøpeboksmodul.
1. Velg produktsamlingsmodulen i den venstre kjøpeboksmodulen.
1. I den høyre navigasjonsruten merker du av for **Aktiver kobling til kjøp lignende utseende**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den. Etter at siden er publisert, vil PDP inkludere en **Kjøp lignende utseende**-knapp.

Den følgende illustrasjonen viser avmerkingsboksen **Aktiver kobling til kjøp lignende utseende** og knappen **Kjøp lignende utseende** i et eksempel-PDP i områdebyggeren.

![Avmerkingsboksen Aktiver kobling til kjøp lignende utseende og knappen Kjøp lignende utseende i et PDP i områdebyggeren.](./media/SSLecomtooling.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over produktanbefalinger](product-recommendations.md)

[Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktiver produktanbefalinger](enable-product-recommendations.md)

[Velge bort personlige anbefalinger](personalization-gdpr.md)

[Legge til produktanbefalinger i POS](product.md)

[Legge til anbefalinger på transaksjonsskjermen](add-recommendations-control-pos-screen.md)

[Justere anbefalingsresultater for AI-ML](modify-product-recommendation-results.md)

[Opprette kuraterte anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Opprette anbefalinger med demonstrasjonsdata](product-recommendations-demo-data.md)

[Vanlige spørsmål om produktanbefalinger](faq-recommendations.md)
