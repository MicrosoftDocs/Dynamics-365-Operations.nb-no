--- 
title: "Opprette en leverandørkonto"
description: "Denne fremgangsmåten viser hvordan du oppretter en leverandørkonto, og legger til en adresse og kontaktinformasjon."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6ff2357d5266c45be2f403e463c72089d73db21b
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-vendor-account"></a>Opprette en leverandørkonto

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en leverandørkonto, og legger til en adresse og kontaktinformasjon. Fremgangsmåten viser ikke hvordan du fyller ut alle felt for innkjøp og finansielle formål. Hvis du vil vite mer om disse feltene, kan du lese feltbeskrivelsene. Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Leverandørkontoer opprettes vanligvis av en innkjøpsansvarlig eller kundepersonale.


## <a name="create-a-vendor-account"></a>Opprette en leverandørkonto
1. Gå til Innkjøp og leverandører > Leverandører > Alle leverandører.
2. Klikk Ny.
3. Angi en verdi i Leverandørkonto-feltet.
    * Verdien kan fylles ut automatisk. I så fall kan du hoppe over dette trinnet.  
    * Du kan opprette leverandørkontoer for en person eller organisasjon. Dette påvirker hvilke felt som er tilgjengelig. I dette eksemplet skal vi opprette en leverandørkonto for en organisasjon.   
4. Angi eller velg en verdi i Navn-feltet.
    * Hvis leverandøren er en allerede registrert part i systemet, kan du bruke rullegardinlisten og velger dem i dette feltet, og den nye leverandørkontoen arver adresseinformasjonen og kontaktinformasjon som allerede er registrert.  
5. Angi eller velg en verdi i Gruppe-feltet.
    * Leverandørgruppen brukes til å gruppere leverandører som har én av følgende parametere felles: Betalingsbetingelser; avregn termin; finanskontoer for lagerpostering, inkludert mva-gruppen; standard finanskontoer; produktfilterkoder eller konfigurasjon av forsyningsprognose.  
6. Angi et tall i Antall ansatte-feltet.
7. Skriv inn en verdi i feltet Organisasjonsnummer.

## <a name="add-an-address"></a>Legge til en adresse
1. Utvid seksjonen Adresser.
2. Klikk Legg til.
3. Angi eller velg en verdi i Formål-feltet.
    * Du kan velge ett eller flere formål. Disse brukes til å velge den riktige adressen for en angitt formål. Hvis formålet for eksempel er "Faktura", brukes denne adressen når du sender fakturaer.  
4. Skriv inn en verdi i feltet Navn eller beskrivelse.
5. Angi eller velg en verdi i Land/område-feltet.
    * Angi adressedetaljene. Landet/regionen du valgte, bestemmer feltene som du ser, i henhold til adresseformatet for landet/regionen.   
6. Klikk OK.

## <a name="add-contact-information"></a>Legge til kontaktinformasjon
1. Klikk Legg til.
2. Skriv inn en verdi i feltet Beskrivelse.
3. Velg et alternativ i Type-feltet.
4. Angi en verdi i feltet Kontaktnummer/-adresse.
    * Du kan merke av for Primær hvis dette er hovedkontakten.  
5. Klikk Lagre.
6. Lukk siden.
7. Lukk siden.


