---
title: Oversikt over innkjøp og leverandører
description: Denne artikkelen gir en oversikt over hvilke funksjoner som er tilgjengelige i modulen Innkjøp og leverandører.
author: RichardLuan
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogListPage, CatVendorCatalogListPage, PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 58021
ms.assetid: eea24e23-a803-4de0-a218-6485757cde1b
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4911b1729c811aafc5ca76fb4351ab672e3610f6
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019710"
---
# <a name="procurement-and-sourcing-overview"></a>Oversikt over innkjøp og leverandører

[!include [banner](../includes/banner.md)]

Denne artikkelen gir en oversikt over hvilke funksjoner som er tilgjengelige i modulen Innkjøp og leverandører.

Innkjøp og leverandører dekker alle trinnene fra å identifisere et behov for produkter og tjenester gjennom å fremskaffe produktet, mottak, fakturering og behandling av betaling til leverandører. Du kan konfigurere innkjøpsprosesser mot bestemte forretningsbehov ved å definere innkjøpspolicyer og -arbeidsflyter.

## <a name="identifying-a-need-for-product-and-services"></a>Identifisere et behov for produkter og tjenester

Behovet for produkter eller tjenester som kan oppstå fra *rekvisisjoner*, for eksempel når en ansatt trenger et produkt. *Produktkataloger* kan defineres for å rettlede valget av tilgjengelige produkter å velge fra, eller forespørsler kan sendes for produkter som ennå ikke er tilgjengelig i en katalog, slik at innkjøpsavdelingen kan vurdere hvordan produktet kan leveres.  

*Forbruksbeløp* kan brukes til å begrense rekvisisjonsforbruk, og *innkjøpsarbeidsflyten* legger til alternativet om å kreve godkjenning før bestilling kan skje. Det er også mulig å angi budsjettmiddeltildelinger, om nødvendig.  

Innkjøpsavdelingen identifiserer leverandører av ønskede produkter og tjenester, og dette kan omfatte en *tilbudsforespørsel* som sendes til flere potensielle leverandører. Det er mulig å dele spesifikasjonene for det ønskede produktet, og potensielle leverandører kan vise disse for å se om de kan levere et produkt som samsvarer. Leverandører returnere bud som deretter blir gjennomgått ved innkjøpsavdelingen, før de kan velge leverandøren de ønsker å anskaffe fra.  

Bestillinger inkluderer et alternativ for å sende ut en *innkjøpsforespørsel* til leverandøren som et alternativ til en mer omfattende prosess for tilbudsforespørsel. Innkjøpsforespørselen kan brukes til å fastsette betingelser som priser, rabatter og leveringsdato for ordren. Hvis leverandører er definert for å bruke **Leverandør**-portalen, er funksjonalitet for innkjøpsforespørsel deaktivert. I stedet deles ordren på **Leverandør**-portalen, og når en *forespørsel om bekreftelse* sendes, kan leverandøren direkte bekrefte ordren.  

*Leverandørkataloger* kan brukes til å samle inn informasjon om produktsortimentet som leverandører kan levere. Leverandører kan publisere sine egne kataloger slik at det blir enklere å oppdatere katalogen. Det er mulig å knytte en *liste over godkjente leverandører* til et produkt, og dette kan være til hjelp for leverandørvalg når nye bestillinger åpnes, og forhindre bruken av utilsiktede leverandører.

## <a name="procurement"></a>Innkjøp

*Bestillinger* kan opprettes på flere forskjellige måter, blant annet:

- Som et resultat av hovedplanlegging, som har identifisert et behov som krever som et kjøp. Denne prosessen genererer planlagte bestillinger, og når de frigis, genereres det bestillinger.
- Ved hjelp av behandling av innkjøpsrekvisisjoner som fører til innkjøp.
- Via behandling av kjøpsavtaler, der bestillinger opprettes som frigitte ordrer fra avtalene. Dette brukes vanligvis når kjøpsavtaler brukes til å representere rammebestillinger.
- Manuelt, når bestillingen som opprettes, ikke er basert på et annet dokument.

Bestillinger som er konfigurert med *arbeidsflyter for godkjenning av kjøp*, krever godkjenning før de registreres som godkjent, og dette er nødvendig før ordren kan behandles videre.

Bestillinger *bekreftes* for å representere at det er opprettet en avtale med leverandøren. Bestillingen går deretter gradvis gjennom ulike tilstander og blir til slutt fakturert eller avbrutt.  

Når du oppretter en bestilling, er mange av feltene forhåndsutfylt med verdier som standard fra informasjonen som er lagret om leverandøren i på **Leverandører**-siden. Dette betyr at det er et begrenset antall felt du trenger å fylle ut på bestillingen, selv om du kan velge å overstyre standardverdiene.

