---
title: Definere prosesser for lageropptelling
description: Dette emnet beskriver konfigurasjonen av grunnleggende lageropptellingsprosesser ved å opprette en opptellingsgruppe og en opptellingsjournal.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c8550e539a1b3299d89ec2b13550a13e284d807
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961378"
---
# <a name="define-inventory-counting-processes"></a>Definere prosesser for lageropptelling

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver konfigurasjonen av grunnleggende lageropptellingsprosesser ved å opprette en opptellingsgruppe og en opptellingsjournal. Den viser også hvordan du aktiverer opptellingspolicyer på et lager- og varenivå. Disse oppgavene vil vanligvis utføres av en lagersjef. Det er nødvendig med noen eksisterende frigitte produkter og lagre. Hvis du bruker en demonstrasjonsdataselskap, kan du kjøre denne prosedyren i firmaet USMF med alle lagerførte varer.


## <a name="create-a-counting-group"></a>Opprette en opptellingsgruppe
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Lager > Opptellingsgrupper**.
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **Opptellingsgruppe**.
4. Skriv inn en verdi i **Navn**-feltet.
5. Velg et alternativ i **Opptellingskode**-feltet.

    - **Manuelt** – Tar med linjer hver gang du kjører jobben. Du kan med andre ord bestemme telleintervallet for tellegruppen.  
    - **Periode** - Tar med linjer for perioden i opptellingsjournalen når periodeintervallet er utløpt.  
    - **Null på lager** - Hvis lagerbeholdningen når null (0), genereres linjer i opptellingsjournalen når jobben kjøres. Hvis lagerbeholdningen når 0 etter en opptelling, genereres linjer neste gang du starter opptellingen.  
    - **Minimum** – Setter inn linjer i opptellingsjournalen hvis lagerbeholdningen er lik eller mindre enn angitt minimum.  
    - Valgfritt: Hvis du har angitt **Periode** i **Opptellingskode**-feltet, må du skrive inn intervallet for perioden i dette **Opptellingsperiode**-feltet. Enheten for intervaller er dager.  
    - Når du kjører jobben for oppretting av nye linjer i opptellingsjournalen, opprettes nye linjer på intervallet spesifisert i dette feltet, uavhengig av hvor ofte du kjører den samme jobben. Hvis **opptellingsperiode** for eksempel er satt til 7, og journallinjene sist ble generert for en telling den 1. januar, hvis en annen jobb startes den 5. januar, hvis det ikke har gått sju dager, genereres ingen linjer i journalen for periodeintervallet. Hvis du starter jobben på nytt 8. januar, genereres linjer for perioden i opptellingsjournalen siden det har gått 7 dager.  

6. Velg **Lagre**.

## <a name="create-a-counting-journal-name"></a>Opprette et navn på opptellingsjournal
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Journalnavn > Lager**.
2. Velg **Ny**.
3. Skriv inn en verdi i **Navn**-feltet.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Velg **Opptelling** i **Journaltype**-feltet. Valgfritt: Du kan velge en annen bilagsserie-ID hvis du vil ha en bestemt nummerserie for bilaget IDene som genereres når du oppretter opptellingsjournaler. Bilagsserier opprettes på **Nummerserier**-siden.  
6. Velg et alternativ i **Detaljnivå**-feltet.  

    - Dette er detaljnivået som brukes når journalen posteres.  
    - Valgfritt: Du kan endre verdien i Reservering-feltet. Dette er metoden som brukes til å reservere varer under opptelling.   
    - **Manuelt** – Varene reserveres manuelt i Reservering-skjemaet.  
    - **Automatisk** – Ordreantallet er reservert fra varens tilgjengelige lagerbeholdning.   
    - **Nedbryting** – reservasjonen er en del av hovedplanleggingen for transaksjonen.  

7. Velg **Lagre**.

## <a name="set-standard-counting-journal-name"></a>Angi standard navn på opptellingsjournal
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Parametere for beholdnings- og lagerstyring**.
2. Velg fanen **Journaler**.
3. På rullegardinmenyen for **Opptelling**-feltet velger du journalen du opprettet tidligere. Denne journalen blir deretter standard journalnavn for lagerjournaler av typen **Opptelling**.  
4. Velg fanen **Generelt**. Valgfritt: Velg dette alternativet hvis du vil låse en vare under opptellingsprosessen for å forhindre oppdateringer for følgesedler, plukklister eller plukklisteregistreringer  

## <a name="set-the-counting-policy-for-an-item"></a>Angi opptellingspolicyen for en vare
1. I navigasjonsruten går du til **Moduler > Behandling av produktinformasjon > Produkter > Frigitte produkter**.
2. I listen klikker du koblingen for varenummeret på produktet som du vil angi opptellingspolicyer for. Du må velge en vare som spores i beholdning. Et produkt som ikke er lagerført, kan ikke telles. Hvis du bruker demonstrasjonsdataselskapet USMF, kan du velge vare A0001.  
3. Velg **Rediger**.
4. Aktiver/deaktiver utvidelsen av delen **Administrer lager**.
5. På rullegardinmenyen for **Opptellingsgruppe**-feltet velger du opptellingsgruppen du opprettet tidligere. Dette produktet vil nå bli inkludert når journallinjer for lageropptelling opprettes ved hjelp av denne opptellingsgruppen.  
6. Velg **Lagre**.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Angi opptellingspolicyen for en vare i et bestemt lager
1. Velg **Administrer lager** på handlingsruten.
2. Velg **Lagervarer**.
3. Velg **Ny**.
4. På rullegardinmenyen for **Lager**-feltet velger du lageret du vil definere spesifikke opptellingspolicyer for.
5. Velg en opptellingsgruppe i rullegardinmenyen for **Opptellingsgruppe**. Du kan velge en bestemt opptellingsgruppe som skal gjelde for varen i det bestemte lageret som du har valgt. Når tellingen blir utført i dette lageret, overstyrer denne opptellingspolicyen den generelle opptellingspolicyen for varen.  
6. Velg **Lagre**.

