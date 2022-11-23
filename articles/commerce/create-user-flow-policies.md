---
title: Opprette brukerflytpolicyer
description: Denne artikkelen beskriver hvordan du oppretter brukerflytpolicyer i Microsoft Azure-portalen.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 91b9d99dfd8c3d100ca197aa499ca86799bbffc8
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785306"
---
# <a name="create-user-flow-policies"></a>Opprette brukerflytpolicyer

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du oppretter brukerflytpolicyer i Microsoft Azure-portalen.

Brukerflyter er policyene som Azure Active Directory (Azure AD) B2C bruker for å gi sikker pålogging, registrering, redigering av profil og brukeopplevelser ved glemt passord. Dynamics 365 Commerce bruker disse flytene til å utføre policyhandlinger for å kommunisere med Azure AD B2C-leieren. Når en bruker samhandler med disse policyene, omdirigeres de til Azure AD B2C-leieren for å utføre handlingene.

Azure AD B2C gir tre enkle flyttyper for brukere:
- Registrering og pålogging
- Profilredigering
- Tilbakestill passord

Du kan velge å bruke standard brukerflyter i Azure AD, som vil vise en side som ligger på Azure AD B2C. Du kan også opprette en HTML-side for å kontrollere utseendet og funksjonaliteten til brukerflytopplevelsene. 

Hvis du vil tilpasse brukerpolicysidene med sider som er bygd i Dynamics 365 Commerce, kan du se [Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md). Hvis du vil ha mer informasjon, se [Tilpasse grensesnittet til brukeropplevelser i Azure Active Directory B2C](/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Opprette en brukerflytpolicy for registrering og pålogging

Følg fremgangsmåten nedenfor for å opprette en brukerflytpolicy for registrering og pålogging.

1. Velg **Brukerflyter (policyer)** i den venstre navigasjonsruten i Azure-portalen.
1. På siden **Azure AD B2C – brukerflyter (policyer)** velger du **Ny brukerflyt**.
1. Velg policyen **Registrering og pålogging**, og velg deretter den **anbefalte** versjonen.
1. Under **Navn** skriver du inn et policynavn. Dette navnet vil vises etterpå med et prefiks som portalen tilordner (for eksempel "B2C_1_").
1. Under **Identitetsleverandører** i delen **Lokale kontoer**-delen velger du **E-postregistrering**. E-postgodkjenning brukes i de vanligste scenariene for Commerce. Hvis du også bruker godkjenning av leverandør av sosiale identiteter, kan du også velge dem på dette tidspunktet.
1. Velg ønsket valg for firmaet under **Godkjenning med flere faktorer**. 
1. Under **Brukerattributter og krav** velger du alternativer for å samle attributter eller returkrav etter behov. Velg **Vis mer...** for å få hele listen over attributter og kravalternativer. Commerce krever følgende standard alternativer:

    | **Innhent attributt** | **Returkrav** |
    | ---------------------- | ----------------- |
    | E-postadresse          | E-postadresser   |
    | Gitt navn             | Gitt navn        |
    |                        | Identitetsleverandør |
    | Etternavn                | Etternavn           |
    |                        | Brukers objekt-ID  |

1. Velg **Opprett**.

Bildet nedenfor er et eksempel på brukerflyten for registrering for og pålogging på Azure AD B2C.

![Policyinnstillinger for registrering og pålogging.](./media/B2CImage_11.png)

   
### <a name="create-a-profile-editing-user-flow-policy"></a>Opprette en brukerflytpolicy for profilredigering

Følg denne fremgangsmåten for å opprette en brukerflytpolicy for profilredigering.

1. Velg **Brukerflyter (policyer)** i den venstre navigasjonsruten i Azure-portalen.
1. På siden **Azure AD B2C – brukerflyter (policyer)** velger du **Ny brukerflyt**.
1. Velg **Profilredigering**, og velg deretter den **anbefalte** versjonen.
1. Under **Navn** angir du brukerflyten for profilredigering. Dette navnet vil vises etterpå med et prefiks som portalen tilordner (for eksempel "B2C_1_").
1. Under **Identitetsleverandører** i delen **Lokale kontoer**-delen velger du **Logg på via e-post**.
1. Under **Brukerattributter** merker du av følgende avmerkingsbokser:
    
    | **Innhent attributt** | **Returkrav** |
    | ---------------------- | ----------------- |
    |                        | E-postadresser   |
    | Gitt navn             | Gitt navn        |
    |                        | Identitetsleverandør |
    | Etternavn                | Etternavn           |
    |                        | Brukers objekt-ID  |
    
1. Velg **Opprett**.

Det følgende bildet viser et eksempel på brukerflyten for Azure AD B2C-profilredigering.

![Eksempel på Azure AD B2C-profil som redigerer brukerflyt](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Opprette en brukerflytpolicy for tilbakestilling av passord

Følg denne fremgangsmåten for å opprette en brukerflytpolicy for tilbakestilling av passord.

1. Velg **Brukerflyter (policyer)** i den venstre navigasjonsruten i Azure-portalen.
1. På siden **Azure AD B2C – brukerflyter (policyer)** velger du **Ny brukerflyt**.
1. Velg **Tilbakestilling av passord**, og velg deretter den **anbefalte** versjonen.
1. Under **Navn** skriver du inn et navn på brukerflyten for tilbakestilling av passord.
1. Under **Identitetsleverandører** velger du **Tilbakestill passord ved hjelp av e-postadresse**.
1. Velg **Opprett**.
1. Under **Programkrav** merker du av følgende avmerkingsbokser:
    - **E-postadresser**
    - **Gitt navn**
    - **Etternavn**
    - **Brukers objekt-ID**
1. Velg **Opprett**.

Det følgende bildet viser hvor du kan angi at **passordet skal tilbakestilles ved å bruke e-postadresse** i brukerflyten for tilbakestilling av passord i Azure AD B2C.

![Angi Tilbakestill passord med e-postadresse i policy for tilbakestilling av passord](./media/B2CImage_13.png)

## <a name="next-steps"></a>Neste trinn

Hvis du vil fortsette prosessen med å konfigurere en B2C-leietaker i Commerce, går du videre til [Legg til leverandører av sosiale identiteter](add-social-identity-providers.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere en B2C-leier i Commerce](set-up-b2c-tenant.md)

[Opprette eller koble til en eksisterende Azure AD B2C-leier i Azure-portalen](create-link-aad-b2c-tenant.md)

[Opprette B2C-programmet](create-b2c-app.md)

[Legg til leverandører av sosiale identiteter (valgfritt)](add-social-identity-providers.md)

[Oppdater Commerce Headquarters med den nye Azure AD B2C-informasjonen](update-hq-aad-b2c-info.md)

[Konfigurere B2C-leieren i områdebygger for Commerce](config-b2c-tenant-site-builder.md)

[Ekstra B2C-informasjon](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
