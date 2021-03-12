---
title: Definere en telefonsenterkanal
description: Dette emnet beskriver hvordan du oppretter en ny telefonsenterkanal i Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b25626dafc07d576699ceba3cc9ca691db45cb9f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997756"
---
# <a name="set-up-a-call-center-channel"></a>Definere en telefonsenterkanal


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du oppretter en ny telefonsenterkanal i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt


I Dynamics 365 Commerce er et telefonsenter en type Commerce-kanal som kan defineres i programmet. Ved å definere en kanal for telefonsenterenheter kan systemet knytte bestemte data og ordrebehandlingsstandarder til salgsordrer. Selv om et firma kan definere flere telefonsenterkanaler i Commerce, er det viktig å være oppmerksom på at en enkelt bruker bare kan kobles til én telefonsenterkanal. 

Før du oppretter en ny telefonsenterkanal, må du kontrollere at du har oppfylt [Forutsetninger for kanaloppsett](channels-prerequisites.md).

## <a name="create-and-configure-a-new-call-center-channel"></a>Opprette og konfigurere en ny telefonsenterkanal

Hvis du vil opprette og konfigurere en ny telefonsenterkanal, gjør du følgende:

1. I navigasjonsruten går du til **Detaljhandel og handel \> Kanaler \> Telefonsentre \> Alle telefonsentre**.
1. I handlingsruten velger du **Ny**.
1. I **Navn**-feltet oppgir du et navn for den nye kanalen.
1. Velg den aktuelle **juridiske enheten** fra rullegardinlisten.
1. Velg det aktuelle **lagerstedet** fra rullegardinlisten. Denne lokasjonen brukes som standard på salgsordrer som er opprettet for denne telefonsenterkanalen, med mindre andre standarder er definert på kunde- eller varenivået.
1. Angi en gyldig standardkunde i feltet **Standardkunde**. Disse dataene brukes til å hjelpe med automatisk utfylling av standarder når nye kundeoppføringer opprettes. Når du oppretter telefonsenterordrer, er det ikke lurt å opprette ordrer for standardkunden.
1. I feltet **Profil for e-postvarsling** oppgir du en gyldig profil for e-postvarsling. Når telefonsenterordrer opprettes og behandles, brukes e-postvarslingsprofilen til å utløse automatiske e-postvarsler til kunder med informasjon om deres ordrestatus.
1. Angi en infokode for **Prisoverstyring**. Du må kanskje opprette en informasjonskode for dette først. Denne informasjonskoden gir et sett med årsakskoder som brukeren blir bedt om å velge blant når han/hun bruker funksjonen for prisoverstyring på en telefonsenterordre.
1. Oppgi en infokode for **Sperrekode**. Du må kanskje opprette en informasjonskode for dette først. Denne informasjonskoden gir et sett med valgfrie årsakskoder som brukeren blir bedt om å velge blant når han/hun setter en ordre på vent.
1. Angi en infokode for **Kreditt**. Du må kanskje opprette en informasjonskode for dette først. Denne informasjonskoden inneholder årsakskoder som brukeren kan velge blant ved bruk av funksjonen for ordrekreditt i telefonsenteret for å gi diverse refunderinger til kunden av hensyn til kundeservice.
1. Valgfritt: definer finansdimensjoner i hurtigfanen **Finansdimensjoner**. Dimensjonene som angis her, brukes som standard på alle salgsordrer som er opprettet i denne telefonsenterkanalen.
1. Klikk **Lagre**.

Bildet nedenfor viser opprettelsen av en ny telefonsenterkanal.

![Ny telefonsenterkanal](media/channel-setup-callcenter-1.png)

Bildet nedenfor viser et eksempel på en telefonsenterkanal.

