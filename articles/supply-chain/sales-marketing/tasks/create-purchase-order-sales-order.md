---
title: Opprette en bestilling fra en salgsordre
description: Denne fremgangsmåten viser hvordan du oppretter en bestilling som er basert på en salgsordre.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7991476b86ace92cda513ae8906c62ba7fbbe915
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547429"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a>Opprette en bestilling fra en salgsordre

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en bestilling som er basert på en salgsordre. Produktets antall på bestillingen blir deretter utpekt til å dekke behovet for den opprinnelige salgsordren. Oppfylle salgsbehov på denne måten er et alternativ til en mer omfattende og optimalisert metode for planlegging av distribusjonskrav. Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.


## <a name="create-a-purchase-order-from-a-sales-order"></a>Opprette en bestilling fra en salgsordre
1. Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.
2. Klikk Ny.
3. Klikk rullegardinknappen i Kundekonto-feltet for å åpne oppslaget.
4. Finn og velg ønsket post i listen.
5. Klikk OK.
6. Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
7. Finn og velg ønsket post i listen.
    * Hvis du bruker USMF, kan du velge D0001.  
8. Angi et tall i feltet Antall.
9. Klikk Legg til linje.
10. Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
11. Finn og velg ønsket post i listen.
    * Hvis du bruker USMF, kan du velge T0020.  
12. Klikk koblingen i den valgte raden i listen.
13. Angi et tall i feltet Antall.
14. Klikk Lagre.
15. Klikk Salgsordre i handlingsruten.
16. Klikk Bestilling.
    * Opprett bestilling-siden viser alle de åpne salgsordrelinjene som er kopiert fra salgsordren. Du kan se gjennom ordredetaljene, og om nødvendig kan du endre valgte detaljer som for eksempel innkjøpsantall og prisvilkår før du oppretter kjøpene.  
17. Velg alternativet Inkluder alt.
    * Hvis du vil generere bestillinger for bare et delsett av salgsordrelinjene, velger du disse individuelt.  
    * Leverandørkonto-feltet kan eller kan ikke allerede være utfylt med et leverandørnummer. Hvis standardleverandøren er definert for produktet (på den tilknyttede varedekningen), vil denne leverandøren kopieres til linjen. Hvis ikke, må du angi en leverandør manuelt.  I denne veiledningen, uavhengig av om Leverandørkonto-feltet allerede inneholder en verdi eller ikke, instruerer følgende trinn deg om å velge en ny leverandør som er forskjellig for hver linje.  
18. Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.
19. Finn og velg ønsket post i listen.
20. Klikk koblingen i den valgte raden i listen.
21. Mer den andre ordrelinjen.
22. Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.
23. Finn og velg ønsket post i listen.
24. Klikk koblingen i den valgte raden i listen.
25. Klikk Valider.
26. Klikk OK.
    * Meldingen forteller deg at én eller flere bestillinger er opprettet. Systemet genererer en separat bestilling for hver leverandør som du angav for salgsordrelinjene. Dette betyr at hvis flere salgsordrelinjer skal leveres av samme leverandør, genereres en enkelt bestilling med flere linjer.  

## <a name="review-purchase-orders-created-from-sales-orders"></a>Vurdere bestillinger opprettet fra salgsordrer
1. Klikk Generelt i handlingsruten.
2. Velg Relaterte ordrer.
    * Relaterte ordrer-siden viser alle ordrene som ble opprettet fra salgsordren. I dette eksemplet finnes det to bestillinger generert for to ulike leverandører henholdsvis.  
3. Klikk for å følge koblingen i feltet Bestilling.
    * Hver bestillingslinje er tilknyttet salgsordrelinjen som førte til innkjøpet. Tilknytningen til salgsordren er angitt i kategorien Produkt i hurtigfanen Linjedetaljer i feltene Referansetype, Referansenummer og Referanseparti.  
4. Vis eller skjul Linjedetaljer-delen.
5. Klikk kategorien Produkt.
    * Referansepartiet garanterer at kostnadene fra det gjeldende kjøpet belastes den tilknyttede salgsordren.  
    * Du kan navigere til den opprinnelige salgsordren ved å åpne koblingen i feltet Referansenummer.  

