---
title: Ordrebekreftelsesmodul
description: Dette emnet dekker ordrebekreftelsesmoduler og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6914f8c968b03c05a2311a31a4f391c828db5b8b35bc864504dad78f43b3623f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733852"
---
# <a name="order-confirmation-module"></a>Ordrebekreftelsesmodul

[!include [banner](includes/banner.md)]

Dette emnet dekker ordrebekreftelsesmoduler og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.

Ordrebekreftelsesmodulen brukes til å vise ordrebekreftelsesdetaljer etter at en ordre er lagt inn. Den viser ID-en for ordrebekreftelse, ordrekontaktinformasjon og andre ordredetaljer, for eksempel varene som ble kjøpt, betalingsinformasjon, hentealternativer og forsendelsesmetoden.

## <a name="order-confirmation-module-properties"></a>Egenskaper for ordrebekreftelsesmodul

| Egenskapsnavn  | Verdier | Beskrivelse |
|----------------|--------|-------------|
| Overskrift        | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Ordrebekreftelsesmodulen kan ha en overskrift. Som standard brukes **H2**-overskriftskoden for overskriften. Koden kan imidlertid endres for å oppfylle tilgjengelighetskravene. |
| Kontaktnummer | Text | Et kontaktnummer kan angis for spørsmål som er knyttet til ordren. |
| Vis informasjon om hentetidspunkt | Sann eller Usann | Denne egenskapen er tilgjengelig i Dynamics 365 Commerce 10.0.15 og nyere. Hvis den er Sann, vises informasjon om hentetidspunkt hvis det er angitt for en hentevare|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a>Moduler som kan brukes på en ordrebekreftelsesside

Når du oppretter en ordrebekreftelsesside, kan du legge til andre relevante moduler i tillegg til ordrebekreftelsesmodulen. Her er noen eksempler:

- **Anbefalingsmodulen** – Anbefalingsmodulen kan legges til på ordrebekreftelsessiden for å foreslå andre produkter for kunden.
- **Markedsføringsmoduler** – Enhver markedsføringsmodul kan legges til på ordrebekreftelsessiden for å vise markedsføringsinnhold.

## <a name="add-an-order-confirmation-module-to-a-page"></a>Legge til en ordrebekreftelsesmodul på en side

Hvis du vil legge til en ordrebekreftelsesmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Gå til **Maler**, og velg **Ny** for å opprette en ny mal.
1. I dialogboksen **Ny mal**, under **Malnavn**, angir du navnet **Ordrebekreftelsesmal**, og velg deretter **OK**.
1. I **Tekst**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Standardside**-modulen, og deretter velger du **OK**.
1. På **Hoved**-sporet på **Standardside**-modulen velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Ordrebekreftelses**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise malen. Ordrebekreftelsesmodulen blir ikke gjengitt fordi den krever konteksten til ordrebekreftelsesnummeret.
1. Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider**, og velg **Ny** for å opprette en ny side.
1. I **Velg en mal**-dialogboksen velger du **Ordrebekreftelsesmal**. Under **Sidenavn** angir du **Side for ordrebekreftelse**, og velger deretter **OK**.
1. På **Hoved**-sporet på **Standardside**-modulen velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Ordrebekreftelses**-modulen, og deretter velger du **OK**.
1. I egenskapsruten for ordrebekreftelsesmodulen velger du **Overskrift** ved siden av blyantsymbolet.
1. I **Overskriftstekst**-feltet i dialogboksen **Overskrift** angir du overskriftsteksten **Ordrebekreftelse**, og deretter velger du **OK**.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Handlekurvmodul](add-cart-module.md)

[Handlekurvikonmodul](cart-icon-module.md)

[Kassemodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Leveringsalternativmodul](delivery-options-module.md)

[Henteinformasjonsmodul](pickup-info-module.md)

[Gavekortmodul](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]