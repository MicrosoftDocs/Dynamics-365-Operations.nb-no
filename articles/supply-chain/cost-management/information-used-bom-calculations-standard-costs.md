---
title: Informasjon som brukes i stykklisteberegninger med standardkostnader
description: Stykklisteberegninger benytter seg av data fra flere kilder for å beregne standard kostpris for en produsert vare. Kildene inneholder informasjon om varer, stykklisteruter, beregningsformler for indirekte kostnader og etterkalkuleringsversjonen.
author: AndersGirke
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcGroup, BOMCalcTable, ProdParmBOMCalc
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 65571
ms.assetid: ca17e6dd-b16a-4bbc-8682-b16345ab9906
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ec6ffe41d6dae10693b1a1ebd6e5012c32bc2e6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "333766"
---
# <a name="information-used-in-bom-calculations-with-standard-costs"></a>Informasjon som brukes i stykklisteberegninger med standardkostnader

[!include [banner](../includes/banner.md)]

Stykklisteberegninger benytter seg av data fra flere kilder for å beregne standard kostpris for en produsert vare. Kildene inneholder informasjon om varer, stykklisteruter, beregningsformler for indirekte kostnader og etterkalkuleringsversjonen.

Informasjonen om innkjøpte varer som brukes i stykklisteberegninger for standard kostpris, er blant annet:
-   Kost − En innkjøpt vares kost vedlikeholdes som stedsbestemte kostnadsposter i en etterkalkuleringsversjon for standard kostpriser. Hver kostnadspost har et datointervall, og datoen for stykklisteberegning bestemmer hvilken kostnadspost som skal brukes. For eksempel kan en stykklisteberegning med en fremtidig beregningsdato bruke en kostnadspost med uavsluttet status og et datointervall i fremtiden.
-   Kostnadsgruppe − Kostnadsgruppen som er tilordnet til en innkjøpt vare, danner grunnlaget for kostnadssegmentering i de beregnede kostnadene for en produsert vare.
-   Advarselsbetingelser som er innebygd i varens stykklisteberegningsgruppe gjør at stykklisteberegningene kan identifisere potensielle problemer. Dette kan være når den innkjøpte varen har null i kost, null i antall i en stykkliste eller en kostnadspost. Gjeldende advarselsbetingelser kan overstyres når en stykklisteberegning initialiseres.

Informasjonen om produserte varer som brukes i stykklisteberegninger for standard kostpris, er blant annet:
-   Standard ordreantall for lager − Varens standard ordreantall (for lager) fungerer som en standard regnskapspartistørrelse for nedbetaling av konstantkostnader i en stykklisteberegning. Regnskapspartistørrelsen vil også gjenspeile bestillingsmultiplumsantallet hvis dette er angitt.
-   Advarselsbetingelser som er innebygd i varens stykklisteberegningsgruppe gjør at stykklisteberegningene kan identifisere potensielle problemer. Ett eksempel kan være at den produserte varen ikke har en stykkliste eller rute. Gjeldende advarselsbetingelser kan overstyres når en stykklisteberegning initialiseres.

Informasjonen om stykklister som brukes i stykklisteberegninger for standard kostpris, er blant annet:
-   Stykklisteversjon − Stykklisteversjonen som er tilordnet til den produserte varen har et datointervall som er angitt med en fra-dato og en til-dato, og en status for godkjent og aktiv. Stykklisteversjonen kan gjelde for hele firmaet eller være stedsbestemt, og om ønskelig kan den gjenspeile avbruddspunkter for antall.
-   Stykklistelinjevareantall − En komponent krever vanligvis et variabelt antall, men antallet kan også være en konstant. Komponentantallet uttrykkes vanligvis for produksjon av én overordnet vare, men den kan også uttrykkes per 100 eller per 1000 av hensyn til presisjon i desimaler. Komponentantallet kan også beregnes på grunnlag av mål.
-   Stykklistelinjevaresvinn − En komponent kan ha et variabelt eller konstant antall for planlagt svinn.
-   Gyldige datoer for stykklistelinjevarer − En komponent kan ha en gyldig fra-dato og en gyldig til-dato.
-   Produksjonstype for stykklistelinjevarer − Kostnadspartistørrelsen for nedbetaling av konstante kostnader vil gjenspeile antallet for stykklisteberegningen og produksjon-etter-ordre-nedbrytingsmodus, fordi stykklisteberegningen forutsetter at den produserte varen produseres i nøyaktig antall (i stedet for i standard ordreantall).
-   Delstykkliste for en produsert komponent − En produsert komponent kan om ønskelig ha en angitt stykklisteversjon, som i så fall kan brukes i stedet for den gjeldende stykklisteversjonen som er aktiv for varen i en stykklisteberegning.
-   Underrute for en produsert komponent − En produsert komponent kan om ønskelig ha en angitt ruteversjon, som i så fall kan brukes i stedet for den gjeldende ruteversjonen som er aktiv for varen i en stykklisteberegning.
-   Operasjonsnummer og virkninger på svinnprosenter i operasjonen − Operasjonsnummeret knytter en komponent til en bestemt operasjon, og operasjoner kan ha en svinnprosent. Denne tilknytningen gjør at stykklisteberegninger kan ta hensyn til svinnprosenter og kumulative svinnprosenter (på tvers av flere operasjoner) for komponentens behovsantall.
-   Ignorer stykklistelinjevare i kostnadsberegninger − En komponent kan ignoreres til stykklisteberegningsformål.

