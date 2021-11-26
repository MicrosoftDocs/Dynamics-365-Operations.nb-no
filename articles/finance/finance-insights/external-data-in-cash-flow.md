---
title: Bruke eksterne data i kontantstrømprognoser
description: Dette emnet beskriver oppsettrinnene som må fullføres, slik at eksterne data kan registreres eller importeres i kontantstrømprognoser.
author: rcarlson
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: dbfa04228cf63c0874a7d69af4e2b932544c0d7f
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/04/2021
ms.locfileid: "7753008"
---
# <a name="use-external-data-in-cash-flow-forecasts"></a>Bruke eksterne data i kontantstrømprognoser

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Eksterne data kan registreres eller importeres til kontantstrømprognoser. Dette emnet beskriver oppsettrinnene som gjelder spesielt for bruk av eksterne data, og som gjør det mulig å inkludere de eksterne dataene i en kontantstrømprognose.

## <a name="external-data-setup"></a>Oppsett av eksterne data

Bruk kategorien **Ekstern kilde** på siden **Oppsett for kontantstrømprognose** (**Kontant- og bankbehandling \> Kontantstrømprognose \> Oppsett for kontantstrømprognose**) for å angi innstillinger som støtter bruk av eksterne data i kontantstrømprognoser.

Eksterne data kan registreres eller importeres til kontantstrømprognoser. Før eksterne data legges inn eller importeres, må eksterne kilder defineres. Definer eksterne kontantstrømkategorier i kategorien **Ekstern kilde**. En kategori kan enten være **Utgående** eller **Innkommende**. **Likviditet** må velges som posteringstype. I rutenettet **Innstillinger for juridisk enhet** velger du de juridiske enhetene og de tilsvarende hovedkontoene som de eksterne kontantstrømkategoriene gjelder for.

Hvis du vil ha mer informasjon om hvordan du definerer kontantstrømprognoser, kan du se [Kontantstrømprognose](../cash-bank-management/cash-flow-forecasting.md).

## <a name="enter-external-data"></a>Angi eksterne data

Hvis du vil angi og endre eksterne data for kontantstrømprognoser, kan du bruke **Åpne i Excel**-opplevelsen. Velg knappen **Eksterne data** på siden **Oppsett for kontantstrømprognose**, og velg deretter enten **Legg til eksterne data** eller **Rediger eksisterende eksterne data**. Når Microsoft Excel-filen åpnes, kan du angi informasjon i følgende felt:

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
