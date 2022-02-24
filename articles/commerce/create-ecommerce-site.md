---
title: Opprette et e-handelsområde
description: Dette emnet beskriver trinnene og informasjonen som kreves for å opprette et nytt e-handelsområde i Dynamics 365 Commerce-områdebyggeren.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cf084f90d203d84c91ddf7c0d963780b895ef23d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963041"
---
# <a name="create-an-e-commerce-site"></a>Opprette et e-handelsområde

[!include [banner](includes/banner.md)]

Dette emnet beskriver trinnene og informasjonen som kreves for å opprette et nytt e-handelsområde i Dynamics 365 Commerce-områdebyggeren.

Når du lisensierer Dynamics 365 Commerce-mulighetene, blir områdebygger klargjort med et startområde som du kan bruke som grunnlag for ditt eget område. Hvis du imidlertid vil starte fra grunnen av, eller hvis du vil opprette et annet område, må du opprette et nytt område i områdets redigeringsmiljø. 

## <a name="set-up-your-site"></a>Konfigurere området

Gjør følgende for å opprette området.

1. Åpne områdebyggermiljøet. Du kan finne en kobling til områdebyggertjenesten i Microsoft Lifecycle Services (LCS) på siden for miljøfunksjoner for Commerce.
1. Velg **Nytt område** på startsiden for områderedigeringsmiljøet.
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

[Distribuere en ny e-handelsleier](deploy-ecommerce-site.md)

[Knytte et Dynamics 365 Commerce-nettsted til en nettkanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Laste opp masseomdirigeringer for URL-adresse](upload-bulk-redirects.md)

[Konfigurere en B2C-leier i Commerce](set-up-B2C-tenant.md)

[Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md)

[Konfigurere flere B2C-leiere i et Commerce-miljø](configure-multi-B2C-tenants.md)

[Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md)

[Aktivere stedsbasert butikkregistrering](enable-store-detection.md)
