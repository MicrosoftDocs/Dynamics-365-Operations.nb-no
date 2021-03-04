---
title: Ta i bruk innstillinger for beholdning
description: Dette emnet dekker beholdningsinnstillinger og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfa8b2bdc03e3698feda26932db757421097140d
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517070"
---
# <a name="apply-inventory-settings"></a>Ta i bruk innstillinger for beholdning

[!include [banner](includes/banner.md)]

Dette emnet dekker beholdningsinnstillinger og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Beholdningsinnstillinger angir om beholdningen skal kontrolleres før produkter legges til i handlekurven. De definerer også beholdningsrelaterte varemeldinger som for eksempel "På lager" og "Bare noen få igjen." Disse innstillingene sikrer at et produkt ikke kan kjøpes hvis det ikke er på lager.

Dynamics 365 Commerce gir estimater for tilgjengelig beholdning for produkter. Hvis du vil ha informasjon om hvordan estimert beholdningstilgjengelighet blir beregnet, kan du se [Beregne beholdningstilgjengelighet for detaljhandelskanaler](calculated-inventory-retail-channels.md).

I Commerce Site Builder kan du definere beholdningsterskler og -områder for et produkt eller en kategori. De bestemmer om beholdningen kan klassifiseres som på lager, få på lager eller tomt på lager. Hvis du vil ha mer informasjon, kan du se [Konfigurere beholdningsbuffere og beholdningsnivåer](inventory-buffers-levels.md).

> [!NOTE]
> Støtte for beholdningsterskler og -områder er tilgjengelig i Dynamics 365 Commerce 10.0.12-versjonen.

## <a name="inventory-settings"></a>Beholdningsinnstillinger

I Commerce defineres beholdningsinnstillinger fra **Områdeinnstillinger \> Utvidelser \> Lagerstyring** i områdebygger. Det finnes fire beholdningsinnstillinger, hvorav én er foreldet (avviklet):

- **Aktiver lagersjekk i app** – Denne innstillingen aktiverer en beholdningssjekk for et produkt. Kjøpsboks-, handlekurv- og hent i butikk-moduler kontrollerer deretter varebeholdningen, og gjør det bare mulig å legge til et produkt i handlekurven hvis varen er tilgjengelig på lager.
- **Beholdningsnivå basert på** – denne innstillingen definerer hvordan beholdningsnivåene beregnes. De tilgjengelige verdiene er **Total tilgjengelig**, **Fysisk tilgjengelig** og **Terskel for tomt på lager**. I Commerce kan du definere beholdningsterskler og -områder for hvert produkt og hver kategori. Beholdnings-API-ene returnerer beholdningsinformasjon for produkter for både **Totalt tilgjengelig**-egenskapen og **Fysisk tilgjengelig**-egenskapen. Forhandleren avgjør om **Totalt tilgjengelig**- eller **Fysisk tilgjengelig**-verdien skal brukes til å fastslå beholdningsantallet og de tilsvarende områdene for statusene "tilgjengelig på lager" og "tomt på lager".

    **Terskel for tomt på lager**-verdien for **Beholdningsnivå basert på**-innstillingen er en foreldet verdi. Når den er valgt, bestemmes beholdningstellingen av resultatene av **Totalt tilgjengelig**-verdien, men terskelen defineres av den numeriske **Terskel for tomt på lager**-innstillingen som beskrives senere. Denne terskelinnstillingen gjelder for alle produkter på et e-handelsområde. Hvis beholdningen er lavere enn terskelantallet, anses produktet å være tomt på lager. Hvis ikke anses det å være på lager. Egenskapene til **Terskel for tomt på lager**-verdien er begrenset, og vi anbefaler at du ikke bruker den i versjon 10.0.12 og nyere.

- **Beholdningsområder** – denne innstillingen definerer beholdningsområdene meldingen vises for på områdemoduler. Den gjelder bare hvis enten den **Totalt tilgjengelig**-verdien eller **Fysisk tilgjengelig**-verdien er valgt for **Beholdningsnivå basert på**-innstillingen. De tilgjengelige verdiene er **Alle**, **Få eller tomt på lager** og **Tomt på lager**.

    - Når **Alle** er valgt, vises meldinger for alle beholdningsområder – fra på lager ("Tilgjengelig"-melding) til tomt på lager ("Tomt på lager"-meldingen).
    - Når **Få eller tomt på lager** er valgt, vises meldinger for alle beholdningsområder bortsett fra "på lager" ("Tilgjengelig"-melding).
    - Når **Tomt på lager** er valgt, vises bare "Tomt på lager"-meldingen.

- **Terskel for tomt på lager** – denne gamle numeriske innstillingen vil bare tre i kraft hvis **Terskel for tomt på lager**-verdien er valgt for **Beholdningsnivå basert på**-innstillingen.

> [!IMPORTANT] 
> Disse innstillingene er tilgjengelige i Dynamics 365 Commerce 10.0.12-versjonen. Hvis du oppdaterer fra en eldre versjon av Dynamics 365 Commerce, må du manuelt oppdatere appsettings.json-filen. Hvis du vil ha instruksjoner om oppdatering av appsettings.json-filen, se [Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-inventory-settings"></a>Moduler som bruker beholdningsinnstillinger

Modulene kjøpsboks, ønskeliste, butikkvelger, handlekurv og handlekurvikon bruker beholdningsinnstillinger for å vise beholdningsområder og -meldinger.

Bildet nedenfor viser et eksempel på en PDP-side (produktinformasjon) med en melding om at varen finnes på lager ("Tilgjengelig").

![Eksempel på en PDP-modul med en "finnes på lager"-melding](./media/pdp-InStock.png)

Bildet nedenfor viser et eksempel på en PDP med en "Tomt på lager"-melding.

![Eksempel på en PDP-modul med en "ikke på lager"-melding](./media/pdp-outofstock.png)

Bildet nedenfor viser et eksempel på en handlekurv med en melding om at varen finnes på lager ("Tilgjengelig").

![Eksempel på en handlevognmodul med en "finnes på lager"-melding](./media/cart-instock.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Konfigurere lagerbuffere og lagernivåer](inventory-buffers-levels.md)

[Handlekurvmodul](add-cart-module.md)

[Kjøpsboksmodul](add-buy-box.md)

[Kontobehandlingssider og -moduler](account-management.md)

[Butikkvelgermodul](store-selector.md)

[Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]