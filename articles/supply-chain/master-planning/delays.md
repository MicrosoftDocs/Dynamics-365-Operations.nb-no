---
title: Forsinkelser
description: Dette emnet inneholder informasjon om forsinkede datoer i hovedplanlegging. En forsinket dato er en realistisk forfallsdato som en transaksjon mottar hvis den tidligste datoen for fullføring som hovedplanleggingen beregner er senere enn ønsket dato.
author: roxanadiaconu
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8e863ae63466f68e763b133da9f0e9488c6cfa6
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189352"
---
# <a name="delays"></a>Forsinkelser

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon om forsinkede datoer i hovedplanlegging. En forsinket dato er en realistisk forfallsdato som en transaksjon mottar hvis den tidligste datoen for fullføring som hovedplanleggingen beregner er senere enn ønsket dato.

Hovedplanlegging kan beregne den tidligste fullføringsdatoen for en transaksjon, basert på leveringstider, materialtilgjengelighet, tilgjengelig kapasitet og forskjellige planleggingsparametere. 

Hvis hovedplanleggingen beregner en ordredato som kommer før gjeldende dato, kan ikke ordren fullføres i tide. Derfor er ordren forsinket. I så fall fremoverplanlegger hovedplanleggingen ordren fra gjeldende dato og inkluderer leveringstider. Disse leveringstidene starter med komponentvarer på lavere nivå. Ordren får deretter en forsinkelsesdato. En forsinket dato er en realistisk forfallsdato basert på gjeldende data. Hovedplanlegging beregner også antall dager forsinket. 

I noen tilfeller kan det hende du velger ikke å beregne forsinkelser, for eksempel når brukerne vet at de kan fremskynde leveringstider ved å velge alternative leveringsmåter. 

Du kan konfigurere hvordan forsinkelser beregnes for en dekningsgruppe. Du kan deretter knytte dekningsgruppen til en vare senere. 

På siden **Hovedplanleggingsparametere** kan du angi starttidspunktet for beregning av forsinkelser. Hvis en ordre er utført etter dette tidspunktet, legges det til én dag i forsinkelsen av ordren. 

> [!NOTE]
> I tidligere versjoner ble beregnede forsinkelser kalt *terminmeldinger*, forsinkelsesdatoen ble kalt *termindatoen* og en forsinket transaksjon ble kalt *en transaksjon som var satt til fremtiden*.

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a>Begrensede forsinkelser i produksjonsoppsettet med flere stykklistenivåer
Når du arbeider med forsinkelser i et produksjonsoppsett som har flere stykklistenivåer, er det viktig å være oppmerksom på at bare varene som er direkte over varen (i stykklistestrukturen) som forårsaker forsinkelsen, blir oppdatert med en forsinkelse som del av hovedplanleggingen som kjøres. Andre varer i stykklistestrukturen vil ikke få forsinkelsen gjeldende før den første hovedplanleggingen kjøres, når den planlagte bestillingen for det øverste nivået er godkjent eller autorisert. 

For å omgå denne kjente begrensningen kan produksjonsordrene øverst i stykklistestrukturen med forsinkelser godkjennes (eller autoriseres) før den neste hovedplanleggingen kjøres. Dermed beholdes forsinkelsen fra den forsinkede, godkjente planlagte produksjonsordren, og alle underliggende komponenter blir oppdatert i henhold til dette.
Handlingsmeldinger kan også brukes til å identifisere planlagte bestillinger som kan flyttes til en senere dato på grunn av andre forsinkelser i stykklistestrukturen.

## <a name="desired-date"></a>Ønsket dato

På siden **Planlagt ordre**, i fanen **Forsinkelser** finnes **Ønsket dato** for den planlagte bestillingen. Den ønskede datoen for en planlagt bestilling er den grunnleggende datoen for forsinkelser, som er en beregnet dato som tilsvarer **Ønsket dato** som beregnes fra **Nettobehov**. Hvis den planlagte ordren er en stykklistelinje, produksjonslinje eller kanban-linje, er den ønskede datoen basert på **Behovsdato**, og den ønskede datoen vil ikke bli vist på siden **Planlagt ordre**.

## <a name="additional-resources"></a>Tilleggsressurser

[Dekningsinnstillinger](coverage-settings.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]