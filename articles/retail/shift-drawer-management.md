---
title: Behandling av skift og kassaskuff
description: "Denne artikkelen beskriver hvordan du definerer og bruker de to skifttypene for salgssted – delt og frittstående. Delte skift kan brukes av flere brukere på flere steder, mens frittstående skift bare kan brukes av én arbeider om gangen."
author: rubencdelgado
manager: AnnBe
ms.date: 02/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 8a24f8adc4f7886a1f942d83f7a4eb12e7034fcd
ms.openlocfilehash: c1483d3240d266845cea7789b70c038cb98fdfcc
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---

# <a name="shift-and-cash-drawer-management"></a>Behandling av skift og kassaskuff

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du definerer og bruker de to skifttypene for salgssted – delt og frittstående. Delte skift kan brukes av flere brukere på flere steder, mens frittstående skift bare kan brukes av én arbeider om gangen.

Det finnes to skifttyper for salgssted for detaljhandel: frittstående og delt. Frittstående skift kan bare brukes av én arbeider om gangen. Delte Skift kan brukes av flere brukere på flere steder. Derfor utgjør de effektivt ett enkelt skift for flere arbeidere i en butikk.

## <a name="standalone-shifts"></a>Frittstående skift
Frittstående skift brukes i tradisjonelle situasjoner med fast salgssted der kontanter avstemmes uavhengig for hver kasse på salgsstedet. I dagligvareforretninger er det for eksempel vanligvis flere faste kasser på salgsstedet, og en kasserer er tilordnet til hver kasse. I slike tilfeller bruker hver kasse sannsynligvis et frittstående skift, og kassereren er ansvarlig for kassen eller fysisk kontanter i denne kassen. Et frittstående skift omfatter all aktivitet på denne kassen i løpet av kassererens arbeidsskift. Aktiviteter kan omfatte åpningsbeløpet i kassen, fjerning og tillegg av kontanter ved bruk, som deponeringer til bank og flytoppføring, og kasseoppgjøret på slutten av skiftet.

### <a name="set-up-a-stand-alone-shift"></a>Definere et frittstående skift

Et frittstående skift angis på kasseskuffnivå. Denne fremgangsmåten beskriver hvordan du definerer et frittstående skift i en kasse på utsalgstedet.

1.  Klikk **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofiler** &gt; **Maskinvareprofiler**.
2.  Velg maskinvareprofilen som skal brukes for det frittstående skiftet.
3.  I hurtigfanen **Skuff** bekrefter du at alternativet **Skuff for delt skift** er satt til **Nei**.
4.  Klikk **Lagre**.
5.  Klikk **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Kasser**.
6.  Velg kassen som krever et frittstående skift, og klikk deretter **Rediger**.
7.  I feltet **Maskinvareprofil** velger du maskinvareprofilen du valgte i trinn 2.
8.  Klikk **Lagre**.
9.  Klikk på **Detaljhandel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplan**.
10. Velg distribusjonsplanen **1090**, og klikk deretter **Kjør nå** for å synkronisere endringer på salgsstedet.

### <a name="use-a-stand-alone-shift"></a>Bruke et frittstående skift

1.  Logg på salgsstedet.
2.  Hvis ingen skift er åpent, velger du **Åpne et nytt skift**.
3.  Gå til operasjonen **Rapporter startbeløp**, og angi kontantbeløpet som legges til kasseapparatet på starten av arbeidsdagen.
4.  Utfør noen transaksjoner.
5.  På slutten av dagen velger du **Deklarer betalingsmiddel** for å deklarere kontantbeløpet som gjenstår i kassaskuffen.
6.  Angi kontantbeløpet, og klikk deretter **Lagre** for å lagre kasseoppgjøret.
7.  Velg **Lukk skift** for å lukke skiftet.

**Obs!** Andre operasjoner er tilgjengelige under skiftet, avhengig av forretningsprosessene som er på plass. OPerasjonene **Deponer til safe**, **Deponer til bank** og **Fjerning av betalingsmidler** kan brukes for å fjerne penger fra kassen i løpet av dagen eller før skiftet lukkes. Hvis det er lite penger igjen i en kasse, kan operasjonen **Flytoppføring** brukes for å legge til kontanter i kassen.