Operasjonsressursinformasjonen som brukes i stykklisteberegninger for standard kostpris inkluderer:
-   Timekostnader − Timekostnadene som er knyttet til en operasjonsressurs, uttrykkes som kostnadskategorier som er tilordnet til oppsetttid og kjøretid. Disse kostnadskategoriene bør identifiseres for ressursgrupper og operasjonsressurser. Timekostnadene som er tilordnet en kostnadskategori kan være stedsbestemte eller gjelde hele firmaet.
-   Per enhet-kostnader − I noen produksjonsmiljøer tilordnes operasjonsressurskostnader per enhet som produseres, som kan uttrykkes som en forskjellig kostnadskategori for antall. For eksempel kan kostnader som er knyttet til antall, reflektere stykkavlønning for arbeid, eller en malingprodusent kan tilordne operasjonsressurskostnader per liter maling som produseres.
-   Overstyre operasjonsressursinformasjon på ruteoperasjoner − Ressursinformasjonen om kostnadskategorier arves av operasjoner, der den kan overstyres. Stykklisteberegninger vil bruke kostnadskategoriinformasjonen som angis for ruteoperasjonene.
-   Kostnadsgruppe for en kostnadskategori − Kostnadsgruppen som er tilordnet en kostnadskategori sørger for kostnadssegmentering i de beregnede kostnadene for en produsert vare. For eksempel kan forskjellige kostnadsgrupper brukes til å segmentere de beregnede kostnadene som er tilordnet maskiner og arbeid eller oppsett- og kjøretid.

Ruteinformasjonen som brukes i stykklisteberegninger for standard kostpris inkluderer:
-   Ruteversjon − Ruteversjonen som er tilordnet den produserte varen, har gyldig fra- og gyldig til-datoer, og en status for godkjent og aktiv. Ruteversjonen må være stedsbestemt, og om ønskelig kan den gjenspeile avbruddspunkter for antall.
-   Ruteoperasjonstid − Tiden kan angis for kjøretid og oppsettid. Tiden målt i timer uttrykkes vanligvis for produksjon av én overordnet vare, men den kan også uttrykkes per 100 eller per 1000 av hensyn til presisjon i desimaler.
-   Ruteoperasjonstid for sekundære ressurser − En sekundær ressurs har det samme operasjonsnummeret som den primære ressursen, og den har den samme ruteoperasjonstiden. For eksempel kan en operasjon kreve en maskin som den primære ressursen og arbeid og verktøy som sekundære ressurser.
-   Svinnprosent for ruteoperasjoner − Stykklisteberegninger vil ta hensyn til svinnprosenter og kumulative svinnprosenter på tvers av flere operasjoner. Dette gjelder for tiden som kreves i ruteoperasjoner og behovsantallet for komponenter som er knyttet til operasjonsnumre.
-   Kostnadskategorier for en ruteoperasjon − Operasjonsressursinformasjonen om kostnadskategorier arves av operasjoner, der den kan overstyres. Stykklisteberegninger vil bruke kostnadskategoriinformasjonen som angis for ruteoperasjonene.

Informasjonen om administrasjonskostnader i produksjonen som brukes i stykklisteberegninger for standard kostpris inkluderer:
-   Tillegg − En beregningsformel for tillegg gjenspeiler en prosent av en verdi, for eksempel 100 prosent, som er knyttet til en bestemt kostnadsgruppe, for eksempel arbeid.
-   Sats − En beregningsformel for sats gjenspeiler et beløp per enhet, for eksempel NOK 60,00 per time, som er knyttet til en bestemt kostnadsgruppe, for eksempel arbeid.
-   Forholdet mellom tidsbaserte og materialbaserte administrasjonskostnader − Administrasjonskostnader i produksjonen kan knyttes til ruteoperasjoner eller materialkomponenter.

Informasjonen om etterkalkuleringsversjonen som brukes i stykklisteberegninger for standard kostpris inkluderer:
-   Etterkalkuleringstype − Etterkalkuleringsversjonen må inneholde standard kostpriser. Det finnes flere begrensninger for stykklisteberegninger som bruker standard kostpriser. For eksempel angir disse restriksjonene at tillegg må inkluderes i enhetskostnader, og at nedbrytingsmodus for stykklisteberegningen er på et enkelt nivå.
-   Obligatorisk tilbakefallsprinsipp − Etterkalkuleringsversjonen kan kreve et obligatorisk tilbakefallsprinsipp, for eksempel bruk av en angitt etterkalkuleringsversjon eller de aktive kostnadspostene. Det obligatoriske tilbakefallsprinsippet brukes vanligvis sammen med en etterkalkuleringsversjon som representerer de trinnvise oppdateringene i en toversjons tilnærming til kostnadsoppdateringer.
-   Blokkeringsflagg for uavsluttede kostnader − Et blokkeringsflagg kan hindre stykklisteberegninger av uavsluttede kostnader for produserte varer.
-   Angitt fra-dato − Den angitte fra-datoen fungerer som standard beregningsdato for alle stykklisteberegninger som berøres av etterkalkuleringsversjonen.
-   Angitt område − Et angitt område vil begrense stykklisteberegninger til det enkelte området.
-   Innholdet i etterkalkuleringsversjonen må inkludere kostnader − Innholdet må inkludere kostnader. Om ønskelig kan det inkludere salgspriser, slik at foreslåtte salgspriser kan beregnes for produserte varer.

Det kan angis flere kilder til informasjon når en stykklisteberegning initialiseres. Dette inkluderer området, beregningsdatoen og etterkalkuleringsversjonen.





