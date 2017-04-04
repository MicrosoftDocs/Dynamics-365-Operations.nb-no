---
title: Behandling av avvik
description: "Denne artikkelen beskriver det grunnleggende oppsettet som kreves for å bruke avvik. Ekstra oppsett er nødvendig hvis du vil bruke kvalitetsordrer."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 6f25e2930ff265df1f938cdf56e8a0f4993617af
ms.lasthandoff: 03/31/2017


---

# <a name="nonconformance-management"></a>Behandling av avvik

Denne artikkelen beskriver det grunnleggende oppsettet som kreves for å bruke avvik. Ekstra oppsett er nødvendig hvis du vil bruke kvalitetsordrer. 

Følg disse trinnene for å aktivere behandling av avvik:

1.  Definer lagerstyringsparameterne som er knyttet til avvik:
    -   Sett alternativet **Bruk kvalitetsstyring** til **Ja**.
    -   I **Timepris**-feltet angir du en timepris for arbeid i lokal valuta. Timeprisen brukes til å beregne kostnader for operasjoner som er knyttet til et avvik. Timeprisen og de beregnede kostnadene gir referanseinformasjon for et avvik. De samhandler ikke med annen funksjonalitet.
    -   Bruk av **kvalitetsstyring** kategorien på den **rapportoppsett** siden for å definere hvilken type dokument skal skrives ut. Du kan skrive ut en avviksrapport, en avviksbrikke eller et rettelsesrapporten. Du kan definere flere poster for å skrive ut forskjellige dokumenttyper i en rapport, eller for å skrive ut interne og eksterne merknader. Det kan være nyttig å bruke **Dokumenttype**-siden til å definere en unik dokumenttype for avvik, og en unik dokumenttype for rettelser. La oss for eksempel si at du vil angi merknader om et avvik ved hjelp av den unike dokumenttypen for avvik. I dette tilfellet kan du identifisere den unike dokumenttypen i rapportalternativene.
    -   Aktiver nummerserier for avvik og rettelsesreferanser.

2.  Aktiver brukergodkjenning av avvik. Bruk **Navn**-feltet på **Brukere**-siden til å tilordne en ansatt til hver bruker som må godkjenne et avvik. Systemet bruker de ansatte som endrer statusen for et avvik, til å spore avvikshistorikken. Brukere kan ikke godkjenne et avvik med mindre de har fått tilordnet en ansatt-ID.
3.  Definer problemtypene som skal tilordnes til avvik. Bruk **Problemtyper**-siden til å definere en klassifisering av kvalitetsproblemer som oppdages for de ulike avvikstypene. Du kan definere følgende avvikstyper: **Intern**, **Kunde**, **Leverandør**, **Tjenesteforespørsel**, **Produksjon** og **Koproduktproduksjon**. Bruk **Avvikstyper**-siden til å godkjenne en problemtype som skal brukes i én eller flere avvikstyper. En problemtype som for eksempel er knyttet til en defektkode, kan gjelde for alle avvikstyper, mens derimot en problemtype som er knyttet til kundeklager, kanskje bare gjelder for avvikstypene **Kunde** og **Tjenesteforespørsel**.
4.  Definer karantenesoner for å gi veiledning om hvordan materialer med defekter skal håndteres. Bruk **Karantenesoner**-siden til å definere soner som kan tilordnes til et avvik. Avviksetiketten som skrives ut, viser den tilordnede karantenesonen og informasjon om bruk, for å gi veiledning om hvordan materialer med defekter skal håndteres. Sonene kan tilsvare lagerlokasjoner eller operasjonsressurser.
5.  Definer diagnosetypene som skal tilordnes til rettelser. Bruk **Diagnosetyper**-siden til å definere en klassifisering av diagnosehandlinger. En rettelse angir hvilken type diagnosehandling som skal utføres for et godkjent avvik, og hvem som skal utføre denne handlingen. Den angir også den ønskede fullføringsdatoen og den planlagte fullføringsdatoen.
6.  Definer de relaterte operasjonene som skal tilordnes til avvik. Bruk **Operasjoner**-siden til å definere en klassifisering av arbeidet som kan utføres for et godkjent avvik. Når du tilordner en relatert operasjon til et avvik, kan du også gi detaljert informasjon, for eksempel informasjon om tilknyttede materialer, arbeidstimer og tillegg som kreves for å utføre operasjonen. Denne informasjonen brukes til å beregne en estimert kostnad for operasjonen. Den detaljerte informasjonen og de estimerte kostnadene er til referanse. De relaterte operasjonene for kvalitet er annerledes enn operasjonene som kan defineres for en produksjonsrute.


<a name="see-also"></a>Se også
--------

[Opprette og behandle et avvik (aktivitet guide)](https://ax.help.dynamics.com/en/wiki/create-and-process-a-nonconformance/)

[Quality management processes](quality-management-processes.md)

[Definer forutsetninger for avvik management (aktivitet guide)](https://ax.help.dynamics.com/en/wiki/set-up-prequisites-for-nonconformance-management/)


