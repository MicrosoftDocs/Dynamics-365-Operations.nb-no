---
title: Kildeskattrapport for Indonesia
description: Dette emnet beskriver hvordan du konfigurerer og genererer kildeskattrapporten for Indonesia.
author: sndray
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: sndray
ms.search.validFrom: 2021-12-02
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6cf2f9240ea747054578c52343af34b15c250f38
ms.sourcegitcommit: f51e74ee9162fe2b63c6ce236e514840795acfe1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/21/2021
ms.locfileid: "7943662"
---
# <a name="withholding-tax-report-for-indonesia-id-00005"></a>Kildeskattrapport for Indonesia (ID-00005)

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du definerer og genererer PPH-filen for kildeskatt som juridiske enheter i Indonesia bruker til å rapportere kildeskattransaksjoner i e-Bupot-programmet.

Skattemyndigheten (DGT) i Indonesia fastslår at avgiftspliktige entreprenører (PKP) som er registrert på KPP Pratama som skatteskyldere/-innsamlere av inntektsskatt (PPh) Artikkel 23 eller Artikkel 26, må rapportere inntektsskatteartikkel 23 og 26 ved hjelp av e-Bupot-programmet. 

- **Artikkel 23** – Rapporten inneholder alle kildeskattransaksjoner fra leverandører der lands-/områdekoden for primæradressen er koden for Indonesia.
- **Artikkel 26** – Rapporten inneholder alle kildeskattransaksjoner fra leverandører der lands-/områdekoden for primæradressen ikke er koden for Indonesia.

## <a name="prerequisites"></a>Forutsetninger

- Primæradressen for den juridiske enheten må være i Indonesia.
- Funksjonen **Global kildeskatt** må være aktivert i arbeidsområdet **Funksjonsbehandling**. Hvis du vil ha mer informasjon om hvordan du aktiverer funksjoner, kan du se [Oversikt over funksjonsstyring.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="download-electronic-reporting-configurations"></a>Laste ned konfigurasjoner for elektronisk rapportering

Genereringen av en importfil er basert på ER-konfigurasjoner (elektronisk rapportering). Hvis du vil ha mer informasjon om funksjonene og begrepene for rapportering som kan konfigureres, kan du se [Elektronisk rapportering](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

For miljøer av produksjons- og brukergodkjenningstesting (UAT), følger du instruksjonene i [Last ned konfigurasjoner for elektronisk rapportering fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Hvis du vil generere importfilen, laster du opp følgende konfigurasjoner fra repositoriet:

- **Tax declaration model.version.93.xml** eller en nyere versjon
- **Tax declaration model mapping.version.93.153.xml** eller en nyere versjon
- **WHT PPh schema import (ID).version.93.14** eller en nyere versjon

## <a name="set-up-general-ledger-parameters"></a>Konfigurere parametere for økonomimodul

1. Gå til **Avgift** \> **Oppsett** \> **Parametere for økonomimodul**.
2. Velg **WHT PPh-skjemaimport (ID)** i feltet **Tilordning av format for WHT-deklarering** i fanen **Kildeskatt**. 
3. Gå til **Skatt** \> **Oppsett** \> **Kildeskatt** \> **Omsetningstype for kildeskatt** for å definere inntektstypen for kildeskatt for **Kode Bukti Potong**, og tilordne deretter kodene til de relaterte kildeskattgruppene for varer. Kodene kreves for å generere integreringsfilen ved hjelp av e-Bupot-programmet. 

## <a name="generate-the-withholding-import-file"></a>Generer kildeskattimportfilen

Prosessen med å klargjøre og generere e-Bupot-filen for en bestemt periode er basert på kildeskattransaksjonene som ble postert under utligningen eller postering av betalingsavgiftsjobben.

Følg denne fremgangsmåten for å generere filen.

1. Gå til **Skatt** \> **Deklareringer** \> **Kildeskatt** \> **PPH-importfilen e-bupot 23 og 26**.
2. Velg fra-dato og til-dato for rapporten, og velg deretter utligningsperioden.
3. Angi transaksjonsdatoen, og velg deretter **OK**.
4. Velg språket. Alle rapporter oversettes til amerikansk engelsk (**en-us**) og indonesisk (**id**).
5. Velg forretningstypen, og angi deretter sjekk- og dokumentnumrene. 
6. Kontroller om rapporten er signert av lederen. Denne informasjonen rapporteres i filen. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
