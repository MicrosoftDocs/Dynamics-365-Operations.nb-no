---
title: Bruke konfigurasjoner for modelltilordning for aggregerte beregninger på databasenivået
description: Dette emnet beskriver hvordan du utformer en ny konfigurasjon for ER-modelltilordning (elektronisk rapportering) og bruker innebygde ER-funksjoner for effektive aggregerte beregninger.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a392697f6b91bc6555d0d72d09ecd7da32e1a3f
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094271"
---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a>Bruke konfigurasjoner for modelltilordning for aggregerte beregninger på databasenivået

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten gir informasjon om hvordan du utformer en ny konfigurasjon for ER-modelltilordning (elektronisk rapportering) og bruker innebygde ER-funksjoner for effektive aggregerte beregninger. I denne prosedyren skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc. 

Denne fremgangsmåten er opprettet for brukere med rollen som Systemansvarlig eller Utvikler av elektronisk rapportering. Disse trinnene kan fullføres ved hjelp av hvilket som helst datasett.

 For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten ER forbedrer effektiviteten til aggregerte beregninger ved å utføre dem på databasenivå (del 1: Klargjøre konfigurasjoner).

1. Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.
2. Utvid Intrastat-modell i treet.
3. Velg Intrastat-modell\Intrastat-eksempeltilordning i treet.
4. Klikk på Utforming.
5. Klikk på Utforming.
6. Velg Dynamics 365 for Operations\Tabellposter i treet.
7. Klikk på Legg til rot.
    * Legg til en ny datakilde som representerer postene du vil gruppere.  
8. Skriv inn Transaksjoner i Navn-feltet.
    * Transaksjoner  
9. Skriv inn Intrastat i Tabell-feltet.
    * Intrastat  
10. Klikk på OK.
11. Velg Funksjoner\Grupper etter i treet.
    * Denne datakildetypen brukes til å introdusere en ny datakilde under kjøring for å gruppere poster og beregne nødvendige aggregeringer.  
12. Klikk på Legg til rot.
13. Skriv inn TransactionsGroups i Navn-feltet.
    * TransactionsGroups  
14. Klikk på Rediger gruppe etter.
15. Velg Transaksjoner i treet.
    * Velg den tillagte datakilden av typen "Postliste" som representerer postene du vil gruppere.  
16. Klikk på Legg til felt i.
17. Klikk på Hva skal grupperes.
18. Utvid Transaksjoner i treet.
19. I treet velger du Transaksjoner\Retning.
20. Klikk på Legg til felt i.
21. Klikk på Grupperte felt.
    * Velg feltet for å angi grupperingsnivået. Avhengig av valget returnerer datakilden under kjøring så mange grupper med transaksjoner som det finnes retningskoder som skal oppfylles i Intrastat-tabellen.  
22. Velg Transaksjoner\Invoice amount(AmountMST) i treet.
    * Velg feltet for å angi kilden for aggregeringsberegning.  
23. Klikk på Legg til felt i.
24. Klikk på Aggregeringsfelt.
25. Merk den valgte raden i listen.
26. Velg Sum i feltet Metode.
    * Velg aggregeringstypen.  
27. Skriv inn SumOfAmountMST i Navn-feltet.
    * Angi navnet på denne aggregeringen i den konfigurerte datakilden.  
28. Klikk på Lagre.
    * Legg merke til at "Utførelse på"-feltet angir at denne grupperingen skal utføres under kjøring i SQL-databasen.  
29. Lukk siden.
30. Klikk på OK.
31. Utvid Totaler i treet.
32. Utvid TransactionsGroups i treet.
33. Utvid TransactionsGroups\aggregert i treet.
34. Velg TransactionsGroups\aggregert\SumOfAmountMST i treet.
35. Velg 'Totaler\Total fakturaverdi(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')' i treet.
36. Klikk på Bind.
    * Basert på denne innstillingen vil denne datakilden beregne summen av verdiene i feltet "AmountMST" for hver gruppe med transaksjoner. Denne aggregeringsberegningen vil være tilgjengelig som elementet TransactionsGroups.aggregated.TotalAmount.  
37. Utvid TransactionsGroups i treet.
38. Velg TransactionsGroups i treet.
39. Klikk på Rediger.
40. Klikk på Rediger gruppe etter.
41. Utvid Transaksjoner i treet.
42. Velg Transaksjoner\Invoice amount(AmountMST) i treet.
43. Klikk på Legg til felt i.
44. Klikk på Aggregeringsfelt.
45. Merk den valgte raden i listen.
46. Velg Maks i feltet Metode.
47. Skriv inn MaxOfAmountMST i Navn-feltet.
48. Klikk på Lagre.
    * Utførelsen av GROUPBY-datakilder kan for øyeblikket oversettes til SQL-databasenivået med noen begrensninger. Oversettelse kan utføres for datakildene av typen "Postliste" eller datakilder representert som et uttrykk ved hjelp av FILTER-funksjonen. Den kan også gjøres når bare én aggregering er konfigurert for ett enkelt felt for grupperingspostene.  
    * Legg merke til at selv om mer enn én aggregering ble konfigurert for feltet AmountMST, angir "Utførelse på"-feltet fremdeles at denne grupperingen vil bli utført under kjøring i SQL-databasen. Dette er fordi bare én aggregering er bundet til datamodellelementet og skal brukes under kjøring til å hente data fra denne datakilden.  
49. Lukk siden.
50. Klikk på OK.
51. Utvid TransactionsGroups i treet.
52. Utvid TransactionsGroups\aggregert i treet.
53. Velg 'TransactionsGroups\aggregert\MaxOfAmountMST' i treet
54. Velg 'Totaler\Total statistisk verdi(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')' i treet.
55. Klikk på Bind.
56. Utvid TransactionsGroups i treet.
57. Velg TransactionsGroups i treet.
58. Klikk på Rediger
59. Klikk på Rediger gruppe etter.
    * Legg merke til at "Utførelse på"-feltet angir at denne grupperingen vil bli utført under kjøring i minnet fordi begge aggregeringene for det samme feltet er bundet til datamodellelementene.   
60. Merk eller fjern merking for alle rader i listen.
61. Klikk på Slett.
62. Klikk på Ja.
63. Klikk på Slett.
64. Klikk på Ja.
65. Klikk på Legg til felt i.
66. Klikk på Hva skal grupperes.
67. Utvid 'Artikkelpost(Intrastat)' i treet.
68. Klikk på Lagre.
    * Legg merke til at "Utførelse på"-feltet angir at denne grupperingen vil bli utført under kjøring i minnet selv om det ikke er definert noen aggregeringer og den valgte datakilden av typen Tabellposter refererer til den samme Intrastat-tabellen. Dette skyldes at datakilden inneholder enkelte beregnede felt som ennå ikke kan oversettes til SQL-databasenivået.  

