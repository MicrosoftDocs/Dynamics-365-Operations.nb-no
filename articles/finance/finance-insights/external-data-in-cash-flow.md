---
title: Bruke eksterne data i kontantstrømprognoser (forhåndsversjon)
description: Dette emnet beskriver oppsettrinnene som må fullføres, slik at eksterne data kan registreres eller importeres i kontantstrømprognoser.
author: rcarlson
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: ae0eba6d397725cf425d9781a597d904e1958d44
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009399"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a>Bruke eksterne data i kontantstrømprognoser (forhåndsversjon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Eksterne data kan registreres eller importeres til kontantstrømprognoser. Dette emnet beskriver oppsettrinnene som gjelder spesielt for bruk av eksterne data, og som gjør det mulig å inkludere de eksterne dataene i en kontantstrømprognose.

## <a name="external-data-setup"></a>Oppsett av eksterne data

Bruk kategorien **Ekstern kilde** på siden **Oppsett for kontantstrømprognose** (**Kontant- og bankbehandling \> Kontantstrømprognose**) for å angi innstillinger som støtter bruk av eksterne data i kontantstrømprognoser.

Hvis du vil ha informasjon om oppsettet, se [Kontantstrømprognose](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).

Hvis du vil angi eksterne data for kontantstrømprognoser, kan du bruke Åpne i Excel-opplevelsen for å registrere og endre eksterne data. Velg knappen **Eksterne data**, og velg deretter enten **Legg til eksterne data** eller **Rediger eksisterende eksterne data**. Når Microsoft Excel-filen åpnes, kan du angi informasjon i følgende felt:

- **Post-ID**
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

#### <a name="privacy-notice"></a>Personvernerklæring
Forhåndsversjoner (1) kan ha redusert personvern og færre sikkerhetstiltak enn Dynamics 365 Finance and Operations-tjenesten, (2) er ikke inkludert i serviceavtalen (SLA) for denne tjenesten, (3) må ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) har begrenset støtte.
