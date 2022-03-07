---
title: Oversikt over e-handelsområde
description: Dette emnet gir en oversikt over støtte for e-handelsområder i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 53bce671d6aca35335a3b3ef557a94fa60da1edc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251193"
---
# <a name="e-commerce-site-overview"></a>Oversikt over e-handelsområde

[!include [banner](includes/banner.md)]

Dette emnet gir en oversikt over støtte for e-handelsområder i Microsoft Dynamics 365 Commerce. Den inneholder informasjon om hvordan nettbutikker for e-handel blir initialisert og behandlet i Dynamics 365 Commerce. Det inneholder også koblinger til mer informasjon om nettbutikker og informasjon om hvordan du konfigurerer et e-handelsområde. Selv om dette emnet dekker mye av det grunnleggende, dekker det ikke alt som kreves for å konfigurere et e-handelsområde for produksjon. Du finner mer avanserte emner i Dynamics 365 Commerce-dokumentasjonen.

## <a name="online-store-channel"></a>Kanal for nettbutikk

Før du kan opprette området i Dynamics 365 Commerce, må du opprette minst én nettbutikkanal. Hvis du vil ha mer informasjon, kan du se [Sett opp en nettkanal](channel-setup-online.md). 

I Dynamics 365 Commerce bruker du en nettbutikkanal til å opprette produkter, priser, språk, betalingsmåter, leveringsmåter, oppfyllingssentre og andre aspekter av Internett-opplevelsen som skal være tilgjengelig for kundene dine.

Bare én nettbutikkanal må konfigureres før du kan komme i gang med Dynamics 365 Commerce. Et enkelt e-handelsområde kan imidlertid gi Internett-opplevelsen for flere nettbutikker. Hvis for eksempel flere nettbutikker er konfigurert til å støtte forskjellige geografiske områder, kan et enkelt sett med e-handelssider brukes til å gi de unike opplevelsene som er definert av hver butikk. Hvis du vil ha mer informasjon om hvordan du konfigurerer et område til å støtte flere nettbutikker, kan du se [Knytte et nettområde til en kanal](associate-site-online-store.md).

