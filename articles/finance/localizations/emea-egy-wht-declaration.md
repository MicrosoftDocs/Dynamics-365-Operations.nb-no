---
title: Deklarering av kildeskatt for Egypt
description: Dette emnet beskriver hvordan du konfigurerer og genererer deklareringer for kildeskatt for Egypt.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4e3d68ac003fabaa504ffe81b8bf2f7ff8d7538d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839798"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a>Deklarering av kildeskatt for Egypt (EG-00005)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a>Oversikt
Dette emnet beskriver hvordan du kan sette opp og generere deklarering av forskuddsskatt og skjemaene 11 og 41 for deklarering av kildeskatt for juridiske enheter i Egypt 

Alle egyptiske enheter må klargjøre skjema 41, som summerer alle skatter som oppbevares fra lokale leverandører og leverandører. I tillegg til skjema 41 må skjema 11 genereres for detaljert å beskrive alle opptjente avgifter fra utenlandske leverandører. 

Rapporten **Deklarering av kildeskatt** i Dynamics 365 Finance inkluderer følgende rapporter:

- Deklareringsskjema nr. 41
- Deklareringsskjema nr. 11
    
    
## <a name="prerequisites"></a>Forutsetninger
Primæradressen for den juridiske enheten må være i Egypt.
I arbeidsområdet **Funksjonsstyring** må følgende funksjon være aktivert:

   - **Global kildeskatt**

