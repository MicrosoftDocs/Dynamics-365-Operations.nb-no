--- 
title: "Opprette en tilbudsforespørsel"
description: "Denne fremgangsmåten viser hvordan du oppretter en tilbudsforespørsel."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: df6d8620316cf0dcde457b06235d9e041a51e100
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-request-for-quotation"></a>Opprette en tilbudsforespørsel

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en tilbudsforespørsel. Dette gjøres vanligvis av en innkjøpsagent. Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Du må ha definert forespørselstyper før du starter. Når du har fullført denne oppgaven og du har opprettet og sendt en tilbudsforespørsel, kan du deretter angi svarene per leverandør, sammenligne dem og gi dem kontrakten.


## <a name="prepare-a-new-rfq"></a>Klargjøre en ny tilbudsforespørsel
1. Gå til Innkjøp og leverandører > Tilbudsforespørsler > Alle tilbudsforespørsler.
2. Klikk Ny.
    * Følgende innkjøpstyper er tilgjengelige: Bestilling (dette er standard): et dokument som bekrefter tilbudet om å kjøpe produkter eller godkjenning av et tilbud om å selge produkter i bytte mot betaling. Bestilling: typen velges automatisk hvis du oppretter en tilbudsforespørsel direkte fra en innkjøpsrekvisisjon. Hvis du manuelt velger dette alternativet, får du en feilmelding. Kjøpsavtale: En avtale om å kjøpe et spesifikt antall eller en verdi av et produkt over tid. Hvis du velger dette alternativet, må du velge datointervallet som gjelder for kjøpsavtalen.  
3. Skriv inn en verdi i Dokumenttittel-feltet.
4. Angi eller velg en verdi i Forespørselstype-feltet.
    * Hvis en poengberegningsmetode er knyttet til forespørselstypen, blir dette standarden for poengberegningsmetoden for tilbudsforespørselen du oppretter. Du kan endre poengberegningsmetoden senere.  
    * Angi en dato i Leveringsdato-feltet.  
    * Velg datoen du vil motta varene innen.  
    * Angi dato og klokkeslett i feltet Utløpsdato- og klokkeslett.  
    * Angi datoen og klokkeslettet leverandører må svare på tilbudsforespørselen innen.  
5. Angi eller velg en verdi i feltet Lager.
    * Lageradresse er standard leveringsadresse.  
6. Klikk OK.

## <a name="add-lines"></a>Legg til linjer
    * Når du har angitt den grunnleggende informasjonen om tilbudsforespørselen din, kan du angi varene eller tjenestene du vil at leverandører skal byr på. Varen er standard linjetype.   
1. Angi eller velg en verdi i Varenummer-feltet.
    * Hvis du bruker USMF, kan du velge T0020.  
2. Angi et tall i feltet Antall.
3. Klikk Legg til linje.
4. Velg Kategori i Linjetype-feltet.
    * Du kan bruke kategorilinjetypen til å opprette tilbudsforespørsler for ikke-lagervarer eller tjenester. Deretter må du velge typer varer eller tjenester fra et hierarki av innkjøpskategorier.  
5. Angi eller velg en verdi i feltet Innkjøpskategori.
6. Skriv inn en verdi i feltet Produktnavn.
7. Angi et tall i feltet Antall.
8. Angi eller velg en verdi i Enhet-feltet.

## <a name="add-vendors"></a>Legg til leverandører
1. Klikk overskriften for å endre fra visningen Linjer til overskriftsvisningen. 
2. Utvid delen Leverandør.
3. Klikk Legg til leverandører automatisk.
    * Du kan legge til leverandører i tilbudsforespørselen automatisk, basert på innkjøpskategorien for de forespurte varene. Hvis ingen leverandører er godkjent for kategoriene som er inkludert i linjene, kan du legge til leverandører manuelt.  
4. Klikk Legg til.
5. Angi eller velg en verdi i Leverandørkonto-feltet.
6. Klikk Legg til.
7. Angi eller velg en verdi i Leverandørkonto-feltet.
    * Når du har valgt en leverandør, blir statusen opprettet. Dette betyr at leverandørinformasjonen er lagret i tilbudsforespørselen, men at du ikke har sendt tilbudsforespørselen til leverandøren. Du kan legge til en leverandør i en tilbudsforespørsel uansett leverandørstatus.  

## <a name="send-the-rfq-to-vendors"></a>Sende tilbudsforespørselen til leverandører
1. Klikk Send.
    * På siden Sender tilbudsforespørsel kontrollerer du at leverandørene i listen er de du vil skal motta tilbudsforespørselen.  
2. Klikk Skriv ut.
    * Denne dialogboksen lar deg skrive ut tilbudsforespørselen. Hvis du velger å skrive ut et svararket, defineres innholdet i dette i Innkjøp og leverandører-parametere. Hvis du vil velge hvordan du skriver ut svarark når du har åpnet dialogboksen Skriv, klikker du Avanserte utskriftsalternativer. Én tilbudsforespørsel skrives ut for hver leverandør, som inneholder linjene har statusen Opprettet eller Sendt. Annullerte linjer og linjer med registrerte svar, vil ikke bli skrevet ut.   
3. Klikk Avbryt.
4. Klikk OK.
5. Lukk siden.
6. Lukk siden.

## <a name="view-the-rfq-journal"></a>Vise tilbudsforespørseljournalen
1. Gå til Innkjøp og leverandører > Tilbudsforespørsler > Oppfølging av tilbudsforespørsler > Tilbudsforespørseljournaler.
2. Klikk Forhåndsvis/Skriv ut.
3. Klikk Forhåndsvis original.
4. Lukk siden.
5. Lukk siden.

