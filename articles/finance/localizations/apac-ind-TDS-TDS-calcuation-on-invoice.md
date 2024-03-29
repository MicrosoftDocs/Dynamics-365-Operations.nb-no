---
title: TDS-beregning for fakturaer
description: Denne artikkelen har en referanse for transaksjoner der TDS (Tax Deducted at Source) beregnes på fakturanivået.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: efc12e0839fe87e9db435f481ce1fd733c286d6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855370"
---
# <a name="tds-calculation-on-invoices"></a>TDS-beregning for fakturaer

[!include [banner](../includes/banner.md)]

Denne artikkelen har en referanse for transaksjoner der TDS (Tax Deducted at Source) beregnes på fakturanivået.

| Serienummer | Transaksjonstype                                 | Transaksjonsbeløp | Sidenavn og valgbane                                 | Kontotype og motkontotype                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Kjøp fra leverandør / registrering av utgifter   | Debet eller kredit  | Siden Økonomijournaler (Økonomimodul > Journaloppføringer > Økonomijournaler), siden Fakturagodkjenningsjournal (Leverandører > Fakturaer > Fakturagodkjenning), siden Fakturajournal (Leverandører > Fakturaer > Fakturajournal) | Finans (debet), Leverandør (kredit)  Kildeskatt beregnes bare for kombinasjonen av Leverandør og Finans når finanskontoen har posteringstypen **Innkjøp** **kontant**. |
| 2.            | Kjøp fra kunde / registrering av utgifter | Debet eller kredit  | Siden Økonomijournaler (Økonomimodul > Journaloppføringer > Økonomijournaler), siden Fakturajournal (Leverandør > Fakturaer > Fakturajournal) | Finans (debet), Kunde (kredit)                                 |
| 3.            | Kjøp av anleggsmiddel fra leverandør              | Debet eller kredit  | Siden Økonomijournaler (Økonomimodul > Journaloppføringer > Økonomijournaler), siden Ankomstregistreringsjournal (Leverandører > Fakturaer > Ankomstregistrering), siden Fakturajournal (Leverandører > Fakturaer > Fakturajournal) | Anleggsmidler (debet) Leverandør (kredit)                             |
| 4.            | Kjøp av anleggsmiddel fra kunde            | Debet eller kredit  | Siden Økonomijournaler (Økonomimodul > Journaloppføringer > Økonomijournaler), siden Fakturajournal (Leverandør > Fakturaer > Fakturajournal) | Anleggsmidler (debet) Kunde (kredit)                           |
| 5            | Innkjøpsfaktura (TDS skyldig)                  |                    | Bestilling-siden (Leverandører > Bestillinger > Alle bestillinger) |                                                              |
| 6            | Salgsfaktura (TDS til gode)                  |                    | Salgsordre-siden (Kunder > Ordrer > Alle salgsordrer), siden Fritekstfaktura (Kunder > Fakturaer > Alle fritekstfakturaer) |                                                              |
