---
title: Parametere i Aktivastyring
description: I Aktivastyring må generelle parametere knyttet til aktiva, arbeidsordrer og arbeidsordreplanlegging defineres.
author: johanhoffmann
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 750776412ce9d87389a635ef108a34cffe12b68b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015819"
---
# <a name="asset-management-parameters"></a>Parametere i Aktivastyring

[!include [banner](../../includes/banner.md)]

I Aktivastyring må generelle parametere knyttet til aktiva, arbeidsordrer og arbeidsordreplanlegging defineres. Denne artikkelen forklarer hvordan du definerer dem. Velg **Aktivastyring** > **Oppsett** > **Parametere i Aktivastyring** for å åpne siden.

> [!NOTE]
> Hvis du vil konfigurere et system som inneholder demonstrasjonsdata for testing av funksjonene for ressursstyring, kan du se [Distribuere et demomiljø](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) for instruksjoner.

## <a name="the-assets-tab"></a>Aktiva-fanen

**Aktiva**-fanen har følgende innstillinger:

- **Standard funksjonslokasjon** velges automatisk for aktiva når du oppretter nye aktiva.  
- I feltet **Standardkalender** velger du en kalender som skal brukes til å beregne KPI-er for aktiva, hvis ingen ressurser er valgt for et aktivum.  
- I **Vis**-feltet velger du standardvisningen som vises når du åpner **Aktivavisning** (**Aktivastyring** > **Aktiva** > **Aktivavisning**).
- **Standard forespørselstype** er standard meldingstype, som velges automatisk når du oppretter en ny forespørsel.  
- Prognoser på jobbtyper lagres i prosjektet som er valgt i feltet **Prosjektprognose**. For hver jobbtype opprettes det automatisk en ny aktivitet i prognoseprosjektet. Prognoser for jobbtypen blir deretter lagret i prognoseprosjektet.  
- I **Modell**-feltet velger du prognosemodellen som brukes på jobbtypen-og arbeidsordreprognosene.

## <a name="the-work-orders-tab"></a>Arbeidsordrer-fanen

**Arbeidsordrer**-fanen har følgende innstillinger:

- **Standard arbeidsordretype** definerer standardinnstillinger når du oppretter en arbeidsordre.  
- **Preventiv arbeidsordretype** definerer arbeidsordretypen som brukes når du oppretter arbeidsordrer fra vedlikeholdsplaner. Hvis dette feltet er tomt, brukes arbeidsordretypen **Standard arbeidsordretype**.  
- I feltet **Relatert arbeidsordremaske** definerer du det maksimale antallet arbeidsordrer som kan være relatert til en arbeidsordre. Eksempel: ## lar deg ha opptil 99 arbeidsordrer relatert. Hvis du definerer en maske som beskrevet her, blir relaterte arbeidsordrer nummerert [arbeidsordre-ID for arbeidsordren som en arbeidsordre er relatert til]-01, -02, -03 og så videre. Hvis du ikke definerer en maske i dette feltet, vil en tilknyttet arbeidsordre få neste sekvensielle arbeidsordre-ID.  
- Velg **Ja** for **Kopier feil** hvis du vil kopiere feil som er registrert på meldinger, til relaterte arbeidsordrer automatisk. 
- I **Nivå**-feltet definerer du funksjonslokasjonsnivået som settes inn automatisk i en arbeidsordre hvis alle relaterte arbeidsordrejobber refererer til samme funksjonslokasjon. Hvis arbeidsordrejobbene ikke alle er knyttet til den samme funksjonslokasjonen på det definerte nivået, forblir feltet **Funksjonslokasjon** tomt på arbeidsordren. Eksempel: Hvis du setter inn tallet "1" i dette feltet, er dette det øverste nivået i en funksjonslokasjonsdstruktur. Hvis du setter inn tallet "0" i dette feltet, har du ikke definert et bestemt funksjonslokasjonsnivå, bare at alle arbeidsordrejobber i en arbeidsordre må være knyttet til det samme funksjonslokasjonen for at funksjonslokasjonen skal legges til i arbeidsordren.  
- Journaler som brukes ved postering av forbruk på en arbeidsordre, kan velges på hurtigfanen **Generelt** i feltene **Time**, **Vare** og **Utgift**.  
- I feltet **Språkkilde for produkt** velger du hvilket språk som skal brukes for produktnavn i rapporter i Aktivastyring. Du kan velge språket som er definert for firmakontoen, eller språket som er angitt for brukeren som er logget på.  
- Velg **Ja** for **Oppdatering i sanntid** hvis du vil automatisk oppdatere endringer i jobbtypestandarder, vedlikeholdsplaner og vedlikeholdsrunder.
  - Hvis du velger **Nei**, blir endringer i jobbtypestandarder, vedlikeholdsplaner og vedlikeholdsrunder ikke oppdatert automatisk i Aktivastyring.
  - Velg **Nei** hvis du har store datamengder som synkroniseres, for eksempel mange ressurser eller funksjonslokasjoner som er satt opp på vedlikeholdsplaner eller vedlikeholdsrunder, eller et stort antall vedlikeholdsplaner eller runder.  
  - Hvis du endrer jobbtypestandarder eller vedlikeholdsplaner eller vedlikeholdsrunder, og du har valgt **Nei** til sanntidsoppdatering, kan det hende at det ikke vises en advarsel hvis endringene påvirker:
    - Funksjonslokasjoner som er satt opp på vedlikeholdsplaner eller runder  
    - Objekter som er satt opp på vedlikeholdsplaner eller runder  
    - Oppsett av vedlikeholdsplaner  
    - Oppsett av vedlikeholdsrunder  
