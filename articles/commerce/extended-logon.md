---
title: Konfigurere og bruke utvidet påloggingsfunksjonalitet
description: Denne artikkelen beskriver hvordan du konfigurerer og bruker den utvidede påloggingsfunksjonaliteten i Microsoft Dynamics 365 Commerce-salgsstedsappen.
author: boycez
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: boycez
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e27e8d94adccc46559089928b0481442306567ef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884317"
---
# <a name="set-up-and-use-the-extended-logon-capability"></a>Konfigurere og bruke utvidet påloggingsfunksjonalitet

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer og bruker den utvidede påloggingsfunksjonaliteten i Microsoft Dynamics 365 Commerce-salgsstedsappen.

Sky-POS (CPOS) og Magnet POS (MPOS) gir en utvidet påloggingsfunksjonalitet som gjør det mulig for detaljhandelsarbeidere å logge seg på POS-appen ved å skanne en strekkode eller sveipe et kort ved hjelp av en kortleser.

## <a name="set-up-extended-logon"></a>Konfigurere utvidet pålogging

Følg denne fremgangsmåten for å konfigurere utvidet pålogging for POS-kasser i en detaljhandelsbutikk.

1. In Commerce Headquarters går du til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgsstedsprofiler \> Funksjonalitetsprofiler**. 
2. Velg funksjonalitetsprofilen som er knyttet til detaljhandelsbutikken, i den venstre navigasjonsruten.
3. På hurtigfanen **Funksjoner**, under **Flere alternativer for påloggingsgodkjenning** angir du følgende alternativer til **Ja** eller **Nei**, etter behov:

    - **Strekkodepålogging for stab** – Sett dette alternativet til **Ja** hvis du vil at arbeiderne skal logge seg på salgsstedet ved å skanne en strekkode. 
    - **Stabspålogging med strekkode krever passord** – Sett dette alternativet til **Ja** hvis du vil at arbeiderne skal angi et passord når de logger seg på salgsstedet ved å skanne en strekkode.
    - **Kortpålogging for stab** – Sett dette alternativet til **Ja** hvis du vil at arbeiderne skal logge seg på salgsstedet ved å sveipe et kort.
    - **Stabspålogging med kort krever passord** – Sett dette alternativet til **Ja** hvis du vil at arbeiderne skal angi et passord når de logger seg på salgsstedet ved å sveipe et kort.

Strekkoden eller kortet er knyttet til legitimasjon som kan tilordnes en arbeider. Legitimasjonen må ha minst seks tegn. Strengen som inneholder de første fem tegnene, må være unik, og regnes som en *legitimasjons-ID* som brukes til å slå opp en arbeider. Resten av tegnene brukes til sikkerhetsverifisering. Du har for eksempel to kort, ett med legitimasjonen 12345DGYDEYTDW og ett med legitimasjonen 12345EWUTBDAJH. Siden disse to kortene har samme legitimasjons-ID, 12345, kan ikke begge tilordnes arbeidere.

## <a name="assign-extended-logon"></a>Tilordne utvidet pålogging

Som standard kan bare ledere tilordne utvidet pålogging til arbeidere. Hvis du vil tilordne utvidet pålogging, kan du gå til **Utvidet pålogging** i POS. Søk deretter etter en arbeider ved å angi arbeiderens operatør-ID i søkefeltet. Velg arbeideren, og klikk deretter **Tilordne**. Dra eller skann utvidet pålogging for å tilordne arbeideren på neste side. Hvis dra eller skanning blir lest, blir **OK**-knappen tilgjengelig. Klikk **OK** for å lagre den utvidede påloggingen for denne arbeideren.

## <a name="delete-extended-logon"></a>Slett utvidet pålogging

Du kan slette den utvidede påloggingen som er tilordnet til en arbeider, ved å søke etter arbeideren ved hjelp av **Utvidet pålogging** operasjonen. Velg arbeideren, og klikk deretter **Ikke tilordnet**. All utvidet påloggingslegitimasjon som er knyttet til denne arbeider fjernes.

## <a name="use-extended-logon"></a>Bruk utvidet pålogging

Når utvidet pålogging er konfigurert, og en strekkode eller magnetstripe er tilordnet til en arbeider, trenger arbeideren bare å dra eller skanne kortet mens salgsstedets påloggingsside vises. Hvis et passord kreves også før pålogging kan fortsette, blir arbeideren bedt om å angi passordet sitt.

## <a name="extend-extended-logon"></a>Utvid utvidet pålogging

Ut av esken-implementeringen av den utvidede påloggingsfunksjonen krever at legitimasjonen har minst seks tegn, og at de første fem tegnene (legitimasjons-ID-en) er unike. Det var opprinnelig ment som et utvalg som utviklerne kan tilpasse for å oppfylle kravene til en bestemt implementering. (Det kan for eksempel tilpasses for å støtte flere tegn eller bruke forskjellige sikkerhetsverifiseringsregler.) Hvis du vil ha detaljert informasjon om hvordan du bygger utvidelser for utvidet pålogging, kan du se [Utvide den utvidede påloggingsfunksjonen for MPOS og Cloud POS](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/12/14/extending-the-extended-logon-functionality-for-mpos-and-cloud-pos/).

Påloggingstjenesten kan også utvides for å støtte flere utvidede påloggingsenheter, for eksempel håndholdte skannere. Hvis du vil ha mer informasjon, kan du se i [dokumentasjonen for utvidelsesmuligheter for salgssted](dev-itpro/pos-extension/pos-extension-overview.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
