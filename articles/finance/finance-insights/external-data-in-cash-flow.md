---
title: Eksterne data i kontantstrømprognoser
description: Denne artikkelen beskriver oppsettrinnene som må fullføres, slik at eksterne data kan registreres eller importeres i kontantstrømprognoser.
author: RyanCCarlson2
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f0cb05770dc2fbd4e13af261b5f0a0e117a2f6d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846980"
---
# <a name="external-data-in-cash-flow-forecasts"></a>Eksterne data i kontantstrømprognoser

[!include [banner](../includes/banner.md)]

Eksterne data kan registreres eller importeres til kontantstrømprognoser. Denne artikkelen beskriver oppsettrinnene som gjelder spesielt for bruk av eksterne data, og som gjør det mulig å inkludere de eksterne dataene i en kontantstrømprognose.

## <a name="external-data-setup"></a>Oppsett av eksterne data

Bruk kategorien **Ekstern kilde** på siden **Oppsett for kontantstrømprognose** (**Kontant- og bankbehandling \> Kontantstrømprognose \> Oppsett for kontantstrømprognose**) for å angi innstillinger som støtter bruk av eksterne data i kontantstrømprognoser.

Eksterne data kan registreres eller importeres til kontantstrømprognoser. Før eksterne data legges inn eller importeres, må eksterne kilder defineres. Definer eksterne kontantstrømkategorier i kategorien **Ekstern kilde**. En kategori kan enten være **Utgående** eller **Innkommende**. **Likviditet** må velges som posteringstype. I rutenettet **Innstillinger for juridisk enhet** velger du de juridiske enhetene og de tilsvarende hovedkontoene som de eksterne kontantstrømkategoriene gjelder for.

Hvis du vil ha mer informasjon om hvordan du definerer kontantstrømprognoser, kan du se [Kontantstrømprognose](../cash-bank-management/cash-flow-forecasting.md).

## <a name="enter-external-data"></a>Angi eksterne data

Hvis du vil angi og endre eksterne data for kontantstrømprognoser, kan du bruke **Åpne i Excel**-opplevelsen. Velg knappen **Eksterne data** på arbeidsområdesiden **Kontantstrømprognose**, og velg deretter enten **Legg til eksterne data** eller **Rediger eksisterende eksterne data**. Når Microsoft Excel-filen åpnes, kan du angi informasjon i følgende felt:

- **Post-ID** (unik)
- **Beskrivelse** (valgfritt)
- **Eksternt kildenavn** – Velg en av verdiene i listen som du definerte da du konfigurerte Finance Insights.
- **Juridisk enhet**
- **Dato**
- **Beløp i transaksjonsvaluta**
- **Valutakode**
- **Standarddimensjon** (valgfritt)
- **Dokumentnummer** (valgfritt)
- **Kontonummer** (valgfritt)
- **Kontonavn** (valgfritt)

## <a name="importing-external-data-by-using-the-data-management-framework"></a>Importere eksterne data ved hjelp av dataadministrasjonsrammeverk

Du kan importere eksterne data for kontantstrømprognoser ved hjelp av **Dataadministrasjon**-arbeidsområdet og enheten for **ekstern kildeoppføring for kontantstrømprognose**.

Hvis du i tillegg må flytte oppsettdata fra ett miljø til et annet, er følgende enhetsområde tilgjengelig for oppsettabellene som kreves:

- Oppsett av ekstern kilde for kontantstrømprognose
- Oppsett av juridisk enhet for ekstern kilde for kontantstrømprognose

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
