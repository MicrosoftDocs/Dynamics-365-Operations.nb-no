---
title: Bruke visningsinnstillinger for produktdimensjoner
description: Dette emnet dekker visningsinnstillingene for produktdimensjoner og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 80a0861c51ea14ddb6bce02d757667adac34e740cd04311e26211d9bdbae4ed8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716228"
---
# <a name="apply-display-settings-for-product-dimensions"></a>Bruke visningsinnstillinger for produktdimensjoner

[!include [banner](includes/banner.md)]


Dette emnet dekker visningsinnstillingene for produktdimensjoner og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce støtter størrelse, stil og fargedimensjoner for å skille produktvarianter. Dimensjoner vises som regel som tekstverdier, for eksempel Liten, Middels og Stor for størrelser, og Svart og Brun for farger. Hvis et produkt støtter mange variasjoner, kan det være vanskelig å bla gjennom produktvarianter fordi flere valg kreves for å vise bildet for hver variant. For å gjøre det enklere å bla gjennom produktvarianter, kan versjon 10.0.20-utgivelsen av Commerce bruke bilder og heksadesimalkoder (heksadesimal) til å vise dimensjoner som prøver.

I Commerce-områdebyggeren defineres dimensjonsinnstillinger på **Områdeinnstillinger \> Utvidelser \> Dimensjonsinnstillinger**. Illustrasjonen nedenfor viser et eksempel på dimensjonsinnstillinger i områdekonfigurator.

![Eksempel på områdeinnstillinger i Commerce-områdebyggeren.](./dev-itpro/media/swatch_site_settings.PNG)

To dimensjonsinnstillinger er tilgjengelige:

- **Dimensjoner som skal vises som bilde** – Angi hvilke dimensjoner som skal vises som prøver på e-handelsområdesider, for eksempel produktdetaljsider (PDPer) og resultatlistesider for søk. En hvilken som helst kombinasjon av farge-, størrelse- og stildimensjoner kan vises som en prøve. Hvis en dimensjon er valgt for visning som en prøve, vil gjengivelse av Commerce-modulen se etter en tilgjengelig konfigurasjon av en heksakodeprøve. Hvis ingen heksakode er konfigurert, vil systemlogikk se etter en konfigurasjon av en bilde-URL-prøve. Hvis verken en heksakode eller en bilde-URL er konfigurert, vises teksten.

    Illustrasjonen nedenfor viser et eksempel der en PDP på en e-handelsside inneholder farge- og størrelsesprøver. I dette eksemplet konfigureres en heksakode for fargedimensjonen. Derfor vises prøver som farger. Men verken en heksakode eller en bilde-URL er konfigurert for størrelsesdimensjonen. Derfor vises tekst.

    ![Eksempel på fargedimensjonen som vises som prøver på en produktdetaljside for e-handel.](./dev-itpro/media/swatch_pdp.png)

- **Dimensjoner som skal vises i produktkortet** – Angi hvilke dimensjoner som skal vises på produktkort som vises i lister og på listesider. Før en dimensjon kan vises på et produktkort, må denne innstillingen være aktivert for denne dimensjonen. Innstillingen **Dimensjoner som skal vises som bilde** bør også være aktivert. Virkemåten for valg av prøve på produktkort er optimert for fargedimensjonen. For andre dimensjoner kan det være nødvendig å angi et visningstillegg for å tilpasse virkemåten for valg av prøve.

    Illustrasjonen nedenfor viser et eksempel der en listeside på et e-handelområde inneholder produktkort som inneholder fargeprøver.

    ![Eksempel på fargedimensjonen som vises som prøver på en listeside for e-handel.](./dev-itpro/media/swatch_searchresults.PNG)

Hvis du vil ha mer informasjon om hvordan du konfigurerer produktdimensjoner slik at de vises som prøver på områdesider, kan du se [Konfigurere produktdimensjonsverdier som skal vises som prøver](./dev-itpro/dimensions-swatch.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Modul for søkeresultater](search-result-module.md)

[Kjøpsboksmodul](add-buy-box.md)

[Konfigurere produktdimensjonsverdier som skal vises som prøver](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
