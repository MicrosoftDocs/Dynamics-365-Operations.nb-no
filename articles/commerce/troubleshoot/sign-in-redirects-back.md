---
title: Påloggingskobling omdirigerer tilbake til et e-handelsområde
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når en påloggingskobling omdirigerer tilbake til e-commerce-området i stedet for å gå til påloggingssiden.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36f10c9f68570a6c67da6b4b6e4155f4634f633a
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585457"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>Påloggingskobling omdirigerer tilbake til et e-handelsområde

[!include [banner](../../includes/banner.md)]

Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når en påloggingskobling omdirigerer tilbake til e-commerce-området i stedet for å gå til påloggingssiden.

## <a name="description"></a>beskrivelse

Når du har konfigurert en ny Microsoft Azure Active Directory B2C-leietaker (Azure AD B2C) i Commerce-områdebyggeren, blir brukere som velger koblingen **Logg på**, sendt tilbake til hovedsiden for e-handel uten å gå til påloggingssiden.

## <a name="resolution"></a>Oppløsning

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a>Bekreft at svaradressen er riktig konfigurert i Azure AD B2C-programmet

Hvis du vil bekrefte at svaradressen er riktig konfigurert i Azure AD B2C-programmet, gjør du følgende.

1. Gå til [Azure-portalen](https://portal.azure.com/).
1. Velg Azure AD B2C-programmet du opprettet for områdetilgang.
1. Velg programmet du opprettet i løpet av Azure AD B2C-oppsettet.
1. Under **Svar-URL** må du kontrollere at listen inneholder oppføringer for både URL-adressen for områdedomenet og den e-handelsgenererte URL-adressen, som vist i eksemplet nedenfor.

    ![URL-oppføringer for Azure AD B2C-svar](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> Både områdets domene-URL og den e-handelsgenererte URL-adressen må være i et gyldig URL-format som ikke omfatter ledende eller etterfølgende skråstreker.

## <a name="additional-resources"></a>Tilleggsressurser

[Registrere et webprogram i Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[Konfigurere en B2C-leier i Commerce](../set-up-b2c-tenant.md)
