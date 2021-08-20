---
title: Redigere og overvåke hentesalgs- og kassastyringstransaksjoner
description: Dette emnet beskriver hvordan du redigerer og kontrollerer hentesalgs- og kassastyringstransaksjoner i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 85c4bd4c03b6ac09f2226d1767deabde1879f869e4b7c4d45e4d4c2a1d8effb3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765344"
---
# <a name="edit-and-audit-cash-and-carry-and-cash-management-transactions"></a>Redigere og overvåke hentesalgs- og kassastyringstransaksjoner

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du redigerer og kontrollerer hentesalgs- og kassastyringstransaksjoner i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Dynamics 365 Commerce-kunder bruker både første- og tredjeparts salgsstedsprogrammer (POS). Når det gjelder førsteparts salgsstedsprogrammet blir butikktransaksjoner hentet til Commerce Headquarters fra kanalene fra en satsvis prosess. Når det gjelder tredjeparts programmer trekkes transaksjoner inn i Commerce Headquarters via integrering. I begge tilfeller må det utføres en konsekvenskontrollprosess når transaksjoner trekkes inn i Commerce Headquarters. Denne prosessen kjører flere valideringer på transaksjonene, og bare transaksjoner som er validert, trekkes inn i utdraget slik at de kan posteres i Commerce Headquarters.

Commerce-transaksjoner består kanskje ikke validering av flere årsaker. En feil i integreringskoden eller POS-programmet kan forårsake inkonsekvente data. Det kan også hende at en brukerfeil fører til inkonsekvente data. En bruker sletter for eksempel et produkt etter at det ble synkronisert til kanalen, eller en bruker lukker en regnskapsperiode uten å postere transaksjoner for den perioden. Selv om disse transaksjonene blir flagget og utelatt fra utdragene, kan de forstyrre en kundens daglige prosess med å postere daglige salg til finans. I Commerce kan du redigere transaksjonene som ikke kan valideres, samtidig som du også reviderer alle endringene.

## <a name="edit-transactions"></a>Rediger transaksjoner

I Commerce versjon 10.0.5 er hentesalgstransaksjoner, for eksempel salg og returer, de eneste transaksjonene som kan redigeres. Kundeordrer og elektroniske ordrer kan ikke redigeres. I Commerce versjon 10.0.6 og nyere kan du også redigere kontantstyringstransaksjoner.

Følg denne fremgangsmåten for å redigere transaksjoner i Commerce Headquarters.

