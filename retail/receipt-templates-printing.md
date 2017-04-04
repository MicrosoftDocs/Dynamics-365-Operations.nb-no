---
title: Kvitteringsmaler og utskrift
description: "Denne artikkelen beskriver hvordan du oppretter og endrer skjemaoppsett for å styre hvordan kvitteringer, fakturaer og andre dokumenter blir skrevet ut. Microsoft Dynamics 365 for operasjoner - Retail inkluderer oppsett skjemautformer som du kan bruke til å opprette og endre forskjellige typer skjemaoppsett."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fabaacbc7187b38a1745c2139a9eb7760f2be987
ms.lasthandoff: 03/31/2017


---

# <a name="receipt-templates-and-printing"></a>Kvitteringsmaler og utskrift

Denne artikkelen beskriver hvordan du oppretter og endrer skjemaoppsett for å styre hvordan kvitteringer, fakturaer og andre dokumenter blir skrevet ut. Microsoft Dynamics 365 for operasjoner - Retail inkluderer oppsett skjemautformer som du kan bruke til å opprette og endre forskjellige typer skjemaoppsett.

**Viktig:** du må definere skjemaoppsett og mottak profiler for å skrive ut kvitteringer og andre dokumenter fra moderne Kvitteringen og sky POS. Du kan inkludere flere skjemaoppsett i en profil for mottak. Deretter kan du tilordne kvitteringsprofilen til en skriver ved å endre en maskinvareprofil.

## <a name="set-up-a-receipt-format"></a>Konfigurere en kvitteringsprofil
1.  Klikk **Retail og commerce**&gt;**kanaloppsett**&gt;**POS installasjonsprogrammet**&gt;**POS**&gt;**mottak Formater**.
2.  På siden **Kvitteringsformat** klikker du **Ny** for å opprette et nytt skjemaoppsett, eller velger et eksisterende skjemaoppsett.
3.  I **Kvitteringsformat**-feltet skriver du inn en ID for skjemaoppsettet, og deretter velger du kvitteringstypen som oppsettet brukes for. Du kan også skrive inn en beskrivelse og et kort navn for kvitteringen i **Tittel**-feltet.
4.  På hurtigkategorien **Generelt** velg et alternativ for å definere virkemåten for utskrift:
    -   **Skrives alltid ut** – Kvitteringen skrives automatisk ut etter behov.
    -   **Ikke skriv ut** – Kvitteringen skrives ikke ut.
    -   **Spør bruker** – Brukeren blir spurt om å skrive ut kvitteringen.
    -   **Etter behov** – Dette alternativet brukes bare for gavekvitteringer. Når dette alternativet er valgt, kan brukeren skrive ut en gavekvittering fra siden **Endre**, hvis en gavekvittering er nødvendig.

## <a name="design-a-receipt-format"></a>Utforme et kvitteringsformat
Bruke skjemaoppsettutformingen til grafisk å opprette oppsettet for skjemadokumentet. Siden **Utforming av kvitteringsformat** består av tre deler: **hode**, **linjer** og **bunntekst**. Noen typer skjemaoppsett bruker elementer fra alle tre delene, mens andre typer bruker elementer fra bare én eller to deler. Hvis du vil vise elementene som er tilgjengelige for hver del, klikker du den aktuelle knappen i navigasjonsruten til venstre på siden.

1.  Klikk **Retail og commerce**&gt;**kanaloppsett**&gt;**POS installasjonsprogrammet**&gt;**POS**&gt;**mottak Formater**.
2.  På siden **Kvitteringsformat** velger du et skjemaoppsett, og klikk deretter **Utforming**.
3.  Klikk **Kjør** for å installere utformingsverten for detaljhandel.
4.  I varslingsfeltet som vises nederst i Internet Explorer-vinduet, klikker du **Åpne** for å installere ettklikksutformingen. (Varselfeltet kan vises på et annet sted i andre lesere.) Fremdriftsindikatoren viser fremdriften for installasjonen.
5.  Når installasjonen er fullført, angir du Dynamics-365 for operasjoner brukernavn og passord, og klikk deretter **logge på** til å starte utformingen.
6.  Når legitimasjonen er validert og utformingen starter, kan du begynne å utforme kvitteringsformatet eller endre et eksisterende format.
7.  Hvis du vil opprette elementene for skjemaet, velger du delen **Hode**, **Linjer** eller **Bunntekst**, og deretter drar du et element fra denne delen til arbeidsområdet. De fleste elementene inneholder variabler som automatisk fylles ut med data fra databasen. Andre elementer, for eksempel **Tekst**, lar deg skrive ut egendefinert tekst på kvitteringen. **Obs!** Du kan angi hvor mange linjer som hver del skal omfatte, ved å justere antallet nederst til høyre i denne delen. For å gjøre det lettere å endre en del kan du øke høyden ved å dra størrelseslinjen nederst i delen. Høyden på delen i arbeidsområdet påvirker ikke antall linjer på selve kvitteringen.
8.  Når du har dratt et element til arbeidsområdet, angir du egenskapene for delen i **Objektinformasjon**-ruten nederst på siden. Angi én eller flere av følgende innstillinger:
    -   **Juster** – Sett justeringen for feltet til **Venstre** eller **Høyre**.
    -   **Fylltegn** – Angi mellomromstegnet. Det brukes et tomt felt som standard, men du kan angi hvilket som helst tegn.
    -   **Prefiks** – Angi verdien som vises i begynnelsen av det valgte feltet. Denne innstillingen gjelder bare for **Linjer**-delen av oppsettet.
    -   **Tegn** – Angi maksimalt antall tegn som feltet kan inneholde hvis elementet har en variabel. Hvis teksten i feltet er lengre enn de antallet tegn du angir, avkortes teksten for å få plass i feltet.
    -   **Variabel** – Det merkes automatisk av for dette alternativet hvis elementet inneholder en variabel og ikke kan tilpasses.
    -   **Skrifttype** – Sett skriftstilen til **Normal** eller **Fet**. Fete bokstaver bruker dobbelt så mye plass som vanlige bokstaver. Derfor kan det hende at enkelte tegn blir avkortet.
    -   **Slett** – Klikk denne knappen for å fjerne den valgte delen fra skjemaoppsettet.

## <a name="assign-receipt-profiles"></a>Tilordne kvitteringsprofiler
Kvitteringsprofiler tilordnes direkte til skrivere i maskinvareprofilen.

1.  Åpne maskinvareprofilen ved å klikke **Retail og commerce**&gt;**kanaloppsett**&gt;**POS installasjonsprogrammet**&gt;**POS profiler**&gt;**maskinvareprofil**.
2.  Velge skriveren, og deretter i feltet **Kvitteringsprofil **tilordne kvitteringsprofilen som skal brukes for kassen.

**Obs!** Hvis det brukes to skrivere, kan én skriver brukes til å skrive ut standard 40-kolonners termiske kvitteringer. Den andre skriveren brukes vanligvis til å skrive ut helsides kvitteringstyper som trenger mer informasjon. Disse kvitteringstypene omfatter kundeordrekvitteringer og kundefakturaer.