Når en nettbutikk er satt opp, kan den knyttes til Dynamics 365 Commerce-området som vil fungere som din nettbutikkfasade. Hvis du vil ha mer informasjon om nettbutikker og hvordan du konfigurerer dem, kan du se [Konfigurere nettbutikker](https://docs.microsoft.com/dynamics365/unified-operations/retail/online-stores).

## <a name="deploy-a-new-e-commerce-tenant"></a>Distribuere en ny e-handelsleier

Under initialisering av et e-handelsområde blir du bedt om å oppgi et domenenavn. Hvis du vil ha mer informasjon om domener i Commerce, kan du se [Konfigurer domenenavnet](configure-your-domain-name.md) og [Domener i Dynamics 365 Commerce](domains-commerce.md). Hvis du vil distribuere en ny e-handelsleier ved hjelp av [Microsoft Dynamics Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide), følger du fremgangsmåten i [Distribuer en ny e-handelsleier](deploy-ecommerce-site.md). Når e-handelsleieren er konfigurert i LCS, får du en kobling til Commerce-områdebygger. Deretter kan du bruke Commerce-områdebygger til å initialisere og konfigurere e-handelsområdene.

## <a name="initialize-your-e-commerce-site"></a>Initialiser e-handelsområdet ditt

Når du starter Commerce-områdebygger fra LCS, vises siden **Områder**. Denne siden inneholder to forhåndskonfigurerte områder, **standard** og **fabrikam**, som vist i eksemplet i følgende illustrasjon.

![Områder-siden i Commerce-områdebygger](media/e-commerce-site-01.png)

Når du velger et av disse områdene, blir du bedt om å velge et domenenavn, en standard nettbutikkanal, et støttet språk for den valgte kanalen og en bane. Hvis bare én kanal er brukt, kan du la banen være tom. Flere nettbutikkanaler eller språk kan konfigureres senere i Commerce-områdebygger. Hver tilleggskanal eller hvert språk vil kreve en unik bane. Du har for eksempel to nettkanaler knyttet til ett enkelt område, og domenenavnet for området er `www.fabrikam.com`. I dette tilfellet kan banen for en kanal være standardverdien som ikke har noen bane (`https://www.fabrikam.com`), og den andre kanalen kan settes til en ny bane, for eksempel **site2**, som får nettadressen `https://www.fabrikam.com/site2`. Følgende illustrasjon viser et eksempel på en dialogboks for initialisering av område i Commerce-områdebygger.

![Dialogboksen for initialisering av område i Commerce-områdebygger](media/e-commerce-site-02.png)

**Områder**-siden inneholder også en **Nytt område**-knapp. Dialogboksen som vises når du velger denne knappen, ligner på dialogboksen for områdeinitialisering, men den brukes til å opprette et nytt område. Nye områder er tomme. De inneholder ikke samme standardmaler, fragmenter, sider og bilder som leveres med **standard**-og **fabrikam**-områder. Du kan imidlertid, etter behov, åpne en støtteforespørsel for å be om at en kopi av standardinnholdet legges til på et nytt, tomt område. Hvis du vil ha mer informasjon, kan du se [Opprette et e-handelsområde](create-ecommerce-site.md).

Når et nytt område er initialisert, vises **startsiden** for Commerce-områdebygger. Denne siden inneholder koblinger til vanlige handlinger og veiledningsinnhold, som vist i eksemplet i den følgende illustrasjonen.

![Koblinger på startsiden i Commerce-områdebygger](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a>Endre nettbutikkanaler eller legge til nettbutikkanaler i et e-handelsområde

Etter at et e-handelsområde er opprettet, kan du endre kanalen som den er tilknyttet, ved å følge trinnene i [Tilknytt et e-handelsområde med en nettkanal](associate-site-online-store.md). Eksemplet i illustrasjonen nedenfor viser hvordan et kanaldriftsenhetsnummer (OUN) kan endres på **Kanaler**-siden (**Områdeinnstillinger \> Kanaler**). Når du er ferdig med å gjøre endringer, må du velge **Lagre og publiser**. På denne måten sikrer du at endringen er publisert.

![Kanaler-siden i Commerce-områdebygger](media/e-commerce-site-04.png)

Du kan legge til nye kanaler ved å velge **Legg til en kanal**. Hvis du vil legge til nye språk i en kanal, velger du kanalen og velger deretter **Legg til en nasjonal innstilling** i kanaldialogboksen som vises. Før nasjonale innstillinger kan vises i dialogboksen, må de være forhåndskonfigurert for nettbutikkanalen i Commerce Headquarters.

![Kanal-dialogboksen i Commerce-områdebygger](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a>Konfigurere en Azure B2C-leier

Dynamics 365 Commerce bruker forretning-til-forbruker (B2C) for Azure Active Directory (Azure AD) til å støtte brukerlegitimasjon og godkjenningsflyter. Hvis du vil ha informasjon om hvordan du konfigurerer Azure B2C-leieren, kan du se [Konfigurere en B2C-leier i Commerce](set-up-b2c-tenant.md), [Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md) og [Konfigurere flere B2C-leiere i et Commerce-miljø](configure-multi-b2c-tenants.md).

## <a name="overview-of-the-default-site-pages"></a>Oversikt over standard områdesider

**Standard**- og **fabrikam**-områdene inneholder forhåndskonfigurerte maler, fragmenter og sider som kan hjelpe deg med å komme i gang. Hvis du vil ha mer informasjon, kan du se følgende emner:

- [Oversikt over startside](quick-tour-home-page.md)
- [Oversikt over produktdetaljside](quick-tour-pdp.md)
- [Oversikt over sider for handlekurv og kasse](quick-tour-cart-checkout.md)
- [Oversikt over kontobehandlingssider](quick-tour-account-management.md)

## <a name="manage-site-settings"></a>Administrere områdeinnstillinger

Hvis du vil ha informasjon om hvordan du administrerer områdeinnstillingene, kan du se emnene nedenfor:

- [Behandle brukere og roller for e-handel](manage-ecommerce-users-roles.md)
- [Vurderinger for søkemotoroptimalisering (SEO) for området](/search-engine-optimization-considerations.md)
- [Behandle policy for innholdssikkerhet (CSP)](manage-csp.md)
- [Velge et områdetema](select-site-theme.md)

## <a name="manage-site-content"></a>Administrere områdeinnhold

Hvis du vil ha informasjon om hvordan du administrerer områdeinnhold, kan du se emnene nedenfor:

- [Ordliste for sidemodell](page-elements-overview.md)
- [Dokumentere statuser og livssyklus](document-states-overview.md)
- [Maler og oppsett](templates-layouts-overview.md)
- [Arbeide med fragmenter](work-with-fragments.md)
- [Arbeide med moduler](work-with-modules.md)
- [Oversikt over behandling av digitale aktiva](dam-overview.md)
- [Oversikt over modulbibliotek](starter-kit-overview.md)

## <a name="additional-resources"></a>Tilleggsressurser

[Opprette et e-handelsområde](create-ecommerce-site.md)

[Distribuere et nytt e-handelsområde](deploy-ecommerce-site.md)

[Knytte et nettområde til en kanal](associate-site-online-store.md)

[Konfigurere domenenavnet](configure-your-domain-name.md)

[Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md)

[Aktivere stedsbasert butikkregistrering](enable-store-detection.md)

[Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]