- På hurtigfanen **Kategori** kan standardkategorier knyttet til forbruk på arbeidsordrer defineres.  

## <a name="the-work-order-scheduling-tab"></a>Fanen Planlegging av arbeidsordre

Fanen **Planlegging av arbeidsordre** gir følgende innstillinger i hurtigfanen **Generelt**:

- **Tidsplanhorisont** definerer perioden i dager, beregnet fra den forventede startdatoen for arbeidsordren, der arbeidsordrejobber planlegges.  
- **Hovedplanen** gjelder ressurser i modulen **Organisasjonsadministrasjon**. Hvis du velger en hovedplan i dette feltet, vil du kunne se kapasitetsreservasjoner som er knyttet til arbeidsordrer i **Kapasitetsreservasjoner** (**Organisasjonsadministrasjon** > **Ressurser** > **Ressurser** > velg ressurs > **Ressurs**-fanen > **Kapasitetsreservasjoner**-knappen). Hvis du lar dette feltet stå tomt, kan du se kapasitetsbelastningen relatert til arbeidsordrer i **Kapasitetsbelastning** (**Organisasjonsadministrasjon** \> **Ressurser** \> **Ressurser** \> velg ressurs \> **Ressurs**-fanen \> **Kapasitetsbelastning**-knappen).  

>[!NOTE]
>Valget angående bruk av en hovedplan i modulen **Aktivastyring** og det tilknyttede skjemaet som brukes til å få en oversikt over kapasitetsreservasjoner eller kapasitetsbelastning, er standard oppsett. Avhengig av oppsettet i feltet **Hovedplan** kan du få tilgang til kapasitetsinformasjon i **Kapasitetsreservasjoner** eller **Kapasitetsbelastning** i modulen **Organisasjonsstyring**. Det er ikke mulig å opprette et oppsett der kapasitetsreservasjoner vises i begge visningene.  

Feltene som er beskrevet i listen nedenfor, er knyttet til beregnede vurderingsresultater, som brukes til å beregne arbeidsordreprioritet under planlegging av arbeidsordrer.

