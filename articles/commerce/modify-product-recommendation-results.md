---
title: Justere resultater for AI-ML-basert produktanbefaling
description: Denne artikkelen beskriver hvordan du skreddersyr produktanbefalingsresultater basert på kunstig intelligens-maskinopplæring (AI-ML) til virksomheten.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d74fa013d44e0f113bdf0ce0ca9efeb943926e9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901708"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a>Justere resultater for AI-ML-basert produktanbefaling


[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du justerer produktanbefalingsresultater basert på kunstig intelligens-maskinopplæring (AI-ML) til virksomheten. 

Når produktanbefalinger er aktivert, vil standardinnstillingene tre i kraft. Disse parameterne vil fungere for mange behov. Det er best å planlegge å bruke litt tid på å vurdere om resultatene passer til salgsbevegelsen til produktene. Vi foreslår å evaluere resultatene i noen dager før du endrer parameterne etter behov, før ny testing. 

## <a name="understanding-recommendation-list-parameters"></a>Forstå parametere for anbefalingsliste

Før du endrer parameterne, kan du lære om hvordan de påvirker resultatene nedenfor.

### <a name="trending-product-list"></a>"Tendenser"-liste

"Tendenser"-listen har to parametere som kan endres:

![Eksempel på standardparametere for "Tendenser"-liste](./media/exampletrendingparameters.png)

1. **Inkluder nye produkter fra siste X dager** – Produkter som er lagt til innen det angitte antallet dager før gjeldende dato, kan brukes til å velge produktkandidater. Standardverdien i bildet foreslår at produkter som gamle har 180 dager, kan brukes i produktlisten for tendenser.
1. **Inkluder salg fra X dager** – Salgstransaksjoner som har oppstått innen det angitte antallet dager før gjeldende dato, kan brukes til å bestille produkter. Standardverdien ovenfor foreslår at alle innkjøp som er gjort for et produkt i løpet av de siste 30 dagene, blir brukt til å bestemme plasseringen av produktet i produktlisten for trendvarer. 

### <a name="best-selling-product-list"></a>Produktliste for bestselgere

Avhengig av virksomheten kan bestselgerlisten gi forskjellige resultater enn tendenser, selv om begge bruker transaksjonsdata til å bestille produkter. Siden bestselgere ikke er avkuttet basert på sortimentdato, kan bestselgere fremdeles utheve svært populære, eldre produkter som kan ha blitt slettet fra trendlisten. 

Produktlisten for "Bestselgere" har én parameter som kan endres:

![Eksempel standardparameter for bestselgerliste.](./media/examplebestsellingparameters.PNG)

1. **Inkluder salg fra X dager** – Salgstransaksjoner som har oppstått innen det angitte antallet dager før gjeldende dato, kan brukes til å bestille produkter. Standardverdien ovenfor foreslår at alle innkjøp som er gjort for et produkt i løpet av de siste 30 dagene, blir brukt til å bestemme plasseringen av produktet i produktlisten for bestselgere. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>Legge til eller fjerne produkter fra anbefalingslister manuelt

### <a name="for-new-trending-or-best-selling-lists"></a>For listene "Nye produkter", "Tendenser" og "Bestselgere"

1.  Gå til **Retail og Commerce** > **Produktanbefalinger** > **Anbefalingsparametere**.
1.  Velg **Anbefalingslister** i listen over delte parametere.
1.  Velg listen du vil legge til eller fjerne produkter fra.
1.  Hvis du vil legge til produkter i tabellen, velger du **Legg til linje**. 
1.  Under Produkt-kolonnen søker du etter et produkt etter **navn** eller **produktnummer**.

    ![Eksempel på å søke etter et produkt i den listen over nye produkter.](./media/examplenewlistconfiguration1.png)

1.  Velg ett av to alternativer under Linjetype-kolonnen:
    -   **Inkluder** – tvinger frem et produkt til fronten av listen
    -   **Ekskluder** – fjerner et produkt fra å vises i listen
    
    ![Eksempel på å inkludere eller ekskludere et produkt fra listen over nye produkter.](./media/examplenewlistconfiguration2.png)

1.  Når du endrer **Visningsrekkefølge**, endres visningsrekkefølgen for produkter merket **inkluder**, i listen.
    - Hvis to produkter har samme verdi for **visningsrekkefølge**, kan den endelige rekkefølgen for disse to resultatene avvike fra backoffice.
1.  Slik fjerner du produkter fra tabellen: Merk linjen for å fjerne, og velg **Fjern**.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>For "Folk liker også"- eller "Ofte kjøpt sammen"-lister

Når det gjelder "Ofte kjøpt sammen"- eller "Folk liker også"-lister brukes maskinopplæring til å analysere forbrukskjøpsmønstre til å anbefale relaterte produkter som ofte kjøpes sammen for et unikt seed-produkt. 
 
Et *seed-produkt* er produktet du vil generere resultater for. I forbindelse med manuell justering av anbefalingslister, legger du til eller fjerner resultater for dette produktet. 

Følg disse trinnene for å legge til eller fjerne resultater for et seed-produkt manuelt:
1.  Velg **seed-produkt**. 
1.  Under **Produkt**-kolonnen søker du etter et produkt etter **Navn** eller **Produktnummer**.
![Eksempel på søk etter produkt på listen Ofte kjøpt sammen.](./media/exampleFBTlistconfiguration1.png)
1. Velg ett av to alternativer under **Linjetype**-kolonnen:
    - **Inkluder** – tvinger frem et produkt til fronten av listen
    - **Ekskluder** – fjerner et produkt fra å vises i listen     
![Eksempel på å inkludere eller ekskludere et produkt på listen Ofte kjøpt sammen.](./media/exampleFBTlistconfiguration2.png)
1.  Slik fjerner du produkter fra tabellen: Merk linjen for å fjerne, og velg Fjern.


## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over produktanbefalinger](product-recommendations.md)

[Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktiver produktanbefalinger](enable-product-recommendations.md)

[Aktivere personlige anbefalinger](personalized-recommendations.md)

[Velge bort personlige anbefalinger](personalization-gdpr.md)

[Aktivere Kjøp lignende utseender-anbefalinger](shop-similar-looks.md)

[Legge til produktanbefalinger på salgssted](product.md)

[Legge til anbefalinger i transaksjonsskjermbildet](add-recommendations-control-pos-screen.md)

[Opprette kuraterte anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Opprette anbefalinger med demonstrasjonsdata](product-recommendations-demo-data.md)

[Vanlige spørsmål om produktanbefalinger](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]