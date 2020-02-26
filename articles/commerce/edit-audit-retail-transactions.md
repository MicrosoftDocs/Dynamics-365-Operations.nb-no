---
title: Redigere og overvåke detaljhandelstransaksjoner
description: Dette emnet beskriver funksjonaliteten for redigering og overvåking av butikktransaksjoner.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 97211ee36dbaa704d3a967e9b742ff1cae708707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004395"
---
# <a name="edit-and-audit-retail-store-transactions"></a>Redigere og overvåke detaljhandelstransaksjoner

[!include [banner](includes/banner.md)]



Dynamics 365 Commerce-kunder bruker både første- og tredjeparts salgsstedsprogrammer (POS). Med det førsteparts salgsstedsprogrammet blir butikktransaksjoner hentet til Headquarters fra kanalene fra en satsvis prosess. Med tredjeparts programmer trekkes transaksjoner inn i Headquarters via integrering. Når transaksjoner trekkes inn i Headquarters i begge tilfeller, må det utføres en konsekvenskontroll som kjører flere valideringer på transaksjonene, slik at bare godkjente transaksjoner blir trukket over til utdraget som skal posteres i Headquarters. 

Commerce-transaksjoner består ikke validering av flere årsaker. En feil i integreringskoden eller en feil i salgsstedsprogrammet kan for eksempel forårsake inkonsekvente data eller en bruker feil, for eksempel å slette et produkt etter at den ble synkronisert til kanalen eller lukke en regnskapsperiode uten å postere transaksjoner for den perioden, kan det føre til inkonsekvente data.

Selv om disse transaksjonene blir flagget og utelatt fra utdragene, kan transaksjonene forstyrre en kundens daglige prosess med å postere daglige salg til finans.

I Commerce kan du redigere de bestemte transaksjonene som ikke kan valideres, samtidig som du reviderer alle endringene. 

## <a name="edit-and-audit-transactions"></a>Redigere og overvåke transaksjoner

I Retail versjon 10.0.5 er hentesalgstransaksjoner, for eksempel salg og returer, de eneste transaksjonene som kan redigeres. Redigering av kundeordrer eller elektroniske ordrer støttes ikke. I Retail versjon 10.0.6 og høyere støttes også redigeringen av kontantstyringstransaksjoner.

1. Installer Dynamics Excel-tillegget.

2. Gå til arbeidsområdet **Finans for handelsbutikk**. Flisen **Transaksjonsvalideringsfeil** inneholder en forhåndsfiltrert visning av skjemaet for transaksjonen som mislyktes med én eller flere av valideringsreglene.
 
3. Åpne skjemaet. Klikk posten som ikke ble validert, klikk **Office-tillegg**, og klikk deretter **Rediger valgt transaksjon**. En Excel-fil med detaljer om den valgte transaksjonen åpnes, med følgende regneark:

    - Linjer: Dette regnearket har hode- og produktlinjer og relaterte data for transaksjonen.
    - Betalinger: Dette regnearket har detaljene for betalingslinjene for transaksjonen.
    - Rabatter: Dette forslaget har rabattrelaterte detaljer for transaksjonen.
    - Avgifter: Dette forslaget har avgiftsrelaterte detaljer for transaksjonen.
    - Gebyrer: Dette forslaget har gebyrrelaterte data for transaksjonen.

4. I Excel-filen endrer du de aktuelle feltene, og deretter laster du opp dataene tilbake i Headquarters ved hjelp av publiseringsfunksjonen i Dynamics Excel-tillegget. Når de er publisert, vil endringene gjenspeiles i systemet. Under publisering utføres ingen validering av endringer som brukerne gjør.

