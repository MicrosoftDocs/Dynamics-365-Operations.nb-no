---
title: Kategorimodul
description: Dette emnet dekker fanemoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 8375c33bd6ffd3004cfc9d7b686d9a0edc77cdef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209233"
---
# <a name="tab-module"></a>Kategorimodul

[!include [banner](includes/banner.md)]

Dette emnet dekker fanemoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

Kategorimoduler er beholdere-lignende moduler som brukes til å organisere informasjonen på en områdeside i kategorier. De kan brukes på en hvilken som helst side hvor informasjon må presenteres i kategorier.

I hver kategorimodul kan én eller flere kategorielementmoduler legges til. Hver kategorielementmodul representerer én enkelt kategori. I hver kategorielementmodul kan én eller flere moduler legges til. Det er ingen begrensninger på hvilke modultyper som kan legges til i en kategorielementmodul.

Bildet nedenfor viser et eksempel på en kategorimodul på en områdeside. I dette eksemplet er kategorien **Forsendelse** valgt.

![Eksempel på en kategorimodul](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a>Egenskaper for kategorimoduler

| Egenskapsnavn | Verdier | beskrivelse |
|---------------|--------|-------------|
| Overskrift | Tekst | Denne egenskapen angir en valgfri tekstoverskrift for kategorimodulen. |
| Aktiv kategoriindeks | Tall | Denne egenskapen angir kategorien som skal være aktiv som standard når en side lastes inn. Hvis ingen verdi er angitt, er standardfunksjonen at det første kategorielementet er aktivt. |

## <a name="tab-item-module-properties"></a>Egenskaper for kategorielementmoduler

| Egenskapsnavn | Verdier | beskrivelse |
|---------------|--------|-------------|
| Stillingstittel | Tekst | Denne egenskapen angir overskriftteksten for kategorielementmodulen. |

## <a name="add-a-tab-module-to-a-page"></a>Legge til en kategorimodul på en side

Hvis du vil legge til en kategorimodul på en side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Bruk Fabrikam-markedsføringsmalen (eller en mal som ikke har begrensninger) for å opprette en ny side som heter **Butikkpolicy-side**.
1. På **Hoved**-sporet på **Standardside** velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Kategori**-modulen, og deretter velger du **OK**.
1. Velg **Overskrift** ved siden av blyantsymbolet i egenskapsruten i kategorimodulen.
1. I **Overskrift**-dialogboksen, under **Overskriftstekst**, angir du overskriftsteksten (f.eks. **Policyer**). Velg deretter **OK**.
1. I **Kategori**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Kategorielement**-modulen, og deretter velger du **OK**.
1. I egenskapsruten for kategorielementmodulen, under **Tittel**, skriver du inn tittelteksten (f.eks. **Levering**).
1. I **Kategorielement**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Tekstblokk**-modulen, og deretter velger du **OK**.
1. I egenskapsruten for tekstblokkmodulen legger du til et avsnitt med tekst under **Rik tekst**.
1. I **Kategori**-sporet legger du til et par ekstra kategorielementmoduler med overskrifter. Legg til en tekstblokkmodul med innhold i hver enkelt kategorielementmodul.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden. Siden viser en kategorimodul som inneholder kategorielementmoduler med innholdet du la til.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Beholdermodul](add-container-module.md)

[Samsvarsmodul](add-accordion.md)

[Tekstblokkmodul](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]