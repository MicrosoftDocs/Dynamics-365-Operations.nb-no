---
title: Trekkspillmodul
description: Dette emnet dekker trekkspillmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: fa2515a0cbc5b69a1a69e15ec9e1ba2739fa2fbeffb5b0eb22b49fd8cab18e6f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719533"
---
# <a name="accordion-module"></a>Samsvarsmodul

[!include [banner](includes/banner.md)]

Dette emnet dekker trekkspillmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

Slike moduler er beholder-lignende moduler som brukes til å organisere informasjonen eller modulene på en side gjennom en skuffelignende funksjon. En trekkspillmodul kan brukes på en hvilken som helst side.

I hver trekkspillmodul kan én eller flere trekkspillelementmoduler legges til. Hver trekkspillelementmodul representerer en skjulbar skuff. I hver trekkspillelementmodul kan én eller flere moduler legges til. Det er ingen begrensninger på hvilke modultyper som kan legges til i en trekkspillelementmodul.

Bildet nedenfor viser et eksempel på en trekkspillmodul som brukes til å organisere informasjon på en side med vanlige spørsmål om en butikk.

![Eksempel på en trekkspillmodul.](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a>Egenskaper for trekkspillmoduler

| Egenskapsnavn | Verdier | beskrivelse |
|---------------|--------|-------------|
| Overskrift | Tekst | Denne egenskapen angir en valgfri tekstoverskrift for trekkspillmodulen. |
| Vis alle | **Sann** eller **Usann** | Hvis verdien er satt til **Sann**, aktiveres vis/skjul-funksjonaliteten slik at alle elementene i denne modulen kan utvides og skjules. |
| Samhandlingsstil | **Uavhengig** eller **Bare utvid ett element** | Denne egenskapen angir samhandlingsstilen for trekkspillelementer. Hvis verdien er satt til **Uavhengig**, kan hvert enkelt trekkspillelement utvides eller skjules uavhengig av hverandre. Hvis verdien er satt til **Bare utvid ett element**, kan bare ett element utvides om gangen. Når et element utvides, skjules tidligere utvidede elementer. |

## <a name="accordion-item-module-properties"></a>Egenskaper for trekkspillelementmoduler

| Egenskapsnavn | Verdier | beskrivelse |
|----------------|--------|-------------|
| Stillingstittel | Tekst | Denne egenskapen angir overskriftteksten for trekkspillelementmodulen. Ved å velge tittelområdet kan brukerne vise eller skjule delen. |
| Utvid som standard | **Sann** eller **Usann** | Hvis verdien er satt til **Sann**, utvides trekkspillelementet som standard når siden lastes inn. |

## <a name="add-an-accordion-module-to-a-faq-page"></a>Legge til en trekkspillmodul på en side med vanlige spørsmål

Hvis du vil legge til en trekkspillmodul på en side med vanlige spørsmål, og angi egenskapene i områdebygger, følger du disse trinnene.

1. Gå til **Sider**, og bruk Fabrikam-markedsføringsmalen (eller en mal som ikke har begrensninger) for å opprette en ny side som heter **Vanlige spørsmål om butikken**.
1. På **Hoved**-sporet på **Standardside** velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Trekkspill**-modulen, og deretter velger du **OK**.
1. Velg **Overskrift** ved siden av blyantsymbolet i egenskapsruten i trekkspillmodulen.
1. I **Overskrift**-dialogboksen, under **Overskriftstekst**, skriver du **Vanlige spørsmål**. Velg deretter **OK**.
1. I egenskapsruten i trekkspillmodulen merker du av for **Vis alle utvidet**-ruten, og i **Samhandlingsstil**-feltet velger du **Uavhengig**.
1. I **Trekkspill**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Trekkspillelement**-modulen, og deretter velger du **OK**.
1. I egenskapsruten for trekkspillelementmodulen, under **Tittel** skriver du inn tittelteksten (f.eks. **Hvordan fungerer returordningen?**).
1. I **Trekkspillelement**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Tekstblokk**-modulen, og deretter velger du **OK**.
1. I egenskapsruten for tekstblokkmodulen skriver du inn et avsnitt med tekst (f.eks. **Returer må behandles via kundesenteret. Ring 1-800–FABRIKAM for retur av varer. Produkter har en 30-dagers returpolicy. Returer må iverksettes innenfor denne tidsrammen.**).
1. I **Trekkspill**-sporet legger du til flere trekkspillelementmoduler. Legg til en tekstblokkmodul med innhold i hver enkelt trekkspillelementmodul.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden. Siden viser en trekkspillmodul som har innholdet du la til.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Beholdermodul](add-container-module.md)

[Kategorimodul](add-tab.md)

[Tekstblokkmodul](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]