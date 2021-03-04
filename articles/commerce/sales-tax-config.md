---
title: Konfigurer merverdiavgift for nettordrer
description: Dette emnet gir en oversikt over valg av mva-grupper for ulike nettordretyper i Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 40c20bf13779f73289e43df21b763e1b864686a7
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530203"
---
# <a name="configure-sales-tax-for-online-orders"></a>Konfigurer merverdiavgift for nettordrer

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet gir en oversikt over valg av avgiftsgrupper for ulike nettordretyper. 

Det kan hende at e-handelskanalen vil støtte alternativer som levering eller henting for nettordrer. Mva-relevansen er basert på alternativet som er valgt av nettbrukerne. Når en områdekunde velger å kjøpe en vare på nettet og mottar den levert til en adresse, blir merverdiavgiften bestemt på grunnlag av kundens mva-gruppe for leveringsadresse. Når en kunde velger å hente en kjøpt vare i en butikk, bestemmes merverdiavgiften basert på innstillingen for mva-gruppen for butikken den hentes i. 

## <a name="orders-shipped-to-a-customer-address"></a>Bestillinger sendt til en kundeadresse 

Vanligvis defineres avgifter for nettbestillinger som sender til kundeadresser, av destinasjonen. Hver mva-gruppe har en destinasjonsbasert mva-konfigurasjon der virksomheten kan definere måldetaljer som land/område, fylke, region og poststed i et hierarkisk skjema. Når en nettordre bestilles, bruker Commerce-avgiftsmotoren leveringsadressen for hver linjevare i ordren, og finner mva-grupper med samsvarende målbaserte avgiftskriterier. For en nettordre med en leveringsadresse for linjevare til San Francisco, California, vil avgiftsmotoren for eksempel finne mva-gruppen og mva-koden for California, og deretter beregne merverdiavgift for hver linjevare i henhold til dette.  

## <a name="customer-based-tax-groups"></a>Kundebaserte avgiftsgrupper

I Commerce Headquarters finnes det to steder der kundeavgiftsgrupper er konfigurert:

- **Kundens profil**
- **Kundens leveringsadresse**

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a>Hvis en kundes profil har en avgiftsgruppe konfigurert

En kundes profilpost i hovedkontoret kan ha en avgiftsgruppe konfigurert, men for nettordrer vil ikke avgiftsgruppen som er konfigurert i en kundes profil, bli brukt av avgiftsmotoren. 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a>Hvis en kundes leveringsadresse har en avgiftsgruppe konfigurert

Hvis kundens leveringsadressepost har en avgiftsgruppe konfigurert, og en nettordre (eller linjevare) skal sendes til kundens leveringsadresse, vil avgiftsgruppen som er konfigurert i kundens adressepost, bli brukt av avgiftsmotoren til avgiftsberegning.

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a>Konfigurer en avgiftsgruppe for en kundes leveringsadressepost

Følg denne fremgangsmåten for å konfigurere en avgiftsgruppe for kundens leveringsadressepost i Commerce Headquarters.

1. Gå til **Alle kunder**, og velg deretter ønsket kunde. 
1. Velg ønsket adresse i hurtigfanen **Adresser**, og velg deretter **Flere alternativer \> Avansert**. 
1. Angi merverdiavgiftsverdien etter behov under fanen **Generelt** på **Administrer adresser**-siden.

> [!NOTE]
> Avgiftsgruppen defineres ved hjelp av leveringsadressen for ordrelinjen, og de destinasjonsbaserte avgiftene konfigureres ved selve avgiftsgruppen. Hvis du vil ha mer informasjon, kan du se [Definere avgifter for nettbutikker basert på destinasjon](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="order-pickup-in-store"></a>Hent ordre i butikk

For ordrelinjer der henting i butikk eller henting utenfor butikk angitt, vil avgiftsgruppen fra det valgte butikken for henting, bli brukt. Hvis du vil ha mer informasjon om hvordan du konfigurerer avgiftsgruppen for en gitt butikk, kan du se [Angi andre mva-alternativer for butikker](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

> [!NOTE]
> Når en ordrelinje hentes i en butikk, vil kundens adresseavgiftsinnstillinger (hvis konfigurert) bli ignorert av avgiftsmotoren, og avgiftskonfigurasjonen til butikken det hentes i, blir brukt. 

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over merverdiavgift](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[Beregningsmåter for merverdiavgift i grunnlagsfeltet](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[ Mva-tilordning og overstyringer](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[Hele beløp og alternativer for intervallberegning for mva-koder](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[Beregning av mva-fritak](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]