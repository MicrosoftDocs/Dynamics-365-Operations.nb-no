--- 
title: "Opprette en kjøpsavtale"
description: "Denne prosedyren fører deg gjennom oppretting av en kjøpsavtale."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 22a252d98da5415f50a1d6ffb28f57aae19b5d14
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-agreement"></a>Opprette en kjøpsavtale

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren fører deg gjennom oppretting av en kjøpsavtale. Dette gjøres vanligvis av en innkjøpssjef. Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Du må ha definert kjøpsavtaleklassifiseringer før du starter. Når du har opprettet en avtale, kan du bruke den når du oppretter en bestilling, og dette kopierer kjøpsavtalebetingelsene til hodet og linjene i rekkefølgen som er påvirket av avtalen.


## <a name="create-a-new-purchase-agreement"></a>Opprette en ny kjøpsavtale
1. Gå til Innkjøp og leverandører > Kjøpsavtaler > Kjøpsavtaler.
2. Klikk Ny.
3. Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.
4. Finn og velg ønsket post i listen.
5. Klikk koblingen i den valgte raden i listen.
6. Klikk rullegardinknappen i feltet Kjøpsavtaleklassifisering for å åpne oppslaget.
7. Finn og velg ønsket post i listen.
8. Klikk koblingen i den valgte raden i listen.
9. Utvid seksjonen Generelt.
10. Angi en dato i Utløpsdato-feltet.
    * Denne utløpsdatoen er standard for alle forpliktelseslinjene og bestemmer hvor lenge hver bestemte forpliktelse er gyldig.  
11. I feltet Dokumenttittel skriver du inn et navn for kjøpsavtalen.
    * La feltet Standardforpliktelse være satt til Produktantallsforpliktelse (eller endre det hvis det ikke er satt til dette).  
    * Standardforpliktelsesverdien bestemmer alternativene på avtalelinjene. Hvis du trenger en ny forpliktelsestype når du oppretter avtalelinjene, må du endre standard forpliktelsen i hodet.  Det finnes 4 forskjellige forpliktelser: Produktantallsforpliktelse - for et bestemt antall av et produkt; Produktverdiforpliktelse - for et bestemt valutabeløp for et produkt; Verdiforpliktelse for produktkategori - for et bestemt valutabeløp i en innkjøpskategori der beløpet kan være for en katalogvare eller en ikke-katalogvare; Verdiforpliktelse - for et bestemt valutabeløp som kan bli oppfylt av et et hvilket som helst produkt eller en hvilken som helst innkjøpskategori.  
12. Klikk OK.

## <a name="add-a-commitment"></a>Legge til en forpliktelse
1. Klikk Legg til linje.
2. Merk den valgte raden i listen.
3. Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.
4. Velg produktet du vil legge til en forpliktelse for.
5. Klikk koblingen i den valgte raden i listen.
6. Angi et tall i feltet Antall.
    * Dette er det totale antallet som du har avtalt å kjøpe fra leverandøren.  
7. Angi et tall i feltet Enhetspris.
8. Vis seksjonen Linjedetaljer.
9. Angi alternativet Maks. håndheves til Ja.
    * Maks. håndheves-alternativet begrenser bruken av forpliktelse. Du kan bare kjøpe opptil antallet som er angitt i Antall-feltet for linjen.  
10. Skjul Linjedetaljer-delen.

## <a name="add-header-conditions"></a>Legge til topptekstbetingelser
1. Klikk Alternativer i handlingsruten.
2. Klikk Bytt visning.
3. Klikk Hodevisning.
4. Utvid Vilkår-delen.
5. Klikk rullegardinknappen i Betalingsmåte-feltet for å åpne oppslaget.
    * Betalingsbetingelsene fra leverandørkontoen vises her som standard.       
6. Finn og velg ønsket post i listen.
7. Klikk koblingen i den valgte raden i listen.
8. Klikk rullegardinknappen i feltet Leveringsmåte for å åpne oppslaget.
9. Klikk koblingen i den valgte raden i listen.
10. Klikk rullegardinknappen i feltet Leveringsbetingelser for å åpne oppslaget.
11. Klikk koblingen i den valgte raden i listen.

## <a name="confirm-and-activate-the-agreement"></a>Kontrollere og aktivere avtalen
1. Klikk Kjøpsavtale i handlingsruten.
2. Klikk Bekreftelse.
    * Angi alternativet Merk avtale som gyldig som Ja.  
3. Klikk OK.
4. Klikk Kjøpsavtale i handlingsruten.
5. Klikk Innkjøpsavtalebekreftelser.
    * Med alternativet Forhåndsvis/Skriv ut kan du generere et dokument for kjøpsavtalen som du kan deretter skrive ut eller sende til leverandøren. Hvis du oppdaterer avtalen senere, og bekrefter den på nytt, vil begge versjoner vises her.  
6. Lukk siden.


