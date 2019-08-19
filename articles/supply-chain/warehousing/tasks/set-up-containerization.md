---
title: Definere containerbruk
description: Dette emnet beskriver hvordan du automatiserer containerbruken av laster i Lagerstyring.
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/19
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba435ee145a8516391d7864bdfe338b0f3862f49
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847213"
---
# <a name="set-up-containerization"></a>Definere containerbruk

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emnet beskriver hvordan du automatiserer containerbruken av laster i Lagerstyring. Automatisert containerbruk oppretter containere og plukkarbeidet for forsendelser når en bølge behandles, og arbeidslinjer kan deles inn i antall som får plass i containerne. På denne måten kan lagermedarbeidere plukke varene direkte til den valgte containeren. Sammenlignet med den manuelle pakkeprosessen kan oppgaver som oppretting av beholdere, tilordning av varer og lukking av beholdere, automatiseres av systemet. Denne fremgangsmåten bruker USMF-demofirmaet og utføres av en lagersjef.


## <a name="set-up-a-wave-template"></a>Definere en bølgemal
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Bølger > Bølgemaler**.
2. Velg **Ny**.
3. Angi en verdi i feltet **Navn på bølgemal**.
4. Skriv inn en verdi i feltet **Beskrivelse av bølgemal**.
5. Angi eller velg en verdi i **Område**-feltet.
6. Angi eller velg en verdi i feltet **Lager**.
7. Vis delen **Metoder**. **Valgte metoder**-ruten viser metodene for den valgte bølgemaltypen. Bølgemalen må inneholde containerbruk-metoden.  
8. Skriv inn en verdi i feltet **Bølgetrinn**. Angi en bølgetrinnkode for metoden som legges til, som kan være en hvilken som helst kode. Det er mulig å legge til metoden mer enn én gang og tilordne forskjellige bølgetrinnkoder. Hvis du vil gjøre dette, velg **Kan gjentas for denne metoden** på siden **Bølgebehandlingsmetoder**.  
9. Velg **Lagre**.
10. Lukk siden.

## <a name="set-up-a-container-type"></a>Definere en containertype
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Containere > Containertyper**. Du kan definere containerne på siden i **Containertyper**. Du kan konfigurere de fysiske målene til containere, inkludert taravekt, maksimumsvekt, maksimalt volum, lengde, bredde og høyde. I dette eksemplet har vi bokser med tre forskjellige størrelser.  
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **Containertype**.
4. Angi et tall i feltet **Taravekt**.
5. Angi et tall i feltet **Maksimumsvekt**.
6. Angi et tall i feltet **Volum**.
7. Angi et tall i feltet **Lengde**.
8. Angi et tall i feltet **Bredde**.
9. Angi et tall i feltet **Høyde**.
10. Skriv inn en verdi i **Beskrivelse**-feltet.
11. Velg **Lagre**.
13. Gjenta trinn 2-11 to ganger til for å lage totalt tre containertyper.
14. Lukk siden.

## <a name="set-up-a-container-group"></a>Konfigurere en containergruppe
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Containere > Containergrupper**.
2. Velg **Ny** i handlingsruten. Du kan definere logiske grupper med containertyper. Du kan angi rekkefølgen som containerne skal pakkes i og containernes fyllprosent for hver gruppe. Varens størrelsesdimensjoner brukes til å bestemme om den passer i en container. Containeren som er nærmest størrelsesdimensjonen for varen, brukes. Hvis du har flere containertyper i en gruppe, anbefaler vi at du ordner rekkefølgen etter størrelse, slik at den største containeren kommer først, som nummer 1 i rekkefølgen, og den minste containeren kommer sist.    
3. Skriv inn en verdi som du opprettet tidligere, i feltet **Containergruppe-ID** .
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Gjenta trinn 2-4 for alle de tre containertypene du opprettet tidligere.
6. Velg **Lagre**.
7. Lukk siden.

## <a name="set-up-a-container-build-template"></a>Definere en mal for containerversjon
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Containere > Maler for containerversjoner**.
2. Velg **Ny**. Malen for containerbygging er basert hvilken av containerbrukprosessene som utføres. Hver mal for containerbygging definerer én containerbrukprosess som skal brukes som bølgemal. Alternativet **Rediger spørring** lar deg definere betingelsene som den valgte malen skal behandles etter. Du kan for eksempel bare kjøre containerbruk for bestemte kunder, produkter eller lagre, eller du kan legge til de tilsvarende spørringsområdene i malen. Feltet **Bølgetrinnkode** er hvordan en mal for containerbygging er knyttet til trinnene i en bølgemal. Når bølgen kjøres, fastsettes hvilke maler for containerbygging som brukes til å starte containerbruk. Feltet Grunnleggende spørringstyper bestemmer hva som skal pakkes og hva filterspørringen skal baseres på. 
3. Skriv inn en verdi i feltet **Containermal-ID**.
4. Angi eller velg en verdi i feltet **Containergruppe-ID**.
5. Skriv inn en verdi i feltet **Bølgetrinn**.
6. Merk av for **Tillat oppdeling av plukking**.
7. Velg **Lagre**.
8. Velg **Begrensninger for containerkombinasjoner.** Blanding av brudd i kombinasjonslogikk lar deg definere regler for pakketildelingslinjer i containere. Hvis du for eksempel legger til feltet **Varenummer** når varer tildeles containere, opprettes en ny container når det er et nytt varenummer. Dette er vil hindre at ansatte pakker tildelingslinjer for to ulike kunder i den samme containeren.  
9. Velg **Ny**.
10. Velg et alternativ i feltet **Tabell**.
11. Angi eller velg en verdi i feltet **Feltvalg**.
12. Velg **OK**.

