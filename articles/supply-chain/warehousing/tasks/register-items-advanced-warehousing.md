--- 
title: Registrere varer for en vare for avanserte lageraktiviteter ved hjelp av en journal for vareankomst
description: "Denne fremgangsmåten viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker avanserte lagerstyringsprosesser."
author: BibiSp
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 050d1fcbc59d9bb3253bfed2433987285423b334
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>Registrere varer for en vare for avanserte lageraktiviteter ved hjelp av en journal for vareankomst

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker avanserte lagerstyringsprosesser. Dette gjøres vanligvis av en mottaksassistent. 

Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Du må ha en bekreftet bestilling med en åpen bestillingslinje før du starter denne veiledningen. Varen på linjen må lagres, og den må ikke bruke produktvarianter, og kan ikke ha sporingsdimensjoner. Og varene må være tilknyttet en lagringsdimensjonsgruppe som er aktivert for lagerstyringsprosess. Lageret som brukes, må være aktivert for lagerprosjektstyringsprosesser, og lokasjonen som du bruker for mottak, må være nummerskiltkontrollert. Hvis du bruker USMF, kan du bruke firmakonto 1001, lager 51 og vare M9200 til å opprette din bestilling. 

Noter nummeret på bestillingen som du oppretter, og noter også varenummeret og området som du brukte for bestillingslinjen.


## <a name="create-an-item-arrival-journal-header"></a>Opprette et hode for vareankomstjournal
1. Gå til Vareankomst.
2. Klikk Ny.
3. Skriv inn en verdi i Navn-feltet.
    * Hvis du bruker USMF, kan du velge WHS. Hvis du bruker andre data, må journalen med det valgte navnet ha følgende egenskaper: Kontroller plukklokasjon plukklokasjon må settes til Nei og Karantenestyring må settes til Nei.  
4. Skriv inn en verdi i Nummer-feltet.
5. Skriv inn en verdi i Område-feltet.
    * Velg området som du brukte for bestillingslinjen. Dette skal fungere som en standardverdi som vil være standard for alle linjene i journalen. Hvis du har brukt lageret 51 USMF, kan du velge området 5.  
6. Skriv inn en verdi i Lager-feltet.
    * Velg et gyldig lager for området du har valgt. Dette skal fungere som en standardverdi som vil være standard for alle linjene i journalen. Hvis du bruker eksempelverdiene i USMF, velger du 51.  
7. Skriv inn en verdi i feltet Lokasjon.
    * Velg en gyldig lokasjon i lageret du har valgt. Lokasjonen må være tilknyttet en lokasjonsprofil, som er nummerskiltkontrollert. Dette skal fungere som en standardverdi som vil være standard for alle linjene i journalen. Hvis du bruker eksempelverdiene i USMF, velger du Bulk-008.  
8. Høyreklikk på rullegardinpilen i feltet Nummerskilt, og velg deretter Vis detaljer.
9. Klikk Ny.
10. Skriv inn en verdi i feltet Nummerskilt.
    * Noter verdien.  
11. Klikk Lagre.
12. Lukk siden.
13. Skriv inn en verdi i feltet Nummerskilt.
    * Angi verdien for nummerskiltet du nettopp opprettet. Dette skal fungere som en standardverdi som vil være standard for alle linjene i journalen.  
14. Klikk OK.

## <a name="add-a-line"></a>Legge til en linje
1. Klikk Legg til linje.
2. Skriv inn en verdi i Varenummer-feltet.
    * Angi varenummeret som du brukte på bestillingslinjen.  
3. Angi et tall i feltet Antall.
    * Angi antallet du vil registrere.  
    * Dato-feltet bestemmer hvilken dato når lagerbeholdningen for denne varen skal registreres i lageret.  
    * Parti-ID-en fylles ut av systemet hvis den kan identifiseres unikt fra informasjonen. Ellers må du legge den til manuelt. Dette er et obligatorisk felt, som kobler denne registreringen til en bestemt kildedokumentlinje.  

## <a name="complete-the-registration"></a>Fullføre registreringen
1. Klikk Valider.
    * Dette kontrollerer at journalen er klar for postering. Hvis valideringen mislykkes, må du rette opp feilene før du kan postere journalen.  
2. Klikk OK.
    * Når du har klikket OK, kontrollerer du meldingen. Det skal være en melding om at journalen er OK.  
3. Klikk Poster.
4. Klikk OK.
    * Når du har klikket OK, kontrollerer du meldingslinjen. Det skal være en melding om at operasjonen er fullført.  
5. Lukk siden.


