---
title: Opprette et e-handelsområde
description: Dette emnet beskriver oppgavene som er knyttet til oppretting av et nytt e-handelsområde i Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 54259d3f5dfd8c8e1ff2caaadfac497cc0e133e0
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945841"
---
# <a name="create-an-e-commerce-site"></a>Opprette et e-handelsområde

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet beskriver oppgavene som er knyttet til oppretting av et nytt e-handelsområde i Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Hvis du vil begynne å utvikle ditt e-handelsområde, må du først opprette et nytt område i områdetsredigeringsmiljøet. Før du kan opprette et nytt område må du opprette minst én nettbutikk i Dynamics 365 Retail. 

## <a name="set-up-your-site"></a>Konfigurere området

Gjør følgende for å opprette området.

1. I Microsoft Lifecycle Services (LCS) klikker du koblingen for områderedigeringsmiljøet. 
1. Velg **Nytt område**på startsiden for områderedigeringsmiljøet.
1. Angi følgende informasjon i dialogboksen **Nytt område**.

| Felt                               | Beskrivelse |
|-------------------------------------|-------------|
| Områdenavn                           | Angi visningsnavnet som skal brukes for området, i redigeringsmiljøet for området. Dette navnet vises bare i redigeringsmiljøet og blir ikke vist for kunder. |
| Sikkerhetsgruppe for områdeadministrator | Angi sikkerhetsgruppen for Microsoft Azure Active Directory (Azure AD) som administrerer brukere som har områdeadministratorrollen på dette området. |
| Standardkanal (driftsenhetsnummer) | Velg nettbutikken som dette området skal fungere som webbutikkfasade for. Hvis du vil at ditt e-handelsområde skal støtte flere nettbutikker, må du knytte butikkene til området i **Områdeinnstillinger** etter at området er konfigurert. |
| Standardspråk                            | Angi standardspråket for denne nettbutikken og dette markedet. En nettbutikk kan støtte flere språk. Hvis du vil støtte flere språk for denne nettbutikken eller en annen nettbutikk, kan du konfigurere støtten i **Områdeinnstillinger** etter at området er konfigurert.  |
| Domene                              | Velg et domenenavn som skal være domene for denne nettbutikken. Hvis du ikke har konfigurert noen domener i LCS, kan du la dette feltet stå tomt. Når domenet er konfigurert i LCS, må du legge det til i nettbutikken under **Områdeinnstillinger**.  |
| Bane                              | Når området støtter mer enn ett språk for et gitt domenenavn, kan du bruke banefeltet til å opprette en unik område-URL-adresse for dette domenet og denne språkkombinasjonen. Hvis språket du angav i **Standardspråk**-feltet, er det eneste språket du vil støtte for dette domenet eller vil fortsette å være standardspråket etter at du har lokalisert området til flere språk, anbefaler vi at du lar dette feltet stå tomt. |


Når området er opprettet, kan du kontrollere at det er tilknyttet nettbutikken din, ved å velge kategorien **Produker**. Du skal se sortimentet av produkter som er tilordnet nettbutikken. Du kan også bruke rullegardinmenyen øverst til venstre på siden for å få tilgang til de tildelte produktene etter kategori.

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere domenenavnet](configure-your-domain-name.md)

[Distribuere et nytt e-handelsområde](deploy-ecommerce-site.md)

[Knytte et nettområde til en kanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md)

[Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md)

[Aktivere stedsbasert butikkregistrering](enable-store-detection.md)
