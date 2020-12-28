---
title: Returkostpris og returparti-ID
description: Du vil kanskje at kostnadene for de returnerte produktene skal være lik kostnaden for produktene på tidspunktet da du solgte produktene til kunden. Du kan gjøre dette ved å bruke **Returparti-ID**.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnInventTransIdLookup, ReturnItemNumLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d5ac48dd390e2f57a7312e3c54af53dd49fd4f7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434500"
---
# <a name="return-cost-price-and-return-lot-id"></a>Returkostpris og returparti-ID        

[!include [banner](../includes/banner.md)]



Kostnaden for produkter som er returnert til lager, beregnes ved å bruke den gjeldende kostnaden av produkter. Du vil imidlertid kanskje at kostnadene for de returnerte produktene skal være lik kostnaden for produktene på tidspunktet da du solgte produktene til kunden. Du kan gjøre dette ved å bruke feltet **Returparti-ID** på hurtigfanen **Linjedetaljer** i **Salgsordre**-skjemaet.

Tenk deg for eksempel følgende scenario. Du fakturerer en kunde. Deretter returnerer kunden de leverte produktene til deg. Du kan returnere produkter til lager. I dette tilfellet når du krediterer kunden for de returnerte produktene, beregnes kostnaden for disse produktene ved å bruke gjeldende kostnader av produkter. Men hvis du bruker **Returparti-ID**-feltet, beregnes kostnaden for de returnerte produktene ved å bruke kostnaden på fakturaen til det opprinnelige salget til kunden.

Hvis du vil bruke en annen kostnad enn gjeldende kostnad for returer fra en kunde, kan du bruke en av følgende metoder.

## <a name="method-1-manually-enter-the-return-cost-price"></a>Metode 1: Angi den returnerte kostprisen manuelt

Som standard når du legger varer til en returordre blir varene returnert til lager med den gjeldende kostprisen. Bruk følgende fremgangsmåte for å angi en annen returkostpris.

1.  Klikk **Salg og markedsføring** \> **Vanlig** \> **Returordrer** \> **Alle returordrer**.

2.  I **handlingsturen** i **Ny**-gruppen klikker du **Returordre**.

3.  I skjemaet **Opprett returordre**, velg en kundekonto og klikk deretter **OK**.

4.  I skjemaet **Returordre - autorisasjonsreturnr.: %1, %2**, velg en vare, og angi et negativt antall i **Antall**-feltet.

5.  Klikk hurtigfanen **Linjedetaljer**.

6.  Gå til kategorien **Generelt**, og angi en verdi i feltet **Returkostpris**. Denne verdien brukes når varene er returnert til lager. Hvis du ikke angir en verdi, brukes den gjeldende kostprisen når varene er returnert til lager.

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a>Metode 2: Automatisk generere kostprisen, basert på kundefakturalinjen

Dette er den foretrukne metoden for å opprette returlinjer. Hvis du vil bruke kostnaden for produktene samtidig som da du solgte produktene til kunden, oppretter du en returordre og angir en salgslinje som skal returneres.

1.  Klikk **Salg og markedsføring** \> **Vanlig** \> **Returordrer** \> **Alle returordrer**.

2.  I **handlingsturen** i **Ny**-gruppen klikker du **Returordre**.

3.  I skjemaet **Opprett returordre**, velg en kundekonto og klikk deretter **OK**.

4.  I skjemaet **Returordre - autorisasjonsreturnr.: %1, %2**, i **Handlingsrute**, klikk **Søk etter salgsordre**.

5.  I skjemaet **Søk etter salgsordre** velger du fakturalinjen som skal returneres, og klikk deretter **OK**.
    
    På hurtigfanen **Linjedetaljer** på fanen **Generelt** viser feltet **Returparti-ID** verdien fra den opprinnelige salgslinjen. I tillegg viser feltet **Returkostpris** kostverdien fra den opprinnelige salgsordrelinjen.

## <a name="cost-calculation-example"></a>Eksempel på kostnadsberegning

Når du bruker feltet **Returparti-ID** i en returordrelinje for å angi den returnerte kostprisen, brukes kostnaden på returordrelinjen. Hvis du kjører funksjonen for lagerlukking eller omberegning, justeres kostnaden på den opprinnelige salgsordrelinjen. Kostnaden på returordrelinjen justeres automatisk for å gjenspeile den samme kostnaden per stykk.

1.  Opprett og frigi et produkt som heter Test. I skjemaet **Detaljer om frigitt produkt** angir du følgende informasjon:
    
    1.  På hurtigfanen **Styr kostnader** i feltet **Varegruppe** velger du **Deler**-gruppen.
    
    2.  På hurtigfanen **Generelt** i feltet **Varemodellgruppe** velger du **DEF**.
    
    3.  På hurtigfanen **Kjøp** i **Pris**-feltet skriver du inn 10,00 som kostprisen for varen.
    
    4.  I **handlingsruten** klikker du på **Dimensjonsgrupper**. I feltet **Lagringsdimensjonsgruppe** velger du **Bare område og lager**. I feltet **Sporingsdimensjonsgruppe** velger du **Ingen aktive sporingsdimensjoner**.

2.  Opprett en bestilling for 10 stykker av varen Test til 6,00 per enhet, og poster deretter en faktura for bestillingen.
    
    Opprett en ny bestilling for 10 stykker av varen Test til 8,00 per enhet, og poster deretter en faktura for bestillingen.

3.  Poster en faktura for en salgsordre for å selge fem stykker av varen Test.
    
    I dette tilfellet beregnes salgsordrelinjen til 35,00 (5 enheter \* 7,00 i gjennomsnittlig kostnad per enhet).

4.  Opprett en returordre for kunden. I skjemaet **Søk etter salgsordre** velger du fakturalinjen, og klikk deretter **OK**.

5.  I skjemaet **Returordre - autorisasjonsreturnr.: %1, %2** må du kontrollere at en returordre blir generert for å returnere varen Test. Antall for returordren er satt til -5,00.
    
    Feltet **Returparti-ID** viser en parti-ID. Denne parti-ID-en hentes fra den opprinnelige salgsordren til varen som ble solgt til kunden. Feltet **Returkostpris** viser kostprisen fra den opprinnelige salgsordrelinjen.

6.  Registrer mottaket av de returnerte varene.

7.  Poster en følgeseddel for de returnerte varene.

8.  Poster en faktura for returordren. På listesiden **Alle salgsordrer** velger du en salgsordre der **Returordre** er ordretypen.

9.  Åpne skjemaet **Lagertransaksjoner**. Kontroller at returen er kalkulert til 7,00 per enhet ved hjelp av verdien i feltet **Returkostpris**, for en total på 35,00 i **Kostnadsbeløp**-feltet. Du kan åpne skjemaet **Lagertransaksjoner** fra skjemaet **Returordre - autorisasjonsreturnr.: %1, %2**. I **Linjer**-rutenettet klikker du **Beholdning** \> **Transaksjoner**.

10. I lagerstyring kan du bruke skjemaet **Lukking og justering** til å kjøre prosedyren **3. Lukk**.
    
    Denne handlingen justerer kostnaden på den opprinnelige salgslinjen som ble kalkulert til -35,00 (5 enheter \* 7,00) til -30,00 (5 enheter \* 6,00). Dette er fordi lagermodellgruppen bruker først inn, først ut (FIFO), og 6,00 per enhet er FIFO-kostnaden fra den første bestillingen. I tillegg justerer handlingen kostnaden på retursalgslinjen, slik at den samsvarer med kostnaden per enhet i den opprinnelige salgslinjen. Derfor justeres kostnaden for returlinjen fra 35,00 til 30,00.




