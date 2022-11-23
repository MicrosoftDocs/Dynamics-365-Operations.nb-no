---
title: Opprette et B2C-program
description: Denne artikkelen beskriver hvordan du oppretter et bedrift-til-kunde-program (B2C) på Microsoft Azure-portalen.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: d8956d51bac7bf2a162a370ae5ef1c7e7cdc1e2f
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785288"
---
# <a name="create-a-b2c-application"></a>Opprette et B2C-program

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du oppretter et bedrift-til-kunde-program (B2C) på Microsoft Azure-portalen.

Når B2C-leieren er opprettet, oppretter du et B2C-program i den nye Azure Active Directory B2C-leieren (Azure AD) for å samhandle med Commerce.

Hvis du vil opprette B2C-programmet, gjør du følgende:

1. I Azure-portalen velger du **Appregistreringer** og deretter **Ny registrering**.
1. Under **Navn** angir du navnet du vil gi dette Azure AD B2C-programmet.
1. Under **Støttede kontotyper** velger du **Kontoer i enhver identitetsleverandør- eller organisasjonskatalog (for godkjenning av brukere med brukerflyter)**.
1. For **URI for omadressering** angir du de dedikerte svar-URL-ene som typen **Web**. For informasjon om URL-adresser for svar, og hvordan du kan formatere dem, se [URL-adresser for svar](#reply-urls) nedenfor. En URL-adresse for omdirigering av URI/svar må angis for å aktivere omdirigeringer fra Azure AD B2C tilbake til området når en bruker godkjenner det. Svar/URLen kan legges til under registreringsprosessen, eller den kan legges til senere ved å velge koblingen **Legg til en omdirigerings-URI** fra **Oversikt**-menyen i B2C-programmets **Oversikt**-del.
1. For **Tillatelser** velger du **Gi administratorsamtykke til openid- og offline_access-tillatelser**.
1. Velg **Registrer**.
1. Velg det nyopprettede programmet, og naviger til **Godkjenning**-menyen. 
1. Hvis det angis en svar-URL-adresse, går du til **Implisitt tildeling og hybridflyter** og velger både **Tilgangstokener** og **ID-tokener**-alternativene for å aktivere dem for programmet, og deretter velger du **Lagre**. Hvis en URL-adresse for svar ikke ble lagt inn under registreringen, kan den også legges til på denne siden ved å velge **Legg til en plattform**, velge **Web** og deretter angi omadresserings-URI for programmet. Delen **Implisitt tildeling og hybridflyt** vil deretter være tilgjengelig for å velge både alternativene **Tilgangstokener** og **ID-tokener**.
1. Gå til **Oversikt**-menyen i Azure-portalen, og kopier **Program-ID-en (klient)**. Noter denne ID-en for senere trinn i oppsettet (som blir referert til senere som **Klient-GUID**).

Hvis du vil ha mer informasjon om appregistreringer i Azure AD B2C, kan du se [Den nye appregistreringsopplevelsen for Azure Active Directory B2C](/azure/active-directory-b2c/app-registrations-training-guide)

### <a name="reply-urls"></a>URL-adresser for svar

Svar-URL-adresser er viktige, fordi de gir en tillatelsesliste for returdomener når området kaller Azure AD B2C for å godkjenne en bruker. Dette tillater retur av den godkjente brukeren til domenet de logger seg på fra (områdedomenet). 

I boksen **Svar-URL** på skjermen **Azure AD B2C-programmer \> Nytt program** må du legge til separate linjer for både områdedomet og (når miljøet er klargjort) den Commerce-genererte URL-en. Disse URL-adressene må alltid bruke et gyldig URL-format og må være basis-URLer (ingen etterfølgende skråstreker eller baner). Strengen ``/_msdyn365/authresp`` må deretter legges til de primære URL-adressene, som i følgende eksempler.

- ``https://www.fabrikam.com/_msdyn365/authresp`` (Domenet skal samsvare med hele e-handelsdomenet. Hvis du har flere domener, må du legge til denne URL-adressen for hvert domene.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="next-steps"></a>Neste trinn

Hvis du vil fortsette prosessen med å konfigurere en B2C-leietaker i Commerce, går du til [Opprette brukerflytpolicyer](create-user-flow-policies.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere en B2C-leier i Commerce](set-up-b2c-tenant.md)

[Opprette eller koble til en eksisterende Azure AD B2C-leier i Azure-portalen](create-link-aad-b2c-tenant.md)

[Opprette brukerflytpolicyer](create-user-flow-policies.md)

[Legg til leverandører av sosiale identiteter (valgfritt)](add-social-identity-providers.md)

[Oppdater Commerce Headquarters med den nye Azure AD B2C-informasjonen](update-hq-aad-b2c-info.md)

[Konfigurere B2C-leieren i områdebygger for Commerce](config-b2c-tenant-site-builder.md)

[Ekstra B2C-informasjon](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
