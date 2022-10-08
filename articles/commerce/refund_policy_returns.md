---
title: Opprett og oppdater en retur- og refunderingspolicy for en kanal
description: Denne artikkelen beskriver hvordan du definerer en retur- og refusjonspolicy for en kanal.
author: ShalabhjainMSFT
ms.date: 07/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.custom: ''
ms.search.industry: Retail
ms.openlocfilehash: d01ad490301dd2f4103b8bd3f702db12b93a45a8
ms.sourcegitcommit: bd7b1ffe90b25eb4c68d6aaebd063bf33e09d9cd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/05/2022
ms.locfileid: "9627503"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Opprette og oppdatere en retur- og refunderingspolicy for en kanal

[!include [banner](includes/banner.md)]

Kanalreturpolicyen i Dynamics 365 Commerce gjør det mulig for forhandlere å angi håndhevelser der betalingsmidler kan tillates for å behandle en retur på en salgsstedsenhet (POS).  

Denne artikkelen beskriver trinnene for å definere en retur- og refusjonspolicy for en kanal.

Omfanget av policyen er for øyeblikket begrenset til å angi betalingsmidlene som kan være tillatt for en kanal. "Tillatt"-listen er basert på betalingsmåtene som ble brukt til å utføre innkjøpet. For eksempel:

- Hvis et innkjøp ble foretatt ved hjelp av et gavekort, er butikkpolicyen å bare behandle refusjoner til et nytt gavekort eller gi butikkreditt. 
- Hvis et salg er produsert ved hjelp av kontanter, er alternativene som er tillatt for refusjon, kontanter, gavekort og kundekonto, men ikke kredittkort. 

## <a name="enable-return-policy"></a>Aktivere returpolicy

Denne funksjonen aktivert som standard. Du finner det i arbeidsområdet **Funksjonsbehandling** ved å søke etter **Aktiver returpolicyer for kanal** i listen over funksjonsnavn.


## <a name="configure-return-policy"></a>Konfigurere returpolicy

Følg denne fremgangsmåten for å konfigurere en returpolicy for en detaljhandelsbutikk eller en detaljhandelskanal på nettet.

1. Gå til **Retail og Commerce** \> **Kanaloppsett** \> **Returner** \> **Kanalreturpolicy**.

1. Velg **Ny** for å opprette en ny returpolicymal. Hvis du vil bruke en eksisterende mal, velger du malen i den venstre ruten. For nye maler legger du til et navn og en beskrivelse som gjør det enklere å identifisere policyen når den brukes i kanalen.

   ![Legg til ny returpolicy.](media/Return-policy-page1.png)
     
   
1. I delen **Tillatte betalingsmåter for refusjoner** definerer du **Tillatte** returbetalingsmidler som er spesifikke for hver betalingsmåte.
   ![Angi tillatte betalingsmåter per betalingstype.](media/Return-policy-page2.png)
   
    > [!IMPORTANT]
    > - Betalingsmåtene er avledet fra betalingsmåtene som er angitt for organisasjonen.
    > - Hvis du legger til en tillatt returbetalingstype for hver oppførte betalingsmåte, må du sørge for at returer kan gjøres til den tillatte returbetalingstypen.
    
1. Knytt returpolicymalen til butikkene der den skal brukes. Velg **Legg til** i kategorien **Detaljhandelskanaler**, og knytt til de tilgjengelige kanalene. 

    - I dialogboksen **Velg organisasjonsnoder** velger du butikkene, områdene og organisasjonene som malen skal knyttes til.
    - Bare én returpolicymal kan knyttes til hver butikk.
    - Bruk pilknappene til å velge butikker, områder eller organisasjoner.
    - Ikrafttredelsesdatoen på policyen vil være datoen da policyene brukes på kanalene og kanaljobbene kjøres. 

    ![Dialogboksen Velg organisasjonsnoder.](media/Return-policy-page3.png)

1. På siden **Distribusjonsplan** kjører du jobben **1070** for å vise at kanalreturpolicyen er tilgjengelig for salgsstedet.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>Forhåndsvise kanalreturpolicyen på salgsstedet

Følg trinnene i et av følgende eksempler for å vise de tillatte returbetalingsmidlene på salgsstedet.

1. Logg deg på salgsstedet som en kasserer eller en leder.
1. Under **Skift og skuff** velger du **Vis Journal**.
1. Velg transaksjonen som er del av returen. 
1. Velg varene som skal refunderes, og velg deretter betalingsmåten.  
    - Hvis valgt betalingsmiddelet er i listen over tillatte returbetalingstyper, kan kassereren fullføre transaksjonen.
    - Hvis det valgte betalingsmiddelet ikke er tillatt, vises en feilmelding.
    - Velg **Beløp å betale** for å vise en liste over alle tillatte returbetalingstyper.

- eller -

1. Logg deg på salgsstedet som en kasserer eller en leder.
1. Velg **Returtransaksjon**, og angi kvitterings-ID-en ved hjelp av strekkodeskanning eller manuell oppføring. 
1. Velg transaksjonen som er del av returen. 
1. Velg varene som skal refunderes, og velg deretter betalingsmåten.  
    - Hvis valgt betalingsmiddelet er i listen over tillatte returbetalingstyper, kan kassereren fullføre transaksjonen.
    - Hvis det valgte betalingsmiddelet ikke er tillatt, vises en feilmelding.
    - Velg **Beløp å betale** for å vise en liste over alle tillatte returbetalingstyper.

![Refusjonstype ikke tillatt.](media/Return-policy-page6.png)



![Refusjonstyper tillatt.](media/Return-policy-page5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
