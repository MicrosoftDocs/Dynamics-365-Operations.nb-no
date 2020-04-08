---
title: Opprette en rekvisisjon for forbruk
description: Dette emnet beskriver fremgangsmåten for å opprette en rekvisisjon.
author: mkirknel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ca44b4793f61d1067b9e0740b9a447d3a2363c2
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147394"
---
# <a name="create-a-requisition-for-consumption"></a>Opprette en rekvisisjon for forbruk

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver fremgangsmåten for å opprette en rekvisisjon. Den viser forskjellige måter å søke etter produkter på i innkjøpskatalogen og hvordan du legger til et produkt som ikke finnes i katalogen. Før du starter denne fremgangsmåten, må en innkjøpspolicy være definert med Forbruk som standardtype for rekvisisjon. Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Prosedyren kan bare utføres av en brukerprofil som er definert som arbeider. Denne oppgaven vil vanligvis utføres av en ansatt. Med sikkerhetsrollen som **ansatt** kan du utføre oppgavene, eller hvis du bruker USMF, kan du logge inn med **Alicia**.


## <a name="create-a-new-requisition"></a>Opprett en ny rekvisisjon
1. Gå til **Navigasjonsrute > Moduler > Innkjøp og leverandører > Innkjøpsrekvisisjoner > Innkjøpsrekvisisjoner klargjort av meg**.
2. Velg **Ny**.
3. Gi rekvisisjonen et navn i **Navn**-feltet.
4. Angi en dato i feltet **Ønsket dato**. Som standard kopieres den forespurte datoen og regnskapsdatoen til innkjøpsrekvisisjonslinjene. De kan endres på linjenivå. Ønsket dato er ønsket leveringsdato.  
5. Angi en dato i feltet **Regnskapsdato**. Regnskapsdatoen brukes til å registrere regnskapsoppføringen i økonomimodulen, og til å validere hvorvidt budsjettmidler er tilgjengelige.  
6. Velg **OK**.
7. I **Årsak**-feltet velger du et alternativ fra rullegardinmenyen. Bestillingsårsaken du velger, vises som standard for innkjøpsrekvisisjonslinjene, men du kan endre den på linjenivået.  
8. Velg årsaken.
9. I **Detaljer**-feltet angir du en mer beskrivende begrunnelse for rekvisisjonen.

## <a name="add-a-line-to-the-requisition"></a>Legge til en linje i rekvisisjonen
1. Velg **Legg til linje**. Det finnes to måter å legge til linjer i innkjøpsrekvisisjonen på. Hvis du allerede kjenner produktnummer, eller du allerede vet at du ber om et produkt som ikke er i produktkatalogen, kan du legge til linjen direkte med **Legg til linje**. Den andre måten er å bruke **Legg til produkter**, der du kan bruke søk og filtrering til å finne varer i produktkatalogen.    
2. Velg raden du nettopp opprettet.
    - Bestilleren er arbeideren som har bedt om rekvisisjonen.   
    - Som standard er personen som klargjør rekvisisjonen, arbeideren som har bedt om den. Du må få tillatelse til å klargjøre en rekvisisjonslinje på vegne av en annen arbeider. Hvis du har slike tillatelser, vises de andre arbeiderne i dette oppslaget.  
3. Skriv inn en verdi i **Varenummer**-feltet. Varene som er tilgjengelige for deg å velge, begrenses av kategoritilgangspolicyen og innkjøpskatalogen for den juridiske enheten for innkjøp.   
4. Angi et tall i **Antall**-feltet.

## <a name="add-more-products-to-the-requisition"></a>Legge til flere produkter i rekvisisjonen
1. Velg **Legg til produkter**. Dette er alternativet der du kan søke etter produkter i produktkatalogen.    
2. I **Finn innkjøpskategorinode**-feltet skriver du inn første del av navnet på kategorien du leter etter, og velg deretter **Enter**. Skriv for eksempel inn `comput`.  
3. Bruk **InvokeDefaultButton**-snarveien.
4. Bruk **Filter** til å filtrere listen over produkter i den valgte kategorien.
5. Velg produktkortet som du vil legge til i rekvisisjonen.
6. Velg **Tilføy til linjer**.
7. Angi et tall i **Antall**-feltet.
8. I **Finn innkjøpskategorinode**-feltet skriver du inn første del av navnet på kategorien du leter etter, og velg deretter **Enter**. Skriv for eksempel inn `High`.  
9. Bruk **InvokeDefaultButton**-snarveien.
10. Velg **Tilføy ulistede produkter til linjer** for å legge til et produkt som ikke er oppført i innkjøpskatalogen.
11. Skriv inn en verdi i feltet **Produktnavn**.
12. Skriv inn en verdi i feltet **Enhet**.
13. Velg **OK**.
14. Legg til en beskrivelse av produktet i **Varebeskrivelse**-feltet.
15. Angi et tall i **Antall**-feltet.
16. Angi et tall i **Enhetspris**-feltet. Hvis du kjenner prisen for en bestemt leverandør (som du velger i leverandørkontofeltet), kan du angi denne prisen.   
17. Åpne rullegardinlisten i feltet **Leverandørkonto** for å velge et alternativ. Leverandører som er tilgjengelige i dette feltet avhenger av innkjøpspolicyer og statusen som leverandøren har for gjeldende innkjøpskategori. Som et alternativ til å velge en leverandør her, kan du velge **Foreslå leverandør**.    
18. Velg leverandøren du vil bruke, i listen.
19. Skriv inn en verdi i feltet **Eksternt varenummer**. Dette er et referansenummer for produktet som er kjent av leverandøren. Dette kan for eksempel være varenummeret for produktet i leverandørens egen katalog.  
20. Velg **OK**.

## <a name="distribute-amounts"></a>Fordel beløp
1. Velg **Finans**.
2. Velg **Fordel beløp**. Denne prosessen viser deg hvordan du distribuerer kostnaden for den første linjen mellom 2 kontoer. Dette kan også gjøres senere når rekvisisjonen er til vurdering.  
3. Velg **Del** for å opprette en ny distribusjonslinje.
4. Velg det første kostsenteret som skal ta del i kostnaden i feltet **Finanskonto**.
5. Velg den andre distribusjonslinjen.
6. Angir det andre kostsenteret i Finanskonto-feltet.
7. Velg **Fordel likt**.
8. Lukk siden.

## <a name="view-line-details"></a>Vise linjedetaljer
1. Aktiver/deaktiver utvidelsen av delen **Linjedetaljer**.

## <a name="submit-the-requisition"></a>Sende rekvisisjonen
1. Velg **Arbeidsflyt** for å åpne nedtrekksdialogen.
2. Velg **Send**.
3. Lukk siden.
4. I feltet **Kommentar** skriver du inn en merknad for godkjenneren av rekvisisjonen.
5. Velg **Send**.
6. Lukk siden.
7. Oppdater siden.

