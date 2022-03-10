---
title: Validere en produksjonsflyt og -versjon
description: Denne fremgangsmåten viser hvordan du oppretter en ny produksjonsflyt og en første versjon for lean manufacturing.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d87aa427c2bc3868e255c97ea11fd4e79456eef
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573591"
---
# <a name="validate-a-production-flow-and-version"></a>Validere en produksjonsflyt og -versjon

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en ny produksjonsflyt og en første versjon for lean manufacturing. Forutsetninger: Produksjonsparameterne for lean manufacturing og enheter for klassen Tid må defineres. Du må definere en verdistrøm og en produksjonsgruppe. Se hvitebøkene for Lean manufacturing for å gjøre deg kjent med konseptene for produksjonsflyter og aktiviteter. Denne fremgangsmåten refererer til den juridiske enheten USMF i demodataene. Forutsatt at den juridiske enheten er konfigurert for Lean manufacturing, kan imidlertid andre juridiske enheter brukes.


## <a name="create-a-production-flow"></a>Opprette en produksjonsflyt
1. Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.
2. Klikk på Ny.
3. Skriv inn en verdi i Navn-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk på rullegardinknappen i Navn-feltet for å åpne oppslaget.
6. Klikk på koblingen i den valgte raden i listen.
    * En verdistrøm er en driftsenhet som strekker seg over alle aktiviteter og flyter for verdistrømmen.   På dette stadiet er driftsenhetene begrenset til en juridisk enhet og har ingen ytterligere funksjonalitet.  
7. Klikk på rullegardinknappen i feltet Produksjonsgruppe for å åpne oppslaget.
8. Klikk på koblingen i den valgte raden i listen.
    * Produksjonsgrupper gjør det mulig å definere materialer, arbeid og VIA-kontoer for en produksjonsprosess. Hvis du vil knytte regnskapskonteksten til en produksjonsflyt, må du velge en produksjonsgruppe.  
9. Klikk på Lagre.

## <a name="create-a-production-flow-version"></a>Opprette en produksjonsflytversjon
1. Klikk på Legg til.
2. Angi dato og klokkeslett i feltet Utløpsdato.
    * Du kan oppdatere utløpsdatoen for versjonen på et gitt tidspunkt, selv for aktive versjoner. Bruk utløpet for versjonen til å planlegge å fase ut en versjon.  
3. Klikk på OK.
4. Merk den valgte raden i listen.
5. Skriv inn en verdi i feltet Enhet.
6. Velg taktenheten.
7. Angi et nummer i feltet Gjennomsnittlig takttid.
    * Definer en målrettet gjennomsnittlig takttid for taktkontrollen for produksjonsflytversjonen.   Takten defineres som antall per tidsperiode.  I det gitte eksemplet er takttiden 0,2 timer per 10 stykker. For en arbeidstid på 8 timer tilsvarer dette en daglig produksjonskapasitet på 400 stykker.  
8. I feltet Antall per syklus angir du et tall.
9. Vis eller skjul Versjonsdetaljer-delen.
10. Angi et nummer i feltet Minste takttid.
    * Minste takttid må være mindre enn eller lik den gjennomsnittlige takttiden.  
11. Angi et nummer i feltet Største takttid.
    * Største takttid må være større enn eller lik den gjennomsnittlige takttiden.  
12. Angi et antall dager i perioden for faktisk syklustid
    * Perioden for faktisk syklustid er antall dager jobber aggregeres fra det faktiske minuttet bakover for å beregne den faktiske syklustiden. Verdien kan endres når som helst, og brukes bare for beregning av de faktiske syklustider.  
13. Klikk på Lagre.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]