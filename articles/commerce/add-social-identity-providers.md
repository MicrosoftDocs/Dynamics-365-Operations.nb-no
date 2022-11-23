---
title: Legge til leverandører av sosiale identiteter
description: Denne artikkelen beskriver hvordan du legger til leverandører av sosiale identiteter på Microsoft Azure-portalen.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 5596097a5484acafda54adcfffa68fb59c8fbc65
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785281"
---
# <a name="add-social-identity-providers"></a>Legge til leverandører av sosiale identiteter

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du legger til leverandører av sosiale identiteter på Microsoft Azure-portalen.

Leverandører av sosiale identiteter gjør det mulig for brukere å bruke sine sosiale kontoer for godkjenning. Det er valgfritt å legge til leverandør for godkjenning av sosiale identiteter i Dynamics 365 Commerce. 

Hvis godkjenning av sosial identitetsleverandør ikke er lagt til, vil standard Azure Active Directory (Azure AD) B2C-profiler være hovedprofilene til brukerbasen. Brukerne velger sine egne brukernavn (foretrukket e-postadresse) og angir et passord. Azure AD B2C vil godkjenne brukere direkte. 

Hvis godkjenning av sosial identitetsleverandør er lagt til og en bruker velger en av de tilbudte sosiale identitetsleverandørene, opprettes fremdeles en enhet i Azure AD B2C-leieren. Azure AD B2C vil deretter godkjenne brukerens legitimasjonsbeskrivelser med den sosiale identitetsleverandøren.

> [!NOTE]
> Påloggingen av identitetsleverandøren oppretter en post i B2C-leieren, men i et annet format enn lokale kontoer, ettersom den kaller den eksterne referansen for sosial identitetsleverandør for godkjenning. Brukeren kan bruke samme e-postadresse på tvers av sosiale identitetsleverandører, som betyr at e-postbrukernavnet som brukes til godkjenning, ikke kan være unikt for leieren. Azure AD B2C vil bare sørge for at brukere har en unik e-postadresse på lokale B2C-kontoer.

Før du kan legge til en sosial identitetsleverandør for godkjenning, må du gå til identitetsleverandørens portal og konfigurere et identitetsleverandørprogram som beskrevet i Azure AD i B2C-dokumentasjonen. Nedenfor finner du en liste over koblinger til dokumentasjonen.

- [Amazon](/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (Én leier)](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Microsoft-konto](/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Legge til og konfigurere en leverandør av sosiale identiteter

> [!NOTE]
> Det å legge til leverandører for sosial identitet er et valgfritt trinn når du konfigurerer en B2C-leietaker i Microsoft Dynamics 365 Commerce.

Følg denne fremgangsmåten for å legge til og konfigurere en leverandør av sosiale identiteter.  

1. I Azure-portalen går du til **Identitetsleverandører**.
1. Velg **Legg til**. Skjermbildet **Legg til identitetsleverandør** vises.
1. Under **Navn** skriver du inn navnet som skal vises for brukere på påloggingsskjermen.
1. Under **Type identitetsleverandør** velger du en identitetsleverandør fra listen.
1. Velg **OK**.
1. Velg **Konfigurer denne identitetsleverandøren** for å få tilgang til skjermbildet for **oppsett av sosial identitetsleverandør** .
1. Under **Klient-ID** angir du klient-IDen som hentes fra oppsettet for identitetsleverandørprogram.
1. Under **Klienthemmelighet** angir du klienthemmeligheten som hentes fra oppsettet for identitetsleverandørprogram.
1. Knytt brukerflyt til policyer for pålogging/registrering:
1. Gå til **Azure AD B2C – brukerflyter (policyer) \> {policyen for pålogging/registrering} \> Identitetsleverandører**.
1. Hvis du vil tilknytte brukerflytpolicyen for pålogging/registrering, velger du hver identitetsleverandør du har angitt for kontoen. Hvis du vil teste disse flytene, velger du **Kjør brukerflyt** for hver identitetsleverandør. En ny kategori viser påloggingssiden som viser den nye valgboksen for identitetsleverandør.

Følgende bilde viser eksempler på skjermbildene **Legg til identitetsleverandør** og **Konfigurere sosial identitetsleverandør** i Azure AD B2C.

![Legge til en leverandør av sosiale identiteter i programmet.](./media/B2CImage_14.png)

Det følgende bildet viser et eksempel på hvordan du kan velge identitetsleverandører på siden Azure AD B2C **identitetsleverandører**.

![Velg hver sosial identitetsleverandør du vil aktivere for policyen.](./media/B2CImage_16.png)

Bildet nedenfor viser et eksempel på et standard påloggingsskjermbilde med en påloggingsknapp for sosial identitetsleverandør.

> [!NOTE]
> Hvis du bruker de egendefinerte sidene som er innebygd i Commerce for brukerflytene, må knappene for sosiale identietsleverandører legges til ved hjelp av utvidbarhetsfunksjonene i Commerce-modulbiblioteket. Når du setter opp programmer hos en bestemt sosial identitetsleverandør, kan det i noen tilfeller være at URL-adresser eller konfigurasjonsstrenger skiller mellom store og små bokstaver. Se tilkoblingsinstruksjonene til den sosiale identitetsleverandøren for å få mer informasjon.
 
![Eksempel på standard påloggingsskjerm med påloggingsknappen for sosial identitetsleverandør.](./media/B2CImage_17.png)

## <a name="next-steps"></a>Neste trinn

Hvis du vil fortsette prosessen med å konfigurere en B2C-leietaker i Commerce, [Oppdater Commerce Headquarters med den nye Azure AD B2C-informasjonen](update-hq-aad-b2c-info.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere en B2C-leier i Commerce](set-up-b2c-tenant.md)

[Opprette eller koble til en eksisterende Azure AD B2C-leier i Azure-portalen](create-link-aad-b2c-tenant.md)

[Opprette B2C-programmet](create-b2c-app.md)

[Opprette brukerflytpolicyer](create-user-flow-policies.md)

[Oppdater Commerce Headquarters med den nye Azure AD B2C-informasjonen](update-hq-aad-b2c-info.md)

[Konfigurere B2C-leieren i områdebygger for Commerce](config-b2c-tenant-site-builder.md)

[Ekstra B2C-informasjon](additional-b2c-info.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
