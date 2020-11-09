---
title: Ordredetaljermodulen
description: Dette emnet dekker ordredetaljmoduler og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 06/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6610d2abe0a1b03ddd763f9a65fc1dab42f1da1b
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015186"
---
# <a name="order-details-module"></a>Ordredetaljermodulen

[!include [banner](includes/banner.md)]

Dette emnet dekker ordredetaljmoduler og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Ordredetaljmodulen brukes til å vise ordrebekreftelsesdetaljer etter at en ordre er lagt inn. Den viser ID-en for ordrebekreftelse, ordrekontaktinformasjon og andre ordredetaljer, for eksempel varene som ble kjøpt, betalingsinformasjon og forsendelsesmetoden.

## <a name="order-details-module-properties"></a>Egenskaper for ordredetaljermodul

| Egenskapsnavn  | Verdier | beskrivelse |
|----------------|--------|-------------|
| Overskrift        | Overskriftstekst og overskriftskode ( **H1** , **H2** , **H3** , **H4** , **H5** eller **H6** ) | Ordredetaljermodulen kan ha en overskrift. Som standard brukes **H2** -overskriftskoden for overskriften. Koden kan imidlertid endres for å oppfylle tilgjengelighetskravene. |
| Kontaktnummer | Text | Et kontaktnummer kan angis for spørsmål som er knyttet til ordren. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Moduler som kan brukes på en ordredetaljside

Når du oppretter en ordredetaljside, kan du legge til andre relevante moduler i tillegg til ordredetaljmodulen. Her er noen eksempler:

- **Anbefalingsmodulen** – Anbefalingsmodulen kan legges til på ordredetaljsiden for å foreslå andre produkter for kunden.
- **Markedsføringsmoduler** – Enhver markedsføringsmodul kan legges til på ordredetaljsiden for å vise markedsføringsinnhold.

## <a name="add-an-order-details-module-to-a-page"></a>Legge til en ordredetaljermodul på en side

Hvis du vil legge til en ordredetaljermodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Gå til **Maler** , og velg **Ny** for å opprette en ny mal.
1. I dialogboksen **Ny mal** , under **Malnavn** , angir du navnet **Ordredetaljmal** , og velg deretter **OK**.
1. I **Tekst** -sporet velger du ellipsen ( **…** ), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Standardside** -modulen, og deretter velger du **OK**.
1. På **Hoved** -sporet på **Standardside** -modulen velger du ellipseknappen ( **...** ), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Ordredetaljer** -modulen, og deretter velger du **OK**.
1. Velg **Lagre** , og velg deretter **Forhåndsvisning** for å forhåndsvise malen. Ordredetaljmodulen blir ikke gjengitt, fordi den krever konteksten til ordrebekreftelsesnummeret.
1. Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider** , og velg **Ny** for å opprette en ny side.
1. I **Velg en mal** -dialogboksen velger du **Ordredetaljmal**. Under **Sidenavn** angir du **Side for ordredetaljer** , og velger deretter **OK**.
1. På **Hoved** -sporet på **Standardside** -modulen velger du ellipseknappen ( **...** ), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Ordredetaljer** -modulen, og deretter velger du **OK**.
1. I egenskapsruten for ordredetaljmodulen velger du **Overskrift** ved siden av blyantsymbolet.
1. I **Overskriftstekst** -feltet i dialogboksen **Overskrift** angir du overskriftsteksten **Ordredetaljer** , og deretter velger du **OK**.
1. Velg **Lagre** , og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Handlekurvmodul](add-cart-module.md)

[Handlekurvikonmodul](cart-icon-module.md)

[Kassemodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Leveringsalternativmodul](delivery-options-module.md)

[Gavekortmodul](add-giftcard.md)
