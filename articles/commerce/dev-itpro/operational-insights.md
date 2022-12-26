---
title: Konfigurer Operational Insights
description: Denne artikkelen beskriver hvordan du konfigurerer og bruker funksjonen Operational Insights i Microsoft Dynamics 365 Commerce.
author: ashishMSFT
ms.date: 12/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: ca0d31e403275d6131fa6d53f0a7b46a7ddb651d
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832130"
---
# <a name="set-up-operational-insights"></a>Konfigurer Operational Insights

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer og bruker funksjonen Operational Insights i Microsoft Dynamics 365 Commerce.

Operational Insights er en Dynamics 365 Commerce-funksjon som er utformet for å gi kundene bedre oversikt i servicetilstanden og forretningsfunksjonaliteten ved å sende telemetri direkte til en kundeeid Application Insights-konto.

Ved å aktivere Operational Insights for miljøene i Commerce headquarters kan du samle inn en utvalgt liste over hendelser fra både Commerce Scale Unit (CSU) og salgsstedsenhetene. Disse hendelsene kan hjelpe deg med å forstå bedre hvordan systemene fungerer, og de gir deg overvåking av viktige tekniske tall og forretningsmåledata.

Selv om du ikke vil samle inn denne telemetrien hele tiden, kan du dra nytte av å aktivere eller deaktivere innsamling raskt for bestemte miljøer. På denne måten kan telemetrien hjelpe deg med å feilsøke eller rette under utvikling eller i produksjon.

## <a name="access-logs-in-application-insights"></a>Få tilgang til logger i Application Insights

Hvis du vil ha tilgang til loggene for Commerce CSU- og salgsstedskomponenter via Application Insights, kan du fullføre prosedyrene i denne delen.

### <a name="minimum-version-requirements-for-csu"></a>Minimumsversjonskrav til CSU

CSU har følgende krav til minimumsversjon:

- 10.0.23 (Retail Server, versjon 9.33.22062.15 og nyere)
- 10.0.24 (Retail Server, versjon 9.34.22062.14 og nyere)
- 10.0.25 (Retail Server, versjon 9.35.22062.13 og nyere)
- 10.0.26 og nyere (alle versjoner)

### <a name="enable-diagnostic-events-in-application-insights"></a>Aktiver diagnosehendelser i Application Insights

> [!IMPORTANT]
> Hvis du tidligere har brukt en forhåndsversjon av Operational Insights, må du bruke fremgangsmåten nedenfor for å aktivere Operational Insights. På denne måten sikrer du at pålitelig og sikker tilgang til hendelser kan fortsette.

