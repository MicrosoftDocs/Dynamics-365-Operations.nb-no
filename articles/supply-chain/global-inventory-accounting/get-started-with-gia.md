---
title: Komme i gang med Globalt lagerregnskap
description: Denne artikkelen beskriver hvordan du kommer i gang med Globalt lagerregnskap.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 463a66002ec7a6536c9ff829f9ea2c3734138eae
ms.sourcegitcommit: 6221a25f81aa83ab335de7cb6b6c3014dbec0116
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/19/2022
ms.locfileid: "9177156"
---
# <a name="get-started-with-global-inventory-accounting"></a>Komme i gang med Globalt lagerregnskap

[!include [banner](../includes/banner.md)]

Ved hjelp av Globalt lagerregnskap kan du utføre flere lagerregnskap i Globalt lagerregnskap-finanskontoer du har definert. Du må knytte hver finanskonto for Globalt lagerregnskap til en *konvensjon*. En konvensjon er en samling av følgende typer regnskapspolicyer:

- Kostnadsobjekt
- Målingsgrunnlag for inndata
- Kostnadsflytforutsetning
- Kostnadselement

> [!NOTE]
> Selv etter at du har aktivert Globalt lagerregnska, kan du fremdeles utføre lagerregnskap i Microsoft Dynamics 365 Supply Chain Management, som vanlig.

Globalt lagerregnskap er et tillegg. Hvis du vil gjøre funksjonene tilgjengelige, må du installere det fra Microsoft Dynamics Lifecycle Services (LCS). Du kan velge å evaluere det i et testmiljø før du aktiverer det for produksjonsmiljøer.

Globalt lagerregnskap støtter for øyeblikket ikke alle kostnadsstyringsfunksjonene som er innebygd i Supply Chain Management. Det er derfor viktig at du vurderer om funksjonssettet som for øyeblikket er tilgjengelig, oppfyller kravene dine.

## <a name="how-to-get-the-global-inventory-accounting-add-in"></a><a name="sign-up"></a>Slik får du tilleggsprogrammet Globalt lagerregnskap

> [!IMPORTANT]
> Hvis du vil bruke Globalt lagerregnskap, må du ha et LCS-aktivert miljø med høy tilgjengelighet (ikke et OneBox-miljø). I tillegg må du kjøre Supply Chain Management versjon 10.0.19 eller senere.

### <a name="supply-chain-management-version-10019-to-10026"></a>Supply Chain Management-versjon 10.0.19 til 10.0.26

