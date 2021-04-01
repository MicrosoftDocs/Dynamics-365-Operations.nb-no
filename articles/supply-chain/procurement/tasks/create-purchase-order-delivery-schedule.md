---
title: Opprette en bestilling med en leveringsplan
description: Dette emnet viser hvordan du oppretter en leveringsplan for en bestilling.
author: RichardLuan
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eb88b59cd70145b731d819b203c64f118c78c405
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237185"
---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Opprette en bestilling med en leveringsplan

[!include [banner](../../includes/banner.md)]

Dette emnet viser hvordan du oppretter en leveringsplan for en bestilling. En leveringsplan brukes når et antall i en ordre eller en journal blir bedt om å bli levert i flere leveranser. Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF. Dette gjøres vanligvis av en innkjøpsagent.

## <a name="create-a-delivery-schedule"></a>Opprette en leveringsplan
1. I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Bestillinger > Alle bestillinger**.
2. Velg **Ny** i handlingsruten.
3. Angi `US-101` i **Leverandørkonto**-feltet.
4. Velg **OK**.
5. Angi `M0001` i feltet **Varenummer**.
6. I **Antall**-feltet angir du `10`.
7. Velg **Bestillingslinje**.
8. Velg **Leveringsplan**.
- Siden **Leveringsplan** lar deg angi antall leveranser der det totale antallet på ordrelinjen skal leveres fra leverandøren.  
- Som standard kopieres det totale antallet og andre leveringsdetaljer for den opprinnelige innkjøpslinjen til den første leveringslinjen for planen. I dette eksemplet skal vi opprette en tidsplan for to forsendelser, der datoen for den andre forsendelsen er forskjøvet med en uke fra den første forsendelsen.  
9. I **Antall**-feltet endrer du antallet til `4`.
10. Velg **Ny**.
11. Angi `6` som restantallet i **Antall**-feltet.
- Velg en dato som er én uke etter datoen i den første leveringslinjen, i datofeltet for levering.  
- Du kan holde oversikt over det totale antallet som er tildelt til leveringsplanlinjene, ved å se på feltene **Total** og **Gjenværende**. Når det gjenstående antallet er null, er det fullstendige antallet fra den opprinnelige linjen tildelt til tidsplanen.  
12. Vis **Gebyrkonvertering**-delen.
- Alternativene her lar deg kontrollere hvor du vil at gebyrer skal fordeles over leveringsplanlinjene. Hvis du velger **Kopier bruttobeløp**, kopieres gebyrbeløpet på den opprinnelige ordrelinjen til hver leveringslinje. Alternativet **Tildel til leveringslinjer** deler opprinnelige linjegebyr i henhold til antallet på hver leveringslinje.  
13. Skjul **Gebyrkonvertering**-delen.
14. Velg **OK**.
- Leveringsplanen er nå brukt på ordren.  
- Den opprinnelige ordrelinjen, kalt en kommersiell linje, er konvertert til en ordrelinje med flere leveringer. Den er merket med et eget ikon og fungerer som et hode for leveringslinjene.  
15. Velg den andre ordrelinjen, som er den første av de to leveringslinjene.
- De to nye linjene, referert til som leveringslinjer, utgjør en leveringsplan. Ordren behandles mot disse linjene og ikke den opprinnelige linjen. Hvis dokumenter, for eksempel bekreftelser, produktkvitteringsjournaler eller fakturaer, skrives ut, vises bare leveringslinjene.  

## <a name="change-the-delivery-schedule"></a>Endre leveringsplanen
Du kan endre antallet på leveringslinjer. Hvis du gjør dette, oppdateres den kommersielle linjen automatisk til det totale antallet i leveringslinjene.  
1. I **Antall**-feltet i den første leveringslinjen, endrer du antallet fra `4` til `5`.
2. Velg den første bestillingslinjen (den kommersielle linjen).  
- Antallet på den kommersielle linjen er endret til 11.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Behandle produktkvitteringer ved hjelp av leveringsplaner
Bestillingen må bekreftes før produktmottaket kan behandles. I dette eksemplet registreres mottaket direkte på bestillingen. Mottaket kan også ha blitt registrert når varene ble mottatt i lageret.  
1. Klikk på **Innkjøp** i handlingsruten.
2. Velg **Bekreft**.
3. Klikk på **Mottak** i handlingsruten.
4. Velg **Produktkvittering**. Skriv inn en verdi i **Produktkvittering**-feltet.
- Dette feltet brukes til å angi en referanse som skal brukes som bilag for produktkvitteringsjournalen.  
- I **Antall**-feltet velger du **Bestilt antall**. Dette alternativet betyr at mottaket behandles for antallet som ordrelinjene ble opprettet med.  
- Kontroller at feltet **Skriv ut produktkvittering** er satt til **Nei**. Utskrift er ikke nødvendig i dette eksemplet.  
5. Vis **Linjer**-delen.
- Legg merke til hvordan produktkvitteringen opprettes for de to leveringslinjene og ikke for den opprinnelige ordrelinjen. Hvis mottaket er registrert i lageret, vil det være registrert på leveringsplanlinjene.  
6. Skjul **Linjer**-delen.
7. Klikk på **OK** for å postere kvitteringen.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]