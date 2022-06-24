---
title: Kontrollere tilgjengelighet for sideinnhold
description: Denne artikkelen beskriver hvordan du kontrollerer tilgjengeligheten for sideinnhold i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: caccb6085947193e4a5f8a8555722dd073f0c275
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884766"
---
# <a name="verify-page-content-accessibility"></a>Kontrollere tilgjengelighet for sideinnhold

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du kontrollerer tilgjengeligheten for sideinnhold i Microsoft Dynamics 365 Commerce.

Når du er ferdig med å endre en side, bør du sørge for at innholdet er tilgjengelig for alle på Internett. I redigeringsverktøyene for handel kan du enkelt kontrollere tilgjengeligheten til sideinnholdet ved hjelp av den integrerte [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-tjenesten. Denne tjenesten verifiserer sideinnholdet ditt mot de seneste retningslinjene for [tilgjengelighet i World Wide Web Consortium (W3C)](https://www.w3.org/standards/webdesign/accessibility).

[Microsoft Accessibility Insights](https://accessibilityinsights.io/)-integreringen må være aktivert på leier- eller områdenivået før du kan bruke den.

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a>Aktivere Microsoft Accessibility Insights for alle områdene i leieren

Følg denne fremgangsmåten for å aktivere [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-integrasjon for alle Commerce-områder i leieren.

> [!NOTE]
> For å få tilgang til leierinnstillinger må du være logget på Commerce som systemadministrator.

1. Logg på Commerce som systemadministrator.
1. I den venstre navigasjonsruten velger **Leierinnstillinger** (ved siden av tannhjulsymbolet) for å utvide den.
1. Velg **Funksjoner** under **Leierinnstillinger**.
1. Sett alternativet **Tilgjengelighetskontroll** til **På**.

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a>Aktivere Microsoft Accessibility Insights for et enkelt område

Følg denne fremgangsmåten for å aktivere [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-integrasjon for et enkelt Commerce-område.

1. Under **Områder** velger du **Fabrikam** (eller navnet på området).
1. Velg **Områdeinnstillinger** i navigasjonsruten til venstre for å utvide den.
1. Velg **Funksjoner** under **Områdeinnstillinger**.
1. Sett alternativet **Tilgjengelighetskontroll** til **På**.

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a>Kontrollere tilgjengeligheten til innholdet på startsiden

Hvis du vil bruke den integrerte [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-tjenesten til å skanne og kontrollere innholdet på startsiden i Commerce, følger du denne fremgangsmåten.

1. Under **Områder** velger du **Fabrikam** (eller navnet på området).
1. Velg **Sider** i navigasjonsruten til venstre.
1. Finn og velg startsside for å åpne den i sideredigeringsprogrammet.
1. På kommandolinjen velger du **Kontroller tilgjengelighet**. Siden **Kontroller tilgjengelighet** vises.
1. Når skanningen er fullført, kan du se gjennom innholdet i rapporten.
1. Hvis noen av kontrollene mislyktes, velger du hvert mislykket kontrollelement for å utvide det slik at du kan vise flere detaljer.
1. Hvis du vil lukke rapporten etter at du er ferdig med å se gjennom den, blar du til bunnan av siden **Kontroller tilgjengelighet** og velger **OK**.

## <a name="additional-resources"></a>Tilleggsressurser

[Endre en eksisterende områdeside](modify-existing-page.md)

[Legg til en ny områdeside](add-new-page.md)

[Velge sideoppsett](select-page-layouts.md)

[Behandle metadata for søkemotor](manage-seo-metadata.md)

[Lagre, forhåndsvise og publisere en side](save-preview-publish-page.md)

[Supplere en produktside](enrich-product-page.md)

[Supplere en kategorimålside](enrich-category-page.md)

[Opprette dynamiske e-handelssider basert på URL-parametere](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
