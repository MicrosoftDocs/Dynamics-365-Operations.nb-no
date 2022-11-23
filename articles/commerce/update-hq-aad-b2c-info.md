---
title: Oppdater Commerce Headquarters med den nye Azure AD B2C-informasjonen
description: Denne artikkelen beskriver hvordan du oppdaterer Microsoft Dynamics 365 Commerce headquarters med Azure Active Directory (Azure AD) bedrift-til-kunde-informasjon (B2C).
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: c65949ff97182d2692319ac2af00e3ef35a79580
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785324"
---
# <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Oppdater Commerce Headquarters med den nye Azure AD B2C-informasjonen

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du oppdaterer Microsoft Dynamics 365 Commerce headquarters med Azure Active Directory (Azure AD) bedrift-til-kunde-informasjon (B2C).

Når Azure AD B2C-klargjøringstrinnene ovenfor er fullført, må Azure AD B2C-programmet registreres i Dynamics 365 Commerce-miljøet.

Følg denne fremgangsmåten for å oppdatere Headquarters med den nye Azure AD B2C-informasjonen:

1. I Commerce går du til **Delte handelsparametere** og velger **Identitetsleverandører** på den venstre menyen.
1. Under **Identitetsleverandører** gjør du følgende:
    1. I **Utsteder**-boksen angir du utstederstrengen for identitetsleverandør. Du finner utstederstrengen ved å se [Hente utstederstreng for hovedkvarteroppsett](#obtain-issuer-string-for-headquarters-setup) nedenfor.
    1. I **Navn**-boksen angir du et navn på utstederposten.
    1. I **Type**-boksen angir du **Azure AD B2C (id_token)**.
1. Gjør følgende med ovenstående element for B2C-identitetsleverandør valgt under **Beroende parter**:
    1. I boksen **Klient-ID** angir du B2C-program-IDen, som du finner i **Application ID**-boksen på B2C-programmets egenskapsside.
    1. I **Type**-boksen angir du **Offentlig**.
    1. I **Brukertype**-boksen angir du **Kunde**.
1. Velg **Lagre** i handlingsruten.
1. I Commerce-søkeboksen søker du etter **Distribusjonsplan**
1. I den venstre navigasjonsmenyen på siden **Distribusjonsplaner** velger du jobben **1110 Global konfigurasjon**.
1. Velg **Kjør nå** i handlingsruten.

### <a name="obtain-issuer-string-for-headquarters-setup"></a>Hente utstederstreng for Hovedkvarteroppsett

Følg denne fremgangsmåten for å hente utstederstreng for identitetsleverandør.

1. På Azure AD B2C-siden i Azure-portalen kan du navigere til brukerflyten **Registrering og pålogging**.
1. Velg **Sideoppsett** på den venstre navigasjonsmenyen, gå til **Oppsettsnav**, velg **Side for enhetlig registrering og pålogging**, og velg deretter **Kjør brukerflyt**.
1. Kontroller at programmet er satt til det tiltenkte Azure AD B2C-programmet du opprettet ovenfor, og velg deretter brukerflytkoblingen som vises under hodet **Kjør brukerflyt** som omfatter ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``. (Ikke velg **Kjør brukerflyt**.) Det åpnes en ny fane med metadata for policyen for å hente utstederstrengen.
1. På metadatasiden som vises i nettleserfanen, kopierer du utstederstrengen for identitetsleverandør (verdien for **utsteder** som begynner med «https://» og slutter med «/v2.0/») som ser ut som i følgende eksempel.
   - ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
**ELLER**: Hvis du vil konstruere den samme metadata-URL-en manuelt, gjør du følgende:

1. Opprett en URL-adresse for metadata i følgende format ved hjelp av B2C-leieren og-policyen: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Eksempel: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Angi URL-adressen for metadata på adresselinjen i en leser.
1. I metadataene kopierer du URL-adressen for utsteder av identitetsleverandør (verdien for **"utsteder"**).
    - Eksempel: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="next-steps"></a>Neste trinn

Hvis du vil fortsette prosessen med å konfigurere en B2C-leietaker i Commerce, kan du gå til [Konfigurere B2C-leieren i områdebygger for Commerce](config-b2c-tenant-site-builder.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere en B2C-leier i Commerce](set-up-b2c-tenant.md)

[Opprette eller koble til en eksisterende Azure AD B2C-leier i Azure-portalen](create-link-aad-b2c-tenant.md)

[Opprette B2C-programmet](create-b2c-app.md)

[Opprette brukerflytpolicyer](create-user-flow-policies.md)

[Legg til leverandører av sosiale identiteter (valgfritt)](add-social-identity-providers.md)

[Konfigurere B2C-leieren i områdebygger for Commerce](config-b2c-tenant-site-builder.md)

[Ekstra B2C-informasjon](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
