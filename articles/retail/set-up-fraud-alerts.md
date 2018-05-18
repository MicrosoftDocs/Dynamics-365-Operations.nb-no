---
title: Definere svindelvarsler
description: "Dette emnet forklarer hvordan du definerer regler for å varsle kundeservicerepresentanter om potensiell falsk informasjon når ordrer behandles. Du kan definere spesifikke sperrekoder som skal brukes automatisk eller manuelt til å sette mistenkelige ordrer på vent."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans, SysOperationTemplateForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f57cdb44d5ed3b078478cf47b74d1a79ba10323c
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-fraud-alerts"></a>Definere svindelvarsler

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du definerer kriterier og regler for å sperre potensielle svindelordrer for videre gjennomgang. Funksjon for svindelgjennomgang brukes til å fastslå gyldigheten av informasjonen i en salgsordre. Hvis informasjonen i salgsordren ser mistenkelig ut basert på organisasjonens svindelvilkår og -regler, kan ordren sperres for videre gjennomgang av en administrator.

> [!NOTE]
> Denne funksjonen kan bare brukes med salgsordrebehandling for telefonsenterkanalen for detaljhandel. 

Når telefonsenterkanalen defineres, må **Aktiver ordrefullføring** settes til **Ja**. Når ordrefullføring er aktivert, kan brukere vise ordreoversikten og klikke på **Send** for å fullføre ordren. Brukere får også alternativer for å sperre salgsordren manuelt for svindelgjennomgang. Salgsordrer som registreres av en telefonsenterbruker behandles via svindelkontrollregler og -kriterier under sendeprosessen.

Det finnes to typer svindelkriterier som systemet refererer til for å kontrollere om ordren skal sperres for svindelgjennomgang:

-   **Statiske regler** bruker en bestemt verdi, for eksempel et telefonnummer som har blitt svartelistet, eller en e-postadresse som er flagget som kjent som bruket for tidligere svindeltransaksjoner. På siden **Statiske svindeldata** kan svindelinformasjon legges til manuelt eller gjennom dataoimport, med poengsummer som er knyttet til svindelinformasjonen. Hvis svindelkontroll er aktivert, vil alle angitte salgsordrer bli sammenlignet med de statiske dataene. Hvis dataene finnes i kundens faktureringsadresse eller leveringsadresse, eller hvis dataene finnes i leveringsadressen på salgslinjen, summeres poengsummen av alle unike treff.  
-   **Dynamiske regler** er satt sammen fra variabler og betingelser som er definert for disse variablene. Med dynamiske regler kan ikke andre kriterier som ikke er definert i statiske regler kontrolleres. Mer komplekse "AND/OR"-setninger kan brukes til å vurdere flere betingelser for å avgjøre om det er et positivt treff mot regelkriteriene og salgsordren som sendes. Hvis en bruker for eksempel vil sperre for svindelgjennomganng alle ordrer for kunder som er knyttet til en bestemt kundegruppeverdi, og som har bestilt et bestemt produkt, vil betingelsene for å validere kunden og validere produkter, defineres på **Regler**-siden med en "AND"-betingelse. Ordren sperres bare for svindelgjennomgang hvis begge betingelsene er sanne og poengsumverdien som er knyttet til regelen, fører til at ordrens totale svindelpoengsum overstiger den minste svindelpoengsummen som definert i parametere for telefonsenter.

En telefonsenterbruker kan også manuelt legge en ordre i svindelsperrekøen. Hvis brukeren som angir ordren mener at kunden som bestiller kan være mistenkelig og ønsker at en annen person skal se gjennom gyldigheten av ordren før den behandles, kan brukeren som angir ordren velge alternativet **Manuell sperre for svindel** fra rullegardinmenyen **Sperrer** på siden **Salgsordresammendrag** (denne vises etter at ordrefunksjonen **Fullfør** er kalt). Brukeren blir bedt om å angi en merknad for å forklare hvorfor de synes ordren kan være en svindel, slik at kontrolløren har mer kontekst.

Alle ordrer som er sperret under den manuelle sperringen for svindel eller av systematisk beregning av svindelpoengsum, vises på siden **Ordresperrer** der ordren kan gjennomgås og deretter avbrytes eller frigis til behandling.

> [!NOTE]
> Bruk av flere regler eller svært komplekse regler, vil føre til dårlig systemytelse når salgsordrer sendes. Funksjonen for varsling om svindel er ikke optimalisert for å håndtere store mengder statiske svindeldata og mange aktive regler. Det er viktig å huske at alle regelen vurderes i sendefunksjonen for ordreregistreringen for telefonsenteret. Reglene evalueres mot salgsordrehodet og alle ordrelinjer. Jo flere regler som finnes og jo mer kompliserte regelsetningene er, jo lenger tid det tar behandlingen. Hvis du har et stort antall linjeelementene på ordren, og et stort antall aktive regler og statiske dataoppføringer, kan denne systematisk prosessen for gjennomgang og validering av alle dataene og beregning av svindelpoengsum ha en alvorlige innvirkning på ytelsen.  Organisasjoner som bruker denne funksjonen bør alltid teste og bekrefter at behandlingstiden for ordrensending er akseptabel før utførelse av endringer av regler eller statiske svindelkriterier i produksjonsmiljøet.

