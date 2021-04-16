---
title: Opprette en produksjonsflytversjon
description: Denne prosedyren fokuserer på å opprette en ny produksjonsflytversjon.
author: cvocph
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a4b4847046af541644338157d95e6fcba315f9c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829000"
---
# <a name="create-a-production-flow-version"></a>Opprette en produksjonsflytversjon

[!include [banner](../../includes/banner.md)]

Denne prosedyren fokuserer på å opprette en ny produksjonsflytversjon. For denne prosedyren må produksjonsparameterne for lean manufacturing og måleenheter for klassen Tid defineres. Du må også definere en verdistrøm og en produksjonsgruppe. Hvis du vil vite mer om produksjonsflyter og aktiviteter i lean manufacturing, kan du se i hvitebøkene om Lean manufacturing for Microsoft Dynamics AX Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="create-a-production-flow"></a>Opprette en produksjonsflyt
1. Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.
2. Klikk på Ny.
3. Skriv inn en verdi i Navn-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk på rullegardinknappen i Navn-feltet for å åpne oppslaget.
6. Klikk på koblingen i den valgte raden i listen.
    * Velg en driftsenhet av typen verdistrøm. En verdistrøm er en driftsenhet som strekker seg over alle aktiviteter og flyter for verdistrømmen. På dette stadiet er driftsenhetene begrenset til en juridisk enhet og har ingen ytterligere funksjonalitet.  
7. Klikk på rullegardinknappen i feltet Produksjonsgruppe for å åpne oppslaget.
8. Klikk på koblingen i den valgte raden i listen.
    * Velg en produksjonsgruppe for produksjonsflyten. Produksjonsgrupper gjør det mulig å definere materialer, arbeid og VIA-kontoer for en produksjonsprosess. Hvis du vil knytte regnskapskonteksten til en produksjonsflyt, må du velge en produksjonsgruppe.  
9. Klikk på Lagre.

## <a name="create-a-production-flow-version"></a>Opprette en produksjonsflytversjon
1. Klikk på Legg til.
2. Angi dato og klokkeslett i feltet Utløpsdato.
    * Om nødvendig kan du definere en utløpsdato for versjonen. Du kan oppdatere den når som helst, selv for aktive versjoner. Du kan bruke den til å planlegge å fase ut en versjon.  
3. Klikk på OK.
4. Merk den valgte raden i listen.
5. Skriv inn en verdi i feltet Enhet.
6. ResolveChanges taktenheten.
7. Angi et nummer i feltet Gjennomsnittlig takttid.
    * Definer gjennomsnittlig takttid for versjonen. Definer en målrettet gjennomsnittlig takttid for taktkontrollen for produksjonsflytversjonen. Takten defineres som antall per tidsperiode. I eksemplet er takttiden 0,2 timer per 10 stykker. For en arbeidstid på 8 timer tilsvarer dette en daglig produksjonskapasitet på 400 stykker.  
8. I feltet Antall per syklus angir du et tall.
    * Definer antall per syklus knyttet til den gjennomsnittlige takttiden.  
9. Aktiver/deaktiver utvidelsen av delen Versjonsdetaljer.
10. Angi et nummer i feltet Minste takttid.
    * Definer den minste takttiden. Minste takttid må være mindre enn eller lik den gjennomsnittlige takttiden.  
11. Angi et nummer i feltet Største takttid.
    * Største takttid må være større enn eller lik den gjennomsnittlige takttiden.  
12. Angi et tall i feltet Periode for faktisk syklustid (dager).
    * Angi antall dager i perioden for faktisk syklustid. Perioden for faktisk syklustid er antall dager jobber aggregeres fra det faktiske minuttet bakover for å beregne den faktiske syklustiden. Verdien kan endres når som helst, og brukes bare for beregning av de faktiske syklustider.  
13. Klikk på Lagre.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]