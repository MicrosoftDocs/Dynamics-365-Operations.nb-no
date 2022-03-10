---
title: Komme i gang med Globalt lagerregnskap
description: Dette emnet beskriver hvordan du kommer i gang med Globalt lagerregnskap.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f5b3c013996253de75cd85c4bcfc52ed159e8f9d
ms.sourcegitcommit: 8c17717b800c2649af573851ab640368af299981
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/23/2021
ms.locfileid: "7860515"
---
# <a name="get-started-with-global-inventory-accounting"></a>Komme i gang med Globalt lagerregnskap

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Ved hjelp av Globalt lagerregnskap kan du utføre flere lagerregnskap i Globalt lagerregnskap-finanskontoer du har definert. Du må knytte hver finanskonto for Globalt lagerregnskap til en *konvensjon*. En konvensjon er en samling av følgende typer regnskapspolicyer:

- Kostnadsobjekt
- Målingsgrunnlag for inndata
- Kostnadsflytforutsetning
- Kostnadselement

> [!NOTE]
> Selv etter at du har aktivert Globalt lagerregnska, kan du fremdeles utføre lagerregnskap i Microsoft Dynamics 365 Supply Chain Management, som vanlig.

Globalt lagerregnskap er et tillegg. Hvis du vil gjøre funksjonene tilgjengelige, må du installere det fra Microsoft Dynamics Lifecycle Services (LCS). Du kan velge å evaluere det i et testmiljø før du aktiverer det for produksjonsmiljøer.

Globalt lagerregnskap støtter for øyeblikket ikke alle kostnadsstyringsfunksjonene som er innebygd i Supply Chain Management. Det er derfor viktig at du vurderer om funksjonssettet som for øyeblikket er tilgjengelig, oppfyller kravene dine.

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a>Slik får du offentlig forhåndsversjon av Globalt lagerregnskap

> [!IMPORTANT]
> Hvis du vil bruke Globalt lagerregnskap, må du ha et LCS-aktivert miljø med høy tilgjengelighet (ikke et OneBox-miljø). I tillegg må du kjøre Supply Chain Management versjon 10.0.19 eller senere.

Hvis du vil registrere deg for offentlig forhåndsversjon av Globalt lagerregnskap, kan du sende LCS-miljø-IDen med e-post til [Globalt lagerregnskap-teamet](mailto:GlobalInvAccount@microsoft.com). Når du er godkjent for programmet, sender teamet deg en oppfølgings-e-post som inneholder en betanøkkel for Globalt lagerregnskap og tjenesteendepunktene. Når du har mottatt betanøkkelen, kan du [installere tillegget](#install).

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

### <a name="set-up-dataverse"></a>Definer Dataverse

Før du definerer Dataverse, kan du legge til serviceprinsippene for Globalt lagerregnskap i leietakeren ved å følge disse trinnene.

1. Installer Azure AD-modul for Windows PowerShell v2 som beskrevet i [Installere Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).
1. Kjør følgende PowerShell-kommando.

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

Deretter oppretter du programbrukere for Globalt lagerregnskap i Dataverse ved å følge disse trinnene.

1. Åpne URL-adressen for Dataverse-miljøet.
1. Gå til **Avansert innstilling \> System \> Sikkerhet \> Brukere** og opporett en appbruker. Bruk **Vis**-feltet til å endre sidevisningen til *Programbrukere*.
1. Velg **Ny**.
1. Angi **Program-ID**-feltet til *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.
1. Velg **Tilordne rolle**, og velg deretter *Systemadministrator*. Hvis det finnes en rolle kalt *Common Data Service-bruker*, velger du den også.
1. Gjenta de forrige trinnene, men sett feltet **Program-ID** til *5f58fc56-0202-49a8-ac9e-0946b049718b*.

Hvis du vil ha mer informasjon, kan du se [Opprette en appbruker](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

Hvis standardspråket for Dataverse-installasjonen ikke er engelsk, følger du denne fremgangsmåten.

1. Gå til **Avanserte innstillinger \> Administrasjon \> Språk**.
1. Velg *Engelsk* (*LanguageCode=1033*), og velg deretter **Bruk**.

## <a name="install-the-add-in"></a><a name="install"></a>Installer tillegget

Følg denne fremgangsmåten for å installere tillegget, slik at du kan bruke Globalt lagerregnskap.

1. [Registrer deg](#sign-up) for offentlig forhåndsversjon av Globalt lagerregnskap.
1. Logg på [LCS](https://lcs.dynamics.com/Logon/Index).
1. Gå til **Administrasjon av forhåndsvisningsfunksjoner**.
1. Velg plusstegnet (**+**).
1. I **Kode** -feltet angir du betanøkkelen for tillegget for Globalt lagerregnskap. (Du skal ha mottatt betanøkkelen via e-post da du registrerte deg.)
1. Velg **Fjern blokkering**.
1. Åpne LCS-miljøet der du vil legge til tjenesten.
1. Gå til **Detaljerte opplysninger**.
1. Gå til **Power Platform-integreringen**, og velg **Oppsett**.
1. Merk av for avmerkingsboksen i dialogboksen for **Oppsett av Power Platform-miljø**, og velg deretter **Oppsett**. Vanligvis tar oppsettet mellom 60 og 90 minutter.
1. Når oppsettet av Microsoft Power Platform-miljøet er fullført, går du til hurtigfanen **Miljøtillegg** og velger **Installer et nytt tillegg**.
1. Velg **Globalt lagerregnskap**.
1. Følg installasjonsveiledningen, og godta vilkårene.
1. Velg **Installer**.
1. I hurtigfanen **Miljøtillegg** skal du se at Globalt lagerrenskap blir installert. Etter noen minutter skal statusen endres fra *Installerer* til *Installert*. (Det kan hende du må oppdatere siden for å se denne endringen.) På dette tidspunktet er Globalt lagerregnskap klar til bruk.

## <a name="set-up-the-integration"></a>Defininere integreringen

Følg denne fremgangsmåten for å sette opp integreringen mellom Globalt lagerregnskap og Supply Chain Management.

1. Logg på Supply Chain Management.
1. Gå til **Systemadministrasjon \> Funksjonsbehandling**.
1. Velg **Se etter oppdateringer**.
1. I kategorien **Alle** søker du etter funksjonen som kalles *Globalt lagerregnskap*.
1. Velg **Aktiver nå**.
1. Gå til **Globalt lagerregnskap \> Oppsett \> Parametere for Globalt lagerregnskap \> Integreringsparametere**.
1. I feltene **Datatjenesteendepunkt** og **Endepunkt for Globalt lagerregnskap** angir du URL-adressene fra e-postmeldingen som Globalt lagerregnskap-teamet sendte da du registrerte deg for forhåndsvisningen.

Globalt lagerregnskap er nå klart til bruk.