Hvis du vil installere Globalt lagerregnskap for Supply Chain Management-versjon 10.0.19 til 10.0.26, starter du ved å [installere tilleggsprogrammet](#install). Send deretter ID-en for LCS-miljøet og firmanavnet via e-post til [Globalt lagerregnskap-teamet](mailto:GlobalInvAccount@microsoft.com). Teamet sender deg en oppfølgings-e-post som inneholder Globalt lagerregnskap-tjenesteendepunktene.

### <a name="supply-chain-management-version-10027-and-later"></a>Supply Chain Management versjon 10.0.27 og nyere

Hvis du vil installere Globalt lagerregnskap for Supply Chain Management-versjon 10.0.27 og nyere, trenger du bare å [installere tilleggsprogrammet](#install). Når det gjelder disse versjonene av Supply Chain Management, konfigureres Globalt lagerregnskap-tjenesteendepunktene automatisk, slik at du ikke trenger å finne dem manuelt. Hvis du får problemer mens du konfigurerer tillegget, bør du ta kontakt med [Globalt lagerregnskap-teamet](mailto:GlobalInvAccount@microsoft.com).

## <a name="licensing"></a>Lisensiering

Globalt lagerregnskap lisensieres sammen med standardfunksjonene for lagerregnskap som er tilgjengelig for Supply Chain Management. Du trenger ikke kjøpe en tilleggslisens for å bruke Globalt lagerregnskap.

## <a name="prerequisites"></a>Forutsetninger

### <a name="set-up-microsoft-power-platform-integration"></a>Konfigurer Microsoft Power Platform-integrering

Før du kan aktivere tilleggfunksjonalitet, må du integrere med Microsoft Power Platform ved å følge disse trinnene.

1. Åpne LCS-miljøet der du vil legge til tjenesten.
1. Gå til **Detaljerte opplysninger**.
1. Velg **Oppsett**-knappen i delen **Power Platform-integrering**.
1. Merk av for avmerkingsboksen i dialogboksen for **Oppsett av Power Platform-miljø**, og velg deretter **Oppsett**. Vanligvis tar oppsettet mellom 60 og 90 minutter.
1. Når oppsettet av Microsoft Power Platform-miljøet er fullført, viser siden navnet på miljøet. I tillegg viser delen **Power Platform-integrering** setningen "Power Platform-miljøoppsettet er fullført." Globalt lagerregnskap krever ikke et program med dobbel skriving.

Hvis du vil ha mer informasjon, kan du se [Konfigurere etter miljødistribusjon](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="install-or-update-the-add-in-and-solution"></a><a name="install"></a>Installer eller oppdater tillegget og løsningen

Bruk fremgangsmåten nedenfor til å installere eller oppdatere tillegget og løsningen for globalt lagerregnskap. Delen av fremgangsmåten du bør følge, avhenger av om du installerer for første gang, eller bare trenger å oppdatere løsningen for en eksisterende installasjon.

- Hvis du aldri har installert tilleggsprogrammet før, følger du fremgangsmåten nedenfor for å installere både tilleggsprogrammet og løsningen.
- Hvis du allerede bruker globalt lagerregnskap, men må oppdatere løsningen i [Power Platform-administrasjonssenteret](https://admin.powerplatform.microsoft.com), utfører du bare trinn 6 og hopper over alle de andre trinnene.

Slik installerer eller oppdaterer du tilleggsprogrammet og løsningen:

1. Logg på [LCS](https://lcs.dynamics.com/Logon/Index).
1. Åpne LCS-miljøet der du vil legge til tjenesten.
1. Gå til **Detaljerte opplysninger**.
1. Gå til **Power Platform-integrering**, og velg **Oppsett**.
1. Merk av for avmerkingsboksen i dialogboksen for **Oppsett av Power Platform-miljø**, og velg deretter **Oppsett**. Vanligvis tar oppsettet mellom 60 og 90 minutter.
1. Når konfigurasjonen av Microsoft Power Platform-miljøet er fullført, kan du logge deg på [administrasjonssenteret for Power Platform](https://admin.powerplatform.microsoft.com) og deretter installere eller oppdatere løsningen for globalt lagerregnskap ved å gjøre følgende:
   1. Velg miljøet der du vil installere eller oppdatere løsningen.
   1. Velg **Dynamics 365-apper**.
   1. Velg **Installer app**.
   1. Velg **Dynamics 365 Global Inventory Accounting**.
   1. Velg **Neste** for å installere.
1. Når løsningen er fullstendig installert, kan du gå tilbake til LCS-miljøet. I hurtigfanen **Miljøtillegg** velger du **Installer et nytt tillegg**.
1. Velg **Globalt lagerregnskap**.
1. Følg installasjonsveiledningen, og godta vilkårene.
1. Velg **Installer**.
1. I hurtigfanen **Miljøtillegg** skal du se at Globalt lagerrenskap blir installert. Etter noen minutter skal statusen endres fra *Installerer* til *Installert*. (Det kan hende du må oppdatere siden for å se denne endringen.) På dette tidspunktet er Globalt lagerregnskap klar til bruk.

Hvis standardspråket for Dataverse-installasjonen ikke er engelsk, følger du denne fremgangsmåten:

1. Gå til **Avanserte innstillinger \> Administrasjon \> Språk**.
1. Velg *Engelsk* (*LanguageCode=1033*), og velg deretter **Bruk**.

## <a name="set-up-the-integration"></a>Defininere integreringen

Følg denne fremgangsmåten for å sette opp integreringen mellom Globalt lagerregnskap og Supply Chain Management.

1. Logg på Supply Chain Management.
1. Gå til **Systemadministrasjon \> Funksjonsbehandling**.
1. Velg **Se etter oppdateringer**.
1. I **Alle**-fanen søker du etter funksjonen som kalles *(Forhåndsversjon) Globalt lagerregnskap*.
1. Velg **Aktiver nå**.
1. Gå til **Globalt lagerregnskap \> Oppsett \> Parametere for Globalt lagerregnskap \> Integreringsparametere**.
1. Gjør ett av følgende, avhengig av hvilken versjon av Supply Chain Management du kjører:
    - **Supply Chain Management-versjon 10.0.19 til 10.0.26**: I feltene **Datatjenesteendepunkt** og **Endepunkt for Globalt lagerregnskap** angir du URL-adressene som ble sendt til deg via e-post fra Globalt lagerregnskap-teamet (se også [Slik får du tilleggsprogrammet Globalt lagerregnskap](#sign-up)).
    - **Supply Chain Management-versjon 10.0.27 og nyere**: Du trenger ikke å angi endepunktene, så du kan hoppe over dette trinnet.

Globalt lagerregnskap er nå klart til bruk.