## <a name="shared-shifts"></a>Delte skift
Et delt skift brukes i et miljø der flere kasserere deler en kassaskuff eller et sett med kassaskuffer hele arbeidsdagen. Vanligvis brukes et delt skift i mobile salgsstedsmiljøer. I et mobilt miljø er ikke hver kassereren tildelt og ansvarlig for én enkelt kassaskuff. I stedet må alle kasserere kunne utføre et salg og legge til kontanter i kassaskuffen som er nærmest dem. I dette scenariet er pengeskuffene som deles mellom kasserere inkludert i et delt skift. Alle kassaskuffer i et delt skift er inkludert i det samme skiftet for aktiviteter som er knyttet til behandling av kontanter for skiftet. Derfor skal startbeløpet for skiftet inkludere summen av alle kontanter i alle kassaskuffer som er inkludert i det delte skiftet. På samme måte skal kassaoppgjøret være summen av alle kontanter i alle kassaskuffer som er inkludert i det delte skiftet. **Obs!** Bare ett delt skift kan være åpent om gangen i hver butikk. Delte skift og frittstående skift kan brukes i den samme butikken.

### <a name="set-up-a-shared-shift"></a>Definere et delte skift

1.  Klikk **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgsstedsprofiler** &gt; **Maskinvareprofiler**.
2.  Velg maskinvareprofilen som skal brukes for det delte skiftet.
3.  I hurtigfanen **Skuff** setter du alternativet **Skuff for delt skift** til **Ja**.
4.  Klikk **Lagre**.
5.  Klikk **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Kasser**.
6.  Velg kassen som krever et delt skift, og klikk deretter **Rediger**.
7.  I feltet **Maskinvareprofil** velger du maskinvareprofilen du valgte i trinn 2.
8.  Klikk **Lagre**.
9.  Klikk på **Detaljhandel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplan**.
10. Velg distribusjonsplanen **1090**, og klikk deretter **Kjør nå** for å synkronisere endringer på salgsstedet.

### <a name="use-a-shared-shift"></a>Bruke et delte skift

1.  Logg på salgsstedet.
2.  Hvis salgsstedet ennå ikke er koblet til en maskinvarestasjon, velger du **Ikke-skuff-operasjon**, og velg deretter operasjonen **Velg maskinvarestasjon** for å aktivere en maskinvarestasjon for det delte skiftet. Dette trinnet er nødvendig bare første gang en kasse legges til i et miljø med delte skift.
3.  Logg av salgsstedet, og logg deretter på.
4.  Velg **Opprett et nytt skift**.
5.  Velg **Rapporter startbeløp**.
6.  Angi startbeløpet for alle kassaskuffer i butikken som er en del av det delte skiftet, og klikk deretter **Lagre**.
    -   Hvis du vil legge til et startbeløp i hver etterfølgende kassaskuff, bruker du operasjonen **Velg maskinvarestasjon** for å aktivere maskinvarestasjonen.
    -   Hvis du vil legge til en bestemt kassaskuff, bruker du operasjonen **Åpne skuff**.
    -   Fortsett til alle kassaskuffene i det delte skiftet har sin del av startbeløpet.

7.  Åpne hver kassaskuff på slutten av dagen, og fjerner kontantene.
8.  Når du har fjernet kontantene fra den siste kassaskuffen, teller du alle kontantene fra alle kassaskuffene.
9.  Bruk operasjonen **Deklarer betalingsmiddel** for å deklarere det totale kontantbeløpet fra alle kassaskuffene som er inkludert i det delte skiftet.
10. Bruk operasjonen **Lukk skift** for å lukke det delte skiftet.

## <a name="shift-operations"></a>Skiftoperasjoner
Forskjellige handlinger kan utføres for å endre statusen for et skift, eller for å øke eller redusere pengebeløpet i skuffen. Avsnittet nedenfor beskriver disse skiftoperasjonene for Dynamics 365 for Retail Modern POS og Cloud POS.

**Åpne skift**

POS krever at en bruker har et aktivt, åpent skift for å utføre handlinger som vil resultere i en finanstransaksjon, for eksempel salg, retur eller kundeordre.  

