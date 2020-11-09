---
title: Opprette en innkjøpsgjentakelsesordre
description: Dette emnet viser hvordan du oppretter en gjentatt bestilling ved å kopiere linjer fra et tidligere bestillingsdokument til en ny eller eksisterende bestilling.
author: mkirknel
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bf5e92ad6bc62dd008a51aacca891cb7253a723
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018035"
---
# <a name="create-a-repeat-purchase-order"></a>Opprette en innkjøpsgjentakelsesordre

[!include [banner](../../includes/banner.md)]

Dette emnet viser hvordan du oppretter en gjentatt bestilling ved å kopiere linjer fra et tidligere bestillingsdokument til en ny eller eksisterende bestilling. Det finnes to metoder for å opprette gjentatte ordrer. Du kan bruke handlingene som er tilgjengelige på dokumentnivå i handlingsruten, eller du kan bruke linjedetaljhandlingene. handlinger på dokumentetnivå er hovedsaklig beregnet på å opprette en ny bestilling ved å legge til linjer og hodeinformasjon fra en annen ordre, mens linjedetaljerhandlingen er hovedsaklig for å legge til linjer i en eksisterende ordre. Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF. Denne oppgaven utføres vanligvis av en innkjøpsagent.


## <a name="create-a-new-repeat-purchase-order"></a>Opprette en gjentatt innkjøpsreturordre
1. I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Bestillinger > Alle bestillinger**. Først prøver vi alternativet for å kopiere informasjon til en ny ordre.  
2. Velg **Ny**.
3. Angi `US-101` i **Leverandørkonto** -feltet.
4. Velg **OK**.
5. Velg **Bestilling** i handlingsruten.
6. Velg **Fra alle**. Dette er siden der du kan kopiere fra eksisterende ordre til ordren din. Det finnes ulike alternativer for hvordan linjene kopieres og ulike typer dokumenter som du kan kopiere fra. Vi skal først se på alternativene for hvordan linjene kopieres. 
7. Utvid seksjonen **Parametere**.

    - **Antallsfaktor** -feltet er nyttig hvis du vil bruke et antall som er forskjellig fra det som er i ordren du kopierer fra. Hvis du for eksempel vil bestille to ganger antallet som er i linjene du kopierer fra, skriver du inn 2 i dette feltet, og systemet vil deretter legge til linjer der det opprinnelige antallet er doblet.  
    - **Snu fortegn** -feltet støtter også endring av det bestilte antallet ved å endre fortegnet for antallet for ordrelinjer som er lagt til. Dette kan være nyttig hvis du vil tilbakeføre en transaksjon, ved å opprette bestillingslinjer negerer transaksjonen. Dette alternativet velges automatisk når siden åpnes fra handlingen **Opprett kreditnota**.  
    - Alternativet **Kopier gebyrer** lar deg kopiere gebyrer til den nye ordren fra dokumentet du kopierer ordrelinjene fra.  
    - Alternativet **Beregn priser** bruker gjeldende priser og rabatter i stedet for å kopiere disse fra dokumentet du kopierer annen informasjon fra.  
    - Alternativet **Kopier presist** oppretter en nøyaktig kopi av verdiene i alle feltene i ordrehodet og linjene i dokumentet. Hvis det ikke er merket av for dette alternativet, brukes standardverdiene for mange av feltene som er relatert til leverandører og produkter, som om du oppretter den nye ordren manuelt. Hvis ordren du kopierer fra for eksempel har overstyrt standard fakturakonto for leverandøren, vil den samme fakturakontoen kopieres til bestillingen. Hvis du ikke velger alternativet **Kopier presist** , brukes i stedet standard fakturakonto for leverandøren på bestillingen.  
    - Alternativet **Slett innkjøpslinjer** sletter alle bestillingslinjene som allerede finnes på bestillingen som du kopierer til, før du bruker de nye linjene. Vær forsiktig når du bruker dette alternativet, siden dette sletter alle eksisterende linjer uten advarsel.  
    - Hvis du bruker alternativet **Kopier ordrehode** , trenger du ikke opprette hodeinformasjon manuelt på den nye bestillingen. Legg merke til at dette alternativet vil føre til at standardverdier brukes for feltene som er knyttet til leverandøren. Bruk alternativet **Kopier presist** hvis dokumentet du kopierer fra har ikke-standardverdier du vil kopiere.   
    - Du kan kopiere fra forskjellige dokumentkilder, og hver har en egen del på denne siden. Delen **Bestillinger** lar deg for eksempel kopiere fra eksisterende bestillinger.  

8. I delen **Bestillinger** velger du linjene du vil kopiere til utklippstavlen. Det er mulig å velge flere bestillingslinjer fra andre bestillinger og kopiere dem også til bestillingen. Det er også mulig å legge til linjer fra andre typer innkjøpsdokumenter. De neste trinnene går gjennom de ulike alternativene.  
9. Vis **Bekreftelse** -delen. Her kan du velge bestillingsbekreftelser å kopiere fra. Bestillingsbekreftelser identifiseres med tilhørende innkjøpsjournal-ID eller bestillings-ID.  
10. Vis **Produktkvitteringer** -delen. Her kan du velge produktkvitteringsjournaler å kopiere fra. Produktkvitteringsjournalene identifiseres med produktkvitteringsbilaget eller bestillings-ID-en.   
11. Vis **Fakturaer** -delen. Her kan du velge leverandørfakturaer å kopiere fra. Fakturaene identifiseres av fakturabilaget eller bestillings-ID-en.   
12. Vis delen **Valgte linjer eller topptekst som skal kopieres**. Denne visningen viser et sammendrag av alle dokumenter og linjer som du har valgt å kopiere til bestillingen.   
13. Velg **OK**. Linjene du valgte, er nå kopiert til den nye bestillingen.   

## <a name="copy-lines-to-an-existing-purchase-order"></a>Kopiere linjer til en eksisterende bestilling  

I stedet for å kopiere en hel ordre, er det mer vanlig å opprette en ny bestilling og fullstendig informasjon i bestillingshodet, og deretter kopiere enkeltlinjer fra eksisterende ordrer.  

1. Velg **Bestillingslinje**.
2. Velg **Fra alle**. Siden som åpnes, er identisk med den som ble vist før, men forskjellige alternativer er valgt når den åpnes fra ordrelinjevisningen. La oss gå gjennom parameterne.   
3. Utvid seksjonen **Parametere**.

    - Alternativet **Slett innkjøpslinjer** er ikke valgt. Dette betyr at du kan kopiere nye linjer til ordren uten å fjerne eksisterende linjer.   
    - Alternativet **Kopier ordrehode** er heller ikke valgt, siden vi bare legger til flere linjer til ordren.   
    - I dette eksemplet skal vi kopiere linjer fra en eksisterende bestilling.   

4. Velg linjen for den ønskede bestillingen. Legg merke til at linjen med enkeltordren i denne bestillingen også er valgt.  
5. Velg **OK**. Den ekstra ordrelinjen er lagt til bestillingen.  

