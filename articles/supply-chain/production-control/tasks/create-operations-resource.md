--- 
title: Opprette en operasjonsressurs
description: "En operasjonsressurs utfører aktivitetene for et prosjekt eller en produksjonsprosess."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e05eb5df2d29e90ed24fb13ed16543ad470dfe6b
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-an-operations-resource"></a>Opprette en operasjonsressurs

[!include[task guide banner](../../includes/task-guide-banner.md)]

En operasjonsressurs utfører aktivitetene for et prosjekt eller en produksjonsprosess. Denne prosedyren viser hvordan du definerer en operasjonsressurs. Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.

1. Gå til Ressurser.
2. Klikk Ny.
3. Skriv inn en verdi i Ressurs-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.

## <a name="define-capacity-and-consumption-parameters"></a>Definere parametere for kapasitet og forbruk
1. Utvid delen Operasjon.
2. Angi et nummer i Svinnprosent-feltet.
3. Angi eller velg en verdi i Oppsettkategori-feltet.
    * Angi kostkategorien som definerer hvordan du kan ta hensyn til kostnadene for oppsett.  
4. Angi eller velg en verdi i Kjøretid-feltet.
    * Angi kostkategorien som definerer hvordan du kan ta hensyn til kostnadene for operasjonstid.  
5. Angi eller velg en verdi i Antallskategori-feltet.
    * Angi kostkategorien som definerer hvordan du kan ta hensyn til ressurskostnadene basert på produsert antall.  
6. Velg et alternativ i Kapasitetsenhet-feltet.
    * Angi enheten som skal brukes til å uttrykke kapasitet for operasjonsressursen.  
7. Angi et tall i Kapasitet-feltet.
8. Angi et tall i Effektivitetsprosent-feltet.
    * Angi effektiviteten som du forventer fra operasjonsressursen. Effektivitetsprosenten justerer produksjonen for operasjonsressursen, og påvirker tiden som er reservert for ressursen.  
9. Angi et tall i prosentfeltet for grovplanlegging.
    * Angi maksimumsprosenten av kapasiteten til operasjonsressursen du vil bruke til grovplanlegging.  
10. Velg Ja i Begrenset kapasitet-feltet.
    * Sett dette alternativet til Ja hvis operasjonsressursen skal planlegges på grunnlag av faktisk kapasitet som er tilgjengelig, og hvis eksisterende kapasitetsreservasjoner skal anses. Hvis dette alternativet er satt til Nei, antas operasjonsressursen å ha ubegrenset kapasitet, og ressursen kan være overbestilt.  
11. Velg Ja i Flaskehalsressurs-feltet.

## <a name="define-working-times"></a>Definere arbeidstider
1. Utvid seksjonen Kalendere.
2. Klikk Legg til.
3. Angi eller velg en verdi i Kalender-feltet.
    * Angi arbeidstidskalenderen som definerer kapasiteten (i timer) for ressursen.  
4. Finn og velg ønsket post i listen.
5. Klikk koblingen i den valgte raden i listen.

## <a name="define-resource-capabilities"></a>Definere ressursfunksjoner
1. Vis delen Muligheter.
2. Klikk Legg til.
    * En funksjon er muligheten for en operasjonsressurs til å utføre en bestemt aktivitet. Planleggingsmotoren tildeler ressurser ved å sammenligne ressurskravene for hver aktivitet med egenskapene til de tilgjengelige operasjonsressursene.  
3. Angi eller velg en verdi i Funksjon-feltet.
4. Angi et nummer i Nivå-feltet.
    * Angi ferdighetsnivået som ressursen behandler muligheten med.  
5. Angi et tall i Prioritet-feltet.
    * Angi prioriteten for operasjonsressursen med hensyn til kapasiteten. Når du planlegger etter prioritet, velges først operasjonsressursen med den høyeste prioriteten (lavest numerisk verdi).  

## <a name="assign-resource-to-resource-group"></a>Tilordne ressurs til ressursgruppe
1. Utvid seksjonen Ressursgrupper.
2. Klikk Legg til.
    * Ressursgruppen definerer området, produksjonsenheten og lagerkonteksten for operasjonsressurser. Operasjonsressursen kan bare planlegges når tilordnet til en ressursgruppe, og bare på området der ressursgruppen finnes.  
3. Angi eller velg en verdi i Ressursgruppe-feltet.
4. Angi eller velg en verdi i Innleveringssted-feltet.
    * Angi lagerlokasjonen der operasjonsressursen forbruker materialer.  