Hvis du vil aktivere diagnosehendelser for Commerce-komponenter, må du ha en Application Insights-konto. Du kan bruke en eksisterende konto eller [opprette en ny konto](/azure/azure-monitor/app/create-workspace-resource#create-workspace-based-resource). Av hensyn til personvern anbefaler vi at du bruker separate Application Insights-kontoer for produksjons-, sandkasse- og utviklingsmiljøer. Når du har opprettet en konto, må du aktivere funksjonen **Operational Insights** i headquarters.

Følg denne fremgangsmåten for å aktivere diagnosehendelser i Application Insights.

1. I headquarters åpner du **Funksjonsbehandling**-arbeidsområdet og aktiverer funksjonen **Operational Insights**.
1. Gå til **Systemadministrasjon \> Oppsett \> Operational Insights**.
1. Sett alternativet **Commerce-kanalhendelser** til **Ja** i fanen **Konfigurer**.
1. Angi verdier for **LCS-miljø-ID** og **miljømodus** for hvert miljø der du planlegger å bruke Application Insights, i fanen **Miljøer**. Du finner miljø-ID-en for hvert miljø på siden **Miljødetaljer** for dette miljøet i Microsoft Dynamics Lifecycle Services. Dette trinnet er nødvendig for å forhindre at diagnosehendelser sendes til feil miljø ved en feiltakelse når operasjoner for databasekopiering utføres.
1. På fanen **Application Insights-register** angir du verdien for Application Insights-**instrumenteringsnøkkelen** og tilsvarende **Miljømodus**-verdi for miljøene der du planlegger å bruke hver Application Insights-konto.
1. Når du har fullført den forrige konfigurasjonen, må du kjøre **CDX-jobb 1110**-jobben. Du kan vente til denne jobben kjøres på egen plan, eller du kan kjøre den manuelt.
1. I Lifecycle Services går du til **Miljødetaljer \> Commerce \> Administrer**, velger en CSU-forekomst og velger deretter **Start på nytt**. Gjenta dette trinnet for hvert CSU.
1. Gjenta de forrige trinnene for hvert miljø der du har tenkt å bruke Application Insights.

> [!NOTE]
> - Telemetrihendelsene i Operational Insights kan endres. Vi anbefaler at du bruker Operational Insights-hendelser til å utføre foreløpig analyse og feilsøking på egen hånd, og ikke til å definere instrumentbord eller varsler. Hvis du bruker hendelser til formål utover selvbetjeningssøk, anbefaler vi at du validerer og oppdaterer spørringene etter hver CSU/POS-utgivelse.
> - Fra og med Commerce, versjon 10.0.29 aktiverer fremgangsmåtene i denne delen også strømming for salgsstedhendelser for Operational Insights i Application Insights-kontoen. Hvis du vil ha mer informasjon, kan du se [Operational Insights for salgssted – hendelser og spørringer](https://download.microsoft.com/download/9/2/b/92be35b0-0e24-4a4d-940d-6f4db29791c0/Operational-Insights-Commerce-POS-events-queries.pdf).

#### <a name="use-the-dllhostexeconfig-file-to-control-pos-operational-insights-events"></a>Bruk DLLHost.exe.config-filen til å kontrollere salgstedshendelser for Operational Insights

For å bruke DLLHost.exe.config-filen til å kontrollere salgstedshendelser for Operational Insights følger du denne fremgangsmåten.

1. I et tekstredigeringsprogram åpner du **EXEHost.exe.config**-filen på **C:\\Programfiler (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker**.
1. I **diagnosticsSection**-delen fjerner du synke-XML-elementet som har klassenavnet **Microsoft.Dynamics.Retail.Diagnostics.OperationalInsightsLogger**.
1. Lagre filen.

### <a name="disable-diagnostic-events-in-application-insights"></a>Deaktiver diagnosehendelser i Application Insights

> [!IMPORTANT]
> Hvis du vil deaktivere diagnosehendelser og ikke lenger sende dem til Application Insights, må du fullføre fremgangsmåten nedenfor. Du kan ikke bare deaktivere funksjonen Funksjonsbehandling.

Følg denne fremgangsmåten for å deaktivere diagnosehendelser i Application Insights.

1. Gå til **Systemadministrasjon \> Operational Insights** i headquarters.
1. Sett alternativet **Commerce-kanalhendelser** til **Nei** i fanen **Konfigurer**.
1. Når du har fullført den forrige konfigurasjonen, må du kjøre **CDX-jobb 1110**-jobben. Du kan vente til denne jobben kjøres på egen plan, eller du kan kjøre jobben manuelt.
1. I Lifecycle Services går du til **Miljødetaljer \> Commerce \> Administrer**, velger en CSU-forekomst og velger deretter **Start på nytt**. Gjenta dette trinnet for hvert CSU.
1. Gjenta de forrige trinnene for hvert miljø der du har tenkt å slå av Application Insights.

Hvis du vil deaktivere diagnosehendelser for et enkelt miljø, sletter du instrumenteringsnøkkelen på fanen **Application Insights-register** på siden **Operational Insights**. Deretter fullfører du trinn 3 og 4 i fremgangsmåten over.

> [!NOTE]
> I Commerce, versjon 10.0.29 og nyere deaktiverer fremgangsmåtene i denne delen også strømming for salgsstedhendelser for Operational Insights i Application Insights-kontoen. 
