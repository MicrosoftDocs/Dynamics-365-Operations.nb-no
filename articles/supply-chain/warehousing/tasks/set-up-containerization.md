--- 
title: Definere containerbruk
description: "Denne fremgangsmåten beskriver hvordan du automatiserer containerbruken av laster i Lagerstyring."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: aeb7d956560c513c08d5e20dcf20989b49137a52
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-containerization"></a>Definere containerbruk

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten beskriver hvordan du automatiserer containerbruken av laster i Lagerstyring. Automatisert containerbruk oppretter containere og plukkarbeidet for forsendelser når en bølge behandles, og arbeidslinjer kan deles inn i antall som får plass i containerne. På denne måten kan lagermedarbeidere plukke varene direkte til den valgte containeren. Sammenlignet med den manuelle pakkeprosessen kan oppgaver som oppretting av beholdere, tilordning av varer og lukking av beholdere, automatiseres av systemet. Denne fremgangsmåten bruker USMF-demofirmaet og utføres av en lagersjef.


## <a name="set-up-a-wave-template"></a>Definere en bølgemal
1. Gå til Lagerstyring > Oppsett > Bølger > Bølgemaler.
2. Klikk Ny.
3. Angi en verdi i feltet Navn på bølgemal.
4. Skriv inn en verdi i feltet Beskrivelse av bølgemal.
5. Angi eller velg en verdi i Område-feltet.
6. Angi eller velg en verdi i feltet Lager.
7. Vis delen Metoder.
    * Valgte metoder-ruten viser metodene for den valgte bølgemaltypen. Bølgemalen må inneholde containerbruk-metoden.  
8. Finn og velg ønsket post i listen.
9. Skriv inn en verdi i feltet Bølgetrinn.
    * Angi en bølgetrinnkode for metoden som legges til, som kan være en hvilken som helst kode. Det er mulig å legge til metoden mer enn én gang og tilordne forskjellige bølgetrinnkoder. Hvis du vil gjøre dette, velg Kan gjentas for denne metoden på siden Bølgebehandlingsmetoder.  
10. Klikk Lagre.
11. Lukk siden.

## <a name="set-up-a-container-type"></a>Definere en containertype
1. Gå til Lagerstyring > Oppsett > Containere > Containertyper.
    * Du kan definere containerne på siden i Containertyper. Du kan konfigurere de fysiske målene til containere, inkludert taravekt, maksimumsvekt, maksimalt volum, lengde, bredde og høyde. I dette eksemplet har vi bokser med tre forskjellige størrelser.  
2. Klikk Ny.
3. Skriv inn en verdi i feltet Containertype.
4. Angi et tall i feltet Taravekt.
5. Angi et tall i feltet Maksimumsvekt.
6. Angi et tall i feltet Volum.
7. Angi et tall i feltet Lengde.
8. Angi et tall i feltet Bredde.
9. Angi et tall i feltet Høyde.
10. Skriv inn en verdi i feltet Beskrivelse.
11. Klikk Lagre.
12. Klikk Ny.
13. Skriv inn en verdi i feltet Containertype.
14. Skriv inn en verdi i feltet Beskrivelse.
15. Angi et tall i feltet Taravekt.
16. Angi et tall i feltet Maksimumsvekt.
17. Angi et tall i feltet Volum.
18. Angi et tall i feltet Lengde.
19. Angi et tall i feltet Bredde.
20. Angi et tall i feltet Høyde.
21. Klikk Lagre.
22. Klikk Ny.
23. Skriv inn en verdi i feltet Containertype.
24. Skriv inn en verdi i feltet Beskrivelse.
25. Angi et tall i feltet Taravekt.
26. Angi et tall i feltet Maksimumsvekt.
27. Angi et tall i feltet Volum.
28. Angi et tall i feltet Lengde.
29. Angi et tall i feltet Bredde.
30. Angi et tall i feltet Høyde.
31. Klikk Lagre.
32. Lukk siden.

## <a name="set-up-a-container-group"></a>Konfigurere en containergruppe
1. Gå til Lagerstyring > Oppsett > Containere > Containergrupper.
2. Klikk Ny.
    * Du kan definere logiske grupper med containertyper. Du kan angi rekkefølgen som containerne skal pakkes i og containernes fyllprosent for hver gruppe. Varens størrelsesdimensjoner brukes til å bestemme om den passer i en container. Containeren som er nærmest størrelsesdimensjonen for varen, brukes. Hvis du har flere containertyper i en gruppe, anbefaler vi at du ordner rekkefølgen etter størrelse, slik at den største containeren kommer først, som nummer 1 i rekkefølgen, og den minste containeren kommer sist.    
3. Skriv inn en verdi i feltet Containergruppe-ID.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk Ny.
6. Merk den valgte raden i listen.
7. Angi eller velg en verdi i feltet Containertype.
8. Klikk Ny.
9. Merk den valgte raden i listen.
10. Angi eller velg en verdi i feltet Containertype.
11. Klikk Ny.
12. Merk den valgte raden i listen.
13. Angi eller velg en verdi i feltet Containertype.
14. Klikk Lagre.
15. Lukk siden.

## <a name="set-up-a-container-build-template"></a>Definere en mal for containerversjon
1. Gå til Lagerstyring > Oppsett > Containere > Maler for containerbygging.
2. Klikk Ny.
    * Malen for containerbygging er basert hvilken av containerbrukprosessene som utføres. Hver mal for containerbygging definerer én containerbrukprosess som skal brukes som bølgemal. Alternativet Rediger spørring lar deg definere betingelsene som den valgte malen skal behandles etter. Du kan for eksempel bare kjøre containerbruk for bestemte kunder, produkter eller lagre, eller du kan legge til de tilsvarende spørringsområdene i malen. Feltet Bølgetrinnkode er hvordan en mal for containerbygging er knyttet til trinnene i en bølgemal. Når bølgen kjøres, fastsettes hvilke maler for containerbygging som brukes til å starte containerbruk. Feltet Grunnleggende spørringstyper bestemmer hva som skal pakkes og hva filterspørringen skal baseres på.  
3. Merk den valgte raden i listen.
4. Skriv inn en verdi i feltet Containermal-ID.
5. Angi eller velg en verdi i feltet Containergruppe-ID.
6. Skriv inn en verdi i feltet Bølgetrinn.
7. Merk av for Tillat oppdeling av plukking.
8. Klikk Lagre.
9. Klikk Begrensninger for containerkombinasjoner.
    * Blanding av brudd i kombinasjonslogikk lar deg definere regler for pakketildelingslinjer i containere. Hvis du for eksempel legger til feltet Varenummer når varer tildeles containere, opprettes en ny container når det er et nytt varenummer. Dette er vil hindre at ansatte pakker tildelingslinjer for to ulike kunder i den samme containeren.  
10. Klikk Ny.
11. Velg et alternativ i feltet Tabell.
12. Angi eller velg en verdi i feltet Feltvalg.
13. Klikk OK.


