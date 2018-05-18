--- 
title: "Definere et menyelement for mobilenhet for å fullføre arbeid i en bestilling"
description: "Denne fremgangsmåten viser hvordan du definerer et Mobilenhet-menyelement."
author: BibiSp
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b80c258d6a779a8fc5bb6c846abd3af7e69d5e06
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-in-a-purchase-order"></a>Definere et menyelement for mobilenhet for å fullføre arbeid i en bestilling

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du definerer et Mobilenhet-menyelement. I dette eksemplet brukes menyelementet til å utføre arbeid av typen Bestilling. Arbeidsklassen som er tilknyttet menyelementet, bestemmer hvilket arbeid som er gyldig. Du kan bruke denne veiledningen i USMF-demodatafirmaet. Denne fremgangsmåten utføres av en lagersjef.


## <a name="create-a-mobile-device-menu-item"></a>Opprette et menyelement for mobilenhet
1. Gå til Menyelementer på mobilenheten.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Menyelementnavn.
    * Angi en unikt verdi. Du kan for eksempel skrive inn Bestillingsflytting. Husk verdien. Du trenger den senere.  
4. Skriv inn en verdi i Tittel-feltet.
    * Dette er tittelen som skal vises på mobilenheten. Du kan for eksempel skrive inn Bestillingsflytting.  
5. Velg Arbeid i feltet Modus.
6. Velg Ja i feltet Bruk eksisterende arbeid.
    * Dette menyelementet for mobilenheten brukes til å utføre eksisterende arbeid. Derfor må du sette denne verdien til Ja.  
    * Feltet Vis beholdningsstatus angir om beholdningsstatusen for i lagerbeholdningen vises for lagermedarbeideren på mobilenheten.  
7. Velg Systemgruppering i feltet Styrt av.
    * Når du velger noe i Styrt av-feltet, vises flere felt i Generelt-delen på denne siden. Feltene som vises, avhenger av hva du valgte. Når du velger Systemgruppering, legges to nye felt til. Disse er beskrevet nedenfor.  
8. Velg WorkPoolID i Systemgruppering-feltet.
    * Når lagermedarbeidere åpne dette menyelementet, blir de bedt om å skanne en ID for arbeidsutvalg. Alle arbeidsordrer med denne ID-en for arbeidsutvalg og åpne arbeidsordrelinjer med én av arbeidsklassene som er lagt til på dette menyelementet, overføres til brukeren.  
9. Skriv inn en verdi i feltet Systemgrupperingsetikett.
    * Denne teksten vises for brukerne på mobilenheten. Du kan for eksempel skrive inn Arbeidsutvalg.  
10. Velg Ja i feltet Overstyr nummerskilt under plassering.
    * Dette alternativet lar lagermedarbeidere overstyre målnummerskiltet når varer legges på en lokasjon som er styrt av nummerskilt.  
11. I feltet Gruppe plassert velger du Ja.
    * Hvis alle plasseringslinjene på arbeidsordren deler samme lokasjon, mottar brukeren en kombinert plasseringsinstruksjon for alle linjer.  
    * ID for revisjonsmal: En revisjonsmal lar det angi at arbeidsprosessen for et menyelement skal avbrytes, slik at en annen operasjon kan utføres. Hvis dette menyelementet for eksempel er for innkommende arbeid, kan revisjonsmalen kreve at arbeideren kontrollerer temperaturen. Punktet der prosessen avbrytes, er angitt i revisjonsmalen og kan for eksempel være når arbeid er startet eller fullført, eller når statusen endres.  
12. Utvid Arbeidsklasser-delen.
13. Klikk Ny.
14. Skriv inn Innkjøp i feltet Arbeidsklasse-ID.
    * Arbeidsutvalget begrenser arbeidet som menyelementet kan brukes til. I dette tilfellet vil det bli brukt for åpne arbeidsordrelinjene som har kjøp ID-en for innkjøpsarbeidsklasse.  
15. Klikk Lagre.

## <a name="set-up-work-confirmation"></a>Definere arbeidsbekreftelse
1. Klikk Arbeidsbekreftelsesoppsett.
2. Velg Plukk i Arbeidstype-feltet.
3. Merk av for Automatisk bekreftelse.
    * Arbeidsinstruksjonen med arbeidstypen Plukk bekreftes automatisk. Denne instruksjonen presenteres ikke for brukeren.  
4. Klikk Ny.
5. Velg Plasser i Arbeidstype-feltet.
6. Merk av for Lokasjonsbekreftelse.
    * Lagermedarbeideren vil bli bedt om å utføre en bekreftelsesskanning av lokasjonen når varen plasseres.  
7. Klikk Lagre.
8. Lukk siden.
9. Lukk siden.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Legge til menyelementet på en meny for mobilenhet
1. Gå til menyen Mobilenhet.
2. Klikk Rediger.
3. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Navn-feltet med verdien innkommende.
    * Du vil finne menyen for inngående menyelementer. I USMF kalles dette Inngående.  
4. Velg en verdi i treet.
5. Klikk på pilen som peker mot høyre.
6. Klikk Lagre.
7. Lukk siden.


