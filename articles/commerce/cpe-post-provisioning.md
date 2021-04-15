---
title: Konfigurere et evalueringsmiljø for Dynamics 365 Commerce
description: Dette emnet forklarer hvordan du konfigurerer et evalueringsmiljø i Microsoft Dynamics 365 Commerce etter klargjøring.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e80830a1cb0864c7eef19857b91e36ad27cdef
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795865"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a>Konfigurere et evalueringsmiljø for Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer et evalueringsmiljø i Microsoft Dynamics 365 Commerce etter klargjøring.

Fullfør prosedyrene i dette emnet bare etter at evalueringsmiljøet i Commerce er klargjort. Hvis du vil ha informasjon om hvordan du klargjør Commerce-evalueringsmiljøet, kan du se [Klargjøre et Commerce-evalueringsmiljø](provisioning-guide.md).

Når evalueringsmiljøet i Commerce er klargjort ende til ende, må du fullføre flere trinn etter klargjøring før du kan begynne å evaluere miljøet. Hvis du vil fullføre disse trinnene, må du bruke Microsoft Dynamics Lifecycle Services (LCS, ) og Dynamics 365 Commerce.

## <a name="before-you-start"></a>Før du starter

1. Logg på [LCS-portalen](https://lcs.dynamics.com).
1. Gå til prosjektet.
1. Fra den øverste menyen velger du **Skybaserte miljøer**.
1. Velg miljøet fra listen.
1. Velg **Logg på miljøet** i miljøinformasjonen til høyre. Du vil bli sendt til Commerce Headquarters.
1. Kontroller at den juridiske enheten **USRT** er valgt i øvre høyre hjørne.

Under aktiviteter etter klargjøring i Commerce Headquarters må du kontrollere at den juridiske enheten **USRT** alltid er valgt.

## <a name="configure-the-point-of-sale"></a>Konfigurere salgsstedet

### <a name="associate-a-worker-with-your-identity"></a>Knytt en arbeider til din identitet

Hvis du vil knytte en arbeider med identiteten din i Commerce Headquarters, følger du denne fremgangsmåten.

1. Bruk menyen til venstre, og gå til **Moduler \> Retail og Commerce \> Ansatte \> Arbeidere**.
1. Finn og velg følgnede post i listen **000713 - Andrew Collette**.
1. Klikk **Commerce** i handlingsruten.
1. Velg **Tilknytt eksisterende ID**.
1. I feltet **E-post** (til høyre for **Søk ved hjelp av e-post**) skriver du inn e-postadressen din.
1. Velg **Søk**.
1. Velg posten med navnet ditt.
1. Velg **OK**.
1. Velg **Lagre**.

### <a name="activate-cloud-pos"></a>Aktivere Skysalgssted

Hvis du vil aktivere Cloud POS, følger du denne fremgangsmåten i LCS.

1. Fra den øverste menyen velger du **Skybaserte miljøer**.
1. Velg miljøet fra listen.
1. Velg **Logg på Cloud Point of Sale** i miljøinformasjonen til høyre.
1. Velg **Neste** for å åpne dialogboksen **Før du starter**.
1. La **Server-URL**-feltet være slik det er. Velg **Neste**.
1. Logg på ved hjelp av Microsoft Azure Active Directory (Azure AD)-kontoen din.
1. Under **Butikknavn** velger du **San Francisco**, og deretter velger du **Neste**.
1. Under **Register og enhet** velger du **SANFRAN-1**.
1. Velg **Aktiver**. Du er logget av og tatt til påloggingssiden for salgsstedet.
1. Du kan nå logge på Cloud POS-opplevelsen ved hjelp av operatør-ID-en **000713** og passordet **123**.

## <a name="set-up-your-site-in-commerce"></a>Konfigurere området i Commerce

Følg denne fremgangsmåten for å begynne å konfigurere evalueringsområdet i Commerce.

1. Logg på områdebyggeren ved hjelp av URL-adressen du noterte da du startet e-handel under klargjøring (se [Initialisere e-handel](provisioning-guide.md#initialize-e-commerce)).
1. Klikk på **Fabrikam**-området for å åpne dialogboksen for områdeoppsett.
1. Velg domenet du angav da du startet e-handel.
1. Velg **Fabrikam-utvidet nettbutikk** for standardkanal. (Pass på at du velger den **utvidede** nettbutikken.)
1. Velg **nb-no** for standardspråk.
1. Behold verdien i **Bane**-feltet slik det er.
1. Velg **OK**. Listen over sider på området vises.

## <a name="enable-jobs"></a>Aktivere jobber

Følg disse trinnene for å aktivere jobber i Commerce.

1. Logg på miljøet (hovedkontor).
1. Gå til **Retail og Commerce \> Forespørsler og rapporter \> Satsvise jobber** ved hjelp av menyen til venstre.

    De resterende trinnene i denne prosedyren må fullføres for hver av følgende jobber:

    * Behandle e-postvarsling for detaljistordre
    * Produkttilgjengelighet
    * P-0001
    * Synkroniser ordrejobb

1. Bruk hurtigfilteret til å søke etter jobben ved hjelp av navnet.
1. Hvis statusen for jobben er **Utfører**, utfører du følgende trinn:

    1. Velg posten.
    1. Velg **Endre status** i kategorien **Satsvis jobb** i handlingsruten.
    1. Velg **Avbryt**, og velg deretter **OK**.

Du kan også angi et intervall for regelmessighet til ett (1) minutt for følgende jobber:

* Behandle e-postvarslingsjobb for detaljistordre
* P-0001-jobb
* Synkroniser ordrejobb

### <a name="run-full-data-synchronization"></a>Kjøre fullstendig datasynkronisering

Hvis du vil kjøre full datasynkronisering i Commerce, gjør du følgende i Commerce Headquarters.

1. Bruk menyen til venstre og gå til **Moduler \> Retail og Commerce \> Hovedkvarteroppsett \> Handelsplanlegger \> Kanaldatabase**.
1. Velg kanalen med navnet **scXXXXXXXXX**.
1. I handlingsruten velger du **Fullstendig datasynkronisering**.
1. Angi **9999** som distribusjonsplan.
1. Velg **OK**.
1. Velg **OK**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Teste kredittkortinformasjon for å utføre testinnkjøp

Hvis du skal utføre testtransaksjoner på området, kan du bruke denne testkredittkortinformasjonen:

- **Kortnummer:** 4111-1111-1111-1111
- **Utløpsdato:** 10/20
- **Verdi for kortbekreftelse (CVV-kode):** 737

> [!IMPORTANT]
> Du bør ikke prøve å bruke faktisk kredittkortinformasjon på testområdet under noen omstendigheter!

## <a name="next-steps"></a>Neste trinn

Når klargjøringen og konfigurasjonstrinnene er fullført, er du klar til å bruke evalueringsmiljøet. Bruk URL-adressen for Commerce-områdebygger for å gå til redigeringsopplevelsen. Bruk URL-adressen for Commerce-området for å gå til kundeområdet for detaljhandel.

Hvis du vil konfigurere valgfrie funksjoner for Commerce-evalueringsmiljøet, kan du se [Konfigurere valgfrie funksjoner for et Commerce-evalueringsmiljø](cpe-optional-features.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over Dynamics 365 Commerce-evalueringsmiljø](cpe-overview.md)

[Klargjøre et evalueringsmiljø for Dynamics 365 Commerce](provisioning-guide.md)

[Konfigurere valgfrie funksjoner for et evalueringsmiljø for Dynamics 365 Commerce](cpe-optional-features.md)

[Konfigurere BOPIS i et evalueringsmiljø for Dynamics 365 Commerce](cpe-bopis.md)

[Vanlige spørsmål om Dynamics 365 Commerce-evalueringsmiljø](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-webområde](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