Når du logger på salgsstedet, kontrollerer systemet først om brukeren har et aktivt skift i det gjeldende registret. Hvis ikke kan brukeren deretter velge å åpne et nytt skift, gjenoppta et eksisterende skift eller fortsette å logge på i "ikke-skuff"-modus, avhengig av systemkonfigurasjonen og tillatelsene.

**Rapporter startbeløp**

Denne operasjonen er ofte den første handlingen som skal utføres et nylig åpnet skift. Brukere angir startbeløpet i skuffen for skiftet. Dette er viktig fordi over-/underberegningen som skjer når du lukker et skift, utgjør dette beløpet.

**Flytoppføring**

Flyt-oppføringene er ikke-salgstransaksjoner som utføres i et aktivt skift, og de øker pengebeløpet i skuffen. Et vanlig eksempel på en flytoppføring er å legge til flere vekslepenger i skuffen når det er lite.

**Fjerning av betalingsmidler**

Fjerning av betalingsmidler er ikke-salgstransaksjoner som utføres i et aktivt skift for å redusere pengebeløpet i skuffen. Dette brukes vanligvis sammen med en flytoppføring i et annet skift. Register 1 har for eksempel lite vekslepenger, så brukeren på Registrer 2 utfører en fjerning av betalingsmidler for å redusere beløpet i skuffen. Brukeren i Registrer 1 kan deretter utføre en flytoppføring for å øke beløpet.

**Avbryt skift**

Brukere kan deaktivere sine aktive skift for å frigjøre det gjeldende registret for en annen bruker, eller flytte skiftet til et annet register (dette er ofte kalt en "flytende kasse"). 

Suspendering av skiftet forhindrer eventuelle nye transaksjoner eller endringer til skiftet før det gjenopptas.

**Gjenoppta skift**

Denne operasjonen gjør det mulig for en bruker å gjenoppta et tidligere suspendert skift i et register som ikke allerede har et aktivt skift.

**Kasseoppgjør**

Kasseoppgjøret er handling brukeren utfører for å angi totale pengebeløpet som er i skuffen, vanligvis før skiftet lukkes. Dette er verdien som sammenlignes med det forventede skiftet for å beregne over-/underbeløpet.

**Deponer til safe**

Deponeringer til safe kan når som helst utføres på et aktivt skift. Denne operasjonen fjerner penger fra skuffen, slik at de kan overføres til en sikrere plassering, så som en safe på bakrommet. Det totale beløpet som er registrert for deponeringer til safe, er fremdeles inkludert i skifttotalene, men trenger ikke regnes som en del av kasseoppgjøret.

**Deponer til bank**

I likhet med deponeringer til safe utføres også deponeringer til bank på aktive skift. Denne operasjonen fjerner penger fra skiftet for å klargjøre for bankinnskuddet.

**Lukk skift usporet**

Et lukket usporet skift er et skift som ikke lenger er aktivt, men ikke er fullstendig lukket. Lukkede usporede skift kan ikke gjenopptas som et suspendert skift, men prosedyrer som å deklarere startbeløp og kasseoppgjør, kan utføres på et senere tidspunkt eller fra et annet register.

Lukkede usporede skift brukes ofte til å frigjøre et register for en ny bruker eller skift, uten å telle, avstemme og lukke dette skiftet fullstendig først. 

**Lukk skift**

Denne operasjonen beregner totaler for skift, over-/underbeløp, og fullfører deretter et aktivt eller lukket usporet skift. Lukkede skift kan ikke gjenopptas eller endres.  

**Behandle skift**

Denne operasjonen gir brukerne muligheten til å vise alle aktive, suspenderte og lukkede usporede skift for butikken. Avhengig av tillatelsene kan brukere utføre sine endelige lukkingsprosedyrer, for eksempel kasseoppgjør og lukke skift for lukkede usporede skift. Denne operasjonen lar også brukere vise og slette ugyldige skift hvis et skift står i en ugyldig tilstand etter å ha byttet mellom frakoblet og tilkoblet modus. Disse ugyldige skiftene inneholder ingen økonomisk informasjon eller transaksjonsdata som trengs for avstemming. 

