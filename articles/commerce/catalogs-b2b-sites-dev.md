---
title: Utvidbarhetsinnvirkning for Commerce-kataloger for B2B-tilpasninger
description: Denne artikkelen beskriver påvirkningen av handelskatalogene for B2B-funksjonen i Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 06d304226270c9c63c6907190dc1038a38f70e44
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136807"
---
# <a name="extensibility-impact-of-commerce-catalogs-for-b2b-customizations"></a>Utvidbarhetsinnvirkning for Commerce-kataloger for B2B-tilpasninger

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver påvirkningen av **handelskatalogene for B2B-funksjonen** i Microsoft Dynamics 365 Commerce.

Hvis du er interessert i å utvide katalogkonteksten til egendefinerte scenarioer, kan det hende at tilpasningene må oppdateres. Denne oppdateringen følger standardprosessen som kunder må følge, fordi tilpasningene kanskje ikke automatisk støtter de siste funksjonene etter at oppgraderinger er utført. Hvis tilpasningene inkluderer alle nye funksjoner eller reparasjonsfiler for reparasjoner de har erfaringer med, anbefaler vi at du oppdaterer tilpasningskoden tilsvarende. Denne oppdateringen likner på endringene som Microsoft kan ha gjort for kjernekoden.

Gå gjennom tilpasningstilfeller som følger, for å finne ut om tilpasningene må oppdateres.

> [!NOTE]
> - Alle handels-API-er (Application Programming Interfaces) må være katalogbevisste. Det er derfor kritisk at du har sender **CatalogID**-parameteren.
> - Standardkatalogen (**CatalogID**=**0**) er ikke en gyldig katalog for påloggede B2B-brukere (bedrift-til-bedrift). Derfor vil alle API-kall som sender 0 eller bruker en standardverdi, mislykkes, fordi områdebrukere ikke har tilgang til katalog 0. For å få riktig opplevelse må kunde-API-kall oppdateres slik at de sender katalog-ID-en som ble valgt i katalogvelgeren. Hvis du bruker en standardverdi og brukeren bytter kataloger, må nettstedet angi dataene for den valgte katalogen. I samsvar med API-ene som kjøres fra kjernehandelskoden, bør derfor tilpassede API-er sende den valgte katalogen.

Følgende tilpasningstilfeller krever utviklingsoppdateringer:

- **Sak 1:** En kunde introduserer sin egen [datahandling](e-commerce-extensibility/data-actions.md) som kaller en produktrelatert API eller datahandling. Følgende oppdateringstrinn kreves:

    1. Hvis datahandlingen bruker en direkte API-samtale, oppdaterer du datahandlingen slik at den sender katalog-ID-en, som vist i eksemplet nedenfor.

        ![Oppdatert datahandling som sender katalog-ID-en.](./media/customization1_a.png)

    1. Hvis datahandlingen kaller en annen produktrelatert datahandling i tilpasningen, må koden oppdateres slik at den sender noen nye parametere, for eksempel **requestContext**. **RequestContext**-parameteren brukes til å hente gjeldende katalog-ID, som vist i eksemplet nedenfor.

        ![Oppdatert datahandling som sender den nye parameteren.](./media/customization1_b.png)

- **Sak 2:** En kunde har en [overstyrt datahandling](e-commerce-extensibility/data-action-overrides.md). Følgende oppdateringstrinn kreves:

    - Oppdater datahandlingen som for sak 1.

- **Sak 3:** En kunde har en visningsutvidelse, skriptinnsprøytningsmodul eller [klonet modul](e-commerce-extensibility/modules-overview.md#clone-a-module-library-module) som inneholder kall til API-er eller datahandlinger. Følgende oppdateringstrinn kreves:

    - Oppdater koden som for sak 1, som vist i eksemplet nedenfor.

       ![Oppdatert kode som sender den nye parameteren.](./media/customization3.png)

- **Sak 4:** En kunde bruker et **getById**-API-kall. Følgende oppdateringstrinn kreves:

    - Bytt til **getByIds**-API-kallet i stedet, fordi **getById**-APT-kallet har noen begrensninger, og støtter ikke katalogbevissthet.

- **Sak 5:** En kunde har en datahandling som henter informasjon for flere produkter som kan være fra ulike kataloger. Følgende oppdateringstrinn kreves:

    - Del API-kall etter katalog-ID. For handlekurv-API-er kan for eksempel handlekurven inneholde produkter fra ulike kataloger. Produktlinjene må grupperes etter katalog-ID, og de bør kalle API for hver katalog separat, som vist i eksemplet nedenfor.

        ![Oppdatert datahandling som grupperer produktlinjer etter katalog-ID.](./media/customization5.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Opprett handelskataloger for B2B-områder](catalogs-b2b-sites.md)

[Vanlige spørsmål om handelskataloger for B2B](catalogs-b2b-sites-FAQ.md)

[Katalogvelgermodul](catalog-picker.md)
