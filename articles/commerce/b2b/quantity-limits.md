---
title: Angi produktantallsgrenser for B2B-e-handelsområder
description: Dette emnet beskriver hvordan du konfigurerer produktantallsgrenser for bedrift-til-bedrift-e-handelsområder (B2B).
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 18dc138693dc9fb0e8cf8727de77b5f8584cde79
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690202"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a>Angi produktantallsgrenser for B2B-e-handelsområder

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer produktantallsgrenser for bedrift-til-bedrift-e-handelsområder (B2B).

De fleste produkter har en måleenhet som definerer grupperingen. Grupperingen påvirker hvordan produktene kan selges. Enkelte produkter kan ha en tilleggsgruppering for antall. Denne grupperingen bestemmer om produktene kan selges som individuelle enheter eller multiplumsenheter, og om det er en grense for minimum eller maksimum ordreantall som må følges.

Funksjonen for antallsbegrensning sikrer at minimums-, maksimums-, multiplums- og standardantall som er konfigurert i Microsoft Dynamics 365 Commerce (i standardinnstillingene for bestilling eller i innstillingene for Commerce-områdebygger), brukes for kundeordrer som er plassert på et e-handelsområde. Produktantallsgrenser støttes for øyeblikket ikke for salgsstedet og telefonsentrene.

Mange forhandlere gir mulighet for kundeordrer (også kalt spesialordrer) for å møte ulike behov. Her er noen vanlige scenarier:

- En kunde ønsker at produkter av bestemte varianter skal selges i multiplum eller få.
- En kunde ønsker å plukke opp produkter fra en butikk eller lokasjon som er forskjellig fra butikken eller plasseringen der kunden kjøpte disse produktene. Emballasjestandardene for butikkene er imidlertid forskjellige fra emballasjestandardene for online salgsdistribusjon.
- En kunde ønsker å kjøpe et produkt med begrenset kvantum som har en grense for maksimalt antall varer som kan kjøpes.

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a>Slå på funksjonen for standard ordreinnstillinger i Commerce Headquarters

Før du kan definere produktantallsgrenser, må standard ordreinnstillingsfunksjon være aktivert i Commerce Headquarters.

Følg disse trinnene for å aktivere funksjonen for standard ordreinnstillinger.

1. Gå til **Systemadministrasjon \> Arbeidsområder \> Funksjonsbehandling**.
1. Finn og velg funksjonen for **Støtte for innstillinger for område- og standardordre i kundeordren**.
1. Velg **Aktiver nå** nederst i høyre rute. 

## <a name="define-quantity-settings"></a>Definere antallsinnstillinger 

Du kan definere mengdeinnstillingene på siden **Standard ordreinnstillinger**.

Følg denne fremgangsmåten for å definere antallsinnstillingene. 

1. Gå til Produkt **Detaljhandel og handel \> Produkter og kategorier \> Utgitte produkter etter kategori**.
1. Velg et frigitt produkt.
1. På handlingsruten, i fanen **Administrer lager** i gruppen **Ordreinnstillinger**, velger du **Standard ordreinnstillinger**. 
1. På siden **Standard ordreinnstillinger** i hurtigkategorien **Salgsordre** i delen **Salgsantall** angir du produktsalgstallene:

    - **Flere** – Antallet som produktet kan kjøpes i multiplum av.
    - **Minste ordreantall** – Det minste antallet produkter som må kjøpes.
    - **Største ordreantall** – Det største antallet produkter som kan kjøpes.
    - **Standard ordreantall** – Standardantallet som angis automatisk når produktet velges.

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a>Slå på funksjonen for antallsbegrensninger for B2B-ordreantall i Commerce-områdebygger

Følg disse trinnene for å slå på funksjonen for antallsbegrensninger for B2B-ordreantall i Commerce-områdebygger.

1. Gå til **Områdeinnstillinger \> Tillegg**
1. Under **Aktiver antallsgrenser for ordre** velger du **Aktivert for B2B-kunder** i rullegardinlisten. 

> [!NOTE] 
> Oppdaterte innstillinger for områdebygger trer i kraft bare etter at filen app.settings.json er oppdatert. Hvis du vil ha mer informasjon, kan du se [Oppdateringer for SDK og modulbibliotek](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="additional-resources"></a>Tilleggsressurser

[Definere et e-handelsområde for B2B](set-up-b2b-site.md)

[Administrere B2B-forretningspartnere ved hjelp av kundehierarkier](partners-customer-hierarchies.md)

[Administrere forretningspartnerbrukere på e-handelsområder for B2B](manage-b2b-users.md)

[Konfigurere kundekontobetalingsmetode for B2B-e-handelsområder](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