### <a name="prices-and-discounts"></a>Priser og rabatter

Priser og rabatter omfatter informasjon om priser, rabatter og rabattbetingelsene som de tilbyr. Priser og rabatter kan representeres som *forretningsavtaler*. Forretningsavtaler representerer leverandørens prislister med priser eller rabatter, og har et bestemt sett med datoer som avtalen gjelder for. Priser og rabatter kan forhandles og vises gjennom *kjøpsavtaler* med betingelser som forpliktelser om å kjøpe bestemte volumer eller pengebeløp som en forutsetning for de forhandlede betingelsene. *Rabattavtaler* kan opprettes med leverandører der innkjøp av bestemte produkter eller en gruppe produkter kan utløse en rabatt fra leverandøren avhengig av innkjøpsbeløpet eller volum.

### <a name="delivery-options"></a>Alternativer for levering

Det finnes ulike alternativer for leveringsprosessen som er knyttet til en bestilling. Bestilte produkter kan deles inn i *leverings* planer, der deler av det bestilte antallet kan planlegges for levering på forskjellige datoer. Leveringen kan også inkludere *direkte levering* initiert fra en salgsordre, som automatiserer generering følgeseddelen på salgsordren samtidig som produktet registreres på bestillingen. Bestillinger kan også være en del en *konsernintern ordrekjede*, også kalt konserninterne bestillinger, der produkter bestilles fra en samsvarende konsernintern salgsordre. I denne situasjonen er noen trinn automatiske på tvers av de to relaterte konserninterne ordrene.

### <a name="supplementary-items"></a>Tilleggsvarer

Produkter kan defineres for å inkludere *tilleggsvarer*. På denne måten foreslås produkter som er relatert til produktet som bestilles. Tilleggsproduktene kan være nødvendige, eller de kan være valgfrie. I noen tilfeller kan det legges til tilleggsvarer som gratis produkter som følger med innkjøpet av andre produkter.

### <a name="purchase-order-charges"></a>Bestillingstillegg

Tillegg kan tilordnes til bestillingen. Dette kan skje automatisk gjennom oppsett av automatiske tillegg eller ved å legge til tilleggene manuelt. Tillegg kan tilordnes til ordren på overskriftsnivå, eller på ordrelinjenivå. Regnskap for tillegg kan defineres på forskjellige måter. Du kan for eksempel definere et tillegg som skal regnes som en produktkostnad. Hvis du gjør dette, må tilleggene tilordnes på ordrelinjenivå før ordren kan bekreftes. Det finnes et alternativ som kan hjelpe deg med å fordele tillegg fra ordrehodet til linjene.

## <a name="product-receipt-and-invoicing"></a>Produktkvittering og fakturering

Bestillinger som inneholder fysiske produkter, krever vanligvis at *ankomstregistreringen* skal skje i et lager, og deretter registreres en *produktkvittering* for ordren. Bestillinger med produkter som oppfyller rekvisisjoner, kan konfigureres slik at den ansatte som har bedt om produktene, må også må angi en *bekreftelse av mottak*.  

Enkelte bestillinger kan være produkter som er tjenester eller andre ikke-fysiske produkter der mottak i et lager ikke er nødvendig. Du kan opprette produkter som tjenester, eller *innkjøpskategorier* kan brukes direkte på bestillingen for slike ordrer. Med disse ordrene utelates noen ganger regnskap for produktkvittering, og ordren faktureres direkte, eller alternativt utføres produktkvitteringsregistrering på bestillingen uten noen tidligere ankomstregistrering.  

Mottak av produkter kan resultere i automatisk forbruk for et bestemt formål. Dette inkluderer implisert forbruk med direktelevering, forbruk mot et prosjekt, eller regnskapsføring av produktet som et anleggsmiddel.  

Når *leverandørfakturaer* mottas fra leverandøren, kan de først bli registrert i *ankomstregistrering* uavhengig av bestillingen, og deretter senere bli godkjent som en post mot bestillingen. Registrering av leverandørfaktura med bestillingen inkluderer samsvar for produktkvitteringen mot fakturaen.  

*Regnskapsdistribusjoner* kan angis i bestillingen for å beskrive hvordan regnskap skal skje i Finans, og kan også definere hvordan budsjettmiddeltildelinger hentes når dette er inkludert i konfigurasjonen.  

Fakturerte bestillinger registrerer gjelden i leverandørkontoen i leverandører, der *leverandørbetaling* kan behandles fra.

## <a name="vendor-performance"></a>Leverandørytelse

Ytelse og gjennomgang av innkjøp støttes via *innkjøps- og leverandørrapporter,* som inkluderer forbruksanalyse og analyse av leverandørytelse.