5. Du kan vise et fullstendig revisjonsspor for endringene ved å klikke **Vis revisjonsspor** i hodet for **Detaljhandelstransaksjon** for endringer i hodenivå og i den relevante delen og posten på den riktige transaksjonssiden. Alle endringer som er relatert til salgslinjer, vil for eksempel være synlige på siden **Salgstransaksjoner**, endringer som er knyttet til betalinger, vil være synlige på siden **Betalingstransaksjoner** osv. Revisjonsdetaljene som opprettholdes for endringene, er som følger:

   - Endringsdato og -klokkeslett
   - Felt 
   - Gammel verdi
   - Ny verdi
   - Endret av

6. Når endringene er gjort og publisert, må du kjøre alternativet **Valider butikktransaksjoner** på nytt for å validere at endringene du gjorde er konsekvente og gyldige.

> [!NOTE]
> Du kan bare redigere transaksjoner som ikke ble validert. Hvis du vil redigere transaksjoner som har bestått valideringen, endrer du valideringsstatusen til transaksjonen du vil endre til **Feil** eller **Ingen**, og deretter kan du redigere den. 


## <a name="bulk-edit-transactions"></a>Masseredigere transaksjoner

I Retail versjon 10.0.6 og senere støttes alternativet for masseredigering på utdragsnivå. 

1. Bruk Excel-tillegget til å åpne en oppgave som har transaksjoner du vil endre, ved hjelp av trinn 1-3 ovenfor.

2. Velg ett av alternativene nedenfor.

    - **Redigere hentesalgstransaksjoner**. Med dette alternativet kan du redigere alle hentesalgstransaksjonene som er inkludert i utdraget. Følgende Excel-regneark er tilgjengelige.
    
       - **Transaksjon**: Dette regnearket inneholder all informasjon på hodenivå for salgstransaksjonene.
       - **Salgstransaksjon**: Dette regnearket inneholder all informasjon på linjenivå for salgstransaksjonene.
       - **Betalingstransaksjoner**: Dette regnearket inneholder all informasjonen for betalingslinjer for salgstransaksjonene.
       - **Rabattransaksjoner**: Dette regnearket inneholder all informasjonen for rabattlinjer for salgstransaksjonene.
       - **Avgiftstransaksjon**: Dette regnearket inneholder all informasjonen på avgiftslinjer for salgstransaksjonene.
       - **Gebyrtransaksjoner**: Dette regnearket inneholder all informasjonen for gebyrlinjer for salgstransaksjonene.

    - **Redigere kassastyringstransaksjoner**. Med dette alternativet kan du redigere alle kassastyringstransaksjonene som er inkludert i utdraget. Følgende Excel-regneark er tilgjengelige.
     
       - **Transaksjon**: Dette regnearket inneholder all informasjon på hodenivå for kassastyringstransaksjonene.
       - **Betalingsmiddeltransaksjoner til bank**: Dette regnearket inneholder alle detaljene for bankdeponeringstransaksjon.
       - **Betalingsmiddeltransaksjoner til safe**: Dette regnearket inneholder alle detaljene for safedeponeringstransaksjon.
       - **Kasseoppgjør**: Dette regnearket inneholder alle detaljene for kasseoppgjørstransaksjon.
       - **Inntekts-/utgiftstransaksjon**: Dette regnearket inneholder alle detaljene for linje på inntekts-/utgiftstransaksjon.
       - **Betalingstransaksjoner**: Dette regnearket har all betalingsrelatert informasjon for operasjonen **Betal faktura**, i tillegg til inntekts-/utgiftstransaksjonen.

3.  Valideringer utføres ikke når du publiserer masseredigerte transaksjoner. Du må forsikre deg om at alle redigeringer er nøyaktige, og at data i gjengivelsen på regnearkene beholdes. Hvis du for eksempel vil endre transaksjonsdatoen for å administrere scenariene der regnskaps -eller lagerperioden for de åpne transaksjonene er lukket, må du endre datoen i alle Excel-regneark som har kolonnen **Forretningsdato**. Hvis du vil validere transaksjoner etter at de er redigert, kan du bruke **Valider transaksjoner på nytt** på **Utdrag**-siden.
