---
title: Opprette et e-handelsområde
description: Dette emnet beskriver trinnene og informasjonen som kreves for å opprette et nytt e-handelsområde i Dynamics 365 Commerce-områdebyggeren.
author: bicyclingfool
ms.date: 03/10/2022
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 37734e2ceea3a50c70a2f7945329d4a9cf660cc6
ms.sourcegitcommit: 9c19898e1f41495f804c7f07e2636b53a098c4c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/10/2022
ms.locfileid: "8402781"
---
# <a name="create-an-e-commerce-site"></a>Opprette et e-handelsområde

[!include [banner](includes/banner.md)]

Dette emnet beskriver trinnene og informasjonen som kreves for å opprette et nytt e-handelsområde i Dynamics 365 Commerce-områdebyggeren.

Når du lisensierer Dynamics 365 Commerce-mulighetene, blir områdebygger klargjort med et startområde som du kan bruke som grunnlag for ditt eget område. Hvis du imidlertid vil starte fra grunnen av, eller hvis du vil opprette et annet område, må du opprette et nytt område i områdets redigeringsmiljø. 

## <a name="site-creation-prerequisites"></a>Forutsetninger for opprettelse av område

En områdebyggerbruker må ha en Microsoft Azure Active Directory-brukerkonto (Azure AD) inkludert i Azure AD-sikkerhetsgruppen som er tilordnet for systemadministratorene for e-handel. Hvis du vil ha mer informasjon, kan du se [Distribuere en ny e-handelsleier](deploy-ecommerce-site.md).

> [!NOTE]
> Azure AD-gjestebrukere kan ha ulike tilgangstillatelser i Azure AD-leieren. Selv om de er tatt med i Azure AD-sikkerhetsgruppen som er tilordnet for systemadministratorene for e-handel, må kanskje innstillinger for tillatelsen **Eksterne brukere** i Azure AD justeres for en gjestebruker for at vedkommende skal kunne opprette et e-handelsområde i Commerce. 

Følg denne fremgangsmåten for å justere innstillinger for **Eksterne brukere** i Azure AD.

1. I Azure-portalen går du til Azure AD-leieren.
1. Gå til **Brukerinnstillinger \> Eksterne brukere**, og velg koblingen **Administrer innstillinger for eksternt samarbeid**. Dermed åpnes siden **Innstillinger for eksternt samarbeid** der du kan angi tilgang for gjestebrukere, innstillinger for gjesteinvitasjon og begrensninger for samarbeid. 
1. Juster innstillingene for eksternt samarbeid i samsvar med firmaets sikkerhetspolicyer. 

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

## <a name="rename-your-site"></a>Gi nytt navn til nettstedet ditt

Hvis du vil gi et nytt navn til nettstedet ditt i områdebygger, følger du denne fremgangsmåten.

1. Hvis du vil åpne områdelistevisning, velger du **Områdeveksling** øverst til høyre, og deretter velger du **Behandle områder**. 
1. Merk av i avmerkingsboksen ved siden av området du vil gi nytt navn, og velg deretter **Gi nytt navn** på kommandolinjen.
1. I dialogboksen **Nytt områdeavn** skriver du inn det nye områdenavnet og velger deretter **OK**. Områdelisten oppdateres for å vise områdets nye navn.

## <a name="delete-a-site"></a>Slett et nettsted

Følg denne fremgangsmåten for å slette et nettsted i områdebygger.

1. Hvis du vil åpne områdelistevisning, velger du **Områdeveksling** øverst til høyre, og deretter velger du **Behandle områder**.
1. Velg nettstedet du vil slette, og velg deretter **Slett** på kommandolinjen.
1. I dialogboksen **Slett \<site name\>** skriver du inn navnet på nettstedet og velger deretter **Slett**.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
