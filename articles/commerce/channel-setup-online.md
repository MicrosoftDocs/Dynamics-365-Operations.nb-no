---
title: Konfigurere en nettkanal
description: Dette emnet beskriver hvordan du oppretter en ny Internett-kanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b6bf158361f95b6551b29f195616cf21f908b802
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800645"
---
# <a name="set-up-an-online-channel"></a>Konfigurere en nettkanal


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du oppretter en ny Internett-kanal i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Dynamics 365 Commerce støtter flere kanaler for detaljhandel. Disse detaljhandelskanalene omfatter nettbutikker, telefonsentre og detaljhandelsbutikker (også kalt fysiske butikker). Med en nettbutikk kan kundene kjøpe produkter i forhandlerens nettbutikk i tillegg til den vanlige butikken.

Hvis du vil opprette en nettbutikk i Commerce, må du først opprette en Internett-kanal. Før du oppretter en ny Internett-kanal, må du kontrollere at du har oppfylt [Forutsetninger for kanaloppsett](channels-prerequisites.md).

Før du kan opprette et nytt område må du opprette minst én nettbutikk i Commerce. Hvis du vil ha mer informasjon, kan du se [Opprette et e-handelsområde](create-ecommerce-site.md).

## <a name="create-and-configure-a-new-online-channel"></a>Opprette og konfigurere en ny Internett-kanal

Hvis du vil opprette og konfigurere en ny Internett-kanal, gjør du følgende:

1. I navigasjonsruten går du til **Moduler \> Kanaler \> Nettbutikker**.
1. I handlingsruten velger du **Ny**.
1. I **Navn**-feltet oppgir du et navn for den nye kanalen.
1. Angi den riktige juridiske enheten i rullegardinlisten **Juridisk enhet**.
1. Angi det riktige lageret i rullegardinlisten **Lager**.
1. Velg riktig tidssone i feltet **Tidssone for butikk**.
1. Velg riktig valuta i **Valuta**-feltet.
1. Angi en gyldig standardkunde i feltet **Standardkunde**.
1. Angi en gyldig adressebok i feltet **Adressebok for kunde**.
1. I feltet **Funksjonalitetsprofil** velger du en funksjonalitetsprofil hvis det er aktuelt.
1. I feltet **Profil for e-postvarsling** oppgir du en gyldig profil for e-postvarsling.
1. Velg **Lagre** i handlingsruten.

Bildet nedenfor viser opprettelsen av en ny Internett-kanal.

![Ny Internett-kanal](media/channel-setup-online-1.png)

Bildet nedenfor viser et eksempel på en Internett-kanal.

![Eksempel på Internett-kanal](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a>Definere språk

Hvis området for e-handel støtter flere språk, kan du utvide delen **Språk** og legge til flere språk etter behov.

## <a name="set-up-payment-account"></a>Definere betalingskonto

I delen **Betalingskonto** kan du legge til en tredjeparts betalingsleverandør. Hvis du vil ha informasjon om hvordan du definerer en Adyen-betalingskobling, kan du se [Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md).

## <a name="additional-channel-setup"></a>Ekstra kanaloppsett

Andre oppgaver som kreves for oppsett av Internett-kanal, omfatter definere betalingsmåter, leveringsmåter og gruppetilordning for oppfyllelse.

Bildet nedenfor viser oppsettsalternativene **Leveringsmåter**, **Betalingsmåter** og **Gruppetilordning for oppfyllelse** i kategorien **Oppsett**.

![Ekstra konfigurasjonshandlinger for Internett-kanal](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a>Definere betalingsmåter

Hvis du vil definere betalingsmåter, følger du disse trinnene for hver betalingstype som støttes på denne kanalen.

1. I handlingsruten velger du kategorien **Oppsett** og deretter **Betalingsmåter**.
1. I handlingsruten velger du **Ny**.
1. Velg en ønsket betalingsmåte i navigasjonsruten.
1. I delen **Generelt** angir du et **operasjonsnavn** og konfigurerer eventuelle andre ønskede innstillinger.
1. Konfigurer eventuelle tilleggsinnstillinger som kreves for betalingstypen.
1. Velg **Lagre** i handlingsruten.

Bildet nedenfor viser et eksempel på en kontantbetalingsmåte.

![Eksempel på betalingsmåter](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Definer leveringsmåter

Du kan se de konfigurerte leveringsmåtene ved å velge **Leveringsmåter** fra kategorien **Oppsett** i **handlingsruten**.  

Hvis du vil endre eller legge til en leveringsmåte, følger du disse trinnene.

1. I navigasjonsruten går du til **Moduler \> Lagerstyring \> Leveringsmåter**.
1. Velg **Ny** i handlingsruten for å opprette en ny leveringsmåte, eller velg en eksisterende måte.
1. I delen **Detaljhandelskanaler** velger du **Legg til linje** for å legge til kanalen. Legge til kanaler ved hjelp av organisasjonsnoder i stedet for å legge til hver kanal for seg, kan effektivisere tillegg av kanaler

Bildet nedenfor viser et eksempel på en leveringsmåte.

![Definer leveringsmåter](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a>Definere en gruppetilordning for oppfyllelse

Hvis du vil konfigurere en gruppetilordning for oppfyllelse, gjør du følgende.

1. I handlingsruten velger du kategorien **Oppsett** og deretter **Gruppetilordning for oppfyllelse**.
1. I handlingsruten velger du **Ny**.
1. I rullegardinlisten **Oppfyllelsesgruppe** velger du en oppfyllelsesgruppe.
1. Angi en beskrivelse i rullegardinlisten **Beskrivelse**.
1. Velg **Lagre** i handlingsruten.

Det følgende bildet viser et eksempel på et oppsett for gruppetilordning for oppfyllelse.

![Definere gruppetilordning for oppfyllelse](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over kanaler](channels-overview.md)

[Forutsetninger for kanaloppsett](channels-prerequisites.md)

[Definere en detaljhandelskanal](channel-setup-retail.md)

[Definere en telefonsenterkanal](channel-setup-callcenter.md)

[Dynamics 365 Payment Connector for Adyen](../retail/dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]