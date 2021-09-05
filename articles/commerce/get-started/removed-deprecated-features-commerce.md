---
title: Funksjoner som er fjernet eller avskrevet i Dynamics 365 Commerce
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Commerce.
author: josaw
ms.date: 08/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 3ac08a409284681ba9bcc4825b936c0330d14e04
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386747"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Funksjoner som er fjernet eller avskrevet i Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Commerce.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging. 

> [!NOTE]
> Detaljert informasjon om objekter i Finance and Operations-apper finnes i [Tekniske referanserapporter](/dynamics/s-e/). Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av Finance and Operations-apper.

## <a name="features-removed-or-deprecated-in-the-commerce-10021-release"></a>Fjernede eller avskrevne funksjoner i Commerce 10.0.21

[!include [banner](../includes/preview-banner.md)]

### <a name="retail-sdk-distributed-by-using-lifecycle-services"></a>SDK for Retail distribuert ved hjelp av Lifecycle Services

SDK for Retail sendes i Lifecycle Services (LCS). Denne distribusjonsmodusen avskrives i versjon 10.0.21. Fremover vil referansepakker, biblioteker og eksempler i SDK for Retail bli publisert i offentlige repositorier på GitHub.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | SDK for Retail leveres i LCS. LCS-prosessen tar et par timer å fullføre, og prosessen må gjentas for hver oppdatering. Fremover vil referansepakker, biblioteker og eksempler i SDK for Retail bli publisert i offentlige repositorier på GitHub. Utvidelseseksempler og referansepakker kan enkelt brukes, og oppdateringene fullføres på et par minutter. |
| **Erstattet med en annen funksjon?**   |  [Last ned eksempler og referansepakker i SDK for Retail fra GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md) |
| **Berørte produktområder**         | Retail SDK |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Per versjon 10.0.21 fjernes SDK-en som sendes via virtuelle LCS-maskiner, i oktober 2022. |

### <a name="retail-deployable-package-and-combined-pos-hardware-station-and-cloud-scale-unit-installers"></a>Pakker som kan distribueres i Retail, og kombinerte installasjoner på salgssted, i maskinvarestasjoner og skyskalaenheter

Pakker som kan distribueres i Retail, generert ved hjelp av Retail SDK MSBuild, blir avskrevet i 10.0.21. Fremover kan du bruke CSU-pakken (Cloud Scale Unit) for skyskalaenhetstillegg (Commerce Runtime, kanaldatabase, hodeløse Commerce API-er, betalinger og salgssted i skyen(POS)). Bruk installasjonsprogrammer kun for bare utvidelse for POS, maskinvarestasjon og skyskalaenhet, selvbetjent.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | En distribuerbar Retail-pakke er en kombinert pakke som inneholder et fullstendig sett med utvidelsespakker og installeringer. Denne kombinerte pakken gjør distribusjonen kompleks, fordi CSU-tillegg går til skyskalaenheten, og installeringer distribueres i butikker. Installasjonsprogrammene inkluderer utvidelsen og basisproduktet, som gjør oppdateringene vanskelige. For hver oppgradering kreves det en kodefletting og pakkegenerering. For å forenkle denne prosessen er utvidelsespakkene nå delt inn i komponenter for enkel distribusjon og behandling. Med den nye fremgangsmåten skilles det mellom tillegg og installering av basisprodukt, og de kan vedlikeholdes og oppgraderes uavhengig uten at koden flettes eller pakkes om.|
| **Erstattet med en annen funksjon?**   | CSU-tillegg, installering av POS-utvidelse, installering av maskinvaretillegg |
| **Berørte produktområder**         | Dynamics 365 Commerce – utvidelse og distribusjon |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Per versjon 10.0.21 vil støtte for distribusjon av RetailDeployablePackage i LCS fjernes i oktober 2022. |

Hvis du vil ha mer informasjon, kan du se:

