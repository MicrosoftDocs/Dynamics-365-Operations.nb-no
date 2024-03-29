---
title: Opprette salgsordrefakturaer
description: Denne artikkelen beskriver hvordan du fakturerer en salgsordre, inkludert fletting av fakturaer og satsvis behandling.
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ff76eac54da6621d999d9b629fac920ba8de294
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778391"
---
# <a name="create-sales-order-invoices"></a>Opprette salgsordrefakturaer

[!include [banner](../../includes/banner.md)]

Denne artikkelen beskriver hvordan du fakturerer en salgsordre, inkludert fletting av fakturaer og satsvis behandling. Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.


## <a name="create-an-invoice-from-a-sales-order"></a>Opprette en faktura fra en salgsordre
1. Gå til **Navigasjonsrute > Moduler > Kunder > Ordrer > Salgsordrer som er sendt, men ikke fakturert**.
2. Velg en salgsordre fra listen. 
3. Klikk på **Faktura > Generer > Faktura** i **handlingsruten**. Legg merke til at denne salgsordren har flere følgesedler tilknyttet. Den viser bare ordet *flere* i stedet for følgeseddelnummeret.  
4. Utvid seksjonen **Parametere**.
    - Postering må settes til **Ja** for å postere fakturaen. Du kan også slå av postering, og du kan bare skrive ut fakturaen. Du kan imidlertid oppnå samme resultat ved å opprette en proformafaktura i stedet for en faktura.  
    - Dette alternativet brukes for satsvise jobber. Spørringen kjøres når den satsvise jobben kjøres.
5. Velg **Etter** i feltet **Skriv ut**.
6. Velg **Ja** for **Skriv ut faktura**. Utskriftsbehandling kan skrive ut flere eksemplarer av fakturaen, og også sende fakturaen via e-post som en PDF-fil.  
7. Velg **Summer** i feltet **Skriv ut tillegg**.
8. I feltet **Kontroller kredittgrense** velger du **Saldo**.
9. Klikk på **Avbryt**.

## <a name="combine-orders-into-a-single-invoice"></a>Kombinere ordrer til én enkelt faktura
1. Gå til **Navigasjonsrute > Moduler > Kunder > Ordrer > Alle salgsordrer**.
2. Finn en kunde som har flere fakturaer som er åpne.
3. Velg flere åpne salgsordrer fra samme kunde.
4. Klikk på **Faktura > Generer > Faktura** i **handlingsruten**.
5. Utvid seksjonen **Parametere**.
6. Velg **Alle** i **Antall**-feltet. Legg merke til at det finnes to fakturaer som er oppført i oversiktsdelen. Nå skal vi slå dem sammen til én enkelt faktura.  
7. I feltet **Samleoppdatering for** velger du **Fakturakonto**.
8. Klikk på **Ordne** for å slå sammen salgsordrene til én enkelt faktura. De to ordrene er nå slått sammen til én enkelt faktura.   
9. Klikk på **Avbryt**.
10. Klikk **Ja**.

## <a name="post-invoices-in-a-batch"></a>Postere fakturaer i en satsvis jobb
1. Gå til **Navigasjonsrute > Moduler > Kunder > Fakturaer > Partifakturering > Faktura**.
2. Klikk **Velg**.
3. Klikk **OK**.
4. Klikk på **Parti**.
5. Velg **Ja** i **Satsvis behandling**.
6. Klikk på **Regelmessighet**.
7. Velg **Dager**.
8. Klikk **OK**.
9. Klikk **OK**.
10. Klikk på **Avbryt**.
11. Klikk **Ja**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
