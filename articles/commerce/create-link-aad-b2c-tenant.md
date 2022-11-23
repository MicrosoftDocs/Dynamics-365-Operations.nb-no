---
title: Opprette eller koble til en eksisterende Azure AD B2C-leier i Azure-portalen
description: Denne artikkelen beskriver hvordan du oppretter eller kobler til en eksisterende Azure Active Directory (Azure AD) bedrift-til-kunde-leietaker (B2C) på Microsoft Azure-portalen.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 0aa12387f00ffc3dd10688c6385c7952f089ab12
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785299"
---
# <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>Opprette eller koble til en eksisterende Azure AD B2C-leier i Azure-portalen

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du oppretter eller kobler til en Azure Active Directory (Azure AD) bedrift-til-kunde-leietaker (B2C) på Microsoft Azure-portalen. Hvis du vil ha mer informasjon, kan du se [Opplæring: Opprette en Azure Active Directory B2B-leier](/azure/active-directory-b2c/tutorial-create-tenant).

For å opprette eller koble til en eksisterende Azure AD B2C-leier i Azure-portalen følger du disse trinnene.

1. Logg på [Azure-portalen](https://portal.azure.com/).
1. Velg **Opprett en ressurs** fra menyen for Azure-portal. Pass på at du bruker abonnementet og katalogen som skal kobles til Commerce-miljøet.

    ![Opprette en ressurs i Azure-portalen.](./media/B2CImage_1.png)

1. Gå til **Identitet \> Azure Active Directory B2C**.
1. På siden **Opprett ny B2C-leier eller koble til en eksisterende leier** bruker du et av alternativene nedenfor som passer best til firmaets behov:

    - **Opprett en ny Azure AD B2C-leier**: Bruk dette alternativet til å opprette en ny Azure AD B2C-leier.
        1. Velg **Opprett en ny Azure AD B2C-leier**.
        1. Under **Organisasjonsnavn** angir du organisasjonsnavnet.
        1. Skriv inn det opprinnelige domenenavnet under **Opprinnelig domenenavn**.
        1. For **Land eller område** velger du aktuelt land eller område.
        1. Velg **Opprett** for å opprette leieren.

     ![Opprette en ny Azure AD-leier.](./media/B2CImage_2.png)

     - **Koble en eksisterende Azure AD B2C-leier til Azure-abonnementet**: Bruk dette alternativet hvis du allerede har en Azure AD B2C-leier du vil koble til.
        1. Velg **Koble en eksisterende Azure AD B2C-leier til Azure-abonnementet**.
        1. For **Azure AD B2C-leier** velger du den riktige B2C-leieren. Hvis det vises en melding i valgboksen om at det ikke ble funnet noen kvalifiserte B2C-leiere, har du ikke en eksisterende kvalifisert B2C-leier, og må opprette en ny.
        1. For **Ressursgruppe** velger du **Opprett ny**. Angi et **navn** på ressursgruppen som skal inneholde leieren, velg **ressursgruppelokasjonen**, og velg deretter **Opprett**.

    ![Koble en eksisterende Azure AD B2C-leier til Azure-abonnementet.](./media/B2CImage_3.png)

1. Når den nye Azure AD B2C-katalogen er opprettet (dette kan ta litt tid), vil det vises en kobling til den nye katalogen på instrumentbordet. Denne koblingen fører deg til siden "Velkommen til Azure Active Directory B2C".

    ![Koble til ny Azure AD-katalog](./media/B2CImage_4.png)

> [!NOTE]
> Hvis du har flere abonnementer i Azure-kontoen eller har konfigurert B2C-leieren uten å koble til et aktivt abonnement, vil et **Feilsøking**-banner gi deg beskjed om å koble leieren til et abonnement. Velg feilsøkingsmeldingen, og følg instruksjonene for å løse problemet med abonnement.

Bildet nedenfor viser et eksempel på et Azure AD B2C **Feilsøking**-banner.

![Advarsel som viser at katalogen ikke har et aktivt abonnement.](./media/B2CImage_5.png)

## <a name="next-steps"></a>Neste trinn

Hvis du vil fortsette prosessen med å konfigurere en B2C-leietaker i Commerce, går du til [Opprette B2C-programmet](create-b2c-app.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere en B2C-leier i Commerce](set-up-b2c-tenant.md)

[Opprette B2C-programmet](create-b2c-app.md)

[Opprette brukerflytpolicyer](create-user-flow-policies.md)

[Legg til leverandører av sosiale identiteter (valgfritt)](add-social-identity-providers.md)

[Oppdater Commerce Headquarters med den nye Azure AD B2C-informasjonen](update-hq-aad-b2c-info.md)

[Konfigurere B2C-leieren i områdebygger for Commerce](config-b2c-tenant-site-builder.md)

[Ekstra B2C-informasjon](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
