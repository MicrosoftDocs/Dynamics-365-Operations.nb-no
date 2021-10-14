---
title: Tilpasse og bruke kundeportalen
description: Dette emnet beskriver hvordan du tilpasser kundeportalen etter at den er lagt til i systemet.
author: Henrikan
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 548a81d8145d6762508163f17ca7367cb5ecd849
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579022"
---
# <a name="customize-and-use-the-customer-portal"></a>Tilpasse og bruke kundeportalen

[!include [banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet beskriver de ulike sidene som er tilgjengelige som standard i kundeportalen. Den forklarer funksjonene til sidene samt hvordan du kan tilpasse dem.

Kundeportalen tilbyr enkelte nettsider og handlinger som standard. Følgende områdekart gir en oversikt over disse nettsidene og handlingene, og rollene som kan utføre handlingene.

![Områdekart for kundeportal.](media/customer-portal-site-map.png "Områdekart for kundeportal")

## <a name="typical-customizations"></a>Vanlige tilpasninger

Følgende emner hjelper deg å lære grunnleggende kunnskaper om Power Apps-portaler samt hvordan du kan tilpasse portaler:

- [Arbeide med maler](/powerapps/maker/portals/work-with-templates) – dette emnet gir en generell oversikt over hvordan Power Apps-portaler fungerer, og hvordan du kan utføre enkle tilpasninger av portaler.
- [Behandle portalinnhold](/dynamics365/portals/manage-portal-content) – dette emnet beskriver hvordan du kan administrere og tilpasse innholdet på portalen.
- [Rediger CSS](/powerapps/maker/portals/edit-css) – dette emnet hjelper deg med å utføre mer avanserte tilpasninger i brukergrensesnittet til portalen.
- [Opprett et tema for portalen](/dynamics365/portals/create-theme) – dette emnet hjelper deg med å opprette et brukergrensesnitt-tema for portalen.
- [Opprette og vise portalinnhold enkelt](/dynamics365/portals/create-expose-portal-content) – dette emnet hjelper deg med å styre de underliggende dataene og tabellene som du bruker for portalen.
- [Konfigurere en kontakt for bruk på en portal](/powerapps/maker/portals/configure/configure-contacts) – dette emnet forklarer hvordan du oppretter og tilpasser brukerroller, og hvordan sikkerhet og godkjenning fungerer i Power Apps-portaler.
- [Konfigurere merknader for tabellskjemaer og nettskjemaer på portaler](/powerapps/maker/portals/configure-notes) – dette emnet forklarer hvordan du legger til dokumenter og ekstra lagringsplass på portalen.
- [Feilhåndtering for portalnettstedet](/powerapps/maker/portals/admin/view-portal-error-log) – dette emnet forklarer hvordan du viser feillogger for portaler og lagrer dem i Microsoft Azure Blob Storage-kontoen.

## <a name="customize-the-order-creation-process"></a>Tilpasse prosessen for ordreopprettelse

Når en bruker sender en ordre ved hjelp av kundeportalen, synkroniseres ordren automatisk til det tilsvarende Dynamics 365 Supply Chain Management-miljøet. Siden brukeren er en ekstern kunde, blir noe påkrevd informasjon med hensikt skjult fra vedkommende. Denne informasjonen fylles automatisk ut når skjemaet sendes inn.

Denne delen viser hvordan du bør konfigurere kontakter for å unngå feil. Den forklarer felter som angis automatisk, og hvordan du kan endre verdien i disse feltene hvis du trenger det.

### <a name="the-out-of-box-order-creation-process"></a>Standardprosessen for ordreopprettelse

Her er standardtrinnene for å sende en ordre fra kundeportalen.

1. På hjemmesiden velger du **Opprett ordre**-flisen for å åpne **Opprett ordre**-veiviseren.
1. På **Ordreinformasjon**-siden angir du følgende felter:

    - **Ønsket leveringsdato** – angi leveringsdatoen.
    - **Leveringsadresse** – angi adressen som ordren skal leveres til.
    - **Firma** – velg navnet på kundens firma. Dette feltet angis automatisk for brukere som ikke er administratorer.
    - **Rekvisisjonsnummer** – angi rekvisisjonsnummeret for ordren. Dette feltet er ikke obligatorisk.
    - **Leveringsland/-område** – angi landet eller området som varene skal leveres til. Dette feltet angis automatisk for brukere som ikke er administratorer.

    ![Ordreinformasjonsside.](media/customer-portal-order-information.png "Ordreinformasjonsside")

1. Velg **Neste**.
1. På **Varer**-siden velger du **Legg til vare**.

    ![Varer-side.](media/customer-portal-items.png "Varer-side")

1. I **Vareinformasjon**-dialogboksen angir du følgende felt:

    - **Produktnavn** – finn og velg et produkt som skal legges til i ordren.
    - **Antall** – angi antallet for det valgte produktet.
    - **Enhet** – Angi måleenheten (f.eks. **per.**, **kg** eller **boks**).
    - **Estimert nettobeløp** – verdien beregnes som den estimerte prisen på varen × antallet for den valgte enheten.

    ![Dialogboksen Vareinformasjon.](media/customer-portal-item-information.png "Dialogboksen Vareinformasjon")

1. Velg **Send** for å legge til varen i ordren.
1. Gjenta trinn 4 til 6 til du har lagt til alle varene du vil bestille.
1. Når du er ferdig med å legge til varer, velger du **Neste** på **Varer**-siden.
1. På **Ordre informasjon**-siden ser du et sammendrag av ordren. Se gjennom ordreinnholdet og leveringsdetaljene. Hvis alt ser riktig ut, velger du **Send** for å sende ordren.

    ![Fullført ordreinformasjonsside.](media/customer-portal-order-submit.png "Fullført ordreinformasjonsside")

### <a name="standard-data-setup"></a>Standard datakonfigurasjon

For å bidra til en enklere brukeropplevelse fyller kundeportalen automatisk ut verdier for flere obligatoriske felt. Disse verdiene er basert på informasjon i kontaktposten for kunden som sender ordren.

For hver [kontaktrad](/powerapps/maker/portals/configure/configure-contacts) som tilhører en kunde, og som skal bruke kundeportalen til å sende ordrer, må det angis verdier for følgende obligatoriske felt. Hvis ikke oppstår det feil.

- **Firma** – Den juridiske enheten som ordren tilhører.
- **Potensiell kunde** – Kundekontoen som er knyttet til den valgte ordren
- **Prisliste** – Den egendefinerte prislisten for kunden
- **Valuta** – Valutaen prisen oppgis i
- **Leveringsland/-område** – Landet eller området som varene skal leveres til

Følgende felt angis automatisk for salgsordretabellen:

- **Språk** – Språket for ordren (som standard hentes verdien fra kontaktposten.)
- **Leveringsland/-område** – landet eller området som varene skal leveres til (som standard hentes verdien fra kontaktposten.)
- **Kontaktperson** – Brukeren som kan kontaktes for informasjon om ordren (som standard hentes verdien fra kontaktposten.)
- **Firma** – Den juridiske enheten som ordren tilhører (som standard hentes verdien fra kontaktposten.)
- **Potensiell kunde** – Kundekontoen som er knyttet til ordren (som standard hentes verdien fra kontaktposten.)
- **Fakturakunde** – Faktureringskontoen for ordren (standardverdien er den potensielle kunden fra kontaktposten.)
- **Salgsordrenavn** – navnet på salgsordren (standardverdien er **salgsordre**.)
- **Valuta** – Valutaen prisen oppgis i (som standard hentes verdien fra kontaktposten.)
- **Prisliste** – Den egendefinerte prislisten for kunden (som standard hentes verdien fra kontaktposten.)
- **Beskrivelse av leveringsadresse** – leveringsadressen for salgsordren (standardverdien er **beskrivelse av leveringsadresse**.)

### <a name="modify-the-order-creation-process"></a>Endre prosessen for ordreopprettelse

Du kan fritt endre utseendet og brukergrensesnittet til kundeportalen hvis du ikke endrer prosessen for grunnleggende ordreoppretting. Hvis du vil endre prosessen for oppretting av ordrer, er det noen få ting du bør huske på.

Ikke fjern følgende kolonner fra salgsordreenheten i Microsoft Dataverse, siden de kreves for å opprette en salgsordre med dobbel skriving:

- **Firma** – Den juridiske enheten som ordren tilhører.
- **Navn** – navnet på salgsordren
- **Valuta** – Valutaen prisen oppgis i
- **Prisliste** – Den egendefinerte prislisten for kunden
- **Leveringsland/-område** – Landet eller området som varene skal leveres til
- **Potensiell kunde** – Kundekontoen som er knyttet til den valgte ordren
- **Språk** – språket i ordren (dette språket er vanligvis språket til den potensielle kunden.)
- **Beskrivelse av leveringsadresse** – leveringsadressen for salgsordren

Følgende kolonner er obligatoriske for varer:

- **Produkt** – produktet som skal bestilles
- **Antall** – antallet av det valgte produktet
- **Enhet** – måleenheten (f.eks. **per.**, **kg** eller **boks**)
- **Leveringsland/-område** – landet eller området det skal leveres til
- **Beskrivelse av leveringsadresse** – leveringsadressen for ordren

Du må kontrollere at kundeportalen på en eller annen måte sender inn verdier for alle disse kolonnene.

Hvis du vil legge til kolonner på siden eller fjerne kolonner, kan du se [Opprette eller redigere hurtigopprettingsskjemaer for en strømlinjeformet dataregistreringsopplevelse](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).

Hvis du vil endre hvordan kolonner forhåndsinnstilles og hvordan verdier angis når siden lagres, kan du se følgende informasjon i dokumentasjonen for Power Apps-portaler:

- [Forhåndsutfylle felt](/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [Angi verdi ved lagring](/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a>Tilpasse startsiden

Alle kontrollene i kundeportalen er innebygde Power Apps-portalkontroller. Du kan tilpasse dem ved å følge fremgangsmåten i [Opprette en side](/powerapps/maker/portals/compose-page) i Power Apps-portaldokumentasjonen.

Den eneste egendefinerte kontrollen som er inkludert i kundeportalmalen, brukes til å opprette flisene på startsiden.

![Fliser på startsiden.](media/customer-portal-home-page-tiles.png "Fliser på startsiden")

Følg fremgangsmåten nedenfor for å endre flisene.

1. Åpne [Portal Management-appen](/powerapps/maker/portals/configure/configure-portal).
1. Velg **Sidemaler** i navigasjonsruten til venstre.

    ![Navigasjonsrute for Portal Management.](media/customer-portal-nav.png "Navigasjonsrute for Portal Management")

1. Velg sidemalen som heter **Hjem**.
1. I **Webmal**-feltet velger du **Hjem**-koblingen for å åpne kildekoden for denne siden.

    ![Webmal-felt.](media/customer-portal-web-template.png "Webmal-felt")

1. Nå skal du kunne se alle kildekodene for hjemmesiden, og du kan endre dem slik du ønsker.

## <a name="resources"></a>Ressurser

Hvis du vil ha mer informasjon om hvordan du kan definere og tilpasse kundeportalen, kan du se følgende ressurser:

- [Dokumentasjon for Power Apps-portaler](/powerapps/maker/portals/overview)
- [Dokumentasjon for dobbel skriving](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [Om portalens livssyklus](/powerapps/maker/portals/admin/portal-lifecycle)
- [Oppgradere en portal](/powerapps/maker/portals/admin/upgrade-portal)
- [Overføre en portalkonfigurasjon](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Administrasjon livssyklus for løsning: Dynamics 365 for Customer Engagement-apper](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]