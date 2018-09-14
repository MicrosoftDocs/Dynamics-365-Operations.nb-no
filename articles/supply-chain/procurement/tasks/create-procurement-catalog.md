--- 
title: "Opprette en innkjøpskatalog"
description: "Denne veiledningen viser hvordan du oppretter en innkjøpskatalog."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: df844ba3834972441daa61899294b3e95cac96c1
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-procurement-catalog"></a>Opprette en innkjøpskatalog

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne veiledningen viser hvordan du oppretter en innkjøpskatalog. Denne oppgaven vil vanligvis utføres av en innkjøpsansvarlig. Du lærer også hvordan ansatte kan bruke katalogen når de oppretter en rekvisisjon. Før du kan opprette en katalog, må det være et innkjøpskategorihierarki i systemet. Hierarkiet arves av den nye katalogen, sammen med alle produktene som er i hierarkiet. Du kan bruke denne veiledningen i demonstrasjonsdatafirmaet USMF, der innkjøpskategorihierarkiet er tilgjengelig, i tillegg til eksemplene som brukes i fremgangsmåten.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Kontrollere at det finnes et innkjøpskategorihierarki
1. Gå til Innkjøp og leverandører > Innkjøpskategorier.
    * Et innkjøpskategorihierarki er tilgjengelig i demonstrasjonsdatafirmaet USMF, og produktene er lagt til kategorien Kontormaskiner/datamaskiner. Hvis du kjører denne prosedyren som en oppgaveveiledning, må du låse opp i veiledningen hvis du vil bla gjennom kategorien. Hvis et hierarki ikke er tilgjengelig, kan du opprette det ved å klikke Ny. Dette kan bare gjøre én gang.  
2. Lukk siden.

## <a name="create-a-catalog"></a>Opprette en katalog
1. Gå til Innkjøp og leverandører > Kataloger > Innkjøpskataloger.
2. Klikk Ny innkjøpskatalog for å åpne dialogboksen for rullegardinlisten.
3. Skriv inn en verdi i Navn-feltet.
4. Klikk OK.
5. Vis FIRMAINNKJØPSKATEGORIER i treet.
6. Vis KONTORMASKINER i treet.
7. Velg Datamaskiner i treet .
    * Produktene fra innkjøpskategorien vises i listen. Hvis du vil legge til et produkt i kategorien, må du gjøre dette på siden Innkjøpskategorihierarki eller Varedetaljer.  
    * Standard oppdateringstype bestemmer om nye produkter som er lagt til innkjøpskategorihierarkiet, umiddelbart vises i katalogen. Hvis oppdateringstypen er satt til Dynamisk, vises endringene umiddelbart. Hvis oppdateringstypen er Statisk, vises nye produkter bare for personer som bruker katalogen etter at den er publisert på nytt. Publiser-handlingen er tilgjengelig i handlingsruten øverst på siden. Hvis produkter er fjernet fra innkjøpskategorihierarkiet, vises endringen umiddelbart, uavhengig av verdien i feltet Standard oppdateringstype.  
8. Finn og velg ønsket post i listen.
9. Klikk Skjul.
10. Klikk Kategorinavigering i handlingsruten.
11. Klikk Deaktiver.
12. Klikk Kategorinavigering i handlingsruten.
13. Klikk Aktiver.
14. Klikk Aktiver katalog.
15. Lukk siden.

## <a name="make-the-catalog-visible"></a>Gjøre katalogen synlig
1. Gå til Innkjøp og leverandører > Oppsett > Policyer > Innkjøpspolicyer.
2. Velg Policy for innkjøpspolicy for USMF.
    * Du må velge innkjøpspolicyen for den juridiske enheten som arbeideren koblet til, som brukerprofilen kan bestille produkter i. I USMF-demonstrasjonsdataene er administrasjonsbrukeren knyttet til arbeideren kalt Julia Funderburk, og hun bestiller produkter i USMF som standard.  
3. Klikk koblingen i den valgte raden i listen.
4. Velg katalogen du nettopp opprettet.
5. Klikk OK.
6. Lukk siden.
7. Lukk siden.

## <a name="use-the-catalog"></a>Bruke katalogen
1. Gå til Innkjøp og leverandører > Innkjøpsrekvisisjoner > Alle innkjøpsrekvisisjoner.
2. Klikk Ny.
3. Skriv inn en verdi i Navn-feltet.
4. Klikk OK.
5. Klikk Legg til produkter.
6. Finn og velg ønsket post i listen.
    * Du kan bruke kategorihierarkiet til venstre eller filter øverst i listen for å filtrere produktene.  
7. Klikk Tilføy til linjer.
8. Finn og velg ønsket post i listen.
9. Klikk Tilføy til linjer.
10. Klikk OK.


