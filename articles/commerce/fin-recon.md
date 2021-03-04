---
title: Økonomisk avstemming i detaljhandelbutikker
description: Dette emnet beskriver økonomisk avstemming i detaljhandelbutikker for salgssted for Microsoft Dynamics 365 Commerce.
author: anpurush
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5d0520f35391f76b52fd8a333033b0d7ba4f7fe1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414533"
---
# <a name="financial-reconciliation-in-retail-stores"></a>Økonomisk avstemming i detaljhandelbutikker

[!include [banner](includes/banner.md)]

I Microsoft Dynamics 365 Commerce, versjon 10.0.10 og tidligere versjoner er det funksjonalitet på salgsstedsklienten som leverer prosesser på slutten av dagen i detaljhandelbutikker, der selgere og butikkledere utfører operasjoner på slutten av dagen. De kan for eksempel utføre kasseoppgjør, lukke usporede skift, avstemme skifttransaksjoner og lukke skift. Det er imidlertid ingen funksjon i salgsstedet for å fullføre finansinformasjonen for skift, slik at den kan brukes til å postere økonomien i Commerce Headquarters. Butikkledere er vanligvis ansvarlige for å fullføre denne oppgaven. Før de kan godkjenne et skift, må de se gjennom informasjonen, foreta eventuelle rettelser som kreves, og fullføre totalene for det skiftet. De fullførte totalene skal deretter posteres i finansmoduler i Commerce Headquarters.

I tillegg kan butikkledere i versjon 10.0.10 og tidligere versjoner gå gjennom og gjøre noen justeringer i utdragslinjer i Commerce Headquarters. Funksjonen er imidlertid begrenset, og butikkledere har sjelden tilgang til Commerce Headquarters-klienten. I tillegg kan du bare foreta finanshandelsutdrag og -justering når utdrag opprettes i Commerce Headquarters. Denne prosessen er imidlertid som regel en nattprosess. Derfor må butikkledere vente på skiftavloggingen når det opprettes finanshandelsutdrag i Commerce Headquarters.

I Commerce versjon 10.0.11 og senere kan butikkledere gå gjennom, justere og fullføre sine endringer i selve salgsstedsklienten. Disse dataene brukes deretter til å opprette og postere finanshandelsutdrag i Commerce Headquarters.

> [!NOTE]
> Funksjonaliteten som er relatert til økonomisk avstemming i detaljhandelsbutikker, fungerer bare hvis fordeling av feedbasert ordreoppretting er aktivert. Hvis du vil ha mer inforamsjon, kan du se [Fordele feedbasert ordreoppretting for detaljhandelstransaksjoner](trickle-feed.md).

## <a name="set-up-financial-reconciliation"></a>Definere økonomisk avstemming

Følg disse trinnene for å bruke funksjonaliteten for økonomisk avstemming.

1. I **Funksjonsstyring**-arbeidsområdet aktiverer du **Detaljhandelsutdrag – feedbasert**-funksjonen.
1. I funksjonalitetsprofilen for salgssted for den aktuelle butikken setter du **Aktiver økonomisk avstemming i butikk** til **Ja**.

## <a name="more-information-about-financial-reconciliation"></a>Mer informasjon om økonomisk avstemming

Når funksjonaliteten for økonomisk avstemming er aktivert, synkroniseres noen av parameterne som er definert i **Utdrag/lukking**-hurtigfanen på **Detaljhandelsbutikker**-siden i Commerce Headquarters, til kanaldatabasen. Det samme settet med beregningskriterier og beløpsterskler som brukes for detaljhandelsutdrag, blir håndhevet.

Når **Lukk skift**-operasjonen aktiveres, validerer systemet de systemberegnede beløpene og de deklarerte beløpene samsvarer. Hvis de er forskjellige, og differansen overskrider definerte terskler, blir brukeren bedt om å angi de nødvendige justeringene.

Justeringer kan gjøres for hvert betalingsmiddel. Når et betalingsmiddel er valgt, kan brukeren vise totalene for ulike transaksjonstyper og redigere totalene for en bestemt transaksjonstype. Under redigeringen viser systemet det opprinnelige beregnede beløpet og det overstyrte beløpet for transaksjonstypen. Brukeren kan også lagre notater som en del av redigeringsprosessen. Notater kan brukes til revisjonsformål.

Brukere kan ignorere spørsmål og meldinger om validering, og kan fortsette å lukke skiftet. Hvis en bruker imidlertid ignorerer valideringsbekreftelsene, vil de samme problemene forekomme og må korrigeres når skiftet posterer regnskapsoppgjør i Commerce Headquarters.

**Lukk skift**-operasjonen i salgsstedet validerer også at alle transaksjoner i den frakoblede databasen synkroniseres til kanaldatabasen. Hvis det ikke er synkroniserte transaksjoner, mottar brukeren en advarselsmelding, fordi denne situasjonen kan føre til at systembeløpene ikke blir riktig beregnet. I denne situasjonen kan brukeren avslutte **Lukk skift**-operasjonen og forsøke å synkronisere de frakoblede transaksjonene med kanaldatabasen. Brukeren kan også justere de systemberegnede beløpene manuelt for konto for transaksjonene som ikke er synkronisert, slik at det riktige settet med finansnumre er sluttført og postert. 

Når det brukes fordeling av feedbasert postering, slik at posteringen av transaksjoner atskilles fra posteringen av finans, kan du velge å justere de systemberegnede beløpene for manglende frakoblede transaksjoner. På denne måten sikrer du at økonomien alltid er lagt inn og postert på riktig måte, uavhengig av manglende transaksjoner. Frakoblede transaksjoner kan synkroniseres til kanaldatabasen og Commerce Headquarters, og deretter posteres senere, separat fra de økonomiske posteringene.

Detaljer om økonomisk avstemming for et skift synkroniseres til Commerce Headquarters ved hjelp av P-jobben.

Finanshandelsutdrag i Commerce Headquarters kan ikke beregne totaler til å vise detaljene på utdragslinjene. I stedet brukes de avsluttende beløpene i salgsstedsklienten til å opprette og postere finanshandelsutdrag.


[!INCLUDE[footer-include](../includes/footer-banner.md)]