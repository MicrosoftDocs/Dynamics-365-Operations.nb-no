---
title: Definere forutsetninger for behandling av avvik
description: Bruk dette emnet for å aktivere prosjektstyringsprosesser for avvik.
author: perlynne
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c4de822dcda604241416165a961e4b0bacaeb5b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434665"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a>Definere forutsetninger for behandling av avvik

[!include [banner](../../includes/banner.md)]

Bruk dette emnet for å aktivere prosjektstyringsprosesser for avvik. Et avvik beskriver en prosedyre eller vare som har et kvalitetsproblem, der den beskrivende informasjonen inkluderer kilden og problemtypen. Denne prosedyren bruker demonstrasjonsdatafirmaet USMF. Denne prosedyren utføres vanligvis av en kvalitetssjef.


## <a name="enable-quality-management-processes-within-the-company"></a>Aktivere kvalitetsstyringsprosesser i firmaet
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Parametere for beholdnings- og lagerstyring**.
2. Velg kategorien **Kvalitetsstyring**.
3. Velg **Ja** i feltet **Bruk kvalitetsstyring** for å aktivere kvalitetsstyringsprosesser for firmaet.
4. I **Timepris**-feltet angir du et tall i lokal valuta. Timeprisen brukes til å beregne kostnader for operasjoner som er knyttet til et avvik. Timeprisen og de beregnede kostnadene gir referanseinformasjon for et avvik, og de har ingen betydning for annen funksjonalitet.  
5. Velg **Rapportoppsett** for å definere merknadstypene for kvalitetsrapport som skal brukes i ulike typer kvalitetsstyringsrapporter.

## <a name="enable-user-for-nonconformance-processing"></a>Aktivere bruker for behandling av avvik
1. I navigasjonsruten går du til **Moduler > Systemadministrasjon > Brukere > Brukere**. 
2. Bruk hurtigfilteret til å finne brukeren som skal godkjenne eller avvise avvikspostene. Du kan for eksempel filtrere på **Navn**-feltet med verdien `Ricardo`. Hvis du vil behandle godkjenningen av et avvik, må brukeren som godkjenner eller avviser avvik ha en "Navn"-verdi som er tilordnet på siden **Brukere**. Hvis du vil bruke merknader i dokumentet, må brukeren også ha Dokumenthåndtering aktivert i brukeralternativene.  
3. Merk raden med den ønskede posten.
4. Velg **Brukeralternativer**.
5. Velg kategorien **Innstillinger**.
6. Velg **Ja** i feltet **Aktiver dokumentoversikt**.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Definere diagnosetyper for behandling av avvik
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Kvalitetsstyring > Diagnosetyper**. Bruk **Diagnosetyper**-siden til å definere en klassifisering av diagnosehandlinger. En korrigering identifiserer hvilken type diagnosehandling som bør utføres når det gjelder godkjente avvik, hvem som skal utføre den og den ønskede og planlagte fullføringsdatoen.  
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **Diagnose**.
4. Skriv inn en verdi i **Beskrivelse**-feltet.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Definere kvalitetsendringer for behandling av avvik
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Kvalitetsstyring > Kvalitetsstyringstillegg**. Bruk siden **Kvalitetsstyringstillegg** til å definere en klassifisering av tilleggene som skal brukes til operasjoner som er knyttet til avvik.  
2. Velg **Ny**.
3. Skriv inn en verdi i **Tilleggskode**-feltet.
4. Skriv inn en verdi i **Beskrivelse**-feltet.

## <a name="define-the-operations-for-nonconformance-processing"></a>Definere operasjonene for behandling av avvik
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Kvalitetsstyring > Operasjoner**. Bruk **Operasjoner**-siden til å definere en klassifisering av arbeidet som kan utføres for et godkjent avvik. Når du relaterer operasjon til et avvik, kan du angi informasjon om tilknyttede materialer, arbeidstimer og tillegg som kreves for å utføre operasjonen. Denne informasjonen danner grunnlaget for beregning av en estimert kostnad for å utføre operasjonen.  
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **Operasjon**.
4. Skriv inn en verdi i **Beskrivelse**-feltet.

## <a name="define-problem-types-for-nonconformance-processing"></a>Definere problemtyper for behandling av avvik
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Kvalitetsstyring > Problemtyper**. Bruk **Problemtyper**-siden til å definere en klassifisering av kvalitetsproblemer som oppdages i de ulike avvikstypene. Avvikstyper inkluderer **Intern**, **Kunde**, **Leverandør**, **Tjenesteforespørsel**, **Produksjon** og **Koproduktproduksjon**. En enkelt problemtype kan være tilknyttet flere avvikstyper.  
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **Problemtype**.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Velg **Avvikstyper**. Bruk **Avvikstyper**-siden til å godkjenne bruk av en problemtype som skal brukes i én eller flere av avvikstypene. For eksempel kan en problemtype som gjelder en mangelkode, gjelde alle avvikstyper, mens en problemtype som gjelder klager fra kunder, kan gjelde bare for avvikstypene kunde og serviceforespørsel.  
6. Velg **Ny**.
7. Velg et alternativ i **Avvikstype**-feltet i den nye raden.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Definere karantenesoner for behandling av avvik
1. I navigasjonsruten går du til **Moduler > Lagerstyring > Oppsett > Kvalitetsstyring > Karantenesoner**.
2. Velg **Ny**.
3. Skriv inn en verdi i feltet **Karantenesone**.
4. Skriv inn en verdi i **Beskrivelse**-feltet.
5. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]