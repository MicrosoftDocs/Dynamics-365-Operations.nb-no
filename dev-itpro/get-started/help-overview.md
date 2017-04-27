---
title: Hjelpeoversikt
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

# <a name="help-overview"></a>Hjelpeoversikt

Denne artikkelen gir en oversikt over komponentene til hjelpesystemet for Microsoft Dynamics 365 for Operations. Det forklarer også hvordan du kan angi egendefinerte dokumentasjon og opplæring for organisasjonen. 

Dynamics 365 for Operations inkluderer et hjelpesystem som er basert på to hovedkomponenter:

-   Et dokumentasjonsområde
-   Oppgaveveiledninger

Du har tilgang til både artikler og oppgaveveiledninger fra Hjelp-ruten i Dynamics 365 for Operations, som vist i følgende skjermbilde. [![Hjelp-rute](./media/help-pane-ops-task-guides-1024x741.png)](./media/help-pane-ops-task-guides.png) Denne artikkelen beskriver hjelpesystemet og forklarer hvordan du kan opprette egendefinerte dokumentasjons- og opplæringsressurser for organisasjonen.

## <a name="help-on-docsmicrosoftcom"></a>Hjelp på docs.microsoft.com
docs.microsoft.com-området ([docs.microsoft.com/dynamics365/operations](https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations) er den viktigste kilden til produktdokumentasjonen for Dynamics 365 for Operations. Området tilbyr følgende funksjoner:

-   **Tilgang til det mest oppdaterte innholdet** – Området gir oss en raskere og mer fleksibel måte å opprette, levere og oppdatere produktdokumentasjon på. Derfor garanterer det at du har tilgang til den nyeste tekniske informasjonen.
-    **Innhold som er skrevet av eksperter** – Området gir et omfattende sett med produktdokumentasjon som kan forbedres av fellesskapsmedlemmer både innenfor og utenfor Microsoft.
-   ** Tilgang til ulike typer innhold** – Området lar deg raskt få tilgang ulike typer innhold om Dynamics 365 for Operations, for eksempel Microsoft Office Mix-presentasjoner, oppgaveveiledninger, videoer og wiki-artikler.
-    **Innhold som støtter forretningsprosesser** – Området inneholder forretningsprosessfokusert innhold som drar nytte av Business Process Modeler (BPM) i Microsoft Dynamics Lifecycle Services (LCS).

Vi har flyttet alt innhold fra vår tidligere hjelp-wiki til dokumenter. Vi er svært fornøyde med det nye området, og det håper vi du også blir.

### <a name="when-can-we-use-it"></a>Når kan vi bruke den?

Du kan lese innhold på docs nå – den er helt offentlig og søkbar uten å logge på. Du kan bruke hvilke som helst av dine favorittsøkemotorer til å finne innhold. Du kan kommentere artikler på webområdet hvis du velger det, ved å logge på med en GitHub-konto.


## <a name="task-guides"></a>Oppgaveveiledninger
En oppgaveveiledning er en kontrollert, veiledet, interaktiv opplevelse som leder deg gjennom trinnene for en aktivitet eller forretningsprosess. Du kan åpne (spille av) en oppgaveveiledning fra Hjelp-ruten. Når du først klikker en oppgaveveiledning, vil Hjelp-ruten vise de trinnvise instruksjonene for oppgaven. Lokaliserte oppgaveveiledninger er nå tilgjengelige. [![Oppgaveveiledning – lesevisning](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png) For å starte den veiledede interaktive opplevelsen klikker du **Start oppgaveveiledning** nederst i Hjelp-ruten. En svart peker åpnes og angir handlingen som du må utføre. Følg instruksjonene som vises i brukergrensesnittet, og legg inn data i henhold til instruksjonene. [![Oppgaveveiledning – trinnvis instruksjon](./media/task-guide-step-1-ops.png)](./media/task-guide-step-1-ops.png) **Viktig:** Dataene som du angir når du spiller av en oppgaveveiledning, er ekte. Hvis du er i et produksjonsmiljø, legges dataene inn i firmaet som du bruker for øyeblikket.

### <a name="it-all-begins-with-task-recorder"></a>Alt begynner med Oppgaveregistrering

Oppgaveveiledninger opprettes ved hjelp av Oppgaveregistrering. Når du bruker Oppgaveregistrering, registreres alle handlingene du utfører i grensesnittet i Dynamics 365 for Operations (for eksempel velge menyer, endre innstillinger og skrive inn data). Samlet kalles trinnene som du registrerer en oppgaveregistrering. Som forklart i den forrige delen kan oppgaveregistreringer vises i Hjelp-ruten og spilles av som oppgaveveiledninger. Det finnes imidlertid andre måter som du kan bruke oppgaveregistreringer på:

-   **Lagre oppgaveregistreringer til BPM** – Du kan lagre en oppgaveregistrering på en linje i et hierarki i et BPM-bibliotek i LCS. Når du lagrer en oppgaveregistrering på BPM, genereres og vises et flytskjema sammen med trinnene i registreringen. **Merk:** For å vise en oppgaveregistrering i Dynamics 365 for Operations Hjelp-ruten og spille den av som en oppgaveveiledning, må du lagre registreringen i et BPM-bibliotek.
-   **Lagre oppgaveregistreringer som Word-dokumenter** – Ved å lagre en oppgaveregistrering som et Microsoft Word-dokument, kan du enkelt lage utskrivbare opplæringsveiledninger for organisasjonen.

Hvis du vil ha mer informasjon om Oppgaveopptaker, kan du se [Oppgaveopptaker i Dynamics 365 for Operations](../user-interface/task-recorder.md).

### <a name="creating-customized-task-recordings"></a>Opprette egendefinerte oppgaveregistreringer

Du kan opprette dine egne oppgaveregistreringer, eller du kan laste ned og tilpasse oppgaveregistering som Microsoft tilbyr. Du kan derfor opprette tilpasset Hjelp for organisasjonen som viser din spesifikke Dynamics 365 for Operations-implementering. For å vise en oppgaveregistrering i Dynamics 365 for Operations Hjelp-ruten og spille den av som en oppgaveveiledning, må du lagre registreringen i et BPM-bibliotek i LCS. Hvis du er partner og du hever nivået for et bibliotek til et firmabibliotek og inkludere det i en løsning, vil det være tilgjengelig for kundene dine. Hvis du vil se fullstendige instruksjoner, kan du se [Bruke oppgaveregistreringer til å opprette dokumentasjon og opplæring](../user-interface/task-recorder.md).

## <a name="in-product-help"></a>Hjelp i produktet
Hvis du vil ha tilgang til hjelpeinnhold i Dynamics 365 for Operations, velger du **Hjelp**-ikonet (**?**) og velger deretter Hjelp eller trykker på Ctrl + Skift +?. I begge tilfeller åpnes Hjelp-ruten. Fra Hjelp-ruten får du tilgang til artikler eller oppgaveveiledninger. [![](./media/help-pane-wiki-1024x684.png)](./media/help-pane-wiki.png)

### <a name="accessing-articles-from-the-help-pane"></a>Tilgang til artikler fra Hjelp-ruten

Fra Hjelp-ruten har du tilgang til artikler som gjelder for Dynamics 365 for Operations-klienten. Når du først åpner Hjelp-ruten og klikker kategorien **Wiki**, ser du artikler som gjelder for siden du er på i Dynamics 365 for Operations. Hvis det ikke finnes noen artikler, kan du angi nøkkelord for å presisere søket. Når du klikker en artikkel i Hjelp-ruten, åpnes en ny kategori i leseren og viser artikkelen. 

### <a name="accessing-task-guides-from-the-help-pane"></a>Tilgang til oppgaveveiledninger fra Hjelp-ruten

Før du kan få tilgang til oppgaveveiledninger fra **Hjelp**-ruten må en systemadministrator gå til Systemparametere-siden i Dynamics 365 for Operations og konfigurere noen innstillinger. **Merknader:**

-   Hvis du vil konfigurere hjelp, må du være logget på med en konto i samme leier som leier som Dynamics 365 for Operations er distribuert i.
-   Det er ikke mulig å koble til et LCS-biblioteket fra en forekomst av Dynamics 365 for Operations som kjører på en virtuell harddisk (VHD).

[![Skjemaet Systemparametere med innstillinger for hjelp](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) På **Systemparametere**-siden følger du disse trinnene:

1.  **Viktig: **Første gang du åpner kategorien Hjelp, må du koble til Lifecycle Services. Husk å klikke koblingen i midten av skjemaet, vent på tilkoblingen, lukk dialogboksen og klikk OK for å få tilgang til parameterskjemaet.[![Koble til LCS](./media/connect-to-lcs-crop-1024x365.png)](./media/connect-to-lcs-crop.png)
2.  Velg Lifecycle Services-prosjektet du vil koble til.
3.  Velg BPM-bibliotekene (i det valgte prosjektet) du vil hente oppgaveregistreringer fra.
4.  Angi visningsrekkefølge for BPM-bibliotekene. Dette bestemmer hvilken rekkefølge oppgaveregistreringer fra bibliotekene skal vises i, i Hjelp-ruten.

Når systemansvarlig har fullført disse trinnene, kan du åpne Hjelp-ruten og klikke kategorien **Oppgaveveiledninger**. Nå vil du se oppgaveveiledningene som gjelder for siden du er på i Dynamics 365 for Operations. Hvis det ikke finnes noen oppgaveveiledninger, kan du angi nøkkelord for å presisere søket. Når du klikker en oppgaveveiledning i Hjelp-ruten, viser Hjelp-ruten de trinnvise instruksjonene, og du kan spille av oppgaveveiledningen. [![Oppgaveveiledning – lesevisning](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png)

### <a name="where-are-the-translated-task-guides"></a>Hvor er oversatt oppgaveveiledningene?

Oversatte oppgaveveiledninger er utgitt i biblioteker med "Alle språk" i tittelen. Hvis du vil vise lokaliserte oppgaveveiledninger i Microsoft Dynamics 365 for Operations, kontroller at du er koblet til et riktig bibliotek. Språket som en oppgaveveiledning vises i, kontrolleres for hver bruker av språkinnstillingene under **Alternativer** &gt; **Innstillinger**. 
-   Hvis en oppgaveveiledning er oversatt, vil all teksten i oppgaveveiledningen vises på det valgte språket når du åpner oppgaveveiledningen.
-   Hvis en oppgaveveiledning ikke er oversatt, vil bare noe av teksten (teksten til kontrollene) vises på det valgte språket når du åpner oppgaveveiledningen.

## <a name="additional-resources"></a>Tilleggsressurser
Tabellen nedenfor viser webområder som tilbyr Dynamics 365 for Operations-innhold. Våre innholdswebområder er organiserte for å støtte livssyklusen til kunden. Hver fase støttes av et annet sett med områder. Områder med en stjerne (\*) ved siden av navnet, krever at du logger på med en konto som er knyttet til en serviceplan.

| Område                                                                     | beskrivelse                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Docs.microsoft.com](https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations) | Er vert for eller kobler til all produktdokumentasjon for Dynamics 365 for Operations.                                                                                                                                                               |
| [Lifecycle Services](http://lcs.dynamics.com/en/)\*                      | Gir et skybasert samarbeidsområde som kunder og partnere kan bruke til å administrere Dynamics 365 for Operations-prosjekter, fra førsalg til implementering og operasjoner. Dette området er nyttig i alle fasene ved implementering. |
| [CustomerSource](http://www.customersource.com/)\*                       | Inneholder omfattende opplæringsressurser og er det primære brukerstøtteområdet for Dynamics 365 for Operations. Pålogging kan være nødvendig for å få tilgang til bestemte ressurser på området.                                                                      |
| [Kundestøtteblogg](http://aka.ms/AXSupportBlog)                              | Gir tips som posteres av Dynamics 365 for Operations-kundestøtteteamet.                                                                                                                                                  |
| [MSDN](http://aka.ms/AXMSDN)                                             | Er vert for innhold fra tidligere versjoner som er skrevet for utviklere.                                                                                                                                                                       |
| [TechNet](http://aka.ms/TechNet)                                         | Vert for innhold fra tidligere versjoner som er skrevet for IT-medarbeidere og programbrukere.                                                                                                                                           |
| [Dynamics-fellesskapet](http://community.dynamics.com/en/)                  | Vert for blogger, forum og videoer.                                                                                                                                                                                                           |
| [Microsoft.com/Dynamics/](http://www.microsoft.com/dynamics/)                 | Gir informasjon om evaluering og salg.                                                                                                                                                                                                 |



<a name="see-also"></a>Se også
--------

[Dynamics 365 for Operations-hjelpesystem (nedlastbart faktaark)](https://mbs.microsoft.com/files/public/CS/AX2012R3/DynamicsAXHelpSystemFactSheet.pdf)

[Oppgaveopptaker i Microsoft Dynamics 365 for Operations](../user-interface/task-recorder.md)

[Lage dokumentasjon eller opplæring ved hjelp av oppgaveopptak](../user-interface/task-recorder.md)

[Nye eller oppdaterte oppgaveveiledninger (november 2016)](new-task-guides-november-2016.md)
[Nye eller oppdaterte oppgaveveiledninger (august 2016)](new-updated-task-guides-available-august-2016.md)
[Nye eller oppdaterte oppgaveveiledninger (mai 2016)](new-updated-task-guides-available-may-2016.md)
[Nye oppgaveveiledninger (februar 2016)](new-task-guides-available-february-2016.md)






