---
title: Åpne nettadresse på salgssted
description: Denne artikkelen gir en oversikt over forbedringer som har blitt gjort for produkt- og kundesøkfunksjonalitet i Dynamics 365 Commerce.
author: ShalabhjainMSFT
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.custom: 141393
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: ad82cf1039515e58d1717453ee3fb4e3dafd84fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276434"
---
# <a name="open-url-in-pos"></a>Åpne nettadresse på salgssted

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du kan konfigurere en knapp i POS i Dynamics 365 Commerce for å åpne en nettadresse. Denne funksjonen krever ikke tilpasning av koden og kan konfigureres av en person i en ikke-utviklerrolle. 

Denne funksjonen tillater konfigurasjon av en knapp på salgsstedet ved hjelp av knappgruppedesigneren for å åpne en URL-adresse. Dette støttes for øyeblikket i følgende konfigurasjoner:

- Åpne i nytt vindu.
- Åpne på salgssted.
- Åpne i innebygd program.

## <a name="open-in-new-window"></a>Åpne i nytt vindu

Denne konfigurasjonen definerer om du vil åpne URL-adressen i et nytt vindu eller i programmet. Når den konfigureres for å åpne en URL-adresse i programmet, er sidenavigasjonspanelet og den øverste linjen på salgsstedet synlige og tilgjengelige for brukersamhandling. Når den er konfigurert til å åpnes i et nytt vindu, åpnes URL-adressen i et nytt appvindu på Modern POS for Windows og i en ny webleserkategori på alle andre salgsstedsklienter. For å aktivere dette må du konfigurere URL-adressen med **Åpne i nytt vindu**-alternativet valgt.

## <a name="open-within-pos"></a>Åpne på salgssted

Åpning av en URL-adresse på salgsstedet støttes for tiden bare for Modern POS på Windows. På andre klienter er denne funksjonen under utvikling og planlagt for frigivelse i fremtidige oppdateringer. For å aktivere dette må du konfigurere URL-adressen når **Åpne i nytt vindu**-alternativet ikke er valgt.

## <a name="open-a-native-app"></a>Åpne i innebygd program

Med denne funksjonen kan du også angi at ikke-URL-adresser skal åpne et opprinnelig program. Du kan for eksempel angi URL-protokoller, for eksempel MailTo, SIP, IM eller MSTEAMS, som kan behandles av respektive opprinnelige programmer på vertsenheten. For å aktivere dette må du konfigurere URL-adressen med **Åpne i nytt vindu**-alternativet valgt.

- For Windows-datamaskiner kan du se [Eksportere eller importere standard programtilknytninger](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) for å angi standard protokollytilknytninger hvis du setter opp datamaskinen ved å bruke Deployment Image Servicing and Management (DISM).
- Hvis du bruker MDM, for eksempel Intune, til å administrere Windows-datamaskiner, kan du se [Policy for CSP - programstandarder](/windows/client-management/mdm/policy-csp-applicationdefaults).
- Hvis du er en utvikler som bygger et egendefinert webområde, kan du se [Starte standardappen for en URI](/windows/uwp/launch-resume/launch-default-app).

## <a name="open-a-native-app-seamlessly"></a>Åpne i innebygd program sømløst

Windows, iOS og Android tillater også åpning av programmer mer sømløst basert på approtokolltilknytning. Hvis ditt program ikke allerede er konfigurert for å håndtere åpning fra en webleser, må du kanskje få en utvikler til å konfigurere dette.

- For Windows kan du se [Aktivere apper for nettsteder ved hjelp av URI-behandlingsprogrammer](/windows/uwp/launch-resume/web-to-app-linking).
- For iOS kan du se [Universielle koblinger for utviklere](https://developer.apple.com/ios/universal-links/).
- For Android kan du se [Behandle Android-appkoblinger](https://developer.android.com/training/app-links/).

| Kunde                | Åpne i nytt vindu | Åpne innebygd program | Åpne på salgssted | Detaljer                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| Modern POS på Windows | ✓\*                | ✓               | ✓              | \* Åpner i nytt Modern POS-vindu |
| Skybasert salgssted             | ✓\*                | ✓               | X              | \* Åpnes i ny nettleserfane        |
| Modern POS på iOS     | ✓\*                | ✓               | X              | \* Åpnes i ny nettleserfane        |
| Modern POS på Android | ✓\*                | ✓               | X              | \* Åpnes i ny nettleserfane        |

## <a name="before-you-begin"></a>Før du begynner

Før du begynner kan du se hvordan du konfigurerer [Skjermoppsett for salgssted (POS)](pos-screen-layouts.md).

## <a name="open-url-in-pos"></a>Åpne URL-adresse på salgssted

Hvis du vil konfigurere en URL-adresse som skal åpnes i POS, følger du denne fremgangsmåten.

1. På hovedkontoret går du til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgssted \> Skjermoppsett**.
2. Velg **Knappegrupper \> Designer**.
3. Opprett en ny knapp.
4. Velg **Knapp**-egenskaper.
5. Velg **Åpne URL** som handling.
6. Skriv inn URL-en du vil bruke.
7. Konfigurer om du vil åpne URL-adressen i et nytt vindu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
