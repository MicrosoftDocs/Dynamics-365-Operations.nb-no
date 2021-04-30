---
title: Nyheter eller enderinger i Dynamics 365 Human Resources 22. mars 2021
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 22. mars 2021.
author: marcelbf
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b973be365b3afa8461f7709c1ecee835c5dcf2f1
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890657"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-22-2021"></a>Nyheter eller enderinger i Dynamics 365 Human Resources 22. mars 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver funksjoner som er nye, endret eller kommer snart i Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.4049.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjoner er allment tilgjengelige i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Alternativ for å tvinge annullering og tilbakestilling av satsvise jobber som står fast (560976) | NA | [Tilbakestille satsvise jobber som står fast](./hr-admin-troubleshooting-batch-execution.md) |
| Små oppdateringer av brukeropplevelsen for oppretting av ny fordelsplan (419941) | NA | [Opprette en fordelsplan](hr-benefits-plans-setup.md) |

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Dette emnet kan være oppdateringer for å inkludere feilrettingsfiler som ble tatt med i builden etter at dette emnet ble publisert.

| Utstedelsesnummer | Problem |  beskrivelse |
| --- | --- | --- |
| 554239 | Ytelsesforbedringer for enheter som er relatert til tabellen **BusinessProcessTaskAssignment** | Få bedre ytelse for enheter som er relatert til tabellen **BusinessProcessTaskAssignment**, ved å legge til foreslåtte indekser i tabellen. |
| 566061 | Fjern tilbakefallskode for V2-enheter fra nattsynkronisering | Fjern V2-tilbakefallskode for Dataverse-nattsynkronisering. Tilbakefall er ikke lenger nødvendig, og det forhindrer at filtrert synkronisering fungerer som forventet. Endringen forbedrer konsekvensen av Dataverse-datasynkronisering. |
| 538024 | Fordelsplaner for arbeider > Fjern utsjekking medfører feil | Løst feil når du fjerner utsjekking for fordelsplanalternativet i skjemaet Arbeidsfordeler. |
| 557965 | **Fordeler**-arbeidsområdet: **Aktive livshendelser**-koblingen skal alltid være synlig i **Koblinger**-delen | Løst problem der **Aktive livshendelser**-koblingen var synlig i **Koblinger**-delen, men utløste en feil under forsøk på å navigere hvis funksjonen **(Forhåndsversjon) Arbeidsområde for fordelsbehandling** ikke er aktivert. Hvis du vil ha mer informasjon om aktivering av arbeidsområdet, kan du se [Arbeidsområde for fordelsbehandling](hr-benefits-management-workspace.md). |
| 556672 | Kan ikke behandle avsetninger for en ansatt som har sluttet, når **Strømlinjeformet ansattoppføring** er aktivert i Funksjonsbehandling | Alternativet for å avsette permisjons- og fraværsplaner er lagt til i **Flere alternativer** under **Arbeidshistorikk** for ansatte når **Strømlinjeformet ansattoppføring** er aktivert i Funksjonsbehandling. |
| 562656 | Menyelementet **SysRecordChangeLogValidTimeState** skal være inkludert i en sikkerhetsrettighet og en utvidelse av sikkerhetsplikten **SystemExternalBasicMaintain** | Andre roller enn systemadministrator mangler knappen **Vis endringer** i datobehandlingsskjemaene. |
| 505989 | Behandling av livshendelser: Rettighetsendring behandles ikke riktig på grunn av forfallsdatoen som er brukt | Løst et problem der endring i rettighetsbehandling var avhengig av startdatoen for stillingen, og ikke bare gjeldende stilling. |
| 562286 | Avslutt arbeider sender flere oppdateringer til Dataverse | Når en arbeider avsluttes, sendes mer enn én oppdateringsoperasjon til Dataverse, noe som resulterer i to oppdateringsmeldinger for samme endring. Dette kan forårsake flere utløsere hvis en Power Automate-flyt er konfigurert til å utløses fra handlingen. |
| 527340 | Feilen "Urepresenterbar DateTime" vises når permisjons- og fraværsregistreringer åpnes | Når du velger en permisjons- og fraværsregistrering, vises ikke feilen lenger. |
| 561663 | Økt ventetidsintervall for klyngeklargjøring | Oppnå bedre infrastrukturstabilitet og mer konsekvent klargjøring med oppdateringer for klyngeklargjøring. |
| 486129 | Kan ikke redigere egendefinerte felter i **Stillinger > Behandle endringer** | Løst et problem der egendefinerte felter ikke kunne redigeres på fanen **Behandle endringer** for **Stillinger**. |

## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om å aktivere/deaktivere funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Arbeidsområde for fordelsbehandling | [Arbeidsområdet Fordelsbehandling (forhåndsversjon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeidsområde for fordelsbehandling](hr-benefits-management-workspace.md) |
| Du kan hindre at ansatte redigerer kontaktdetaljer for virksomhet. | [Begrense at ansatte redigerer kontaktdetaljer for virksomhet.](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Begrense redigering av personlige opplysninger](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Kommer snart

| Funksjon | Detaljer |
| --- | --- |
| Ferdigheter som angis av en leder for de ansatte, kan godkjennes automatisk av en arbeidsflyt | Kommer snart. |

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 1 i 2021 for Dynamics 365 Human Resources](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]