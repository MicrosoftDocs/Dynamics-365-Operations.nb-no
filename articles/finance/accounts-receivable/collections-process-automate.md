---
title: Automatisering av innkrevingsprosess
description: Dette emnet beskriver prosessen med å definere strategier for innkrevingsprosesser som automatisk identifiserer kundefakturaer som krever en e-postpåminnelse, en innkrevingaktivitet eller en purring som skal sendes til kunden.
author: JodiChristiansen
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 59db852024faf457db7ac145b67619b31555aaf2
ms.sourcegitcommit: 3f6cbf4fcbe0458b1515c98a1276b5d875c7eda7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/10/2021
ms.locfileid: "7486875"
---
# <a name="collections-process-automation"></a>Automatisering av innkrevingsprosess

[!include [banner](../includes/banner.md)]

Dette emnet beskriver prosessen med å definere strategier for innkrevingsprosesser som automatisk identifiserer kundefakturaer som krever en e-postpåminnelse, en innkrevingaktivitet (for eksempel en telefonsamtale) eller en purring som skal sendes til kunden. 

Organisasjoner bruker ofte betydelig tid på å undersøke saldorapporter, kundekontoer og åpne fakturaer for å finne ut hvilke kunder som bør kontaktes om en åpen faktura eller kontosaldo. Denne undersøkelsen tar tid fra en innkrevingsagents tid som brukes til å kommunisere med kunder for å samle forfalte forfalte balanser eller løse fakturatvister. Ved hjelp av automatisering av innkrevingsprosess kan du sette opp en strategibasert tilnærming til innkrevingsprosessen. Dette hjelper deg med å bruke innkrevingsaktiviteter konsekvent ved å levere tilpassede e-postpåminnelser eller programmert prosess for å sende purringer. 

## <a name="collections-process-setup"></a>Oppsett av innkrevingsprosess
Du kan bruke siden **Oppsett av innkrevingsprosess** (**Kreditt og innkreving > Setup > Oppsett av innkrevingsprosess**) til å opprette en prosess for automatiserte innkrevinger som vil planlegge aktiviteter, sende e-postmeldinger og opprette og postere kundepurringer. Prosesstrinnene er basert på den ledende eller eldste fakturaen som er åpen. Hvert trinn bruker denne fakturaen for å bestemme hvilken kommunikasjon eller aktivitet som skal skje med en bestemt kunde.  

Innkrevingsteam sender vanligvis ut tidlig varsel knyttet til hver utestående faktura, slik at en kunde blir varslet når fakturaen er i ferd med å forfalle. Valget **Før purring** kan angis slik at ett trinn i hvert prosesshierarki kan gjøres oppmerksom på for hver faktura når fakturatiden når det trinnet.

### <a name="process-hierarchy"></a>Prosesshierarki
Hvert kundeutvalg kan bare tilordnes til ett prosesshierarki. Hierarkiets rangering av dette trinnet identifiserer hvilken prosess som vil ha forrang hvis en kunde inkluderes i mer enn ett utvalg som har fått tilordnet et prosesshierarki. Utvalgs-ID-en bestemmer hvilke kunder som skal tilordnes til prosessen. Hvert hierarki som er satt opp, kan bare tilordnes én prosessautomatsjon.

De rolige dagene brukes til å sikre at en kunde ikke blir kontaktet for ofte av den automatiserte prosessen. Hvis de rolige dagene for eksempel er satt til to, vil ikke en kunde bli kontaktet av den automatiserte prosessen på minst to dager, selv om den opprinnelige ledende fakturaen er utlignet i sin helhet. 

For å utelate kunder fra prosessautomasjonen hvis aldersfordeling for kunder eller fakturaer er mindre enn en definert verdi, velger du **Kundealdersfordelingssaldo mindre enn** eller **Fakturabeløp mindre enn** i feltet **Utelukk fra prosess**, og angir beløpsverdien.

Merk **Bruk forutsigelse** for å opprette samlingsaktiviteter ved hjelp av kundebetalingsforutsigelser. Aktivitetene som opprettes, vil bruke aktivitetsmalen fra **Betalingsforutsigelser** på siden **Kundeparametere** i kategorien **Automatisering av innkrevingsprosess**. 