Hvis du vil ha mer informasjon om hvordan du aktiverer funksjoner, kan du se [Oversikt over funksjonsstyring.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

1. Gå til **Avgift** > **Oppsett** > **Parametere** > **Parametere for økonomimodul** og sett **Aktiver global kildeskatt** til **Ja** i fanen **Kildeskatt**.
2. I arbeidsområdet **Elektronisk rapportering** importerer du følgende formater for elektronisk rapportering fra repositoriet:

    - WHT-deklarering Excel (EG)

    > [!NOTE]
    > Formatet ovenfor er basert på **mva-deklareringsmodellen** og bruker **tilordningen av mva-deklareringsmodellen**. Denne tilleggskonfigurasjonen blir importert automatisk.

Hvis du vil ha mer informasjon om hvordan du importerer konfigurasjoner for elektronisk rapportering, kan du se [Laste ned konfigurasjoner for elektronisk rapportering fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Laste ned konfigurasjoner for elektronisk rapportering

Implementeringen av WHT-deklareringsskjemaene for Egypt er basert på konfigurasjoner for elektronisk rapportering (ER). Hvis du vil ha mer informasjon om funksjonene og begrepene for rapportering som kan konfigureres, kan du se [Elektronisk rapportering](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

For miljøer av produksjons- og brukergodkjenningstesting (UAT), følger du instruksjonene i emnet [Laste ned konfigurasjoner for elektronisk rapportering fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Hvis du vil generere kildeskattdeklareringer i en egyptisk juridisk enhet, må du laste opp følgende konfigurasjoner:

- Tax declaration model.version.82.xml eller nyere
- Tax declaration model mapping.version.82.133.xml eller nyere
- WHT Declaration Excel (EG).version.82.21 eller nyere

Etter at du har lastet ned ER-konfigurasjonene fra Lifecycle Services (LCS) eller det globale repositoriet, fullfører du fremgangsmåten nedenfor.

1. Gå til arbeidsområdet **Elektronisk rapportering** og velg flisen **Rapporteringskonfigurasjoner**.
1. På siden **Konfigurasjoner** velger du **Exchange > Last fra XML-fil** i handlingsruten.
1. Last opp alle filene i den rekkefølgen de er oppført i de forrige oversiktene. Når alle konfigurasjonene er lastet opp, skal konfigurasjonstreet være til stede i Finance.

## <a name="set-up-application-specific-parameters"></a>Konfigurere programspesifikke parametere

Med det programspesifikke parameteralternativet kan brukere fastsette kriteriene for hvordan avgiftstransaksjonene klassifiseres og beregnes på hver linje i en generert rapport, avhengig av konfigurasjonen til **varegruppen for kildeskatt** eller andre kriterier som er fastsatt i oppslagsdefinisjonen.

Skjema 41 for kildeskattdeklarering inkluderer en bestemt kolonne der kildeskattransaksjonen må klassifiseres i samsvar med skattemyndighetens klassifisering kalt **Rabattkodetype**. I stedet for å inkludere disse nye klassifiseringene som nye oppføringsdata når transaksjonene posteres, bestemmes klassifiseringene basert på forskjellige oppslag som introduseres i **Konfigurasjoner** > **Konfigurere programspesifikke parametere** > **Oppsett** for å oppfylle kravene til kildeskattrapporter for Egypt. 

Følgende konfigurasjon brukes til å klassifisere transaksjonene i rapporten skjema 41 for kildeskattdeklarering:

- **DiscountTaxTypeLookup**-> Kolonne nr. 18 

Fullfør fremgangsmåten nedenfor for å sette opp de ulike oppslagene som brukes til å generere WHT-deklarering og relaterte bøker. 

1. I arbeidsområdet **Elektroniosk rapportering** velger du **Konfigurasjoner** > **Oppsett** for å identifisere hvordan transaksjoner blir klassifisert i rapporten for WHT-deklarering. 
2. Velg den gjeldende versjonen, og velg oppslagsnavnet i hurtigfanen **Oppslag**. For eksempel **DiscountTaxTypeLookup**. Dette oppslaget identifiserer listen over rabattyper som kreves av skattemyndigheten.
3. I hurtigfanen **Betingelser** velger du **Legg til**, og i den nye linjen i kolonnen **Oppslagsresultat** velger du den relaterte linjen som representerer klassifiseringen i **Kolonne 18**.
4. I kolonnen **Varegruppe for kildeskatt** velger du den relaterte koden som brukes til å identifisere klassifiseringen. For eksempel **Tillatt rabatt**.  
5. Gjenta trinn 3 og 4 for alle tilgjengelige oppslag.
6. Velg **Legg til** på nytt for å ta med sluttpostlinjen, og velg **Ikke tilgjengelig** i kolonnen **Oppslagsresultat**. 
7. I den gjenstående kolonnene velger du **Ikke tom**. 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a>Konfigurere parametere for økonomimodul

Hvis du vil generere rapporter for WHT-deklareringsskjema i Microsoft Excel, definerer du et ER-format på siden **Parametere for økonomimodul**.

1. Gå til **Avgift** > **Oppsett** > **Parametere for økonomimodul**.
2. Velg **WHT-deklarering Excel (EG)** i feltet **Tilordning av format for WHT-deklarering** i fanen **Kildeskatt**. Hvis du lar feltet stå tomt, genereres standard mva-rapport i SSRS-format.


![Deklareringsskjema](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a>Generere skjemaene for kildeskattdeklarering
Prosessen med å klargjøre og sende et skjema for kildeskattdeklarering for en bestemt periode er basert på kildeskattransaksjonene som er postert under utligningen og postering av betalingsavgiftsjobben. Hvis du vil ha mer informasjon om global kildeskatt, kan du se [Global kildeskatt](../general-ledger/global-withholding-tax-overview.md).

Fullfør fremgangsmåten nedenfor for å generere mva-deklareringsrapporten.

1. Gå til **Avgift** > **Deklareringer** > **Kildeskatt** > **Kildeskattbetaling*.
2. Velg utligningsperioden og velg deretter Fra-datoen for rapporten. 
3. Angi transaksjonsdatoen, og velg deretter **OK**.
4. I dialogboksen som åpnes, velger du en eller flere av skjematypene **Skjema nr. 41**, **Skjema nr. 11** eller **Ingen**. Hvis du velger **Ingen**, genereres standardrapporten. 
5. Velg språket. Alle rapporter er oversatt i **en-us** og **ar-eg**.
6. Angi avdelingen og navnet på banken der mva-betalingen skal betales.
7. Velg forretningstypen, og angi deretter sjekk- og dokumentnumrene. 
8. Angi enhetstypen. 
9. Angi navnet på personen som er registrert for å tilordne skjemaet, og velg **OK** for å bekrefte rapportgenereringen. 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
