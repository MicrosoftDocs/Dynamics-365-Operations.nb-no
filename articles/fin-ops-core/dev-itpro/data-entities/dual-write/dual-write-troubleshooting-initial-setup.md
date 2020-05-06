---
title: Feilsøke problemer under første oppsett
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer som kan oppstå under det første oppsettet av integrering mellom Finance and Operations-apper og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 76e104c9ebd7db7ebcbaf214e84be6c4353e8a73
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275447"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Feilsøke problemer under første oppsett

[!include [banner](../../includes/banner.md)]



Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service. Dette emnet inneholder informasjon som kan hjelpe deg med å løse problemer som kan oppstå under det første oppsettet av integrering med dobbel skriving.

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="you-cant-link-a-finance-and-operations-app-to-common-data-service"></a>Du kan ikke koble en Finance and Operations-app til Common Data Service

**Nødvendig rolle for å konfigurere dobbel skriving:** Systemadministrator i Finance and Operations-apper og Common Data Service.

Feil på **oppsett-koblingen til Common Data Service**-siden skyldes vanligvis ufullstendige oppsetts- eller tillatelsesproblemer. Kontroller at hele tilstandskontrollen bestås på **Oppsett-koblingen til Common Data Service**-siden, som vist i illustrasjonen nedenfor. Du kan ikke koble til dobbel skriving med mindre hele tilstandssjekken bestås.

![Vellykket tilstandssjekk](media/health_check.png)

Du må ha legitimasjon for Azure AD-leieradministrator for å koble til Finance and Operations- og Common Data Service-miljøene. Når du har knyttet til miljøene, kan brukere logge på ved hjelp av kontolegitimasjonen og oppdatere en eksisterende enhetstilordning.

## <a name="error-when-you-open-the-link-to-common-data-service-page"></a>Feil når du åpner Kobling til Common Data Service-siden

**Nødvendig legitimasjon for å løse problemet:** Azure AD-leieradministrator

Du kan få følgende feilmelding når du prøver å åpne **Kobling til Common Data Service**-siden i en Finance and Operations-app:

*Svarstatuskoden indikerer ikke fullført: 404 (ikke funnet).*

Denne feilen oppstår når samtykketrinnet ikke er fullført. Hvis du vil validere om samtykketrinnet er fullført, logger du på portal.Azure.com ved hjelp av kontoen for Azure AD-leieradministrator og ser om tredjepartsappen som har IDen **33976c19-1db5-4c02-810e-c243db79efde** vises i listen Azure AD **Enterprise-programmer**. Hvis den ikke gjør det, må du gi appsamtykke.

Følg denne fremgangsmåten for å gi samtykke for appen.

1. Åpne følgende URL-adresse ved hjelp av administratorlegitimasjonen. Du skal bli bedt om samtykke.

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. Velg **Godta** for å angi at du gir ditt samtykke til å installere appen som har ID-en **33976c19-1db5-4c02-810e-c243db79efde** i leieren.

    > [!TIP]
    > Denne appen er nødvendig for å koble til Common Data Service- og Finance and Operations-apper. Hvis du har problemer med dette trinnet, åpner du nettleseren i inkognitomodus (i Google Chrome) eller InPrivate-modus (i Microsoft Edge).

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a>Kontroller at firmadata og team med dobbel skriving er riktig konfigurert under kobling

For å sikre at dobbeltskriving fungerer som det skal, opprettes firmaene du velger under konfigurasjonen, i Common Data Service-miljøet. Som standard er disse firmaene skrivebeskyttet, og egenskapen **IsDualWriteEnable** er satt til **Sann**. I tillegg opprettes standard eier av forretningsenheten og teamet og inkluderer firmanavnet. Før du aktiverer tilordningene, må du kontrollere at standard teameier er angitt. Gjør følgende for å finne **Firmaer (CDM\_Firma)**-enheten.

1. Velg filteret øverst til høyre i den modelldrevne appen i Dynamics 365.
2. Velg **Firma** fra rullegardinlisten.
3. Velg **Kjør** for å se resultatene.
4. Velg firmaet som var koblet da du konfigurerte dobbel skriving.
5. Kontroller at feltet **Standard eiende team** har en verdi. I illustrasjonen nedenfor er **Standard eiende team** satt til **USMF Dual Write**.

    ![Kontrollere standard eiende team](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-entities-or-companies-that-can-be-linked-for-dual-write"></a>Finn grensen for antall juridiske enheter eller firmaer som kan kobles til for dobbeltskriving

Du kan få følgende feilmelding når du prøver å aktivere tilordninger:

*Dobbel skriving-feil - Plugin-registrering mislyktes: \[(Kan ikke få partisjonskart for prosjektet DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Feil Overskrider de maksimale partisjonene som er tillatt for tilordning av DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], Det oppstod en eller flere feil.*

Gjeldende grense når du kobler miljøene er omtrent 40 juridiske enheter. Denne feilen oppstår hvis du prøver å aktivere tilordninger, og mer enn 40 juridiske enheter er koblet mellom miljøene.
