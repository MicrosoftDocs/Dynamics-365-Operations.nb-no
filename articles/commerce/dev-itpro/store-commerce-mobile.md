---
title: Store Commerce-app for mobilplattformer
description: Denne artikkelen beskriver hvordan du kommer i gang med å bruke Microsoft Dynamics 365 Commerce Store Commerce-appen for Android og iOS.
author: stuharg
ms.date: 10/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2018-10-29
ms.openlocfilehash: 1f07a130629863ebd9d036378436cf360e90ac26
ms.sourcegitcommit: 98231ff810f41f9fcdc6b536d87e453028aa6db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/07/2022
ms.locfileid: "9642343"
---
# <a name="store-commerce-app-for-mobile-platforms"></a>Store Commerce-app for mobilplattformer

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du kommer i gang med å bruke Microsoft Dynamics 365 Commerce Store Commerce-appene for Android og iOS.

Mobilappene Dynamics 365 Commerce for Android og iOS gjør prosessen med å distribuere mobile salgsstedsenheter til detaljhandelsmiljøet enkel. Store Commerce-mobilappene leverer alle funksjoner og fordeler i [Store Commerce-appen for Windows](store-commerce.md) på telefon- og nettbrettformfaktorer. Store Commerce-mobilappene kan installeres direkte fra appbutikkene Apple App Store og Google Play og krever ikke at en utvikler oppretter en ny programpakker for å distribuere eller oppdatere dem. 

Store Commerce-mobilappene har fullstendig funksjonell paritet med nåværende Retail-hybridapper. I tillegg har Store Commerce for iOS støtte for en egen maskinvarestasjon, slik at iOS-enheter kan kommunisere med nettverksbetalingsterminaler, kvitteringsskrivere og kassaskuffer uten å kreve bruk av en felles maskinvarestasjon. 