+ [Generer en separat pakke for Commerce Cloud Scale Unit (CSU)](../dev-itpro/retail-sdk/retail-sdk-packaging.md#generate-a-separate-package-for-commerce-cloud-scale-unit-csu)
+ [Opprett en Modern POS-utvidelsespakke](../dev-itpro/pos-extension/mpos-extension-packaging.md)
+ [Integrer salgsstedet med en ny maskinvareenhet](../dev-itpro/hardware-device-extension.md)
+ Kodeeksempler
    + [Cloud Scale Unit](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit)
    + [Salgssted, CSU og maskinvarestasjon](https://github.com/microsoft/Dynamics365Commerce.InStore)

### <a name="modernpossln-and-cloudpossln-in-the-retail-sdk"></a>ModernPos.Sln og CloudPOs.sln i Retail SDK

Utvikling av POS-utvidelser ved hjelp av ModernPos.sln, CloudPOs.sln, POS.Extension.csproj og POS-mappen er avskrevet i versjon 10.0.21. Fremover kan du bruke POS-uavhengig emballasje-SDK for POS-tillegg.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Hvis det finnes POS-tillegg i tidligere versjoner av Retail SDK, kreves det en kodefletting og ompakking til den nyeste versjonen av POS. Kodeflettingen var en tidkrevende oppgraderingsprosess, og du måtte vedlikeholde hele Retail SDK i repositoriet. Du måtte også kompilere POS.App-kjerneprosjekt. Hvis du bruker den uavhengige emballasjemodellen, må du bare vedlikeholde filtypen. Prosessen med å oppdatere til den siste versjonen av POS-tilleggene er så enkel som å oppdatere versjonen av pakken NuGet som prosjektet forbruker. Utvidelser kan distribueres uavhengig, og tjenester bruker installeringsnummeret for utvidelsen. Basissalgsstedet kan distribueres og vedlikeholdes separat, og det kreves ingen kodefletting eller ompakking med basisinstallasjonsprogrammet eller -koden. |
| **Erstattet med en annen funksjon?**   | [Salgsstedsuavhengig emballasje-SDK](../dev-itpro/pos-extension/pos-extension-getting-started.md) |
| **Berørte produktområder**         | Dynamics 365 Commerce – utvidelse og distribusjon for salgssted |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Per versjon 10.0.21 blir støtte for kombinerte POS-pakker og utvidelsesmodellen som bruker ModernPos.Sln, CloudPOs.sln og POS.Extensons.csproj in Retail SDK, fjernet i oktober 2022. |

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Fjernede eller avskrevne funksjoner i Commerce 10.0.17

### <a name="full-dataset-generation-interval-is-deprecated"></a>Fullstendig datasettgenereringsintervall blir avskrevet

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Fra og med denne versjonen, i skjemaet **Parametre for planlegging av handel** i Dynamics 365-hovedkontoret, blir feltet **Fullstendig datasettgenereringsintervall i dager** avskrevet. Hvis du også starter i denne versjonen, fjernes feltet visuelt, slik at verdien ikke kan redigeres. Dette blir stående som verdien **0**. |
| **Erstattet med en annen funksjon?**   | Nr. |
| **Berørte produktområder**         | Dynamics 365 Commerce |
| **Distribusjonsalternativ**              | Alle|
| **Status**                         | Avskrevet. Ikke bruk dette feltet eller endre verdien i det.|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Fjernede eller avskrevne funksjoner i Commerce 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-støtte for Dynamics 365 er avskrevet

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Fra og med desember 2020 er Microsoft Internet Explorer 11-støtte for alle Dynamics 365-produkter avskrevet, og Internet Explorer 11 støttes ikke etter august 2021.<br><br>Dette vil påvirke kunder som bruker Dynamics 365-produkter som er utformet for bruk via et Internet Explorer 11-grensesnitt. Etter august 2021 støttes ikke Internet Explorer 11 for slike Dynamics 365-produkter. |
| **Erstattet med en annen funksjon?**   | Vi anbefaler at kundene går over til Microsoft Edge.|
| **Berørte produktområder**         | Alle Dynamics 365-produkter |
| **Distribusjonsalternativ**              | Alle|
| **Status**                         | Avskrevet. Internet Explorer 11 støttes ikke etter august 2021.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Fjernede eller avskrevne funksjoner i Commerce 10.0.11
### <a name="data-action-hooks"></a>Datahandlingsbindinger
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Funksjonen for datahandlingsbindinger er avskrevet på grunn av ytelsesproblemer. |
| **Erstattet med en annen funksjon?**   | Vi anbefaler i stedet å bruke [overstyringer for datahandling](../e-commerce-extensibility/data-action-overrides.md) til å endre forretningslogikken i datahandlingslaget.|
| **Berørte produktområder**         | Datahandlinger for utvidelsesmuligheter for e-handel |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Fra og med versjon 10.0.11 |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Støtte for SDK for Retail for Visual Studio 2015, msbuild 14.0 og SDK for Retail\referansebibliotek og verktøy
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Støtte for SDK for Retail for Visual Studio 2015 er avskrevet og oppdatert til å støtte VS 2017, msbuild 15.0 og alle referansebibliotekene og Commerce-proxy-generatorverktøy i RetailSDK\referanse-mappen flyttet til NuGet-pakker for å forenkle utvidelsesmodellen og SDK-oppgraderingsprosessen.|
| **Erstattet med en annen funksjon?**   | Vi anbefaler at du følger informasjonen i [Overføre SDK for Retail fra Visual Studio 2015 til Visual Studio 2017](../dev-itpro/retail-sdk/migrate-sdk.md) for å oppdatere systemet. |
| **Berørte produktområder**         | SDK for Retail-utvidelser |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Fra og med versjon 10.0.11 |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>Retail Server-utvidelse ved hjelp av IEdmModelExtender og CommerceController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Retail Server-utvidelse ved hjelp av IEdmModelExtender og CommerceController er avskrevet til å gi forenklet utvidelsesmodell. Den nye implementeringen vil bare ha controller-klassen uten ekstra IEdmModelExtender-klasseimplementering. Dette unngår også avhengigheten med en bestemt OData-versjon (hvis OData-versjonen er oppdatert, kan det hende at utvidelser brytes.) |
| **Erstattet med en annen funksjon?**   |  Vi anbefaler at du bruker IController-klasseutvidelsesmodellen ved å importere NuGet-pakken (Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **Berørte produktområder**         | Retail Server-utvidelser |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Fra og med versjon 10.0.11 |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Utvidelse for maskinvarestasjon ved hjelp av IHardwareStationController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Maskinvarestasjonsutvidelse ved hjelp av IHardwareStationController er avskrevet til fordel for forenklet utvidelsesmodell. Den nye implementeringen vil bare ha IController-klassen uten ekstra klasseimplementering og for å unngå avhengigheten med biblioteker med kjernemaskinvarestasjoner, tidligere utvidelse må referere til flere biblioteker.) |
| **Erstattet med en annen funksjon?**   | Det anbefales å bruke IController-klasseutvidelsesmodellen ved å importere NuGet-pakken (Microsoft.Dynamics.Commerce.Hosting.Contracts). |
| **Berørte produktområder**         | Utvidelsesmuligheter for maskinvarestasjon |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Fra og med versjon 10.0.11 |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Fjernede eller avskrevne funksjoner i Commerce 10.0.10
### <a name="pos-operation-803---picking-and-receiving"></a>POS-operasjon 803 - Plukk og mottak
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Plukk- og mottaksoperasjoner avskrives på grunn av ny utforming av den nye operasjonen. |
| **Erstattet med en annen funksjon?**   | Ja. Den er erstattet av to nye POS-operasjoner: innkommende operasjon (804) og utgående operasjon (805).|
| **Berørte produktområder**         | Salgsstedsapplikasjon |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Etter utgivelse 10.0.10 vil ikke plukk- og mottaksoperasjonen lenger motta nye funksjonsoppdateringer. Bare kritiske feilrettinger vil bli utført for denne operasjonen i fremtidige versjoner. Alle kunder oppfordres til å flytte til nye [innkommende operasjoner](../pos-inbound-inventory-operation.md) og [utgående operasjoner](../pos-outbound-inventory-operation.md), som vil fortsette å være en del av vårt langsiktig produktveikart. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Fjernede eller avskrevne funksjoner i Commerce 10.0.7
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>API-er for Commerce GetProductAvailabilities og GetAvailableInventoryNearby
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Nye optimaliserte API-er er opprettet for å erstatte API-ene GetProductAvailabilities og GetAvailableInventoryNearby. |
| **Erstattet med en annen funksjon?**   | Ja: Den erstattes av APIene GetEstimatedAvailability og GetEstimatedProductWarehouseAvailability. |
| **Berørte produktområder**         | SDK for e-handelsprogram |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Avskrevet: Etter versjon 10.0.7 vil det ikke lenger gjøres tekniske investeringer for GetProductAvailabilities og GetAvailableInventoryNearby. Organisasjoner som bruker disse APIene i sine e-handelsdistribusjoner, bør konvertere dem til de nye GetEstimatedAvailability og GetEstimatedProductWarehouseAvailability-APIene og aktivere [funksjonen for beregning av optimalisert produkttilgjengelighet](../calculated-inventory-retail-channels.md).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere kunngjøringer om fjernede eller avskrevne funksjoner
Hvis du vil lære mer om funksjoner som er fjernet eller avskrevet i tidligere versjoner, kan du se [Fjernede eller avskrevne funksjoner i tidligere versjoner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
