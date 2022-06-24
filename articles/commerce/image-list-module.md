---
title: Bildelistemodul
description: Denne artikkelen dekker bildelistemoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8e47c9806c21de24f0e519d0132374d2e1ff2bbf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892806"
---
# <a name="image-list-module"></a>Bildelistemodul

[!include [banner](includes/banner.md)]

Denne artikkelen dekker bildelistemoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.

Bildelistemodulen kan brukes slik at du enkelt kan legge til en samling med bilder (matrise) på områdesider. Hvert bilde i matrisen kan konfigureres med avsnittetstekst og koblings-URL-adresser. Bildelistemodulen passer best til å vise merkelogoer eller en liste som inneholder logoer.

> [!IMPORTANT]
> - Bildelistemodulen er tilgjengelig i Commerce-modulbiblioteket fra Dynamics 365 Commerce 10.0.20-versjonen.
> - Bildelistemodulen presenteres i Adventure Works-emnet.

Illustrasjonen nedenfor viser et eksempel der en bildelistemodul viser en liste over tekst som inneholder logoer på en forretning-til-forbruker-side (B2C) for Adventure Works.

![Eksempel på en bildelistemodul som viser en liste over tekst som inneholder logoer](./media/Image_list.PNG)

Illustrasjonen nedenfor viser et eksempel der en bildelistemodul viser merkelogoer på en forretning-til-forretning-side (B2B) for Adventure Works.

![Eksempel på en bildelistemodul som viser logoer](./media/Image_list_B2B.PNG)

## <a name="image-list-module-properties"></a>Bildelistemodul-egenskaper

| Egenskapsnavn | Verdier | beskrivelse |
|---------------|--------|-------------|
| Overskrift       | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Tekstoverskrift for bildelistemodulen. |
| Bildeliste    | Bilder, tekst og URL-adresser | Hvert element i matrisen er et bilde som følges av avsnittets tekst og en URL. |

## <a name="add-an-image-list-module-to-a-new-page"></a>Legge til en bildelistemodul på en ny side

Hvis du vil legge til en bildelistemodul på en ny side og angi de nødvendige egenskapene i Commerce-områdebyggeren, følger du disse trinnene.

1. Gå til **Maler**, og åpne markedsføringsmalen for områdets hjemmeside (eller opprett en ny markedsføringsmal).
1. I **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Bildeliste**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider**, og åpne områdets hjemmeside (eller opprett en ny hjemmeside ved hjelp av markedsføringsmalen).
1. På **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Bildeliste**, og deretter velger du **OK**.
1. I egenskapsruten for bildelistemodulen legger du til en overskrift (for eksempel **Våre merker**).
1. Legg til et bildelisteelement, og angi et bilde, noe avsnittetstekst og en URL-adresse for omadressering.
1. Legg til og konfigurer flere bildelistemoduler etter behov.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Adventure Works-tema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
