---
title: Oversikt over hjelp
description: "Denne artikkelen gir en oversikt over komponentene til hjelpesystemet for Microsoft Dynamics 365 for Operations. Det forklarer også hvordan du kan angi egendefinerte dokumentasjon og opplæring for organisasjonen."
author: margoc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16381
ms.assetid: 018c148c-9cbd-41e0-8186-d75dbf66288f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 240060606c8a2955c3f0a0d47fb25b0cde64c187
ms.lasthandoff: 03/31/2017


---

# <a name="help-overview"></a>Oversikt over hjelp

Denne artikkelen gir en oversikt over komponentene til hjelpesystemet for Microsoft Dynamics 365 for Operations. Det forklarer også hvordan du kan angi egendefinerte dokumentasjon og opplæring for organisasjonen. 

Dynamics 365 for Operations inkluderer et hjelpesystem som er basert på to hovedkomponenter:

-   Et område for dokumentasjon
-   Oppgaveveiledninger

Du kan få tilgang til både artikler og aktivitet hjelpelinjer fra Hjelp-ruten i Dynamics 365 for operasjoner som vist i følgende skjermbilde. [![Hjelp-rute](./media/help-pane-ops-task-guides-1024x741.png)](./media/help-pane-ops-task-guides.png) denne artikkelen beskriver Hjelp-systemet, og forklarer hvordan du kan opprette egendefinerte dokumentasjon og opplæringsressurser for organisasjonen.

