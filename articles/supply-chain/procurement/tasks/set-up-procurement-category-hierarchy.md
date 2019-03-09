---
title: Definere et innkjøpskategorihierarki
description: Denne prosedyren viser deg hvordan du oppretter nye noder i et innkjøpskategorihierarki og hvordan du konfigurerer en innkjøpskategori som skal brukes i en innkjøpsprosess.
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
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
ms.openlocfilehash: 01809a8a3256342682d8a9cfb296a355310fe4ed
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "334525"
---
# <a name="set-up-a-procurement-category-hierarchy"></a>Definere et innkjøpskategorihierarki

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren viser deg hvordan du oppretter nye noder i et innkjøpskategorihierarki og hvordan du konfigurerer en innkjøpskategori som skal brukes i en innkjøpsprosess. Disse oppgavene vil vanligvis utføres av en innkjøpssjef. Før du starter denne fremgangsmåten, må det være et kategorihierarki av typen Innkjøp. Hvis du bruker en demonstrasjonsdataselskap, kan du kjøre denne prosedyren i firmaet USMF.


## <a name="add-a-new-procurement-category"></a>Legge til en ny innkjøpskategori
1. Gå til Innkjøp og leverandører > Innkjøpskategorier.
2. Klikk Rediger kategorihierarki.
    * Gjeldende innkjøpskategorihierarki vises til venstre på siden. Du er i ferd med å endre hierarkiet.  
3. Klikk Ny kategorinode.
    * Den øverste noden velges som standard. Hvis du bruker denne fremgangsmåten som oppgaveveiledning, kan du klikke knappen Lås opp og velge en annen overordnet node som du vil sette inn den ny noden i. Når det er gjort, låser du oppgaveveiledningen på nytt, og klikker deretter Ny kategorinode.  
4. Skriv inn en verdi i Navn-feltet.
5. Skriv inn en verdi i feltet Beskrivelse.
6. Skriv inn en verdi i feltet Egendefinert navn.
    * Det egendefinerte navnet er valgfritt. Det vises i kategorioppslag sammen med navnet på kategorien.  
7. Klikk Lagre.

## <a name="add-products-to-your-new-procurement-category"></a>Legge til produkter i den nye innkjøpskategorien
1. Gå til Innkjøp og leverandører > Innkjøpskategorier.
    * Merk noden du nettopp la til. Hvis du kjører denne prosedyren som en oppgaveveiledning, må du kanskje låse opp i oppgaveveiledningen for å velge noden.  
2. Aktiver/deaktiver utvidelsen av delen Produkter.
3. Klikk Legg til for å knytte produkter til innkjøpskategorien.
4. Velg produktet du vil legge til i innkjøpskategorien.
5. Klikk pilen for å velge produktet.
6. Velg et annet produkt du vil legge til i innkjøpskategorien.
7. Klikk pilen for å velge produktet.
8. Klikk OK.

## <a name="add-approved-and-preferred-vendors"></a>Legge til godkjente og foretrukne leverandører
1. Aktiver/deaktiver utvidelsen av delen Leverandører.
2. Klikk Legg til.
    * Du kan legge til en leverandør i en innkjøpskategori og angi om en leverandør er foretrukket eller bare godkjent for kategorien. Når du sletter en leverandør fra en kategori, slettes ikke de historiske transaksjonene med leverandøren i kategorien.   
3. Søk etter leverandøren du vil legge til i kategorien.
4. Klikk pilen for å velge leverandøren.
5. Klikk OK.
6. Velg leverandørraden som du vil endre.
7. Velg et alternativ i Leverandørstatus-feltet.
    * Innstillingen for leverandørvalg i kategoripolicyregelen styrer om foretrukne, godkjente, eller alle leverandører er tilgjengelige for innkjøpsrekvisisjoner.   

## <a name="add-additional-information-to-the-category"></a>Legge til ytterligere informasjon i kategorien
1. Aktiver/deaktiver utvidelsen av delen Kriteriegrupper for leverandørevaluering.
    * Med denne kategorien kan du definere hvilke kriterier leverandørene i innkjøpskategorien skal vurderes mot. Dette gjør du klikke Legg til og deretter velge en leverandørevalueringsgruppe som inneholder vilkårene du vil bruke.  
2. Aktiver/deaktiver utvidelsen av delen Spørreskjemaer.
    * Med denne kategorien kan du legge til spørreskjemaer som skal vises på rekvisisjonen, så lenge du angir aktivitetstypen som Rekvisisjon. Bestilleren må deretter fylle ut et spørreskjema, før de sender en rekvisisjon for ett eller flere bestemte produkter i innkjøpskategorien.  
3. Aktiver/deaktiver utvidelsen av delen Vare, mva-grupper.
4. Klikk rullegardinknappen i feltet Merverdiavgiftsgruppe for vare: for å åpne oppslaget.
5. Velg en mva-gruppe.
6. Aktiver/deaktiver utvidelsen av delen Kategoriside.
    * Kategorisider opprettes på siden Kategorihierarki. De inneholder informasjon om innkjøpskategorien, for eksempel informasjon om typen produkter i en kategori, bilder av produkter i en kategori, eller kunngjøringer, for eksempel om rabattene som finnes i en kategori. Informasjonen i en kategoriside vises på innkjøpsrekvisisjoner.  
7. Lukk siden.

