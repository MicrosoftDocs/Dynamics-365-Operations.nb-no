---
title: Opprette nye brukere
description: Brukere er interne ansatte i din organisasjon, eller eksterne kunder og leverandører, som trenger tilgang til systemet for å utføre jobbene sine.
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 480d181e8abb3af5a7406efd13c8bd9961a7490a
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595392"
---
# <a name="create-new-users"></a>Opprette nye brukere

[!include [banner](../../includes/banner.md)]

Før du får tilgang til Finance and Operations-apper, må du først legges til på **Bruker**-siden (**Systemadministrasjon \> Brukere \> Brukere**). Brukere omfatter interne ansatte i organisasjonen eller eksterne kunder og leverandører. Brukere kan importeres eller legges til manuelt. Alle brukere må lisensieres riktig for bruk i samsvar med forskriftene.

Hvis du vil ha informasjon om hvordan du kjøper og lisensierer for Finance and Operations-apper, kan du se [lisensieringsveiledningen for Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).

## <a name="assign-a-license-to-a-user"></a>Tilordne en lisens til en bruker
Systemadministratorer kan [tilordne lisenser til brukere](/office365/admin/subscriptions-and-billing/assign-licenses-to-users) i [administrasjonssenteret for Microsoft 365](/office365/admin/admin-overview/about-the-admin-center).

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a>Legge til en ekstern bruker i Azure AD og tilordne en lisens 
Eksterne brukere må være representert i leierkatalogen (Azure Active Directory (Azure AD)), slik at de kan tilordnes lisenser. Disse eksterne brukerne må legges til for leieren i Azure AD som gjestebrukere og deretter tilordnes de aktuelle lisensene. Et krav for Finance and Operations-apper er at gjestebrukerens firma må bruke Azure AD. Hvis du vil ha mer informasjon, kan du se [Legge til Azure Active Directory B2B-samarbeidsbrukere i Azure-portalen](/azure/active-directory/b2b/add-users-administrator).

## <a name="import-new-users-from-azure-ad"></a>Importere nye brukere fra Azure AD 
1. Gå til **Systemadministrasjon** \> **Brukere** \> **Brukere**.
2. Velg **Importer brukere** i handlingsruten.
3. Velg brukerne som skal importeres. Listen omfatter Azure AD-brukere som for øyeblikket ikke er brukere i dette miljøet.
4. Velg **Importer brukere**.
5. Velg **Lukk**.

> [!NOTE]
> Verdien i **Firma**-feltet angis basert på firmaet i gjeldende økt for administratoren. Etter importen må du tilordne aktuelle roller og organisasjoner. Hvis du vil ha mer informasjon, kan du se [Tilordne brukere til sikkerhetsroller](assign-users-security-roles.md). Det kan også bli nødvendig å knytte brukeren til en **Person** og oppdatere brukeralternativer, for eksempel språk.

## <a name="manually-add-a-new-user"></a>Legge til en ny bruker manuelt
1. Gå til **Systemadministrasjon** \> **Brukere** \> **Brukere**.
2. Velg **Ny** i handlingsruten.
3. I **Bruker-ID**-feltet angir du en unik ID for brukeren.   
4. Angi navnet på brukeren i **Brukernavn**-feltet.  
5. I **Leverandør**-feltet:
 - Bruk standardverdien for interne brukere. Eksempel: Azure AD-leieren med prefikset https://sts.windows.net/.  
 - Når det gjelder brukere uten Azure AD, for eksempel tjeneste-til-tjeneste-kontoer, angir du en enkel tekstverdi. Eksempel: NA. Denne verdien bidrar til å unngå uriktige autentiseringsoppkall som kan føre til feil hvis det brukes en gyldig verdi for identitetsleverandør.  
 - Når det gjelder eksterne brukere eller gjestebrukere, legger du til Azure AD-leiernavnet etter https://sts.windows.net/.
6. I **E-post**-feltet angir du brukerens fulle e-postadresse / hovednavn for bruker.  
7. Velg standard oppstartsfirma for brukeren i **Firma**-feltet. 
8. Velg **Lagre**.

Verdiene for Identitetsleverandør og Telemetri-ID blir oppdatert basert på et [Microsoft Graph](/graph/overview)-kall når brukerposten lagres. Telemetri-ID-en er basert på brukerens objekt-ID / sikkerhetsidentifikator (SID) i Azure AD.

> [!NOTE]
> Når du har lagt til en bruker, må du tilordne aktuelle roller og organisasjoner. Hvis du vil ha mer informasjon, kan du se [Tilordne brukere til sikkerhetsroller](assign-users-security-roles.md). Det kan også bli nødvendig å knytte brukeren til en **Person** og oppdatere **Brukeralternativer**, for eksempel språk.

## <a name="change-a-user-id"></a>Endre en bruker-ID
Hvis du vil endre en bruker-ID, må du gi nøkkelen nytt navn i databasen. Når du endrer en bruker-ID ved å bruke denne fremgangsmåten, endres alle relaterte brukerinnstillinger slik at den nye bruker-ID-en brukes. Bruksinformasjonen i tabellen **SysLastValue** blir for eksempel oppdatert for å henvise til den nye bruker-ID-en.

> [!NOTE]
> Bruker-ID-en er primærnøkkelen i tabellen for brukerinformasjon. Det kan ta litt tid å gi primærnøkkelen nytt navn for eksisterende brukere, fordi alle referanser til nøkkelen også oppdateres i databasen. 

1. Gå til **Systemadministrasjon \> Brukere \> Brukere**.
2. Velg en bruker i listen, og velg **Alternativer \> Postinformasjon**.
3. Velg **Gi nytt navn**.
4. Angi en ny og unik verdi for bruker-ID-en, og deretter **OK**. 
5. Klikk på **Ja** for å bekrefte.

## <a name="additional-resources"></a>Tilleggsressurser

Hvis du vil ha flere alternativer for å implementere B2B-brukere, kan du se [Eksportere B2B-brukere til Azure AD](../implement-b2b.md).

Hvis du vil ha informasjon om forhåndskonfigurerte systemkontoer, kan du se [Forhåndskonfigurerte systemkontoer](../pre-configured-system-accounts.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]