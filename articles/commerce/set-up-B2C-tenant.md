---
title: Konfigurer en B2C-leier i Commerce
description: Denne artikkelen beskriver hvordan du konfigurerer Azure Active Directory (Azure AD) bedrift-til-kunde (B2C)-leietakere for godkjenning av brukerområde i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 3421dd3d67198a99ac236a56cbb4f300cb591a03
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785148"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>Konfigurer en B2C-leier i Commerce

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer Azure Active Directory (Azure AD) bedrift-til-kunde (B2C)-leietakere for godkjenning av brukerområde i Dynamics 365 Commerce.

Dynamics 365 Commerce bruker Azure AD B2C til å støtte brukerlegitimasjon og godkjenningsflyt. En bruker kan registrere seg, logge inn og tilbakestille passordet ved hjelp av disse flytene. Azure AD B2C lagrer sensitiv brukergodkjenningsinformasjon, for eksempel brukernavn og passord. Brukerposten i B2C-leieren vil lagre enten en B2C-post for lokal forretningsforbindelse eller en B2C-post for sosial identitetsleverandør. Disse B2C-postene vil koble tilbake til kundeoppføringen i Commerce-miljøet.

> [!WARNING] 
> Azure AD B2C avvikler gamle (eldre) brukerflyter innen 1. august 2021. Derfor bør du planlegge å migrere brukerflytene til den nye anbefalte versjonen. Den nye versjonen gir funksjonsparitet og nye funksjoner. Modulbiblioteket for Commerce versjon 10.0.15 eller høyere skal brukes med de anbefalte B2C-brukerflytene. Hvis du vil ha mer informasjon, kan du se [Brukerflyter i Azure Active Directory B2C](/azure/active-directory-b2c/user-flow-overview).
 
 > [!NOTE]
 > Commerce-evalueringsmiljøer leveres med en forhåndslastet Azure AD B2C-leier til demonstrasjonsformål. Det er ikke nødvendig å laste inn din egen Azure AD B2C-leier med trinnene nedenfor i evalueringsmiljøet.

> [!TIP]
> Du kan beskytte områdebrukerne ytterligere og forbedre sikkerheten til Azure AD B2C-leierne med identitetsbeskyttelse og betinget tilgang i Azure AD. Hvis du vil gå gjennom funksjonene som er tilgjengelige for Azure AD B2C Premium P1- og Premium P2-leiere, kan du se [Identitetsbeskyttelse og betinget tilgang for Azure AD B2C](/azure/active-directory-b2c/conditional-access-identity-protection-overview).

## <a name="dynamics-environment-prerequisites"></a>Forutsetninger for Dynamics-miljø

Før du begynner, må du sørge for at Dynamics 365 Commerce miljøet og e-handelskanalen er konfigurert på riktig måte ved å oppfylle følgende forutsetninger.

- Sett POS-operasjonene **AllowAnonymousAccess**-verdien til "1" i Commerce Headquarters:
    1. Gå til **POS-operasjoner**.
    1. Høyreklikk i operasjonsrutenettet, og velg **Tilpass**.
    1. Velg **Legg til et felt**.
    1. I listen over tilgjengelige kolonner velger du **AllowAnonymousAccess**-kolonnen for å legge den til.
    1. Velg **Oppdater**.
    1. For **612** "Legg til kunde"-operasjonen endrer du **AllowAnonymousAccess** til "1."
    1. Kjør **1090 (kasser)**-jobben.
- Angi kundekonto for nummerserie **Manuell**-attributt **Nei** i Commerce Headquarters:
    1. Gå til **Retail og Commerce \> Hovedkvarteroppsett \> Parametere \> Kunder-parametere**.
    1. Velg **Nummerserier**.
    1. I **Kundekonto**-raden dobbeltklikker du verdien **Nummerseriekode**.
    1. I hurtigfanen **Generelt** i nummerserien angir du **Manuell** til **Nei**.

Etter at Dynamics 365 Commerce miljøet er distriburert, anbefales det også å [Initialisere data for utgangsverdi](enable-configure-retail-functionality.md) i miljøet.

## <a name="next-steps"></a>Neste trinn

Hvis du vil fortsette prosessen med å konfigurere en B2C-leietaker i Commerce, gå til [Opprette eller koble til en eksisterende Azure AD B2C-leier i Azure-portalen](create-link-aad-b2c-tenant.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Opprette eller koble til en eksisterende Azure AD B2C-leier i Azure-portalen](create-link-aad-b2c-tenant.md)

[Opprette B2C-programmet](create-b2c-app.md)

[Opprette brukerflytpolicyer](create-user-flow-policies.md)

[Legg til leverandører av sosiale identiteter (valgfritt)](add-social-identity-providers.md)

[Oppdater Commerce Headquarters med den nye Azure AD B2C-informasjonen](update-hq-aad-b2c-info.md)

[Konfigurere B2C-leieren i områdebygger for Commerce](config-b2c-tenant-site-builder.md)

[Ekstra B2C-informasjon](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
