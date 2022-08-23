---
title: Dato for mva-register for leverandør
description: Denne artikkelen inneholder informasjon om en funksjon for aktivering av dato for mva-register for leverandør
author: AdamTrukawka
ms.date: 01/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: global
ms.author: atrukawk
ms.search.validFrom: 2022-01-15
ms.dyn365.ops.version: AX 10.0.24
ms.custom: intro-internal
ms.openlocfilehash: 4af770427f5b19eaf2a129b26d54aeacc6c2f148
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278286"
---
# <a name="date-of-vendor-vat-register"></a>Dato for mva-register for leverandør

I Microsoft Dynamics 365 Finance versjon 10.0.24 er et nytt felt, **Dato for mva-register for leverandør**, tilgjengelig for leverandørfakturaer. Dette feltet angir datoen for den avgiftspliktige forsyningen for et innkjøp.

Hvis du vil aktivere det nye feltet, kan du gå til arbeidsområdet **Funksjonsbehandling**, finne og velge funksjonen **Aktiver dato for mva-register for leverandør på leverandørfakturaer** og deretter velge **Aktiver nå**.

Innkommende fakturaer fra leverandørene dine kan ha to datoer: datoen da leverandøren utstedte fakturaen og datoen for den avgiftspliktige forsyningen (det vil si datoen da leverandøren belastet den skyldige merverdiavgiften [mva]). I noen scenarioer kan disse to datoene være forskjellige.

Du kan trekke fra det innkommende mva-beløpet for en innkjøpsfaktura og inkludere fakturaen i mva-rapporter senere, på en dato som er forskjellig fra begge datoene ovenfor. Denne datoen styres av lokale lovgivningsregler om utsettelse av innkommende mva-fradrag for enkelte scenarioer. Dette varierer etter land eller område.

Enkelte mva-rapporter, for eksempel [mva-deklareringsrapporten](emea-cze-vat-declaration-tax-declaration-model.md#vat-control-statement) i Tsjekkia, krever at datoen for den avgiftspliktige forsyningen skal rapporteres for et innkjøpsdokument. Denne datoen må rapporteres slik at skattemyndighetene kan avstemme mva-rapporteringen mellom motparter.

I Finans kan du definere datoer i følgende felter:

- **Fakturadato** – Datoen da fakturaen ble utstedt av leverandøren.
- **Dato for mva-register** – Datoen for mva-beløpfradraget for innkjøpsfakturaen.
- **Dato for mva-register for leverandør** – Datoen for den avgiftspliktige forsyningen til leverandøren.
- **Dato for dokumentmottak** – Datoen da du mottok fakturaen.

Disse feltene er inkludert på følgende sider:

- Leverandørfaktura
- Register for leverandørfaktura
- Godkjenning av leverandørfaktura
- Leverandørfakturajournal

Når leverandørfakturaen er postert, kan du gå gjennom datoene på sidene **Fakturajournal** og **Leverandørtransaksjoner**.