- **Prioritet** – En vurderingspoengsum beregnet sammen med resultatpoengsummen i feltene **Kritikalitet** og **Startdato**. Tallet i dette feltet deles på tallet i **Prioritet**-feltet i en arbeidsordre. Hvis for eksempel verdien "5,00" er satt inn i dette feltet, og en arbeidsordre har prioritet "20", er klassifiseringspoengsummen for prioritet 0,25.  
- **Kritikalitet** – En vurderingspoengsum beregnet sammen med resultatpoengsummen i feltene **Prioritet** og **Startdato**. Tallet i dette feltet ganges med tallet i **Kritikalitet**-feltet i en arbeidsordre. Hvis for eksempel verdien "10,00" er satt inn i dette feltet, og en arbeidsordre har kritikalitet "5", er klassifiseringspoengsummen for kritikalitet 50.  
- **Startdato** – En vurderingspoengsum beregnet sammen med resultatpoengsummen i feltene **Prioritet** og **Kritikalitet**. Dette feltet angir daglig poengsum som en negativ verdi, og sammenlignes med **Forventet start**-feltet i en Arbeidsordre. Hvis for eksempel verdien "10,00" settes inn i dette feltet, og den forventede startdatoen for en arbeidsordre er tre dager fra nå, er klassifiseringsresultatet minus 30,00. Ved å legge til resultatene 0,25 og 50 fra eksemplene i feltene **Prioritet** og **Kritikalitet** som er beskrevet ovenfor, får du totalt pluss 20,25. Dette nummeret sammenlignes med alle andre vurderingsresultater for arbeidsordre under planlegging av arbeidsordrer, og de høyeste vurderingsresultatene planlegges deretter først.  
- **Ansvarlig arbeider** – En vurderingspoengsum beregnet sammen med verdiene for **Ansvarlig arbeidergruppe**, **Foretrukket arbeider**, **Foretrukket arbeidergruppe**, **Aktivasted** og **Startdate**. Hvis verdien "50,00" settes inn i dette feltet, og en ansvarlig arbeider er valgt i en arbeidsordre, får arbeideren 50 poeng i den totale beregningen av arbeideren under planlegging av arbeidsordren.  
- **Ansvarlig arbeidergruppe** – En vurderingspoengsum beregnet sammen med verdiene for **Ansvarlig arbeider**, **Foretrukket arbeider**, **Foretrukket arbeidergruppe**, **Aktivasted** og **Startdato**. Hvis verdien "50,00" settes inn i dette feltet, og en ansvarlig arbeider er valgt i en arbeidsordre, får arbeideren 50 poeng i den totale beregningen av arbeideren under planlegging av arbeidsordren.  
- **Begrens til ansvarlig** – Dette begrenser antall arbeidere som er tilgjengelige for planlegging av arbeidsordrer. Velg **Nei** hvis du vil beregne en poengsum for alle ansatte, uansett om de er definert som ansvarlige arbeidere eller deler av en ansvarlig arbeider gruppe. Velg **Ja** hvis du vil beregne en poengsum for arbeidere som er definert som ansvarlig arbeider på arbeidsordren, og/eller som er inkludert i en ansvarlig arbeider gruppe som er valgt i arbeidsordren.  
- **Foretrukket arbeider** – En vurderingspoengsum beregnet sammen med verdiene for **Ansvarlig arbeider**, **Foretrukket arbeider**, **Foretrukket arbeidergruppe**, **Aktivasted** og **Startdato**. De fire vurderingsresultatene beregnes og legges sammen for å gi en poengsum som brukes til å velge hvilken arbeider som skal tilordnes til hvilken arbeidsordre under planlegging av arbeidsordrer. Hvis verdien "10,00" settes inn i dette feltet, og en arbeider er valgt som foretrukket arbeider i en arbeidsordre, får arbeideren 10 poeng i den totale beregningen av arbeideren under planlegging av arbeidsordren.  
- **Foretrukket arbeidergruppe** – En vurderingspoengsum beregnet sammen med verdiene for **Ansvarlig arbeider**, **Foretrukket arbeider**, **Foretrukket arbeidergruppe**, **Aktivasted** og **Startdato**. Hvis verdien "10,00" settes inn i dette feltet, og en arbeider er tilordnet til en foretrukket arbeidergruppe som er valgt i en arbeidsordre, får arbeideren 10 poeng i den totale beregningen av arbeideren under planlegging av arbeidsordren.  
- **Begrens til foretrukket** – Dette begrenser antall arbeidere som er tilgjengelige for planlegging av arbeidsordrer. Velg **Nei** hvis du vil beregne en poengsum for alle ansatte, uansett om de er definert som foretrukne arbeidere eller deler av en foretrukket arbeidergruppe. Velg **Ja** bare hvis du vil beregne en poengsum for alle ansatte som er definert som foretrukne arbeidere og/eller inkludert i en foretrukket arbeidergruppe.  
- **Sted** – En vurderingspoengsum beregnet sammen med verdiene for **Ansvarlig arbeider**, **Foretrukket arbeider**, **Foretrukket arbeidergruppe**, **Aktivasted** og **Startdato**. Hvis verdien "3000,00" settes inn i dette feltet, får en arbeidsprosess 3000 poeng i beregningen hvis arbeideren er plassert i samme fabrikk eller anlegg som aktivumet som en jobb skal planlegges på.  
  - Hvis firmaet bruker funksjonslokasjoner, får arbeiderne full poengsum hvis de befinner seg på funksjonslokasjonen som er knyttet til anleggsmidlet. Hvis funksjonslokasjonen til anleggsmidlet har et overordnet objekt, får arbeidere på denne funksjonslokasjonen 1/2 poeng. Hvis stedet også har et overordnet sted, får arbeidere på dette stedet 1/3 poeng. Hvis dette stedet også har et overordnet sted, får arbeidere på dette stedet 1/4 poeng osv.  
  - Hvis firmaet ditt bruker aktivasted, som vi ikke anbefaler, brukes sted, område og sone til å beregne stedspoengsummer. Arbeiderne får full poengsum hvis de befinner seg på stedet og i området og sonen som er knyttet til eiendelen. Hvis arbeiderstedet bare samsvarer med sted og område, er rangeringspoengsummen for arbeideren 2/3 for hele poengsummen. Hvis arbeiderstedet bare samsvarer med sted, er rangeringspoengsummen for arbeideren 1/3 av hele poengsummen.  
