---
title: Konfigurere kundekontobetalingsmetode for B2B-e-handelsområder
description: Dette emnet beskriver hvordan du konfigurerer betalingsmåten for kundekonto for e-handelsområder (B2B, business-to-business).
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 62e8f4949dcea1cb201bece171991047ce28da04
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799811"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Konfigurere kundekontobetalingsmetode for B2B-e-handelsområder

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer betalingsmåten for kundekonto for e-handelsområder (B2B, business-to-business).

Forhandlere kan ta imot ulike typer betaling i bytte mot produktene og tjenestene de selger i en e-handelskanal. Hver betalingstype som en forhandler godtar, må konfigureres i Microsoft Dynamics 365 Commerce når systemet defineres. Kundekontoen-betalingsmåten (eller "a konto") må støttes på B2B-e-handelsområder. 

## <a name="prerequisites"></a>Forutsetninger

1. Legg til betalingsmåten for kundekonto i Commerce Headquarters.
2. Knytt kundekontobetalingsmåten til e-handelskanalen.
3. Kontroller at **Tillat a konto** er aktivert for kunden i **Detaljhandel og handel \> Kunder \> Alle kunder \> Betalingsstandarder** i Commerce Headquarters. Kontroller også at **Kredittgrense**-parameterne er angitt på riktig måte for kunden i **Detaljhandel og handel \> Kunder \> Alle kunder \> Kreditt og innkreving** i Commerce Headquarters. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Aktivere kundekontobetalingsmetode i Commerce-områdebygger 

For å aktivere kundekontobetalingsmetode i Commerce-områdebygger, følger du trinnene nedenfor.

1. Gå til **Områdeinnstillinger \> Tillegg**.
1. Sett egenskapen **Aktiver kundekontobetalinger** til **Aktivert for B2B-kunder**. 
1. Velg **Lagre og publiser**.

> [!NOTE]
> De nye innstillingene trer i kraft bare etter at filen app.settings.json er oppdatert. Hvis du vil ha mer informasjon, kan du se [Oppdateringer for SDK og modulbibliotek](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Aktivere betalingsmåten for kundekonto på betalingssiden for B2B-e-handelsområdet

Følg disse trinnene for å aktivere betalingsmåten for kundekonto på betalingssiden for B2B-e-handelsområdet.

1. I Commerce-områdebygger finner og redigerer du utsjekkingsside eller fragmentet som inneholder utsjekkingsmodulen for B2B-e-handelsområdet.
1. I sporet **Container for betalingsdel** velger du **Legg til modul**, og deretter legger du til en **Kundekontobetaling**-modul.
1. Plasser modulen **Kundekontobetaling** ved å velge ellipsen (**...**) og deretter velge **Flytt ned** eller **Flytt opp** etter behov.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Bekrefte at betalingsmåten for kundekonto er aktivert og publisert

For å bekrefte at betalingsmåten for kundekonto er aktivert, følger du trinnene nedenfor.

1. Logg på e-handelsområdet.
1. Legg til et produkt i handlevognen.
1. Gå til utsjekkingssiden. Du skal nå¨se den nye betalingsmåten **Kundekonto**.

## <a name="additional-resources"></a>Tilleggsressurser

[Definere et B2B-e-handelsområde](set-up-b2b-site.md)

[Opprette organisasonsmodellhierarkier for B2B-organisasjoner](org-model.md)

[Administrere forretningspartnerbrukere på B2B-e-handelsområder](manage-b2b-users.md)

[Angi produktantallsgrenser for B2B-e-handelsområder](quantity-limits.md)

[Oppdateringer for SDK og modulbibliotek](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]