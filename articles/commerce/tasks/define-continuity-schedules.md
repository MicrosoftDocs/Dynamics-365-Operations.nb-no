---
title: " Definere kontinuitetsplaner"
description: Denne artikkelen hjelper med å konfigurere et kontinuitetsprogram (også kjent som regelmessige ordrer).
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: faa55c844c8ee8742fbb0868b55a520cec6686aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885090"
---
# <a name="define-continuity-schedules"></a> Definere kontinuitetsplaner

[!include [banner](../includes/banner.md)]

Denne artikkelen hjelper med å konfigurere et kontinuitetsprogram (også kjent som regelmessige ordrer). Denne artikkelen bruker firmaet USRT i demonstrasjonsdataene.


## <a name="create-continuity-program"></a>Opprette kontinuitetsprogram
1. Gå til Detaljhandel og handel > Kontinuitet > Kontinuitetsprogrammer.
2. Klikk Ny.
3. I plan-ID-feltet skriver du inn ID-en for kontinuitetsplanen.
4. Velg Første hendelse i Ordrestart-feltet.
    * Hvis en kunde legger inn en ny ordre for kontinuitetsprogrammet, er det to alternativer for å sende produktet:  1. Første hendelse: det første produktet i kontinuitetsprogrammet vil bli levert.  2 Gjeldende hendelse: gjeldende produkt vil bli sendt. For eksempel. Tre måneder inn i programmet vil kunden motta det tredje i programmet.  
5. Velg Ja for å be om ordrestartdato.
6. Klikk Legg til linje.
7. Skriv inn varenummeret for det første produktet (0013) i Varenummer-feltet.
8. Skriv inn CP.
9. Angi datoen da det første produktet skal være tilgjengelig for ordre.
10. Klikk Legg til linje.
11. Skriv inn 0014 i Varenummer-feltet.
12. Fjern verdien i feltet Datointervallkode slik at feltet er tomt.
    * I denne prosedyren, fjern datointervallet. Du angir datoen som trinnvis fra startdatoen for den første varen.  
13. Her skal du angi intervallet for levering av produktene. Skriv inn 30.
    * For et månedlig program, skal du angi 30 dager for intervallet.  
14. Klikk Legg til linje.
15. Skriv inn 0015 i Varenummer-feltet.
16. Skriv inn Slutt.
17. Klikk Lagre.

## <a name="assign-to-continuity-item"></a>Tilordne til kontinuitetsvare
1. Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.
2. Velg vare 0016.
    * For denne fremgangsmåten velger du varenummer 0016. Du vil vanligvis ha opprettet et frigitt produkt med mer kontinuitetsforretningslogikk når det legges inn på en salgsordre i telefonsenteret.  
3. Klikk koblingen i den valgte raden i listen.
4. Klikk Rediger.
5. Vis eller skjul delen Selg.
6. Her skal du angi kontinuitetsprogrammet som denne varen representerer. Skriv inn tidsplan-ID-en du opprettet tidligere.
    * Når denne varen selges i et telefonsenter, brukes mer forretningslogikk fra det valgte kontinuitetsprogrammet.  
7. Klikk Lagre.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]