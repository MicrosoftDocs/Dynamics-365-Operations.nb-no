---
title: Frafalle, gjenoppta eller reversere rentegebyrer
description: Denne artikkelen beskriver hvordan frafall, gjenopptakelse og snudd avregning for renter og gebyrer.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustInterestJourList
audience: Application User
ms.reviewer: roschlom
ms.custom: 59461
ms.assetid: 25ec29f3-e3ea-4abb-bf6b-f6240873b315
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b50b6ad0abd566fbcaf9cf8ad36af69fb4b3e551
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814182"
---
# <a name="waive-reinstate-or-reverse-interest-fees"></a>Frafalle, gjenoppta eller reversere rentegebyrer

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan frafall, gjenopptakelse og snudd avregning for renter og gebyrer.

Du kan bruke knappene i kategorien **Innkrevning** på listesiden **Alle kunder** til å frafalle, tilbakeføre eller gjenoppta tillegg:

-   Frafalte tillegg blir ettergitt. Du kan frafalle et tillegg for eksempel hvis en kunde protesterer på tillegget og du ønsker å opprettholde et godt forretningsforhold med denne kunden.
-   Tilbakeførte tillegg forfaller på nytt. Du kan gjenoppta tillegg som tidligere var frafalt. Du må kanskje gjenoppta tillegg hvis du finner ut at de ikke skulle ha blitt frafalt.
-   Tilbakeførte tillegg fjernes fra en kundes konto, og de forfaller ikke lenger. Du kan tilbakeføre tillegg hvis for eksempel feil rentesats ble valgt for å beregne beløpet som en kunde skylder. Du kan bruke en separat prosess til å beregne rente på nytt og opprette en rentenota som inneholder nye tillegg for kunden.

Alle disse handlingene endrer en rentenota. En rentenota er et forretningsdokument som informerer kunder når renter eller tillegg er belastet kontoen. Når du frafaller eller tilbakefører renter eller gebyrer, opprettes en kreditnota eller justeringsfaktura automatisk for å utligne tilleggene. Hvis du gjenopptar frafalte tillegg, opprettes en faktura som har et debetbeløp, automatisk for å gjenoppta tilleggene som kunden skylder. Tabellen nedenfor beskriver resultatene av hver handling.

| Handling                                                                                                                                                                                                            | Resultat for kunden                                                                                             | Behandle                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Frafalle hele rentenotaer sammen med alle renter og tillegg som er inkludert. – eller – Velge og frafalle tillegg eller rentetransaksjoner som er en del av rentenotaer.                                        | Tilleggene blir ettergitt.                                                                                           | En kreditnota, eller justeringsfaktura, opprettes for kunden. Kreditnotaen brukes til automatisk å utligne rentenotaen, eller rentetransaksjonene eller tilleggene du valgte. Det utlignede beløpet er lik totalbeløpet for tilleggene, minus eventuelle tidligere betalinger fra kunden og minus eventuelle beløp som tidligere er frafalt eller avskrevet. Hvis beløpet i kreditnotaen overskrider beløpet som kunden skylder, kan du konvertere kreditnotaen til en leverandørfaktura. Du kan deretter gi en refundering til kunden.                                                       |
| Gjenoppta hele rentenotaer sammen med alle renter og tillegg som er inkludert. – eller – Velge og gjenoppta tillegg eller rentetransaksjoner som er en del av rentenotaer.                                | Det gjenopptatte beløpet forfaller på nytt.                                                                                     | En faktura som har et debetbeløp opprettes, og fakturaen utlignes automatisk mot tilleggene som tidligere var frafalt. De faktiske rentenotaene gjenopptas ikke. I stedet opprettes en faktura som viser beløpet som forfaller fra kunden. Kreditnotaene, eller justeringsfakturaene, som ble opprettet for å utligne frafalte rentenotaer, kan fortsatt eksistere hvis de ikke ble brukt til å utligne rentenotaene. Når dette skjer, annulleres de utestående kreditnotaene. Utestående kreditnotaer utlignes vanligvis automatisk når rentenotaer frafalles. En utestående kreditnota kan imidlertid eksistere hvis en kunde har betalt en rentenota, selv om kunden protesterte på tilleggene. |
| Tilbakeføre hele rentenotaer. – eller – Tilbakeføre valgte rentetransaksjoner som er en del av rentenotaer. **Obs!** Du kan ikke tilbakeføre et gebyr. Du kan imidlertid tilbakeføre en hel rentenota som inneholder et gebyr. | Tilleggene forfaller ikke lenger fra kunden. Tilleggene forfaller imidlertid igjen hvis du beregner renten på nytt. | Prosessen er den samme som prosessen for frafalte rentenotaer eller valgte rentetransaksjoner. En kreditnota, eller justeringsfaktura, opprettes for kunden. Denne kreditnotaen brukes til å utilgne rentenotaen automatisk. Du kan bruke en separat prosess til å beregne rente på nytt og opprette en ny rentenota.                                                                                                                                                                                                                                                                                                                                                                                              |

> [!NOTE] 
> Du kan også bruke en separat prosess for å avskrive misligholdt gjeld. Denne prosessen markerer alle kundetransaksjoner for utligning i stedet for å frafalle bare tilleggene som er del av rentenotaer.

