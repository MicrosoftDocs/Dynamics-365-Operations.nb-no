---
title: Behandling av avvik
description: Denne artikkelen beskriver det grunnleggende oppsettet som kreves for å bruke avvik. Ekstra oppsett er nødvendig hvis du vil bruke kvalitetsordrer.
author: perlynne
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9505e810ec1a34b2cb774ccde2273b16f92ba9e7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819382"
---
# <a name="nonconformance-management"></a>Behandling av avvik

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver det grunnleggende oppsettet som kreves for å bruke avvik. Ekstra oppsett er nødvendig hvis du vil bruke kvalitetsordrer.

Følg disse trinnene for å aktivere behandling av avvik:

1.  Definer lagerstyringsparameterne som er knyttet til avvik:
    -   Sett alternativet **Bruk kvalitetsstyring** til **Ja**.
    -   I **Timepris**-feltet angir du en timepris for arbeid i lokal valuta. Timeprisen brukes til å beregne kostnader for operasjoner som er knyttet til et avvik. Timeprisen og de beregnede kostnadene gir referanseinformasjon for et avvik. De samhandler ikke med annen funksjonalitet.
    -   Bruk **Kvalitetsstyring**-fanen på siden **Rapportoppsett** til å definere hvilken type dokument som skal skrives ut. Du kan skrive ut en avviksrapport, en avviksbrikke og en korrigeringsrapport. Du kan definere flere poster for å skrive ut forskjellige dokumenttyper i en rapport, eller for å skrive ut interne og eksterne merknader. Det kan være nyttig å bruke **Dokumenttype**-siden til å definere en unik dokumenttype for avvik, og en unik dokumenttype for rettelser. La oss for eksempel si at du vil angi merknader om et avvik ved hjelp av den unike dokumenttypen for avvik. I dette tilfellet kan du identifisere den unike dokumenttypen i rapportalternativene.
    -   Aktiver nummerserier for avvik og rettelsesreferanser.

2.  Aktiver brukergodkjenning av avvik. Bruk **Navn**-feltet på **Brukere**-siden til å tilordne en ansatt til hver bruker som må godkjenne et avvik. Systemet bruker de ansatte som endrer statusen for et avvik, til å spore avvikshistorikken. Brukere kan ikke godkjenne et avvik med mindre de har fått tilordnet en ansatt-ID.
3.  Definer problemtypene som skal tilordnes til avvik. Bruk **Problemtyper**-siden til å definere en klassifisering av kvalitetsproblemer som oppdages for de ulike avvikstypene. Du kan definere følgende avvikstyper: **Intern**, **Kunde**, **Leverandør**, **Tjenesteforespørsel**, **Produksjon** og **Koproduktproduksjon**. Bruk **Avvikstyper**-siden til å godkjenne en problemtype som skal brukes i én eller flere avvikstyper. En problemtype som for eksempel er knyttet til en defektkode, kan gjelde for alle avvikstyper, mens derimot en problemtype som er knyttet til kundeklager, kanskje bare gjelder for avvikstypene **Kunde** og **Tjenesteforespørsel**.
4.  Definer karantenesoner for å gi veiledning om hvordan materialer med defekter skal håndteres. Bruk **Karantenesoner**-siden til å definere soner som kan tilordnes til et avvik. Avviksetiketten som skrives ut, viser den tilordnede karantenesonen og informasjon om bruk, for å gi veiledning om hvordan materialer med defekter skal håndteres. Sonene kan tilsvare lagerlokasjoner eller operasjonsressurser.
5.  Definer diagnosetypene som skal tilordnes til rettelser. Bruk **Diagnosetyper**-siden til å definere en klassifisering av diagnosehandlinger. En rettelse angir hvilken type diagnosehandling som skal utføres for et godkjent avvik, og hvem som skal utføre denne handlingen. Den angir også den ønskede fullføringsdatoen og den planlagte fullføringsdatoen.
6.  Definer de relaterte operasjonene som skal tilordnes til avvik. Bruk **Operasjoner**-siden til å definere en klassifisering av arbeidet som kan utføres for et godkjent avvik. Når du tilordner en relatert operasjon til et avvik, kan du også gi detaljert informasjon, for eksempel informasjon om tilknyttede materialer, arbeidstimer og tillegg som kreves for å utføre operasjonen. Denne informasjonen brukes til å beregne en estimert kostnad for operasjonen. Den detaljerte informasjonen og de estimerte kostnadene er til referanse. De relaterte operasjonene for kvalitet er annerledes enn operasjonene som kan defineres for en produksjonsrute.


<a name="additional-resources"></a>Tilleggsressurser
--------

[Opprette og behandle et avvik](tasks/create-process-non-conformance.md)

[Kvalitetsstyringsprosesser](quality-management-processes.md)

[Definere forutsetninger for behandling av avvik](tasks/set-up-prerequisites-nonconformance-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]