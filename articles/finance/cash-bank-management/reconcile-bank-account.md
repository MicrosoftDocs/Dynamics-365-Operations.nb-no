---
title: Avstemme en bankkonto
description: Dette emnet beskriver hvordan du avstemmer en bankkonto.
author: panolte
manager: AnnBe
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: panolte
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c77d08d5877ab27f9b6549a5b2a666150938fc08
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446469"
---
# <a name="reconcile-a-bank-account"></a>Avstemme en bankkonto

[!include[banner](../includes/banner.md)]

Når du mottar et bankkontoutdrag, bør du periodisk avstemme juridisk enhet banktransaksjoner med transaksjoner på bankkontoutdraget.

Du kan ikke avstemme et bankkontoutdrag med en bankkonto hvis noen av sjekkene eller betalingene med betalingsbilag på kontoutdraget for øyeblikket har statusen **Venter på annullering**. Etter at en kontrollør har postert eller avvist en sjekktilbakeføring eller annullert et betalingsbilag, er ikke statusen lenger **Venter på annullering**, og du kan da avstemme bankkontoen.

1.  Gå til **Kontant- og bankbehandling** \> **Bankkontoer** \> **Bankkontoer**. Velg bankkontoen som skal avstemmes med bankkontoutdraget, og velg **Avstem** > **Kontoavstemming**.

2.  Angi informasjon i feltene **Bankkontoutdragsdato** og **Bankkontoutdrag**. I feltet **Sluttsaldo** kan du angi saldoen for bankkontoen slik den vises på bankkontoutdraget.

3.  Velg **Transaksjoner** for å åpne siden **Kontoavstemming**.

4.  For hver transaksjon som er inkludert i bankkontoutdraget, merker du av for **Avstemt** hvis beløpet i Dynamics 365 Finance tilsvarer beløpet på bankkontoutdraget. Du kan også angi eller endre verdien i feltet **Banktransaksjonstype**. Denne feltverdien er viktig på grunn av banktransaksjonsstatistikken og for enkelte rapporter.
    

    > [!NOTE]
    > <P>Ikke merk av for <STRONG>Avstemt</STRONG> for transaksjoner som ikke finnes på bankkontoutdraget. Disse transaksjonene vil fortsatt vises på denne siden til de blir avstemt mot et fremtidig bankkontoutdrag.</P>
    > <P>Avmerkingsboksen <STRONG>Avstemt</STRONG> er ikke tilgjengelig hvis transaksjonen har statusen <STRONG>Venter på annullering</STRONG>. Det kan hende at transaksjoner har denne statusen hvis Finance er konfigurert slik at det krever at tilbakeføringer eller annulleringer må sendes til gjennomgang før de posteres. Etter at en kontrollør har postert eller avvist en sjekktilbakeføring eller annullert et betalingsbilag, er ikke statusen lenger <STRONG>Venter på annullering</STRONG>, og du kan da avstemme bankkontoen med bankkontoutdraget.</P>

    
    For å merke av for **Avstemt** for et intervall med kontroller som alle vises på bankkontoutdraget, velger du **Merk sjekkintervall**, og deretter angir du intervallet.

5.  Hvis beløpet for en bankkontotransaksjon ikke samsvarer med beløpet for transaksjonen på kontoutdraget, angir du korreksjonsbeløpet i feltet **Korreksjonsbeløp**.
    

    > [!NOTE]
    > <P>Hvis regnskapsperioden til transaksjonen som skal rettes, er avsluttet, kan ikke feltet <STRONG>Korreksjonsbeløp</STRONG> brukes. Du må i stedet opprette en linje som har en transaksjonsdato som er i en åpen regnskapsperiode. I dette tilfellet må du legge til finansdimensjonene som ble brukt på den opprinnelige transaksjonen, og også mot hovedmotkontoen.</P>



6.  Opprett transaksjoner for poster, for eksempel renter og gebyr, som finnes på bankkontoutdraget, men som ikke er registrert i Finance. Angi **Banktransaksjonstype** og aktuelle finansdimensjoner.

7.  Når transaksjonene på bankkontoutdraget er merket som **Avstemt**, vil beløpet i **Ikke avstemt**-feltet (som blir fortløpende omberegnet etter hver som du gjør endringer) nærme seg null. Når beløpet er null, velger du **Avstem konto** for å postere avstemmingen og transaksjonene og rettingene du har opprettet.
    
    Etter at avstemmingen er postert, kan ikke de inkluderte transaksjonene endres eller korrigeres mer, og de blir ikke vist i fremtidige kontoavstemminger.

8.  Hvis du vil vise banktransaksjoner som ennå ikke er avstemt, bruker du rapporten **Ikke avstemte banktransaksjoner**. Hvis du vil vise kontoutdraget for en bankkonto, bruker du rapporten **Bankkontoutdrag**.

## <a name="cancel-bank-statement-reconciliation"></a>Avbryt avstemming av bankkontoutdrag 

Med funksjonen Avbryt avstemming av bankkontoutdrag kan du avbryte avstemming av bankkontoutdrag. Hvis du vil bruke denne funksjonen, aktiverer du funksjonen **Avbryt avstemming av bankkontoutdrag** i arbeidsområdet **Funksjonsbehandling**. Du må også aktivere parameteren **Tillat redigering av bankkontoutdrag**. Dette gjør du ved å gå til **Kontant- og bankbehandling > Oppsett > Parametere for kontant- og bankbehandling > Bankavstemming**.
 
Avstemminger av bankkontoutdrag kan bare avbrytes i den kronologiske rekkefølgen de ble angitt. Når en avstemming av et bankkontoutdrag avbrytes, tilbakeføres nye transaksjoner og rettelser, og alle andre transaksjoner merkes som ikke avstemt.
 
Hvis du vil annullere avstemming av bankkontoutdrag, velger du bankkontoutdraget og velger **Bankkontoutdrag > Avbryt bankavstemming**. På siden **Avbryt bankavstemming** oppgir du **Årsakskode**, **Årsakskommentar** og **Annulleringsdato**. Velg **OK** for å starte annulleringen. Legg merke til at annulleringsdatoen for bankkontoutdraget må være på eller etter bankkontoutdragsdatoen. Etter at avstemmingen av bankkontoutdraget er annullert, blir feltet **Annulleringsdato** for bankkontoutdraget oppdatert med den angitte **annulleringsdatoen**. Velg **Transaksjoner**-knappen for å vise transaksjonene som avstemmingen ble annullert for.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]