> [!IMPORTANT]
> Store Commerce-appene for Windows, Android og iOS er neste generasjons salgsstedsprogrammer for Dynamics 365 Commerce. Det nåværende Modern POS-programmet (MPOS) og [Retail-hybridappene](hybridapp.md) for mobil blir avskrevet oktober 2023. Microsoft anbefaler at du bruker Store Commerce eller Cloud POS (CPOS) til alle nye salgsstedsdistribusjoner. Eksisterende kunder bør planlegge å gå over fra Retail-hybridappen til Store Commerce. Hvis du vil ha mer informasjon om avskrivningsplanen for MPOS og Retail-hybridappene, kan du [Moderniser teknologistakken i butikken for Dynamics 365 Commerce](https://www.microsoft.com/download/details.aspx?id=103896). 

## <a name="app-architecture"></a>Apparkitektur

Store Commerce-mobilappene bruker den samme topologien som Store Commerce-appen for Windows når de distribueres i hybridmodus. Store Commerce-mobilappene er skallprogrammer som gjengir CPOS direkte fra Commerce Scale Unit (CSU), og kobles til fjernadministrert handel og Commerce headquarters via CSU. Med skallprogrammodellen kan Store Commerce-apper støtte en egen maskinvarestasjon for direkte integrasjon med en betalingsterminal, en skriver, en kassaskuff og andre eksterne enheter. Du trenger ikke å konfigurere delt maskinvarestasjon for å bruke maskinvareenheter. 

Hvis du vil oppdatere en Store Commerce-mobilapp, kan du bare oppdatere CSU. All ny POS-funksjonalitet plukkes automatisk opp av appen. Hvis du vil ha mer informasjon om hvordan du oppdaterer CSU, kan du se [Bruk oppdateringer og utvidelser i Commerce Scale Unit (sky)](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md).

Skallappene vedlikeholdes gjennom appbutikkoppdateringer. Når en underordnet versjon blir tilgjengelig, publiserer Microsoft den i appbutikkene. Microsoft kan også publisere oppdateringer mellom underordnede versjonsoppdateringer for å frigi reparasjonsfiler med høy prioritet.

## <a name="prerequisites"></a>Forutsetninger

Store Commerce-mobilappene krever Dynamics 365 Commerce, spesielt Commerce headquarters- og CSU-komponentene. Tabellen nedenfor viser minimumsversjonene for operativsystemet (OS) og CSU-versjonene som kreves av Android- og iOS-mobilappene. 

| Forutsetning | Android      | iOS  |
| ------------ | ------------ | ---- |
| OS-versjon   | 7.0          | 15.0 |
| CSU-versjon  | 9.38.22266.8 | Defineres senere  |

## <a name="install-the-app"></a>Installere appen

Du kan installere Store Commerce-mobilapper direkte fra Google Play-butikk eller Apple App Store. 

- [Store Commerce-app for Android](https://aka.ms/storecommerceandroid)
- Store Commerce-app for iOS (snart tilgjengelig)

Pakkene Android-app (.apk) og Apple-app (.ipa) kan også lastes ned fra det delte ressursbiblioteket i Microsoft Dynamics Lifecycle Services. 

## <a name="device-and-register-setup"></a>Enhets- og kasseoppsett

Før en kasse kan aktiveres på Store Commerce-mobilappene, må du definere en enhet og en kasse i Commerce headquarters. Hvis du vil ha mer informasjon, kan du se [Enheter og kasser](../implementation-considerations-devices.md). 

### <a name="device-setup"></a>Enhetsoppsett

Følg denne fremgangsmåten for å opprette og definere en ny enhet.

1. I Commerce Headquarters, går du til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Enheter**. 
1. Opprett en ny enhet, og velg enten forekomsten **Modern POS – Android** eller **Modern POS – iOS** som programtype, avhengig av mobilappen du distribuerer. 

    > [!NOTE] 
    > Programtypene **Modern POS – Android** og **Modern POS – iOS** brukes også til å distribuere nåværende hybridapper for Android og iOS. Etter avskrivningen av MPOS, blir etikettene for disse programtypene oppdatert til **Store Commerce – Android** og **Modern POS – iOS**. 

### <a name="register-setup"></a>Kasseoppsett

Du kan opprette en ny kasse og knytte den til enheten du har opprettet, eller du kan knytte en eksisterende kasse til den nye enheten. Hvis du vil ha mer informasjon om kasser, kan du se [Opprett og tilknytt kasser](../tasks/create-associate-registers.md).

### <a name="screen-layout-setup"></a>Oppsett av skjermoppsett

Hvis du endrer formålet til et skjermoppsett som følger med demodataene som følger med Dynamics 365 Commerce-lisensen, på nytt, velger Store Commerce-appen automatisk det inkluderte skjermoppsettet hvis skjermoppløsningen på enheten er mindre enn 480 &times; 853 piksler i stående retning. Hvis du imidlertid oppretter et skjermoppsett fra bunnen av, eller hvis mobilenheten bruker en større oppløsning enn det kompakte oppsettet støtter, må du sørge for at du oppretter en oppløsning og tilknyttede knapperutenett som passer for telefonen eller nettbrettet du planlegger å distribuere til. Hvis du vil ha mer informasjon om skjermoppsettkonfigurasjoner, kan du se [Visuelle konfigurasjoner av brukergrensesnittet for salgssted](../pos-screen-layouts.md). 

Når enheter og kasser er konfigurert, går du til **Retail og Commerce \> ID for Retail og Commerce \> Distribusjonsplaner** i Commerce headquarters og kjører kassejobben.

## <a name="activate-a-device"></a>Aktiver en enhet

Følg denne fremgangsmåten for å aktivere en enhet i en Store Commerce-mobilapp.

1. Åpne appen på mobilenheten.
1. Angi CPOS-nettadressen, som du finner på siden med miljødetaljer i Lifecycle Services, eller på siden **Kanalprofiler** i Commerce headquarters (**Retail og Commerce \> Kanaloppsett \> Kanalprofiler**).
1. Logg deg på ved å bruke legitimasjonen til en arbeider som har tillatelse til å administrere enheter.
1. Velg butikken som er knyttet til kassen som du opprettet eller gjenbrukte i Commerce headquarters.
1. Velg kassen som du tilknyttet enheten du opprettet i Commerce headquarters.
1. Enheten skal nå aktiveres. Du kan logge deg på kassen ved hjelp av operatør-ID-en og passordet for arbeideren som er tilknyttet butikken du har valgt. 

Hvis du vil ha mer informasjon om enhetsaktivering, kan du se [Aktivering av salgsstedsenhet](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation).

## <a name="feature-parity-with-store-commerce-for-windows"></a>Funksjonsparitet med Store Commerce for Windows

Tabellen nedenfor sammenligner funksjonene for Store Commerce-appen på Windows-, Android- og iOS-plattformene.

| Funksjon                                                                               | Windows | Android | iOS |
| ------------------------------------------------------------------------------------- | ------- | ------- | --- |
| Dedikert maskinvarestasjon                                                            | Ja     | Ja     | Ja |
| Delt maskinvarestasjon                                                               | Ja     | Ja     | Ja |
| Kommunikasjon med eksterne nettverksenheter (betalingsterminal, skriver og kassaskuff) | Ja     | Ja     | Ja |
| Eksterne enheter for OLE for Point of Sale (OPOS) gjennom lokal maskinvarestasjon             | Ja     | Nei      | Nei  |
| Frakoblet modus                                                                          | Ja     | Nei      | Nei  |

## <a name="additional-resources"></a>Tilleggsressurser

[Store Commerce-app](store-commerce.md)

[Velg mellom Store Commerce og Cloud POS](../mpos-or-cpos.md)

[Feilsøk problemer med oppsett og installasjon i Store Commerce](../troubleshoot/store-commerce-setup-installation.md)
