---
title: Bruke eksterne kataloger for PunchOut-e-Procurement
description: Dette emnet forklarer hvordan du kan bruke eksterne kataloger til å opprette og sende rekvisisjoner.
author: GalynaFedorova
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests, CatExternalCatalogBasketWizard, CatExternalCatalogPunchoutDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 17c473a93b7451879f1478a8c0c46fe9d8351fc4
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679282"
---
# <a name="use-external-catalogs-for-punchout-e-procurement"></a>Bruke eksterne kataloger for PunchOut-e-Procurement

[!include [banner](../includes/banner.md)]

Når du bruker eksterne kataloger for PunchOut eProcurement, trenger du ikke å vedlikeholde informasjon om leverandørens produkter i dine egne hoveddata. I stedet er handlekurven på webområdet til en leverandør konvertert til rekvisisjonslinjer som har den riktige produktinformasjonen. 

Du bør ikke vedlikeholde beskrivelser og priser for leverandørenes produkter i dine egne hoveddata for produktet. Bruk i stedet eksterne kataloger for PunchOut eProcurement. Deretter, når ansatte oppretter rekvisisjoner, de kan stemple ut til en leverandørs eksterne katalogområde (de forlater med andre ord systemet ditt og går til leverandørens område). Produktene som legges til i handlekurven på leverandørens webområde, kan deretter konverteres til rekvisisjonslinjer. Derfor får du den riktige produktinformasjonen: produkt-ID, navn, pris og så videre.

Hvis du vil bruke eksterne kataloger, må en ansatt opprette en rekvisisjon på siden **Mine innkjøpsrekvisisjoner**.

Den ansatte som oppretter rekvisisjonen, kalles klargjøreren av rekvisjonen. Som klargjører kan du utføre følgende oppgaver.

Bruk linjehandlingen **Eksterne kataloger** for å åpne en side som inneholder alle eksterne kataloger som er tilgjengelige for den angitte bestilleren, den juridiske enheten for innkjøp og mottaksdriftsenheten.

Avhengig av tillatelsene dine, kan du endre bestiller, juridisk enhet for innkjøp og mottaksdriftsenhet. En endring i disse verdiene kan endre listen over eksterne kataloger som er tilgjengelige for en bestiller. De eksterne katalogene som er tilgjengelige, avhenger av de gjeldende aktive innkjøpspolicyene for den juridiske enheten for innkjøp eller mottaksdriftsenheten. Disse policyene kan tillate eller hindre tilgang til bestemte innkjøpskategorier. Listen over eksterne kataloger som er tilordnet disse innkjøpskategoriene, kan derfor bli påvirket.

Hvis du vil ha mer informasjon om policyer, kan du se [Oversikt over innkjøpspolicyer](../procurement/purchase-policies.md).

- For å finne eksterne kataloger for bestemte innkjøpskategorier skriver du inn tekst i katalogsøkefeltet.
- Hvis du vil legge til produkter fra ekstern katalog for en leverandør på leverandørens webområde, klikker du den eksterne katalogen. Legg deretter til produkter i handlekurven, og sjekk ut. Handlekurvene overføres til Microsoft Dynamics 365.

Hvis det finnes flere alternativer for innkjøpskategoriene, velger du den riktige innkjøpskategorien før du legger til linjene i rekvisisjonen.
Når linjer er lagt til en rekvisisjon, kan du legge til flere linjer uten å bruke eksterne kataloger. Du kan også fortsette å bruke eksterne kataloger til å legge til linjer.

Når rekvisisjonen er klar, kan du bruke handlingen **Arbeidsflyt** > **Send** for å sende den til godkjenning.

### <a name="additional-resources"></a>Tilleggsressurser

- [Definere en ekstern katalog for PunchOut-e-Procurement](set-up-external-catalog-for-punchout.md)
- [Kjøp av cXML-forbedringer](purchasing-cxml-enhancements.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]