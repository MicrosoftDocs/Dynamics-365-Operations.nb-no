---
title: Feilsøke problemer med dobbel skriving-modulen i Finance and Operations-apper
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer med dobbel skriving-modulen i Finance and Operations-apper.
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
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172766"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Feilsøke problemer med dobbel skriving-modulen i Finance and Operations-apper

[!include [banner](../../includes/banner.md)]



Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service. Mer spesifikt gir det informasjon som kan hjelpe deg med å løse problemer med **Dobbel skriving**-modulen i Finance and Operations-apper.

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Du kan ikke laste inn dobbel skriving-modulen i en Finance and Operations-app

Hvis du ikke kan åpne **Dobbel skriving**-siden ved å velge **Dobbel skriving**-flisen i **Databehandling**-arbeidsområdet, er dataintegrasjonstjenesten sannsynligvis nede. Opprett en støtteforespørsel for å be om omstart av dataintegrasjonstjenesten.

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a>Feil når du prøver å opprette en ny enhetstilordning

**Nødvendig legitimasjon for å løse problemet:** Azure AD-leieradministrator

Du kan få følgende feilmelding når du prøver å konfigurere en ny enhet for dobbel skriving:

*Svarstatuskoden indikerer ikke fullført: 401 (uautorisert)*

Denne feilen oppstår fordi bare en Azure AD-leieradministrator kan legge til en ny enhetstilordning.

Du kan løse problemet ved å logge på Finance and Operations-appen som en Azure AD-administratorleier. Du må også gå til web.PowerApps.com og validere tilkoblingen på nytt.

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Feil når du åpner bruker grensesnittet for dobbel skriving

Du kan få følgende feilmelding når du prøver å få tilgang til dobbel skriving fra arbeidsområdet **Databehandling**:

*login.microsoftonline.com kunne ikke koble til.*

Du kan løse problemet ved å logge på ved å bruke et InPrivate-vindu i Microsoft Edge, et inkognito-vindu i Chromium, eller et inkognito-vindu i Google Chrome. Du må også oppheve blokkeringen eller fjerne tredjeparts informasjonskapsler.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>Feil når du kobler miljøet for dobbel skriving eller legger til en ny enhetstilordning

**Nødvendig legitimasjon for å løse problemet:** Azure AD-leieradministrator

Du kan støte på følgende feilmelding når du kobler eller oppretter tilordninger:

*Svarstatuskoden indikerer ikke fullført: 403 (tokenexchange).<br> Økt-ID: \<din økt-id\><br> Rotaktivitet-ID: \<din rotaktivitet-id\>*

Denne feilen kan oppstå hvis du ikke har tilstrekkelige tillatelser til å koble dobbel skriving eller opprette tilordninger. Du må bruke en Azure AD-leieradministratorkonto for å koble miljøer og legge til nye enhetstilordninger. Etter installasjonen kan du imidlertid bruke en ikke-administratorkonto til å overvåke status og redigere tilordningene.

## <a name="error-when-you-stop-the-entity-mapping"></a>Feil når du stopper enhetstilordningen

Du kan få følgende feilmelding når du prøver å stoppe enhetstilordningene:

*\[Forbudt\], \[{"status":403,"kilde":"","melding":"Feil fra token-utveksling: Brukeren har ikke tilgang til tilkoblingen dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Den eksterne serveren returnerte en feil: (403) Forbidden.*

Denne feilen oppstår når det koblede Common Data Service-miljøet ikke er tilgjengelig.

Du kan løse problemet ved å opprette en støtteforespørsel for data integrasjonsgruppen. Knytt til nettverkssporingen slik at dataintegrasjonsgruppen kan merke tilordningene som **Kjører ikke** i serverdelen.
