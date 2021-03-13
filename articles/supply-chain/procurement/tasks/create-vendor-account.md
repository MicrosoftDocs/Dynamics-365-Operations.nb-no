---
title: Opprette en leverandørkonto
description: Denne fremgangsmåten viser hvordan du oppretter en leverandørkonto, og legger til en adresse og kontaktinformasjon.
author: RichardLuan
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7f5723fc2aa50fc66c825eb09a01e45833b817e
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022137"
---
# <a name="create-a-vendor-account"></a>Opprette en leverandørkonto

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en leverandørkonto, og legger til en adresse og kontaktinformasjon. Fremgangsmåten viser ikke hvordan du fyller ut alle felt for innkjøp og finansielle formål. Hvis du vil vite mer om disse feltene, kan du lese feltbeskrivelsene. Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Leverandørkontoer opprettes vanligvis av en innkjøpsansvarlig eller kundepersonale.


## <a name="create-a-vendor-account"></a>Opprette en leverandørkonto
1. Gå til **navigasjonsruten > Moduler > Innkjøp og leverandører > Leverandører > Alle leverandører**.
2. Klikk på **Ny**.
3. Angi en verdi i **Leverandørkonto**-feltet.
    - Verdien kan fylles ut automatisk. I så fall kan du hoppe over dette trinnet.  
    - Du kan opprette leverandørkontoer for en person eller organisasjon. Dette påvirker hvilke felt som er tilgjengelig. I dette eksemplet skal vi opprette en leverandørkonto for en organisasjon.   
4. Angi eller velg en verdi i **Navn**-feltet. Hvis leverandøren er en allerede registrert part i systemet, kan du bruke rullegardinlisten og velge dem i dette feltet, og den nye leverandørkontoen arver adresseinformasjonen og kontaktinformasjon som allerede er registrert.
5. Angi eller velg en verdi i **Gruppe**-feltet. Leverandørgruppen brukes til å gruppere leverandører som har én av følgende parametere felles: Betalingsbetingelser, avregn termin, finanskontoer for lagerpostering, inkludert mva-gruppen, standard finanskontoer, produktfilterkoder eller konfigurasjon av forsyningsprognose.
6. Angi et tall i **Antall ansatte**-feltet.
7. Skriv inn en verdi i feltet **Organisasjonsnummer**.

## <a name="add-an-address"></a>Legge til en adresse
1. Vis delen **Adresser**.
2. Klikk på **Legg til**.
3. Angi eller velg en verdi i **Formål**-feltet. Du kan velge ett eller flere formål. Disse brukes til å velge den riktige adressen for en angitt formål. Hvis formålet for eksempel er "Faktura", brukes denne adressen når du sender fakturaer.
4. Skriv inn en verdi i feltet **Navn eller beskrivelse**.
5. Angi eller velg en verdi i **Land/område**-feltet. Angi adressedetaljene. Landet/regionen du valgte, bestemmer feltene som du ser, i henhold til adresseformatet for landet/regionen. 
6. Klikk på **OK**.

## <a name="add-contact-information"></a>Legge til kontaktinformasjon
1. Vis delen **Kontaktinformasjon**.
2. Klikk på **Legg til**.
3. Skriv inn en verdi i **Beskrivelse**-feltet.
4. Velg et alternativ i **Type**-feltet.
5. Angi en verdi i feltet **Kontaktnummer/-adresse**. Du kan merke av for Primær hvis dette er hovedkontakten.  
6. Klikk på **Lagre**.
7. Lukk siden.
8. Lukk siden.

