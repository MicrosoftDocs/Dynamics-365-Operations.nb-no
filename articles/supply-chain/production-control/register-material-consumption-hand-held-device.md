---
title: Registrere materialforbruk med en mobil enhet
description: "Dette emnet beskriver en arbeidsflyt som aktiverer registrering av råvareforbruk i produksjonen ved hjelp av en håndholdt enhet."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 525b5a21047f0f39b9cd15448c4096d17c0e2dbd
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="register-material-consumption-using-a-mobile-device"></a>Registrere materialforbruk med en mobil enhet
Dette emnet beskriver en arbeidsflyt som aktiverer registrering av råvareforbruk i produksjonen ved hjelp av en håndholdt enhet.

<a name="introduction"></a>Introduksjon
------------

Denne arbeidsflyten er relevant hvis det er strenge krav til sporbarhet for materialer. For å vedlikeholde sporbarhet av materialet må det nøyaktige tidspunktet og antallet rapporteres for forbruk i slike tilfeller. Denne prosessen kan ses i motsetning til pre- eller backflushing-operasjoner, der det er en forskyvning mellom tidspunktet for registrering og tidspunktet når det faktiske forbruket finner sted. Dette emnet forklarer hvorfor en strategi for automatisk forbruk ikke kan brukes for noen materialer med krav til sporbarhet. La oss se på et enkelt scenario som forklarer hvordan du konfigurerer en arbeidsflyt for å aktivere registrering av råvareforbruk i produksjonen ved hjelp av en håndholdt enhet. [![opprett en arbeidsflyt for å aktivere registrering av råmaterialforbruk ved å bruke en håndholdt enhet](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a>Scenariodetaljer

En fortløpende produksjonsprosess (5) bruker partikontrollert råmateriale RM-100. Materialet er på lager på lokasjonen Bulk-001 (1) på nummerskilt PL-1 med to partier, B1 og B2, begge med et antall på 100 kilo. Lagerarbeid (2) er frigitt og behandlet for RM-100, og materialet er plukket fra Bulk-001 til produksjonsinnleveringssted PIL-01 (3), som er definert som ikke-nummerskiltkontrollert. Maskinoperatøren veier ut materialer fra produksjonsinnleveringsstedet (3) og registrerer vekten og partinummeret som er brukt (4). Fra produksjonsinnleveringsstedet legges en del av materialet manuelt til produksjonsprosessen i definerte tidsintervaller. Når maskinoperatøren legger til materiale, veies det på en vekt og partinummeret registreres.

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a>Definer arbeidsflyten til å registrere forbruk ved hjelp av en håndholdt enhet
Opprett et ferdigvareprodukt, FG-100, med en stykkliste som har det partikontrollerte råmaterialet RM-100. Legg til to partier, B1 og B2, av RM-100 i et antall på 100 til lokasjon: Bulk-001 på nummerskilt: PL-1. Trekkprinsippet på stykklistelinjen for RM-100 er satt til **manuell**. Angi produksjonsinnleveringsstedet til PIL-01. Du kan gjøre dette ved å velge denne lokasjonen som standard produksjonsinnleveringssted på lager 51.

1.  Opprett et nytt menyelement for mobilenhet: 

-    **Menyelementnavn** - Register materialforbruk. 
-    **Tittel** - Registrer materialforbruk. 
-    **Modus** - Indirekte. 
-    **Aktivitetskode** - Registrer materialforbruk.

2.  Legg til menyelementet på **Produksjonsmobil**-enhetsmenyen.
3.  Opprett en produksjonsordre for det ferdige produktet: 

-    **Varenummer** - FG-100 
-    **Område** - 5 
-    **Lager** - 51 
-    **Antall** - 150

Produksjonsordren blir **estimert** og **frigitt** og lagerarbeid opprettes.

4.  Fullfør arbeidet ved hjelp av arbeidsflyten for råvareplukking for den håndholdte enheten.

Dette tar materialet fra bulklokasjonen til produksjonsinnleveringsstedet PIL-01. Når arbeidet er fullført, har materialet statusen **Plukket på produksjonsinnleveringsstedet**. Statusen etter at arbeidet er behandlet, kan være enten **plukket** eller **fysisk reservert**. Dette er konfigurert med parameteren **Avgangsstatus etter plassering i lager-skjema**.

5.  Start produksjonsordren fra klienten eller den håndholdte enheten ved hjelp av menyelementet **Produksjonsstart**.

Etter at produksjonsordren er startet, kan du registrere materialforbruk i arbeidsflyten for den håndholdte enheten. La oss begynne med å registrere forbruk på 25 kilo av parti B1.

6.  Velg menyelementet **Registrer material****forbruk** på menyen for den håndholdte enheten, og angi følgende detaljer: 

-    Produksjonsordrenummeret. 
-    Lokasjonen der materialet skal forbrukes, i dette tilfellet PIL-01. 
-    Varenummer RM-100. 
-    Partinummer B1. 
-    Et antall på 25.

7.  Velg **OK**.

Legg merke til at meldingen "Journallinje er opprettet" vises på skjermen. På produksjonsordren finnes det en åpen journal av typen **Produksjonsplukkliste** for varenummer RM-100 og partinummer B1. 

Du kan nå velge å fortsette registreringen, for eksempel på partinummeret B2, og hver gang du velger **OK,** legges en ny journallinje til i den åpne journalen. 

Når du er ferdig med registreringen, velger du **Ferdig** for å postere journalen og avslutte arbeidsflyten.

### <a name="additional-comments"></a>Ekstra kommentarer 

-   Hvis en bruker avbryter arbeidsflyten når en journallinje er opprettet, er journalen i en ikke-postert tilstand, men hvis brukeren senere bruker arbeidsflyten for samme produksjonsordre, blir linjene lagt til i den åpne journalen i stedet for en ny journal.
-   Den nye arbeidsflyten støtter også for registrering av serienumre.
-   Det er bare mulig å registrere et varenummer som er definert i stykklisten eller formelen for den valgte produksjonsordren eller partiordren.
-   Materiale kan overforbrukes. Hvis for eksempel materialet er beregnet til bruk med et antall på 100 kilo, kan det bli overforbrukt med et antall på for eksempel 105 kilo.



