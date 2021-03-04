---
title: Behandle rente
description: Denne prosedyren viser hvordan du oppretter, skriver ut og posterer rentenotaer.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 093fbd23f9fcaf62db9988a98a94b8cebf582768
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446417"
---
# <a name="process-interest"></a>Behandle rente

[!include [banner](../../includes/banner.md)]

Denne prosedyren viser hvordan du oppretter, skriver ut og posterer rentenotaer. Denne oppgaven bruker demonstrasjonsfirmaet USMF.


## <a name="set-up-interest-on-the-posting-profile"></a>Konfigurere rente i posteringsprofilen
1. I **navigasjonsruten** går du til > **Moduler > Kreditt og innkreving > Oppsett > Kundeposteringsprofiler**.
2. Klikk **Rediger**.
3. I **Oppsett**-hurtigfanen i **Rentekode**-feltet velger du en rentekode fra rullegardinlisten. Hvis du ikke vil beregne rente for transaksjoner ved hjelp av denne posteringsprofilen, lar du feltet stå tomt. I hurtigfanen **Tabellrestriksjoner** kan du endre måten renter behandles på. Hvis dette feltet er satt til Ja, beregnes rente for denne posteringsprofilen.  

## <a name="calculate-interest"></a>Beregn rente
1. I **navigasjonsruten** går du til > **Moduler > Kreditt og innkreving > Rente > Opprett rentenotaer**.
2. Du må velge transaksjonstypene du vil beregne rente for. Alle åpne transaksjoner for disse typene inkluderes i beregningen.  
3. Hvis du setter **Rente** til Ja, vil du beregne rente på rente. Du bør kontrollere lovene som gjelder for beregning av rente på rente før du inkluderer disse transaksjonene.  
4. I **Fra dato**-feltet angir du en dato som renten skal beregnes fra. Hvis du ikke angir en **Fra dato**, blir alle uposterte rentenotaer avbrutt og rente beregnes på nytt fra transaksjonsdatoen.
5. I **Til dato**-feltet angir du en dato som renten skal beregnes til.
6. Velg et alternativ i feltet **Bruk posteringsprofil fra**. Det finnes tre alternativer for posteringsprofil:
    - Konto – Bruk posteringsprofilen som er tilordnet kundekontoen for hver rentenota. 
    - Velg – Bruk posteringsprofilen som du velger i Posteringsprofil-feltet.
    - Transaksjon – Bruk den individuelle posteringsprofilen fra transaksjoner der rente er beregnet for hver rentenota. Transaksjoner som ikke har en tilordnet posteringsprofil, bruker posteringsprofilen som er angitt i Finans og merverdiavgift-området i Kundeparametere-skjemaet.  
7. Utvid hurtigfanen **Poster som skal inkluderes**.
8. Klikk **Filter**.
9. Angi en kunde-ID i **Kriterier**-feltet. Skriv for eksempel inn US-001.
6. Klikk **OK**.
7. Klikk **OK**.

## <a name="print-interest-notes"></a>Skriv ut rentenotaer
1. I **navigasjonsruten** går du til > **Moduler > Kreditt og innkreving > Rente > Gjennomgå og behandle rentenotaer**.
2. Velg Opprettet i **Status**-feltet.
3. Velg Ikke skrevet ut i feltet **Utskrevet**.
4. Klikk **Skriv ut**.
5. Utvid hurtigfanen **Poster som skal inkluderes**.
6. Klikk **OK**.
7. Lukk siden.

## <a name="post-the-interest-note"></a>Postere rentenotaen
1. Velg en rentenota som er klar til å posteres (statusen er opprettet).
2. Klikk **Poster**.
3. Angir posteringsdatoen for rentenotaen. Velg Ja hvis du vil opprette en økonomimodultransaksjon for hver rentenota. Hvis du ikke velger Ja, akkumuleres renten på alle rentenotaene for kunden og posteres til økonomimodulen i én transaksjon.  
4. Utvid hurtigfanen **Poster som skal inkluderes**.
5. Klikk **OK**.
6. Velg Postert i **Status**-feltet.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]