![Eksempel på telefonsenterkanal](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Ekstra kanaloppsett

Andre oppgaver som kreves for oppsett av telefonsenterkanal, omfatter definere betalingsmåter og leveringsmåter.

Bildet nedenfor viser oppsettsalternativene **Leveringsmåter** og **Betalingsmåter** i kategorien **Oppsett**.

![Ekstra konfigurasjonshandlinger for telefonsenterkanal](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Definere betalingsmåter

Hvis du vil definere betalingsmåter, følger du disse trinnene for hver betalingstype som støttes på denne kanalen. Brukere må velge fra forhåndsdefinerte betalingsmetoder for å koble dem til telefonsenterkanalen. Før du definerer betalingsmetodene for telefonsenteret, må du først definere hovedmetodene for betaling i **Detaljhandel og handel \> Kanaloppsett \> Betalingsmåter \> Betalingsmåter**.

1. I handlingsruten velger du kategorien **Oppsett** og deretter **Betalingsmåter**.
1. I handlingsruten velger du **Ny**.
1. I navigasjonsruten velger du en betalingsmetode fra de tilgjengelige forhåndsdefinerte betalingene.
1. Konfigurer eventuelle tilleggsinnstillinger som kreves for betalingstypen. Når det gjelder kredittkort, gavekort eller fordelskort, kreves det ytterligere oppsett ved å velge **Kortoppsett**-funksjonen. 
1. Konfigurer riktige posteringskontoer for betalingstypen i **Postering**-delen.
1. Klikk på **Lagre** i handlingsruten.

Bildet nedenfor viser et eksempel på en kontantbetalingsmåte.

![Eksempel på betalingsmåter](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a>Definer leveringsmåter

Du kan se de konfigurerte leveringsmåtene ved å velge **Leveringsmåter** fra kategorien **Oppsett** i **handlingsruten**.  

Følg denne fremgangsmåten for å endre eller legge til en leveringsmåte som skal knyttes til telefonsenterkanalen:

1. Velg **Behandle leveringsmåter** fra skjemaet for leveringsmåter for samtalesenteret.
1. Velg **Ny** i handlingsruten for å opprette en ny leveringsmåte, eller velg en eksisterende måte.
1. I delen **Detaljhandelskanaler** velger du **Legg til linje** for å legge til telefonsenterkanalen. Legge til kanaler ved hjelp av organisasjonsnoder i stedet for å legge til hver kanal for seg, kan effektivisere tillegg av kanaler
1. Kontroller at leveringsmåten er konfigurert med data i hurtigfanen **Produkter** og hurtigfanen **Adresser**. Hvis ingen produkter eller leveringsadresser er gyldige for leveringsmåten, vil det føre til feil å velge den under ordreregistrering.
1. Når det er gjort endringer i leveringskonfigurasjoner for telefonsenteret, må jobben **Behandle leveringsmåter** kjøres for å bryte ned endringsmatrisen. Du finner denne jobben ved å navigere til **Detaljhandel og handel \> IT for detaljhandel og handel \> Behandle leveringsmåter**.

Bildet nedenfor viser et eksempel på en leveringsmåte.

![Definer leveringsmåter](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a>Definere kanalbrukere

Hvis du vil opprette en salgsordre som er koblet til telefonsenterkanalen fra Commerce Headquarters, må brukeren som oppretter salgsordren, være koblet til telefonsenterkanalen. Brukeren kan ikke koble en salgsordre som er opprettet i Commerce Headquarters manuelt til telefonsenterkanalen. Koblingen er systematisk, og er basert på brukeren og brukerens forhold til telefonsenterkanalen. En bruker kan bare være koblet til én telefonsenterkanal.

1. I handlingsruten velger du kategorien **Kanal** og deretter **Kanalbrukere**.
1. I handlingsruten velger du **Ny**.
1. Velg en eksisterende **Bruker-ID** fra rullegardinlisten for å koble denne brukeren til telefonsenterkanalen

Når brukeroppsettet for kanalen er fullført og brukeren oppretter en ny salgsordre i Commerce Headquarters, blir salgsordren koblet til den tilknyttede telefonsenterkanalen. Konfigurasjoner for denne kanalen vil bli brukt systematisk på salgsordren. En bruker kan bekrefte hvilken telefonsenterkanal salgsordren er koblet til ved å vise kanalnavnreferansen i salgsordrehodet.


### <a name="set-up-price-groups"></a>Definere prisgrupper

Prisgrupper er valgfrie, men hvis de brukes, kan de styre hvilke salgspriser som skal tilbys kunder som legger inn ordrer i telefonsenterkanalen. Hvis en prisgruppe ikke er konfigurert for kunden, eller hvis katalogprisgrupper ikke er brukt på salgsordren (ved hjelp av feltet **Kildekode-ID** i ordrehodet i samtalesenteret), brukes kanalprisgruppen til å finne varepriser. Hvis det ikke blir funnet en prisgruppe i telefonsenterkanalen, brukes standard hovedpriser. 

Hvis du vil definere en prisgruppe, gjør du følgende:

1. I handlingsruten velger du kategorien **Kanal** og deretter **Prisgrupper**.
1. I handlingsruten klikker du på **Ny**.
1. Velg en **detaljhandelsprisgruppe** fra rullegardinlisten.

## <a name="additional-resources"></a>Tilleggsressurser

[Kanaloppsettsforutsetninger](channels-prerequisites.md)

[Salgsfunksjonalitet for telefonsenter](call-center-functionality.md)

[Definere ordrebehandlingsalternativer for telefonsenter](set-up-order-processing-options.md)

[Telefonsenterkataloger](call-center-catalogs.md)

[Definere og arbeide med svindelvarsler](set-up-fraud-alerts.md)

[Definere kontinuitetsprogrammer for telefonsentre](set-up-continuity-program.md)
