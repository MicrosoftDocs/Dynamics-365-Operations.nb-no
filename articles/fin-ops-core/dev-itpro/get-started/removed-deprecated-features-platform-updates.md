---
title: Fjernede eller avskrevne Platform-funksjoner
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning i plattformoppdateringer av Finance and Operations-apper.
author: sericks007
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 6fc699907d30fff2d05e752ea055cae8d1134d9b
ms.sourcegitcommit: 3eaa71c889545318737b3bc88b05eae1a47ad2c0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/05/2020
ms.locfileid: "3433928"
---
# <a name="removed-or-deprecated-platform-features"></a>Fjernede eller avskrevne Platform-funksjoner

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning i plattformoppdateringer av Finance and Operations-apper.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging. 

> [!NOTE]
> Detaljert informasjon om objekter i Finance and Operations-apper finnes i [Tekniske referanserapporter](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av Finance and Operations-apper.

## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Plattformoppdateringer for versjon 10.0.12 av Finance and Operations-apper

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Skjemautvidelser for rutenett- eller gruppekontroll som inneholder ugyldige feltreferanser

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Egenskapen datagruppe i rutenett- eller gruppekontroller brukes til automatisk å vise alle felt i en feltgruppe. Et rutenett eller en gruppekontroll som er lagt til via en utvidelse, kan inneholde felt som ikke lenger er definert i feltgruppen, eller de kan mangle felt som er definert i feltgruppen. Dette kan føre til inkonsekvent virkemåte ved kjøring. Plattformoppdateringer for versjon 10.0.12 av Finance and Operations-apper kategoriserer nå dette problemet som en kompilerings-*advarsel*. Du kan løse dette problemet ved å åpne skjemautvidelsen og lagre den.
| **Erstattet med en annen funksjon?**   | Denne kompilatoradvarselen vil bli erstattet med en kompilatorfeil i en fremtidig oppdatering. |
| **Berørte produktområder**         | Visual Studio-utviklingsverktøy |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | En kompilatoradvarsel er introdusert i plattformoppdateringer for versjon 10.0.12 av Finance and Operations-apper. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Plattformoppdateringer for versjon 10.0.11 av Finance and Operations-apper

### <a name="explicit-whitelisting-for-self-service-environments"></a>Eksplisitt hvitlisting for selvbetjeningsmiljøer

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Prosessen for IP-hvitlisting er endret. Selvbetjening støtter ikke lenger IP-hvitlisting. |
| **Erstattet med en annen funksjon?**   | Hvis du vil ha mer informasjon, kan du se [Konfigurere betinget tilgang for Azure Active Directory](https://docs.microsoft.com/appcenter/general/configuring-aad-conditional-access).|
| **Berørte produktområder**         | Sikkerhet |
| **Distribusjonsalternativ**              | Sky |
| **Status**                         | **Avviklet:** Denne funksjonen er fullstendig avviklet for selvbetjent distribusjon. |

### <a name="visual-studio-2015"></a>Visual Studio2015

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | For å støtte de siste versjonene av Visual Studio må det gjøres enkelte endringer i X++-utvidelser for Visual Studio. Disse endringene er ikke kompatible med Visual Studio 2015. |
| **Erstattet med en annen funksjon?**   | Visual Studio 2017 vil erstatte Visual Studio 2015 som den distribuerte og påkrevde versjonen. |
| **Berørte produktområder**         | Visual Studio-utviklingsverktøy |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Når de nye virtuelle maskinene (VM-er) med Visual Studio 2017 kunngjøres, må eksisterende VM-er med bare Visual Studio 2015 distribueres på nytt via Lanseringsbølge 1 for 2021. |

### <a name="field-groups-containing-invalid-field-references"></a>Feltgrupper med ugyldige feltreferanser

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Feltgrupper i definisjoner av tabellmetadata kan inneholde feltreferanser som ikke er gyldige. Hvis disse feltgruppene er distribuert, kan dette føre til kjøretidsfeil for kjøring i Financial Reporting og Microsoft SQL Server Reporting Services (SSRS). Platform Update 23 innførte en kompilator-*advarsel* som muliggjorde håndtering av dette sikkerhetsproblemet. Plattformoppdateringer for versjon 10.0.11 av Finance and Operations-apper kategoriserer dette problemet som en kompilerings*feil*.<p>Følg fremgangsmåten nedenfor for å løse problemet.</p><ol><li>Fjern den ugyldige feltreferansen fra definisjonen for tabellfeltgruppen.</li><li>Kompiler på nytt.</li><li>Kontroller at eventuelle feil er tatt hånd om.</li></ol> |
| **Erstattet med en annen funksjon?**   | Denne kompileringsfeilen erstatter kompileringsadvarselen permanent.  |
| **Berørte produktområder**         | Visual Studio-utviklingsverktøy |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | **Avskrevet:** Kompilatoradvarselen er en kompilatorfeil i plattformoppdateringer for versjon 10.0.11 av Finance and Operations-apper. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>ISV-lisenser opprettet ved hjelp av SHA1-nummeralgoritmen

|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Prosessen med å opprette uavhengige programvareleverandørlisenser (ISV) er endret. Hvis du vil ha mer informasjon, kan du se [Uavhengig programvareleverandørlisensiering (ISV)](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Erstattet med en annen funksjon?**   | Ja. Bruk Windows PowerShell til å opprette lisenser. |
| **Berørte produktområder**         | Visual Studio-utviklingsverktøy |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | <strong>Avskrevet:</strong> ISV-lisenser som ble opprettet ved hjelp av SHA1-nummeralgoritmen. Denne algoritmen er avhengig av sertifikater som ble opprettet ved hjelp av MakeCert-verktøyet, og dette verktøyet er avskrevet.<p><strong>Avskrevet:</strong> Bruken av SHA1 for sikkerhet eller nummerering. SHA1 vil slutte å fungere tidlig i 2021. Derfor bør den ikke lenger brukes.<p><strong>Fjernet:</strong> Støtte for Transport Layer Security (TLS)1.0 og TLS 1.1, innkommende eller utgående forespørsler. |

## <a name="platform-update-32"></a>Plattform update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialogboksen Endring av arbeidsflytforespørsel inneholder ikke lenger en rullegardinliste for brukervalg
|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Dette var et sikkerhetsproblem fordi endringsforespørselen kunne sendes til en utilsiktet bruker. Dette var også et bruksproblem, fordi det tvang brukeren til å finne ut hvem arbeidsflytavsenderen var, og manuelt velge dem.  |
| **Erstattet med en annen funksjon?**   | Nei |
| **Berørte produktområder**         | Arbeidsflyt |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Rullegardinlisten for brukervalg ble fjernet fra dialogboksen for forespørselsendring i Platform Update 32. Forespørsler om forespørselsendring sendes automatisk til avsenderen som planlagt. Hvis du vil ha mer informasjon om denne funksjonaliteten, kan du se [Handlinger i godkjenningsprosesser i en arbeidsflyt](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Innebygde koblinger med detaljer som ikke lenger støttes i paginerte dokumenter som er gjengitt av den skybaserte tjenesten 
|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | URL-adresser for navigasjon som er innebygd i dokumenter som er gjengitt av tjenesten, kan inneholde sensitive forretningsdata. Vi fjerner støtte for innebygde gjennomgangskoblinger i dokumenter som et sikkerhetstiltak for å beskytte kundens data bedre. Brukere vil også dra nytte av forbedret ytelse samtidig som de får dokumenter på en proaktiv måte som følge av denne endringen.  |
| **Erstattet med en annen funksjon?**   | Nr. |
| **Berørte produktområder**         | Rapportering |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Denne funksjonen fjernes aktivt fra tjenesten.<br><br>Modern-klienten har mange alternativer for å produsere visninger som omfatter automatisk genererte koblinger som hjelp til å navigere i programmet. Paginerte dokumenter som er gjengitt av tjenesten, anbefales for ekstern kommunikasjon som sendes via e-post, arkiveres og skrives ut for mottakere. Vi har forbedret opplevelsen for forhåndsvisning av dokumenter direkte i Web-leseren, som gir direkte tilgang til lokale skrivere. Hvis du vil ha mer informasjon, se [Forhåndsvise PDF-dokumenter med et innebygd visningsprogram](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere kunngjøringer om fjernede eller avskrevne funksjoner
Hvis du vil lære mer om funksjoner som er fjernet eller avskrevet i tidligere versjoner, kan du se [Fjernede eller avskrevne funksjoner i tidligere versjoner](../migration-upgrade/deprecated-features.md).

