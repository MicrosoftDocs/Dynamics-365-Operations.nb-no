---
title: Behandling av skift og kassaskuff
description: "Denne artikkelen forklarer hvordan du definerer og bruker de to typene retail poenget med salg (POS) SKIFT - delt og frittstående. Delte skift kan brukes av flere brukere på flere steder, mens frittstående skift bare kan brukes av én arbeider om gangen."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 09c7fce1fa83d6a8d6391db667b7260d2a199390
ms.lasthandoff: 03/31/2017


---

# <a name="shift-and-cash-drawer-management"></a>Behandling av skift og kassaskuff

Denne artikkelen forklarer hvordan du definerer og bruker de to typene retail poenget med salg (POS) SKIFT - delt og frittstående. Delte skift kan brukes av flere brukere på flere steder, mens frittstående skift bare kan brukes av én arbeider om gangen.

Det finnes to skifttyper for salgssted for detaljhandel: frittstående og delt. Frittstående skift kan bare brukes av én arbeider om gangen. Delte Skift kan brukes av flere brukere på flere steder. Derfor utgjør de effektivt ett enkelt skift for flere arbeidere i en butikk.

## <a name="standalone-shifts"></a>Frittstående SKIFT
Frittstående skift brukes i tradisjonelle situasjoner med fast salgssted der kontanter avstemmes uavhengig for hver kasse på salgsstedet. I dagligvareforretninger er det for eksempel vanligvis flere faste kasser på salgsstedet, og en kasserer er tilordnet til hver kasse. I slike tilfeller bruker hver kasse sannsynligvis et frittstående skift, og kassereren er ansvarlig for kassen eller fysisk kontanter i denne kassen. Et frittstående skift omfatter all aktivitet på denne kassen i løpet av kassererens arbeidsskift. Aktiviteter kan omfatte åpningsbeløpet i kassen, fjerning og tillegg av kontanter ved bruk, som deponeringer til bank og flytoppføring, og kasseoppgjøret på slutten av skiftet.

### <a name="set-up-a-stand-alone-shift"></a>Definere et frittstående skift

Et frittstående skift angis på kasseskuffnivå. Denne fremgangsmåten beskriver hvordan du definerer et frittstående skift i en kasse på utsalgstedet.

1.  Klikk **Retail og commerce**&gt;**kanaloppsett**&gt;**POS installasjonsprogrammet**&gt;**POS profiler**&gt;**maskinvareprofiler**.
2.  Velg maskinvareprofilen som skal brukes for det frittstående skiftet.
3.  I hurtigfanen **Skuff** bekrefter du at alternativet **Skuff for delt skift** er satt til **Nei**.
4.  Click **Save**.
5.  Klikk **Retail og commerce**&gt;**kanaloppsett**&gt;**POS installasjonsprogrammet**&gt;**registrerer**.
6.  Velg kassen som krever et frittstående skift, og klikk deretter **Rediger**.
7.  I feltet **Maskinvareprofil** velger du maskinvareprofilen du valgte i trinn 2.
8.  Click **Save**.
9.  Klikk **Retail og commerce**&gt;**Retail IT**&gt;**distribusjonsplan**.
10. Velg distribusjonsplanen **1090**, og klikk deretter **Kjør nå** for å synkronisere endringer på salgsstedet.

### <a name="use-a-stand-alone-shift"></a>Bruke et frittstående skift

1.  Logg på salgsstedet.
2.  Hvis ingen skift er åpent, velger du **Åpne et nytt skift**.
3.  Gå til operasjonen **Rapporter startbeløp**, og angi kontantbeløpet som legges til kasseapparatet på starten av arbeidsdagen.
4.  Utfør noen transaksjoner.
5.  På slutten av dagen velger du **Deklarer betalingsmiddel** for å deklarere kontantbeløpet som gjenstår i kassaskuffen.
6.  Angi kontantbeløpet, og klikk deretter **Lagre** for å lagre kasseoppgjøret.
7.  Velg **Lukk skift** for å lukke skiftet.

**Obs! ** Andre operasjoner er tilgjengelige under skiftet, avhengig av forretningsprosessene som er på plass. OPerasjonene **Deponer til safe**, **Deponer til bank** og **Fjerning av betalingsmidler** kan brukes for å fjerne penger fra kassen i løpet av dagen eller før skiftet lukkes. Hvis det er lite penger igjen i en kasse, kan operasjonen **Flytoppføring** brukes for å legge til kontanter i kassen.

## <a name="shared-shifts"></a>Delte skift
Et delt skift brukes i et miljø der flere kasserere deler en kassaskuff eller et sett med kassaskuffer hele arbeidsdagen. Vanligvis brukes et delt skift i mobile salgsstedsmiljøer. I et mobilt miljø er ikke hver kassereren tildelt og ansvarlig for én enkelt kassaskuff. I stedet må alle kasserere kunne utføre et salg og legge til kontanter i kassaskuffen som er nærmest dem. I dette scenariet er pengeskuffene som deles mellom kasserere inkludert i et delt skift. Alle kassaskuffer i et delt skift er inkludert i det samme skiftet for aktiviteter som er knyttet til behandling av kontanter for skiftet. Derfor skal startbeløpet for skiftet inkludere summen av alle kontanter i alle kassaskuffer som er inkludert i det delte skiftet. På samme måte skal kassaoppgjøret være summen av alle kontanter i alle kassaskuffer som er inkludert i det delte skiftet. **Merk:** bare én delt Skift kan være åpent om gangen i hver butikk. Delte skift og frittstående skift kan brukes i den samme butikken.

### <a name="set-up-a-shared-shift"></a>Definere et delte skift

1.  Klikk **Retail og commerce**&gt;**kanaloppsett**&gt;**POS installasjonsprogrammet**&gt;**POS profiler**&gt;**maskinvareprofiler**.
2.  Velg maskinvareprofilen som skal brukes for det delte skiftet.
3.  I hurtigfanen **Skuff** setter du alternativet **Skuff for delt skift** til **Ja**.
4.  Click **Save**.
5.  Klikk **Retail og commerce**&gt;**kanaloppsett**&gt;**POS installasjonsprogrammet**&gt;**registrerer**.
6.  Velg kassen som krever et delt skift, og klikk deretter **Rediger**.
7.  I feltet **Maskinvareprofil** velger du maskinvareprofilen du valgte i trinn 2.
8.  Click **Save**.
9.  Klikk **Retail og commerce**&gt;**Retail IT**&gt;**distribusjonsplan**.
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