## <a name="adjust-interest-for-invoices"></a>Justere rente for fakturaer
I tillegg til å justere rentenotaer kan du fjerne rentetillegg på fakturaer ved hjelp av en av prosessene nedenfor. Begge prosessene foretar også justeringer av de relaterte rentenotaene.

### <a name="correct-an-invoice-that-has-associated-interest"></a>Korrigere en faktura som har tilknyttet rente

Du kan korrigere en postert faktura som er inkludert i en rentenota. Denne prosessen kopierer detaljene fra den eksisterende fakturaen til en ny faktura, slik at bare ønskede korrigeringer blir utført. Fakturaen annulleres, og en ny faktura opprettes. Renter i transaksjonen tilbakeføres også på rentenotaen, hvis rentenotaen ble postert. 

Du kan gjøre rettelsen ved hjelp av **Rett faktura**-knappen i handlingsruten for fritekstfakturaen. Denne knappen er tilgjengelig bare hvis konfigurasjonsnøkkelen **Korreksjon av fritekstfaktura** er valgt.

### <a name="reverse-a-customer-transaction-that-has-associated-interest"></a>Tilbakeføre en kundetransaksjon som har tilknyttede renter

Du kan tilbakeføre en kundetransaksjon på en faktura hvis en faktura ble opprettet med feil. Hvis den tilbakeførte kundetransaksjonen har renter inkludert på en rentenota, og hvis rentenotaen ble postert, tilbakeføres renten for transaksjonen også på rentenotaen. Rentenotaen annulleres hvis den ikke er postert. 

Du kan tilbakeføre kundetransaksjoner ved hjelp av **Tilbakefør**-knappen på siden **Kundetransaksjoner**.

## <a name="waive-or-reinstate-interest-notes"></a>Frafalle eller gjenoppta rentenotaer
Du kan frafalle eller gjenoppta alle tilleggene på rentenotaene som du velger. Når du frafaller tillegg, kan ikke totalbeløpet som skal frafalles, overskride eventuelle beløpsgrenser som er angitt. Du kan bare gjenoppta en rentenota hvis den tidligere er frafalt. 

Du kan frafalle eller gjenoppta rentenotaer ved hjelp av **Rentenota**-knappen i kategorien **Innkrevning** på siden **Kunde**.

## <a name="waive-or-reinstate-interest-transactions"></a>Frafalle eller gjenoppta rentetransaksjoner
Du kan frafalle eller gjenoppta spesifikke rentetransaksjoner på en rentenota i stedet for å justere alle tilleggene på denne rentenotaen. Når du frafaller tillegg, kan ikke totalbeløpet som skal frafalles, overskride eventuelle beløpsgrenser som er angitt. Du kan bare gjenoppta en rentetransaksjon hvis den tidligere er frafalt. 

Du kan frafalle eller gjenoppta rentenotaer ved hjelp av **Transaksjonsrenter**-knappen i kategorien **Innkrevning** på siden **Kunde**.

## <a name="waive-or-reinstate-fees"></a>Frafalle eller gjenoppta gebyrer
Du kan frafalle eller gjenoppta spesifikke gebyrer på en rentenota i stedet for å justere alle tilleggene på denne rentenotaen. Når du frafaller tillegg, kan ikke totalbeløpet som skal frafalles, overskride eventuelle beløpsgrenser som er angitt. Du kan bare gjenoppta et gebyr hvis det tidligere er frafalt. 

Du kan frafalle eller gjenoppta rentenotaer ved hjelp av **Gebyr**-knappen i kategorien **Innkrevning** på siden **Kunde**.

## <a name="reverse-interest-notes"></a>Reverser rentenotaer
Du kan tilbakeføre alle tilleggene på rentenotaer som du velger. Tilbakeførte tillegg fjernes fra en kundes konto, og de forfaller ikke lenger. Når rentenotaen er tilbakeført, kan du beregne rente på nytt og opprette en ny rentenota. 

Du kan tilbakeføre rentenotaer ved hjelp av **Rentenota**-knappen i kategorien **Innkrevning** på siden **Kunde**.

## <a name="reverse-interest-transactions"></a>Tilbakeføre rentetransaksjoner
Du kan tilbakeføre alle rentetransaksjonene som du velger. Tilbakeførte tillegg fjernes fra en kundes konto, og de forfaller ikke lenger. Når transaksjonene er tilbakeført, kan du beregne rente på nytt og opprette en ny rentenota.

Du kan tilbakeføre rentetransaksjoner ved hjelp av **Transaksjonsrenter**-knappen i kategorien **Innkrevning** på siden **Kunde**.

## <a name="view-the-history-of-adjustments-for-charges-that-were-waived-reinstated-or-reversed"></a>Vise justeringshistorikken for tillegg som er frafalt, gjenopptatt eller tilbakeført
Du kan vise den detaljerte historikken for justeringer som er foretatt for rentenotaer, for eksempel brukeren som la inn justeringen, justeringstypen, beløpet og når justeringen ble lagt inn. Du ønsker for eksempel kanskje å vise de tidligere justeringene som er lagt inn for en rentenota, før du oppretter en ny rentenota. 

Du kan tilbakeføre rentetransaksjoner ved hjelp av **Historikk**-knappen i kategorien **Innkrevning** på siden **Kunde**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]