1. Installer [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Åpne arbeidsområdet **Finans for handelsbutikk** i Commerce Headquarters. Flisen **Transaksjonsvalideringsfeil** inneholder en forhåndsfiltrert visning av transaksjonssiden som mislyktes med én eller flere av valideringsreglene.
1. Åpne transaksjons siden, velg posten som ikke ble validert, velg **Office-tillegg**, og velg deretter **Rediger valgt transaksjon**. Det åpnes en Excel-fil som viser detaljene for den valgte transaksjonen. Denne filen inneholder følgende regneark:

    - **Linjer** – Dette regnearket har hode- og produktlinjer for transaksjonen, og også relaterte data for transaksjonen.
    - **Betalinger** – Dette regnearket har detaljene for betalingslinjene for transaksjonen.
    - **Rabatter** – Dette regnearket har rabattrelaterte detaljer for transaksjonen.
    - **Avgifter** – Dette regnearket har avgiftsrelaterte detaljer for transaksjonen.
    - **Gebyrer** – Dette regnearket har gebyrrelaterte data for transaksjonen.

1. I Excel-filen endrer du de aktuelle feltene, og deretter laster du opp dataene tilbake til Commerce Headquarters ved hjelp av publiseringsfunksjonen i Dynamics Excel-tillegget. Etter at dataene er publisert, vil endringene gjenspeiles i systemet. Under publiseringen utføres det ingen validering for endringer som brukerne gjør.
1. Du kan vise et fullstendig overvåkingsspor for endringene ved å velge **Vis overvåkingsspor** i hodet for **Detaljhandelstransaksjon** for endringer på hodenivå, og i den relevante delen og posten på den riktige transaksjonssiden. Alle endringer som er knyttet til salgslinjer, vises for eksempel på siden **Salgstransaksjoner**, og alle endringer som er relatert til betalinger, vises på siden **Betalingstransaksjoner**. Følgende overvåkingsdetaljer beholdes for endringene:

    - Endringsdato og -klokkeslett
    - Felt
    - Gammel verdi
    - Ny verdi
    - Endret av

1. Etter at du har utført og publisert endringene, må du kjøre **Valider butikktransaksjoner** på nytt for å validere at de endringene er konsekvente og gyldige.

> [!NOTE]
> Du kan redigere bare transaksjoner som ikke ble validert. Hvis du vil redigere en transaksjon som har bestått valideringen, endrer du valideringsstatusen til transaksjonen til **Feil** eller **Ingen**, og deretter publiserer du endringen. Du kan deretter redigere dataene i hodet eller i andre underordnede poster for transaksjonen, og publisere hodet eller postene.

## <a name="bulk-edit-transactions-that-are-linked-to-a-statement"></a>Masseredigeringstransaksjoner som er koblet til et utdrag

Commerce-versjon 10.0.6 og nyere støtter alternativet for masseredigeringer på utdragsnivået.

Hvis du vil redigere transaksjoner som er koblet til et utdrag i Commerce Headquarters, følger du denne fremgangsmåten.

1. Åpne siden **Utdrag**, og velg deretter utdraget som inneholder transaksjonene som må redigeres.
1. Velg knappen **Åpne i Microsoft Office**.
1. Velg ett av følgende alternativer avhengig av hva som må redigeres:

    - **Rediger hentesalgstransaksjoner** – Med dette alternativet kan du redigere alle hentesalgstransaksjoner som er inkludert i utdraget. Følgende Excel-regneark er tilgjengelige:

        - **Transaksjon** – Dette regnearket inneholder all informasjon på hodenivå for salgstransaksjonene.
        - **Salgstransaksjon** – Dette regnearket inneholder all informasjon på linjenivå for salgstransaksjonene.
        - **Betalingstransaksjoner** – Dette regnearket inneholder all betalingslinjeinformasjon for salgstransaksjonene.
        - **Rabattransaksjoner** – Dette regnearket inneholder all rabattlinjeinformasjon for salgstransaksjonene.
        - **Avgiftstransaksjon** – Dette regnearket inneholder all avgiftslinjeinformasjon for salgstransaksjonene.
        - **Gebyrtransaksjoner** – Dette regnearket inneholder all gebyrlinjeinformasjon for salgstransaksjonene.

    - **Rediger kassastyringstransaksjoner** – Med dette alternativet kan du redigere alle kassastyringstransaksjoner som er inkludert i utdraget. Følgende Excel-regneark er tilgjengelige:

        - **Transaksjon** – Dette regnearket inneholder all informasjon på hodenivå for kassastyringstransaksjonene.
        - **Betalingsmiddeltransaksjoner til bank** – Dette regnearket inneholder alle detaljene for bankdeponeringstransaksjon.
        - **Betalingsmiddeltransaksjoner til safe** – Dette regnearket inneholder alle detaljene for safedeponeringstransaksjon.
        - **Kasseoppgjør** – Dette regnearket inneholder alle detaljene for kasseoppgjørstransaksjon.
        - **Inntekts-/utgiftstransaksjon** – Dette regnearket inneholder alle detaljene for linje på inntekts-/utgiftstransaksjon.
        - **Betalingstransaksjoner** – Dette regnearket har all betalingsrelatert informasjon for operasjonen **Betal faktura** og inntekts-/utgiftstransaksjonen.

1. Rediger de nødvendige transaksjonene.

    > [!NOTE]
    > Valideringer utføres ikke når du publiserer masseredigerte transaksjoner. Du må sørge for at alle redigeringer er nøyaktige, og at gjengivelsen av data på regnearkene beholdes. Hvis du for eksempel vil endre transaksjonsdatoen slik at du kan administrere scenarioene der regnskaps -eller lagerperioden for de åpne transaksjonene er lukket, må du endre datoen i alle Excel-regneark som har kolonnen **Forretningsdato**. Hvis du vil validere transaksjoner etter at de er redigert, kan du velge **Valider transaksjoner på nytt** på **Utdrag**-siden. Vent til valideringsjobben er fullført før du posterer utdraget.

1. Hvis aggregeringen allerede er generert, kan du åpne siden **Aggregerte transaksjoner** og velge **Generer salgsordre-XML på nytt**.

## <a name="bulk-edit-transactions-that-arent-linked-to-a-statement"></a>Masseredigeringstransaksjoner som ikke er koblet til et utdrag

Commerce-version 10.0.10 og nyere støtter alternativet for masseredigeringstransaksjoner som ikke kan valideres, men som ikke er koblet til et utdrag.

Hvis du vil redigere transaksjoner som ikke er koblet til et utdrag i Commerce Headquarters, følger du denne fremgangsmåten.

1. Åpne siden **Alle butikker** og velg butikken som transaksjoner må redigeres for.
1. Velg knappen **Åpne i Microsoft Office**, og velg deretter **Rediger hentesalgstransaksjoner**.
1. Rediger de nødvendige transaksjonene, og publiser dem deretter.

## <a name="additional-resources"></a>Tilleggsressurser

[Rediger og overvåk nettordretransaksjoner og asynkrone kundeordretransaksjoner](edit-order-trans.md)

[Redigere finansdimensjoner for detaljhandelstransaksjoner](edit-financial-dim.md)

[Opprette en Excel-arbeidsbok for å redigere detaljhandelstransaksjoner](create-excel-edit.md)

[Legge til felt i en Excel-arbeidsbok for å redigere detaljhandelstransaksjoner](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]