## <a name="help-on-docsmicrosoftcom"></a>Hjelp med docs.microsoft.com
docs.microsoft.com-området ([docs.microsoft.com/dynamics365/operations](https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations) er den viktigste kilden til produktdokumentasjonen for Dynamics 365 for operasjoner. Området tilbyr følgende funksjoner:

-   **Tilgang til det mest oppdaterte innholdet** – området gir oss en raskere og mer fleksibel måte å opprette, levere og oppdatere produktdokumentasjonen. Derfor garanterer det at du har tilgang til den nyeste tekniske informasjonen.
-    **Innhold som er skrevet av eksperter** – området inneholder et rikere sett med dokumentasjon som kan bli forbedret av fellesskapsmedlemmer både innenfor og utenfor Microsoft-produkter.
-   ** Tilgang til ulike typer innhold **-området kan du raskt tilgang ulike typer innhold om Dynamics 365 for operasjoner, som Microsoft Office blanding presentasjoner, aktivitet støttelinjer, videoer og wiki-artikler.
-    **Innhold som støtter forretningsprosesser** – området inneholder business process – fokusert innhold som kan dra fordel av Business Process modell (BPM) i Microsoft Dynamics Lifecycle tjenester (LCS).

Vi har flyttet alt innhold fra våre tidligere Hjelp wiki til dokumenter. Vi er svært glade om vår nye området, og håper du vil være for.

### <a name="when-can-we-use-it"></a>Når kan vi bruke den?

Du kan lese innholdet på dokumenter akkurat nå - det er helt offentlig og søkbare uten å kreve pålogging. Du kan bruke hvilke som helst av dine favorittsøkemotorer til å finne innhold. Du kan kommentere artikler på webområdet hvis du velger, ved å logge på med en konto på GitHub.


## <a name="task-guides"></a>Oppgaveveiledninger
En aktivitet guide er en kontrollert, veiledende, interaktiv opplevelse som leder deg gjennom trinnene for en aktivitet eller en forretningsprosess. Du kan åpne guide (play) en aktivitet i Hjelp-ruten. Når du først velge en hjelpelinje for aktiviteten, vises Hjelp-ruten for trinnvise instruksjoner for oppgaven. Lokaliserte aktivitet støttelinjer er nå tilgjengelige. [![Aktivitet guide Lesevisning](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png) Klikk for å starte den veiledende, interaktive opplevelsen, **Start oppgave guide** nederst i Hjelp-ruten. En svart peker åpnes og angir handlingen som du må utføre. Følg instruksjonene som vises i brukergrensesnittet, og legg inn data i henhold til instruksjonene. [![Oppgave veiledning trinn instruksjon](./media/task-guide-step-1-ops.png)](./media/task-guide-step-1-ops.png)**viktig:** data du skriver inn når du spiller av en aktivitet guide er ekte. Hvis du er i et produksjonsmiljø, legges dataene inn i firmaet som du bruker for øyeblikket.

### <a name="it-all-begins-with-task-recorder"></a>Alt begynner med Oppgaveregistrering

Oppgaveveiledninger opprettes ved hjelp av Oppgaveregistrering. Når du bruker Oppgaveregistrering, registreres alle handlingene du utfører i grensesnittet i Dynamics 365 for Operations (for eksempel velge menyer, endre innstillinger og skrive inn data). Samlet kalles trinnene som du registrerer en oppgaveregistrering. Som forklart i den forrige delen kan oppgaveregistreringer vises i Hjelp-ruten og spilles av som oppgaveveiledninger. Det finnes imidlertid andre måter som du kan bruke oppgaveregistreringer på:

-   **Lagre oppgaveregistreringer til BPM** – Du kan lagre en oppgaveregistrering på en linje i et hierarki i et BPM-bibliotek i LCS. Når du lagrer en oppgaveregistrering på BPM, genereres og vises et flytskjema sammen med trinnene i registreringen. **Merk:** For å vise en oppgaveregistrering i Dynamics 365 for Operations Hjelp-ruten og spille den av som en oppgaveveiledning, må du lagre registreringen i et BPM-bibliotek.
-   **Lagre oppgaveregistreringer som Word-dokumenter** – Ved å lagre en oppgaveregistrering som et Microsoft Word-dokument, kan du enkelt lage utskrivbare opplæringsveiledninger for organisasjonen.

Hvis du vil ha mer informasjon om Oppgaveregistrering, se [Oppgaveregistrering i Dynamics 365 for drift](../user-interface/task-recorder.md).

### <a name="creating-customized-task-recordings"></a>Opprette egendefinerte oppgaveregistreringer

Du kan opprette dine egne oppgaveregistreringer, eller du kan laste ned og tilpasse oppgaveregistering som Microsoft tilbyr. Du kan derfor opprette tilpasset Hjelp for organisasjonen som viser din spesifikke Dynamics 365 for Operations-implementering. Hvis du vil vise en aktivitet registrere i Dynamics-365 for operasjoner hjelperuten og spille det som en veiledning for oppgaven, må du lagre innspillingen BPM-biblioteket i LCS. Hvis du er en partner, og heve nivået for et bibliotek til et firma bibliotek og inkludere den i en løsning, vil den være tilgjengelig for kundene dine. Hvis du vil ha fullstendige instruksjoner, se [ved hjelp av oppgaven innspillinger til å lage dokumentasjon eller opplæring](../user-interface/task-recorder.md).

## <a name="in-product-help"></a>Hjelp i produktet
Hvis du vil ha tilgang til Hjelp-innhold i Dynamics 365 for operasjoner, klikker du på **hjelp** (**?**) ikonet og velger hjelp eller trykker Ctrl + Skift +?. I begge tilfeller åpnes Hjelp-ruten. Fra Hjelp-ruten, kan du tilgang til artikler eller oppgave støttelinjer. [![](./media/help-pane-wiki-1024x684.png)](./media/help-pane-wiki.png)

### <a name="accessing-articles-from-the-help-pane"></a>Få tilgang til artikler fra Hjelp-ruten

Fra Hjelp-ruten, kan du tilgang til artikler som gjelder for Dynamics-365 for operasjoner klienten. Når du først åpner Hjelp-ruten og klikk på **Wiki** -kategorien ser du artikler som gjelder for siden du er på i Dynamics 365 for operasjoner. Hvis det finnes ingen artikler, kan du angi nøkkelord for å begrense søket. Når du klikker en artikkel i Hjelp-ruten, en ny fane åpnes i webleseren og viser artikkelen. 

### <a name="accessing-task-guides-from-the-help-pane"></a>Tilgang til oppgaven hjelpelinjer fra Hjelp-ruten

Før du får tilgang til oppgaven støttelinjer fra Hjelp-ruten, har en systemadministrator å gå til den **systemparametere** siden i Dynamics 365 for operasjoner og konfigurere noen innstillinger. **Merknader:**

-   Hvis du vil konfigurere hjelp, må du være logget på med en konto i samme leier som leier som Dynamics 365 for Operations er distribuert i.
-   Det er ikke mulig å koble til et LCS-biblioteket fra en forekomst av Dynamics 365 for Operations som kjører på en virtuell harddisk (VHD).

[![Parametere-skjemaet for systemet med innstillinger for hjelp](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) på den **systemparametere** side, følger du denne fremgangsmåten:

1.  **Viktig: **Første gang du åpner kategorien Hjelp, må du koble til Lifecycle Services. Husk å klikke koblingen midt i skjemaet, venter på tilkoblingen, lukke dialogboksen og klikk OK for å få i Parametere-skjemaet. [![Koble til LCS](./media/connect-to-lcs-crop-1024x365.png)](./media/connect-to-lcs-crop.png)
2.  Velg Lifecycle Services-prosjektet du vil koble til.
3.  Velg BPM-bibliotekene (i det valgte prosjektet) du vil hente oppgaveregistreringer fra.
4.  Angi visningsrekkefølge for BPM-bibliotekene. Dette bestemmer hvilken rekkefølge oppgaveregistreringer fra bibliotekene skal vises i, i Hjelp-ruten.

Når systemansvarlig har fullført disse trinnene, kan du åpne Hjelp-ruten og klikke kategorien **Oppgaveveiledninger**. Nå vil du se aktivitet veiledningene som gjelder for siden du er på i Dynamics 365 for operasjoner. Hvis ingen aktivitet hjelpelinjer ikke blir funnet, kan du angi nøkkelord for å begrense søket. Når du klikker en aktivitet veiledning i Hjelp-ruten, Hjelp-ruten viser trinnvise instruksjoner, og du kan spille av TV-guiden for oppgaven. [![Aktivitet guide Lesevisning](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png)

### <a name="where-are-the-translated-task-guides"></a>Hvor er oversatt aktivitet støttelinjene?

Oversatt aktivitet veiledning er utgitt i biblioteker med "Alle språk" i tittelen. I Dynamics 365 for operasjoner, for å se lokaliserte aktivitet guide hjelper, kontrollerer du at du er koblet til et bibliotek for apppropriate. Språket som en veiledning for oppgaven vises i kontrolleres for hver bruker av språkinnstillingene under **alternativer**&gt;**innstillinger**. 
-   Hvis en aktivitet guide er oversatt, når du åpner denne oppgaven guide all tekst i TV-guiden for oppgaven vises i det valgte språket.
-   Hvis oppgaven veiledning ikke er ennå blitt oversatt, når du åpner det, vises bare noe av teksten (teksten av kontrollene) på det valgte språket.

## <a name="additional-resources"></a>Tilleggsressurser
Tabellen nedenfor viser webområder som tilbyr Dynamics 365 for Operations-innhold. Våre innholdswebområder er organiserte for å støtte livssyklusen til kunden. Hver fase støttes av et annet sett med områder. Områder som har en stjerne (\*) krever at du logger deg på med en konto som er knyttet til en serviceavtale ved siden av navnet.

| Område                                                                     | beskrivelse                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Docs.microsoft.com](https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations) | Er vert for eller kobler til all produktdokumentasjon for Dynamics 365 for Operations.                                                                                                                                                               |
| [Lifecycle Services](http://lcs.dynamics.com/en/)\*                      | Gir et skybasert samarbeidsområde som kunder og partnere kan bruke til å administrere Dynamics 365 for Operations-prosjekter, fra førsalg til implementering og operasjoner. Dette området er nyttig i alle fasene ved implementering. |
| [CustomerSource](http://www.customersource.com/)\*                       | Inneholder omfattende opplæringsressurser og er det primære brukerstøtteområdet for Dynamics 365 for Operations. Pålogging kan være nødvendig for å få tilgang til bestemte ressurser på området.                                                                      |
| [Støtte for blogg](http://aka.ms/AXSupportBlog)                              | Gir tips som posteres av Dynamics 365 for Operations-kundestøtteteamet.                                                                                                                                                  |
| [MSDN](http://aka.ms/AXMSDN)                                             | Er vert for innhold fra tidligere versjoner som er skrevet for utviklere.                                                                                                                                                                       |
| [TechNet](http://aka.ms/TechNet)                                         | Vert for innhold fra tidligere versjoner som er skrevet for IT-medarbeidere og programbrukere.                                                                                                                                           |
| [Dynamics-fellesskapet](http://community.dynamics.com/en/)                  | Vert for blogger, forum og videoer.                                                                                                                                                                                                           |
| [Microsoft.com/Dynamics/](http://www.microsoft.com/dynamics/)                 | Gir informasjon om evaluering og salg.                                                                                                                                                                                                 |



<a name="see-also"></a>Se også
--------

[Hjelpesystemet for Dynamics 365 for operasjoner (nedlastbare Faktaark)](https://mbs.microsoft.com/files/public/CS/AX2012R3/DynamicsAXHelpSystemFactSheet.pdf)

[Oppgaveregistrering i Microsoft Dynamics 365 for operasjoner](../user-interface/task-recorder.md)

[Lage dokumentasjon eller opplæring ved hjelp av oppgaveopptak](../user-interface/task-recorder.md)

[Nye eller oppdaterte oppgaven leder (November 2016)](new-task-guides-november-2016.md)<ph id="t1">
</ph>[ny eller oppdatert aktivitet leder (August 2016)](new-updated-task-guides-available-august-2016.md)<ph id="t2">
</ph>[ny eller oppdatert aktivitet leder (mai 2016)](new-updated-task-guides-available-may-2016.md)<ph id="t3">
</ph>[ny oppgave leder (februar 2016)](new-task-guides-available-february-2016.md)






