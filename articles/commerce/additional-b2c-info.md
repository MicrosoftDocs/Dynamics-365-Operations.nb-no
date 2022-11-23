---
title: Ekstra B2C-informasjon
description: Denne artikkelen gir tilleggsinformasjon om hvordan du definerer B2C-leieren (business-to-consumer) i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/14/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: b60ef15544cd30c44968ee7a588a8a9fb08e8223
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785270"
---
# <a name="additional-b2c-information"></a>Ekstra B2C-informasjon

[!include [banner](includes/banner.md)]

Denne artikkelen gir tilleggsinformasjon om hvordan du definerer B2C-leieren (business-to-consumer) i Microsoft Dynamics 365 Commerce.

### <a name="customer-migration"></a>Kundeoverføring

Hvis du vurderer å overføre kundeposter fra en tidligere identitetsleverandørplattform, kan du arbeide med Dynamics 365 Commerce-teamet for å gjennomgå kundeoverføringsbehovene dine.

Hvis du vil ha mer Azure AD B2C-dokumentasjon om kundeoverføring, kan du se [Overføre brukere til Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Egendefinerte policyer

Hvis du vil ha mer informasjon om tilpassing av Azure AD B2C-samhandlinger og policyflyter utover hva som tilbys av B2C-standardpolicyer, kan du se [Egendefinerte policyer i Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Sekundær administrator

En valgfri, sekundær administratorkonto kan legges til i **Brukere**-delen av B2C-leieren. Dette kan være en direkte konto eller en generell konto. Hvis du må dele en konto på tvers av teamressurser, kan du også opprette en felles konto. På grunn av følsomheten til dataene som er lagret i Azure AD B2C, bør en felles konto overvåkes nøye i henhold til firmaets sikkerhetspraksis.

### <a name="set-up-a-custom-sign-in-domain"></a>Definere et egendefinert domene for pålogging

Azure AD B2C lar deg konfigurere et egendefinert domene for pålogging for Azure AD B2C-leieren. Hvis du vil ha instruksjoner, kan du se [Aktivere egendefinerte domener for Azure Active Directory B2C](/azure/active-directory-b2c/custom-domain). 

Hvis du bruker et egendefinert domene for pålogging, må domenet registreres i Commerce-områdebygger.

Følg fremgangsmåten nedenfor for å registrere et egendefinert domene for pålogging i områdebygger.

1. Velg områdevekslingen i øvre høyre hjørne i områdebyggeren, og velg deretter **Administrer områder**.
1. Velg **Leierinnstillinger \> Oppsett av områdegodkjenning** i navigasjonsruten til venstre.
1. Velg **Administrer** i delen **Områdegodkjenningsprofiler**.
1. På undermenyen til høyre velger du **Rediger**-knappen (blyantsymbolet) ved siden av områdegodkjenningsprofilen du vil angi et egendefinert domene for.
1. I dialogboksen **Rediger områdegodkjenningsprofil** under **Egendefinert domene for pålogging** angir du det egendefinerte domenet for pålogging (for eksempel «login.fabrikam.com»).

> [!WARNING]
> Når du oppdaterer til et egendefinert domene for Azure AD B2C-leieren, påvirker endringen leietakerens utstederdetaljer for tokenet som genereres. Utstederdetaljer omfatter da det egendefinerte domenet i stedet for standarddomenet fra Azure AD B2C. En annen konfigurasjon for **Utsteder** i Commerce headquarters (**Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere \> Delte handelsparametere \> Identitetsleverandører**) endrer systemets samhandling med områdebrukere og kan potensielt opprette en ny kundepost hvis en bruker autentiserer mot den nye utstederen. Alle endringer i et egendefinert domene må testes grundig før du bytter til det egendefinerte domenet i et aktivt Azure AD B2C-miljø.

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere en B2C-leier i Commerce](set-up-b2c-tenant.md)

[Opprette eller koble til en eksisterende Azure AD B2C-leier i Azure-portalen](create-link-aad-b2c-tenant.md)

[Opprette B2C-programmet](create-b2c-app.md)

[Opprette brukerflytpolicyer](create-user-flow-policies.md)

[Legg til leverandører av sosiale identiteter (valgfritt)](add-social-identity-providers.md)

[Oppdater Commerce Headquarters med den nye Azure AD B2C-informasjonen](update-hq-aad-b2c-info.md)

[Konfigurere B2C-leieren i områdebygger for Commerce](config-b2c-tenant-site-builder.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
