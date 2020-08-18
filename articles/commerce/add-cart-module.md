---
title: Handlekurvmodul
description: Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f21268ed4cffed1d5c789f722796cdf05e965819
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621042"
---
# <a name="cart-module"></a>Handlekurvmodul

[!include [banner](includes/banner.md)]

Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En handlekurvmodul viser varene som er lagt til i handlekurven før kunden går videre til kassen. Modulen viser også et ordresammendrag som lar kunden bruke eller fjerne kampanjekoder.

Handlekurvmodulen støtter pålogget utsjekking og Sjekk ut som gjest. Den støtter også koblingen **Tilbake til shopping**. Du kan konfigurere ruten for denne koblingen under **Områdeinnstillinger \> Utvidelser \> Ruter**.

Handlekurvmodulen gjengir data basert på handlekurv-IDen, som er en informasjonskapsel i leseren som er tilgjengelig i hele området. 

Bildet nedenfor viser et eksempel på en handlekurvside på Fabrikam-området.

![Eksempel på en handlevognmodul](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a>Egenskaper og spor for handlekurvmodul

Handlekurvmodulen har egenskapen **Overskrift** som kan settes til verdier som **Handlepose** og **Varer i handlekurven**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduler som kan brukes i handlekurvmodulen

- **Tekstblokk** – Denne modulen støtter tilpassede meldinger i handlekurvmodulen. Meldingene drives av innholdsbehandlingssystemet (CMS). Alle meldinger kan legges til, for eksempel "For problemer med ordren, kontakt 1-800-Fabrikam."
- **Butikkvelger** – Denne modulen viser en liste over nærliggende butikker der en vare er tilgjengelig for henting. Den lar brukere angi en plassering for å finne butikker i nærheten. Hvis du vil ha mer informasjon om denne modulen, se [Butikkvelgermodul](store-selector.md).

## <a name="module-properties"></a>Modulegenskaper

Følgende innstillinger for handlevognmodulen kan konfigureres under **Områdeinnstillinger \> Utvidelser**:

- **Maksimalt antall** – Denne egenskapen brukes til å angi maksimalt antall for hver vare som kan legges til i handlekurven. En forhandler kan for eksempel bestemme at bare 10 av hvert produkt kan selges i en enkelt transaksjon.
- **Beholdning** – Hvis du vil ha informasjon om hvordan du bruker beholdningsinnstillinger, kan du se [Bruk beholdningsinnstillinger](inventory-settings.md).
- **Tilbake til shopping** – Denne egenskapen brukes til å angi ruten for **Tilbake til shopping**-koblingen. Ruten kan konfigureres på områdenivå, slik at forhandlere kan bringe kunden tilbake til hjemmesiden eller en hvilken som helst annen side på området.

## <a name="commerce-scale-unit-interaction"></a>Samhandling med Commerce Scale Unit

Handlekurvmodulen henter produktinformasjon ved hjelp av API-er for Commerce Scale Unit. Handlekurv-IDen fra leserinformasjonskapselen brukes til å hente all produktinformasjon fra Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Legge til en handlekurvmodul på en side

Hvis du vil legge til en handlekurvmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Gå til **Sidefragmenter**, og velg **Ny** for å opprette et nytt sidefragment.
1. I dialogboksen **Nytt sidefragment** velger du **Handlevogn**-modulen.
1. Under **Navn på sidefragment** angir navnet **Handlevognfragment**, og deretter velger du **OK**.
1. Velg **Handlevogn**-sporet.
1. I egenskapsruten til høyre velger du blyantsymbolet, angir overskriftsteksten i feltet, og merker av for avmerkingssymbolet.
1. I **Handlevogn**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Butikkvelger**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.
1. Gå til **Maler**, og velg **Ny** for å opprette en ny mal.
1. I dialogboksen **Ny mal**, under **Malnavn**, angir du et navn på malen.
1. Velg **Brødtekst**-sporet i disposisjonstreet, velg ellipseknappen (**…**), og velg deretter **Legg til fragment**.
1. I dialogboksen **Velg sidefragment** velger du **Handlevognfragmentet**, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider**, og velg **Ny** for å opprette en ny side.
1. I dialogboksen **Velg en mal** velger du malen du opprettet, angir et sidenavn, og deretter velger du **OK**.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Butikkvelgermodul](store-selector.md)

[Kjøpsboksmodul](add-buy-box.md)

[Handlekurvikonmodul](cart-icon-module.md)

[Kassemodul](add-checkout-module.md)

[Ordrebekreftelsesmodul](order-confirmation-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)

[Beregne lagertilgjengelighet for detaljhandelskanaler](calculated-inventory-retail-channels.md)
