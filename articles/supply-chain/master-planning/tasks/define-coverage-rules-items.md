--- 
title: Definere dekningsregler for varer
description: "Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten."
author: YuyuScheller
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 76334f7ee4efe33df4a86aaa11a59748387cec89
ms.openlocfilehash: fe92393cc264df68f084db6974f7d4607d37d3ab
ms.contentlocale: nb-no
ms.lasthandoff: 11/02/2017

---
# <a name="define-coverage-rules-for-items"></a>Definere dekningsregler for varer

[!include [task guide banner](../../includes/task-guide-banner.md)]

Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Denne prosedyren viser hvordan du oppretter dekningsregler og overstyrer dekningsinnstillinger for en bestemt vare. Den viser også hvordan du kan angi standard lagerinnstillinger.


## <a name="create-a-coverage-group"></a>Opprette en dekningsgruppe
1. Gå til Dekningsgrupper.
2. Klikk Ny.
3. Skriv inn en verdi i Dekningsgruppe-feltet.
4. Skriv inn en verdi i Navn-feltet.
5. Skriv inn en verdi i feltet Kalender.
    * Velg kalenderen som hovedplanlegging bruker til å opprette forslag for etterfylling for varer i denne gruppen.  
6. I Dekningskode-feltet velger du et alternativ.
    * Velg Krav for denne prosedyren.  
7. Angi 90 i feltet Dekningshorisont (dager).
    * For varer i denne gruppen oppretter hovedplanleggingen etterfyllingsforslag for opptil 90 dager i fremtiden.  
8. Angi 1 i Negative dager-feltet.
9. Angi 1 i Positive dager-feltet.
10. Vis eller skjul delen Annet.
11. Angi 1 i feltet Påslag dager lagt til i behovsdato.
    * Hvis for eksempel mottaksmarginen er satt til 1 dag, og en bestillingslinje blir planlagt for mottak den 15. mai, beregner hovedplanleggingen den justerte mottaksdatoen som 16. mai.  
12. Angi 1 i feltet Sikkerhetsdager trukket fra behovsdato.
    * Hvis for eksempel mottaksmarginen er satt til 1 dag, og en bestillingslinje blir planlagt for mottak den 15. mai, beregner hovedplanleggingen den justerte mottaksdatoen som 14. mai.  
13. Angi 1 i feltet Respittid, gjenbestilling lagt til vareleveringstiden.
14. Klikk Lagre.

## <a name="create-a-new-product"></a>Opprett et nytt produkt
1. Gå til Frigitte produkter.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Produktnummer.
4. Skriv inn en verdi i feltet Produktnavn.
5. Klikk rullegardinknappen i feltet Varemodellgruppe for å åpne oppslaget.
6. Finn og velg ønsket post i listen.
7. Klikk koblingen i den valgte raden i listen.
8. Klikk rullegardinknappen i feltet Varegruppe for å åpne oppslaget.
9. Finn og velg ønsket post i listen.
10. Klikk koblingen i den valgte raden i listen.
11. Klikk rullegardinknappen i Lagringsdimensjonsgruppe-feltet for å åpne oppslaget.
12. Finn og velg ønsket post i listen.
13. Klikk koblingen i den valgte raden i listen.
14. Klikk rullegardinknappen i Sporingsdimensjonsgruppe-feltet for å åpne oppslaget.
15. Finn og velg ønsket post i listen.
16. Klikk koblingen i den valgte raden i listen.
17. Klikk OK.

## <a name="setup-default-order-settings"></a>Konfigurere standard ordreinnstillinger
1. Klikk Plan i handlingsruten.
2. Klikk Standard ordreinnstillinger.
3. Skriv inn området som brukes som standard ved opprettelse av bestillinger, i feltet Innkjøpssite.
4. Skriv inn området der varen lagres, i feltet Lagersite.
5. Vis eller skjul delen Beholdning.
6. Angi Flere til 10.
7. Angi Min. ordreantall til 10.
8. Angi Maks. ordreantall til 100.
9. Angi Standard ordreantall til 10.
10. Angi et tall i feltet Leveringstid for innkjøp.
11. Merk av eller fjern merket i avmerkingsboksen Virkedager.
12. Klikk Lagre.
13. Velg Bestilling i feltet Standard ordretype.
14. Klikk Lagre.
15. Lukk siden.
    * Lukk siden Standard ordreinnstillinger.  

## <a name="add-an-item-to-a-coverage-group"></a>Legge til en vare i en dekningsgruppe
1. Vis eller skjul delen Plan.
2. Klikk rullegardinknappen i Dekningsgruppe-feltet for å åpne oppslaget.
3. I listen finner du dekningsgruppen du har opprettet.
4. Klikk koblingen i den valgte raden i listen.

## <a name="create-item-coverage-rules"></a>Opprette varedekningsregler
1. Klikk Plan i handlingsruten.
2. Klikk Varedekning.
3. Klikk Ny.
4. Klikk kategorien Generelt.
5. Merk av i boksen i overskriften til Overstyr dekningsgruppeinnstillinger.
6. Angi 60 i feltet Dekningshorisont (dager).
    * Selv om varene i dekningsgruppen Krav er planlagt 90 dager frem i tid, blir elementet planlagt 60 dager frem i tid.  
7. Angi 2 i Negative dager-feltet.
8. Angi 2 i Positive dager-feltet.
9. Klikk kategorien Leveringstid.
10. Merk av i boksen i overskriften for Innkjøp.
11. Angi 5 i feltet Innkjøpstid.
12. Klikk Lagre.


