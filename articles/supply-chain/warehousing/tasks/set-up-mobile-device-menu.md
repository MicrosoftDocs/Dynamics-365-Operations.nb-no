---
title: Definere et menyelement for mobilenhet for å fullføre arbeid av typen Bestilling
description: Dette emnet viser hvordan du definerer et Mobilenhet-menyelement.
author: ShylaThompson
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5df02b1ab1ac5531d54641fd523e3e671d83395ec3d627a0aaf7b1f783e9ad24
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735045"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a>Definere et menyelement for mobilenhet for å fullføre arbeid av typen Bestilling

[!include [banner](../../includes/banner.md)]

Dette emnet viser hvordan du definerer et Mobilenhet-menyelement. I dette eksemplet brukes menyelementet til å utføre arbeid av typen Bestilling. Arbeidsklassen som er tilknyttet menyelementet, bestemmer hvilket arbeid som er gyldig. Du kan bruke denne veiledningen i USMF-demodatafirmaet. Denne fremgangsmåten utføres av en lagersjef.


## <a name="create-a-mobile-device-menu-item"></a>Opprette et menyelement for mobilenhet
1. Gå til **Menyelementer på mobilenheten** ved å angi det i søkefeltet.
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **Menyelementnavn**. Angi en unikt verdi. Du kan for eksempel skrive inn `POMove`. Husk verdien. Du trenger den senere.  
4. Skriv inn en verdi i **Tittel**-feltet. Dette er tittelen som skal vises på mobilenheten. Du kan for eksempel skrive inn `PO Move`.  
5. Velg **Arbeid** i feltet **Modus**.
6. Velg **Ja** i feltet **Bruk eksisterende arbeid**.
    - Dette menyelementet for mobilenheten brukes til å utføre eksisterende arbeid. Derfor må du sette denne verdien til **Ja**.  
    - Feltet **Vis beholdningsstatus** angir om beholdningsstatusen for i lagerbeholdningen vises for lagermedarbeideren på mobilenheten.  
7. Velg **Systemgruppering** i feltet **Styrt av**. Når du velger noe i **Styrt av**-feltet, vises flere felt i **Generelt**-delen på denne siden. Feltene som vises, avhenger av hva du valgte. Når du velger **Systemgruppering**, legges to nye felt til. Disse er beskrevet nedenfor.  
8. Velg **WorkPoolID** i **Systemgruppering**-feltet. Når lagermedarbeidere åpne dette menyelementet, blir de bedt om å skanne en ID for arbeidsutvalg. Alle arbeidsordrer med denne ID-en for arbeidsutvalg og åpne arbeidsordrelinjer med én av arbeidsklassene som er lagt til på dette menyelementet, overføres til brukeren.  
9. Skriv inn en verdi i feltet **Systemgrupperingsetikett**. Denne teksten vises for brukerne på mobilenheten. Du kan for eksempel skrive inn **Arbeidsutvalg**.  
10. Velg **Ja** i feltet **Overstyr nummerskilt under plassering**. Dette alternativet lar lagermedarbeidere overstyre målnummerskiltet når varer legges på en lokasjon som er styrt av nummerskilt.  
11. I feltet **Gruppe plassert** velger du **Ja**.
    - Hvis alle plasseringslinjene på arbeidsordren deler samme lokasjon, mottar brukeren en kombinert plasseringsinstruksjon for alle linjer. 
    - ID for revisjonsmal: En revisjonsmal lar det angi at arbeidsprosessen for et menyelement skal avbrytes, slik at en annen operasjon kan utføres. Hvis dette menyelementet for eksempel er for innkommende arbeid, kan revisjonsmalen kreve at arbeideren kontrollerer temperaturen. Punktet der prosessen avbrytes, er angitt i revisjonsmalen og kan for eksempel være når arbeid er startet eller fullført, eller når statusen endres.  
12. Utvid **Arbeidsklasser**-delen.
13. Velg **Ny**.
14. Skriv inn `Purchase` i feltet **Arbeidsklasse-ID**. Arbeidsutvalget begrenser arbeidet som menyelementet kan brukes til. I dette tilfellet vil det bli brukt for åpne arbeidsordrelinjene som har kjøp ID-en for innkjøpsarbeidsklasse.  
15. Velg **Lagre**.

## <a name="set-up-work-confirmation"></a>Definere arbeidsbekreftelse
1. Velg **Arbeidsbekreftelsesoppsett**.
2. Velg **Plukk** i **Arbeidstype**-feltet.
3. Merk av for **Automatisk bekreftelse**. Arbeidsinstruksjonen med arbeidstypen Plukk bekreftes automatisk. Denne instruksjonen presenteres ikke for brukeren.  
4. Velg **Ny**.
5. Velg Plasser i **Arbeidstype**-feltet.
6. Merk av for **Lokasjonsbekreftelse**. Lagermedarbeideren vil bli bedt om å utføre en bekreftelsesskanning av lokasjonen når varen plasseres.  
7. Velg **Lagre**.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Legge til menyelementet på en meny for mobilenhet
1. Gå til menyen **Mobilenhet** ved å angi det i søkefeltet.
2. Velg **Rediger**.
3. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på **Navn**-feltet med verdien **innkommende**. Du vil finne menyen for inngående menyelementer. I USMF kalles dette **Inngående**.  
4. Velg **en verdi** i treet.
5. Velg pilen som peker mot høyre.
6. Velg **Lagre**.
7. Lukk siden.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]