### <a name="process-details"></a>Prosessdetaljer
Klikk **Ny** for å legge til en ny prosessdetalj i hierarkiet. **Beskrivelse** brukes til å identifisere formålet med eller navnet på trinnet i hierarkiet. Velg **Handlingstype** for å definere trinnet skal opprette en aktivitet, sende en e-post eller opprette en purring. 

- **Forretningsdokument** definerer malen som brukes til å opprette handlingstypen. Dette dokumentet kan være en aktivitetsmal, en e-postmal eller en purring som sendes til hver kunde. Automatisering av innkrevingsprosess oppretter bare purrebrev per kunde, uansett hvordan andre samlingsparametere er definert.
- **Når** definerer prosesstrinnet som skal skje før eller etter den innledende (eldste) forfallsdatoen for faktura, og brukes sammen med nummeret som vises i kolonnen **Dager i forhold til fakturaens forfallsdato**. 
- Merk av for alternativet **Varsel om purring** for å opprette en handling for hver faktura i ett trinn i et prosesshierarki. Varsel om purring-handlinger er vanligvis en tidlig varsel knyttet til utestående fakturaer, slik at en kunde kan bli varslet når en faktura er i ferd med å forfalle. Varsel om purring kan bare merkes for én aktivitet per hierarki. Når du velger en handlingstype for e-post, vil mottakeren bli brukt til å definere om e-postmeldingen sendes til en kunde-, salgsgruppe- eller inkassoagentkontakt. 
- Verdien i feltet **Kontakt for forretningsformål** bestemmer deretter hvilken kontakt fra kundens konto som skal motta kommunikasjonen.

### <a name="business-document-details"></a>Detaljer for forretningsdokument
Detaljene i forretningsdokumentet varierer, basert på handlingstypen som er valgt i prosessdetaljene. Når handlingstypen er en aktivitet, vil aktivitetsmaldetaljene vises. Disse detaljene omfatter navnet på aktivitetsmalen, typen aktivitet som blir opprettet, formålet med aktiviteten, antall dager som er planlagt for fullføring av aktiviteten, og detaljene for aktiviteten. Denne aktiviteten vil deretter koble til den ledende fakturaen som forteller mottakeren om handlingen som er nødvendig for å fullføre aktiviteten.

Hvis handlingstypen er en e-post i prosessdetaljene, vil denne delen inneholde to hurtigkategorier. Den første brukes til å definere mal-ID-en, e-postbeskrivelsen, standardspråket, brukernavnet som blir tilordnet e-postmeldinger som sendes automatisk, og de tilknyttede avsenderes e-postadresser. Det andre gjør det mulig å opprette brødteksten i e-postmeldingen etter at verdiene i feltene **Språk** og **Emne** er lagret ved å velge **Rediger**. Dette åpner et vindu som tillater at HTML-innhold lastes opp. 

> [!Note]
> Du kan lagre en Outlook-e-postmelding som inneholder hovedteksten for kommunikasjonen i HTML-format. Du kan deretter laste opp innholdet i meldingen for å implementere malen. <br> <br> Hvis handlingstypen for purring er valgt, vil det ikke være en detaljinndeling for forretningsdokument på oppsettssiden.

Bruk knappen **Innkrevingsprosesslogg** til å vise den nylige historikken for det valgte prosesshierarkiet. 

Klikk handlingen **Tilordning for innkrevingsprosess** for å vise kunder som er tilordnet en innkrevingsprosess. Bruk **Forhåndsvis kundetilordning** til å vise hierarkiet som en bestemt kunde er tilordnet. Bruk **Forhåndsvis prosesstilordning** til å forhåndsvise kundene som blir tilordnet et hierarki når den kjøres. Klikk **Manuell tilordning** for å vise kunder som manuelt er tilordnet til en prosess, eller velg kunder som skal tilordnes til en prosess.

Klikk handlingen **Prosessimulering** for å forhåndsvise handlingene som skal opprettes hvis den valgte prosessautomasjonen kjøres på dette tidspunktet. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