- **Begrens til sted** – Dette begrenser antall arbeidere som er tilgjengelige for planlegging av arbeidsordrer. Velg **Nei** hvis du vil beregne en poengsum for alle arbeidere på tvers av alle funksjonslokasjoner. Velg **Ja** hvis du bare vil beregne en poengsum for arbeidere som er knyttet til arbeidsordrens funksjonslokasjon.

>[!NOTE]
>De tre "Begrens til..."-feltene øker hastigheten på arbeidsordreplanleggingen ved å begrense antallet poengsummer som beregnes for arbeiderne.

**Arbeiderens startdato** – En vurderingspoengsum beregnet sammen med verdiene for **Ansvarlig arbeider**, **Foretrukket arbeider**, **Foretrukket arbeidergruppe**, **Aktivasted** og **Startdato**. Dette feltet angir daglig poengsum som en negativ verdi, og sammenlignes med **Forventet start**-feltet i en Arbeidsordre. Hvis verdien "10,00" settes inn i dette feltet, og den forventede startdatoen for en arbeidsordre er i morgen, er klassifiseringsresultatet minus 10,00.

  - Forutsatt at ingen ansvarlig arbeider og ansvarlig arbeidergruppe er valgt på en arbeidsordre som skal planlegges – du legger til og trekker fra verdiene for vurderingspoengsummen i eksemplene i feltene **Foretrukket arbeider**, **Foretrukket arbeidergruppe**, **Aktivasted** og **Startdato** ovenfor, får du en total på 3010,00. Dette betyr en høy poengsum for arbeideren som allerede er valgt som foretrukket arbeider, og som er inkludert i den foretrukne arbeidergruppen på arbeidsordren, og arbeideren er også plassert i samme anlegg som aktivumet som en jobb må planlegges for. Dette betyr at det er en god sjanse for at den aktuelle arbeideren vil bli valgt for å fullføre jobben under planleggingen av arbeidsordren.  
  - Hvis verdien "0,00" settes inn i ett av de åtte feltene ovenfor, brukes ikke denne vurderingspoengsummen under planlegging av arbeidsordrer.  

## <a name="the-document-types-tab"></a>Fanen Dokumenttyper

Velg dokumenttypene som skal være tilgjengelige for utskrift av vedlegg som er knyttet til en arbeidsordrerapport. Denne gjøres ved å velge en en dokumenttype i delen **Tilgjengelig** og velge ![fremoverpilen.](media/15-setup-for-objects.png). Hvis du vil fjerne en valgt dokumenttype, velger du dokumenttypen i delen **Valgt** og velger ![tilbakepilen](media/16-setup-for-objects.png).

## <a name="the-number-sequences-tab"></a>Fanen Nummerserier

Velg de nødvendige nummerseriene i denne delen. Det finnes to nummerserier for anleggsmidler: én for manuelt opprettede anleggsmidler, og én for anleggsmidler som er opprettet ved hjelp av ventende anleggsmidler.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
