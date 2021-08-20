---
title: Bruke eksterne data i kontantstrømprognoser (forhåndsversjon)
description: Dette emnet beskriver oppsettrinnene som må fullføres, slik at eksterne data kan registreres eller importeres i kontantstrømprognoser.
author: rcarlson
ms.date: 07/16/2021
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
ms.openlocfilehash: ff2a454b422cc4decc15339e6b328d99df85ccbc66ba3928f6c9e9f21b7b51a7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768849"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a>Bruke eksterne data i kontantstrømprognoser (forhåndsversjon)

[!include [banner](../includes/banner.md)]

Eksterne data kan registreres eller importeres til kontantstrømprognoser. Dette emnet beskriver oppsettrinnene som gjelder spesielt for bruk av eksterne data, og som gjør det mulig å inkludere de eksterne dataene i en kontantstrømprognose.

## <a name="external-data-setup"></a>Oppsett av eksterne data

Bruk kategorien **Ekstern kilde** på siden **Oppsett for kontantstrømprognose** (**Kontant- og bankbehandling \> Kontantstrømprognose**) for å angi innstillinger som støtter bruk av eksterne data i kontantstrømprognoser.

Hvis du vil ha informasjon om oppsettet, se [Kontantstrømprognose](../cash-bank-management/cash-flow-forecasting.md).

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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
