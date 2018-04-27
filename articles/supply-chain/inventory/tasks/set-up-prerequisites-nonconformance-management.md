---
title: Definere forutsetninger for behandling
description: "Bruk denne fremgangsmåten for å aktivere prosjektstyringsprosesser for avvik."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4bb4af7cb7aff101a8b9e6162823515f63b12886
ms.openlocfilehash: 9b5b05a3c00f093066a2714964bb99146427c3bc
ms.contentlocale: nb-no
ms.lasthandoff: 11/02/2017

---
# <a name="set-up-prerequisites-for-management"></a>Definere forutsetninger for behandling

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Bruk denne fremgangsmåten for å aktivere prosjektstyringsprosesser for avvik. Et avvik beskriver en prosedyre eller vare som har et kvalitetsproblem, der den beskrivende informasjonen inkluderer kilden og problemtypen. Denne prosedyren bruker demonstrasjonsdatafirmaet USMF. Denne prosedyren utføres vanligvis av en kvalitetssjef.


## <a name="enable-quality-management-processes-within-the-company"></a>Aktivere kvalitetsstyringsprosesser i firmaet
1. Gå til Lagerstyring > Oppsett > Parametere for beholdnings- og lagerstyring.
2. Klikk kategorien Kvalitetsstyring.
3. Velg Ja i feltet Bruk kvalitetsstyring.
    * Velg denne parameteren for å aktivere kvalitetsstyringsprosesser for firmaet.  
4. Angi et tall i Timepris-feltet.
    * Bruk Timepris-feltet for å angi en timepris for arbeid i lokal valuta. Timeprisen brukes til å beregne kostnader for operasjoner som er knyttet til et avvik. Timeprisen og de beregnede kostnadene gir referanseinformasjon for et avvik, og de har ingen betydning for annen funksjonalitet.  
5. Klikk Rapportoppsett.
    * Denne siden lar deg definere merknadstypene for kvalitetsrapport som skal brukes i ulike typer kvalitetsstyringsrapporter.  
6. Lukk siden.
7. Lukk siden.

## <a name="enable-user-for-nonconformance-processing"></a>Aktivere bruker for behandling av avvik
1. Gå til Systemadministrasjon > Brukere > Brukere.
    * Hvis du vil behandle godkjenningen av et avvik, må brukeren som godkjenner eller avviser avvik ha en "Navn"-verdi som er tilordnet på siden Brukere. Hvis du vil bruke merknader i dokumentet, må brukeren også ha Dokumenthåndtering aktivert i brukeralternativene.  
2. Bruk hurtigfilteret for å søke etter poster. Du kan for eksempel filtrere på Navn-feltet med verdien Ricardo.
    * Bruk filteret til å finne brukeren som skal godkjenne eller avvise avvikspostene.  
3. Klikk koblingen i den valgte raden i listen.
    * Hvis du vil behandle godkjenningen av et avvik, må du passe på at brukeren som godkjenner eller avviser avvik har en "Navn"-verdi som er tilordnet på siden Brukere.  
4. Klikk Brukeralternativer.
5. Klikk kategorien Innstillinger.
6. Velg Ja i feltet Aktiver dokumentoversikt.
    * Hvis du vil bruke merknader i dokumentet, må brukeren også ha Dokumenthåndtering aktivert i brukeralternativene.  
7. Lukk siden.
8. Lukk siden.
9. Lukk siden.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Definere diagnosetyper for behandling av avvik
1. Gå til Lagerstyring > Oppsett > Kvalitetsstyring > Diagnosetyper.
    * Bruk Diagnosetyper-siden til å definere en klassifisering av diagnosehandlinger. En korrigering identifiserer hvilken type diagnosehandling som bør utføres når det gjelder godkjente avvik, hvem som skal utføre den og den ønskede og planlagte fullføringsdatoen.  
2. Klikk Ny.
3. Skriv inn en verdi i feltet Diagnose.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Lukk siden.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Definere kvalitetsendringer for behandling av avvik
1. Gå til Lagerstyring > Oppsett > Kvalitetsstyring > Kvalitetsstyringstillegg.
    * Bruk siden Kvalitetsstyringstillegg til å definere en klassifisering av tilleggene som skal brukes til operasjoner som er knyttet til avvik.  
2. Klikk Ny.
3. Skriv inn en verdi i Tilleggskode-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Lukk siden.

## <a name="define-the-operations-for-nonconformance-processing"></a>Definere operasjonene for behandling av avvik
1. Gå til Lagerstyring > Oppsett > Kvalitetsstyring > Operasjoner.
    * Bruk Operasjoner-siden til å definere en klassifisering av arbeidet som kan utføres for et godkjent avvik. Når du relaterer operasjon til et avvik, kan du angi informasjon om tilknyttede materialer, arbeidstimer og tillegg som kreves for å utføre operasjonen. Denne informasjonen danner grunnlaget for beregning av en estimert kostnad for å utføre operasjonen.  
2. Klikk Ny.
3. Skriv inn en verdi i feltet Operasjon.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Lukk siden.

## <a name="define-problem-types-for-nonconformance-processing"></a>Definere problemtyper for behandling av avvik
1. Gå til Lagerstyring > Oppsett > Kvalitetsstyring > Problemtyper.
    * Bruk Problemtyper-siden til å definere en klassifisering av kvalitetsproblemer som oppdages i de ulike avvikstypene. Avvikstyper inkluderer Intern, Kunde, Leverandør, Tjenesteforespørsel, Produksjon og Koproduktproduksjon. En enkelt problemtype kan være tilknyttet flere avvikstyper.  
2. Klikk Ny.
3. Skriv inn en verdi i feltet Problemtype.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Klikk Avvikstyper.
    * Bruk Avvikstyper-siden til å godkjenne bruk av en problemtype som skal brukes i én eller flere av avvikstypene. For eksempel kan en problemtype som gjelder en mangelkode, gjelde alle avvikstyper, mens en problemtype som gjelder klager fra kunder, kan gjelde bare for avvikstypene kunde og serviceforespørsel.  
6. Klikk Ny.
7. Merk den valgte raden i listen.
8. Velg et alternativ i Avvikstype-feltet.
9. Lukk siden.
10. Lukk siden.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Definere karantenesoner for behandling av avvik
1. Gå til Lagerstyring > Oppsett > Kvalitetsstyring > Karantenesoner.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Karantenesone.
4. Skriv inn en verdi i feltet Beskrivelse.
5. Lukk siden.

