---
title: Påloggingskobling omdirigerer tilbake til et e-handelsområde
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når en påloggingskobling omdirigerer tilbake til e-commerce-området i stedet for å gå til påloggingssiden.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: a1d0ae4e487c391020947c607d5d7cb5d1ba6af4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020609"
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

[Registrere et webprogram i Azure Active Directory B2C](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[Konfigurere en B2C-leier i Commerce](../set-up-b2c-tenant.md)