--- 
title: Opprette en bestilling med en leveringsplan
description: "Denne fremgangsmåten viser hvordan du oppretter en leveringsplan for en bestilling."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1e4a0204d74c8966cd90b52ae13c88e222ebc3ef
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Opprette en bestilling med en leveringsplan

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en leveringsplan for en bestilling. En leveringsplan brukes når et antall i en ordre eller en journal blir bedt om å bli levert i flere leveranser. Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF. Dette gjøres vanligvis av en innkjøpsagent.


## <a name="create-a-delivery-schedule"></a>Opprette en leveringsplan
1. Gå til Innkjøp og leverandører > Bestillinger > Alle bestillinger.
2. Klikk Ny.
3. Angi US-101 i Leverandørkonto-feltet.
4. Klikk OK.
5. Angi M0001 i feltet Varenummer.
6. Angi 10 i Antall-feltet.
7. Klikk Bestillingslinje.
8. Klikk Leveringsplan.
    * Siden Leveringsplan lar deg angi antall leveranser der det totale antallet på ordrelinjen skal leveres fra leverandøren.  
    * Som standard kopieres det totale antallet og andre leveringsdetaljer for den opprinnelige innkjøpslinjen til den første leveringslinjen for planen. I dette eksemplet skal vi opprette en tidsplan for to forsendelser, der datoen for den andre forsendelsen er forskjøvet med en uke fra den første forsendelsen.  
9. I Antall-feltet endrer du antallet til 4.
10. Klikk Ny.
11. Angi 6 som restantallet i Antall-feltet.
    * Velg en dato som er én uke etter datoen i den første leveringslinjen, i datofeltet for levering.  
    * Du kan holde oversikt over det totale antallet som er tildelt til leveringsplanlinjene, ved å se på feltene Total og Gjenværende. Når det gjenstående antallet er null, er det fullstendige antallet fra den opprinnelige linjen tildelt til tidsplanen.  
12. Vis Gebyrkonvertering-delen.
    * Alternativene her lar deg kontrollere hvor du vil at gebyrer skal fordeles over leveringsplanlinjene. Hvis du velger Kopier bruttobeløp, kopieres gebyrbeløpet på den opprinnelige ordrelinjen til hver leveringslinje. Alternativet Tildel til leveringslinjer deler opprinnelige linjegebyr i henhold til antallet på hver leveringslinje.  
13. Skjul Gebyrkonvertering-delen.
14. Klikk OK.
    * Leveringsplanen er nå brukt på ordren.  
    * Den opprinnelige ordrelinjen, kalt en kommersiell linje, er konvertert til en ordrelinje med flere leveringer. Den er merket med et eget ikon og fungerer som et hode for leveringslinjene.  
15. Velg den andre ordrelinjen, som er den første av de to leveringslinjene.
    * De to nye linjene, referert til som leveringslinjer, utgjør en leveringsplan. Ordren behandles mot disse linjene og ikke den opprinnelige linjen. Hvis dokumenter, for eksempel bekreftelser, produktkvitteringsjournaler eller fakturaer, skrives ut, vises bare leveringslinjene.  

## <a name="change-the-delivery-schedule"></a>Endre leveringsplanen
    * Du kan endre antallet på leveringslinjer. Hvis du gjør dette, oppdateres den kommersielle linjen automatisk til det totale antallet i leveringslinjene.  
1. I Antall-feltet i den første leveringslinjen, endrer du antallet fra 4 til 5.
2. Velg den første bestillingslinjen (den kommersielle linjen).
    * Antallet på den kommersielle linjen er endret til 11.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Behandle produktkvitteringer ved hjelp av leveringsplaner
    * Bestillingen må bekreftes før produktmottak kan behandles. I dette eksemplet registreres mottaket direkte på bestillingen. Mottaket kan også ha blitt registrert når varene ble mottatt i lageret.  
1. Klikk Kjøp i handlingsruten.
2. Klikk Bekreft.
3. Klikk Motta i handlingsruten.
4. Klikk Produktkvittering.
5. Skriv inn en verdi i Produktkvittering-feltet.
    * Dette feltet brukes til å angi en referanse som skal brukes som bilag for produktkvitteringsjournalen.  
    * I Antall-feltet velger du Bestilt antall. Dette alternativet betyr at det mottaket behandles for antallet som ordrelinjene ble opprettet med.  
    * Kontroller at feltet Skriv ut produktkvittering er satt til Nei. Utskrift er ikke nødvendig i dette eksemplet.  
6. Vis Linjer-delen.
    * Legg merke til hvordan produktkvitteringen opprettes for de to leveringslinjene og ikke for den opprinnelige ordrelinjen. Hvis du har registrert mottak i lageret, vil det være registrert på leveringsplanlinjene.  
7. Skjul Linjer-delen.
8. Klikk OK for å postere kvitteringen.


