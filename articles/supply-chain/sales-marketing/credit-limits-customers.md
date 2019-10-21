---
title: Kredittgrenser for kunder
description: Denne artikkelen gir en oversikt over hvordan kredittgrenser fungerer i Dynamics 365 Supply Chain Management.
author: omulvad
manager: AnnBe
ms.date: 09/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7be4ab297293bf1c9f720c2c16b2720afdfe771
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2019
ms.locfileid: "2026469"
---
# <a name="credit-limits-for-customers"></a>Kredittgrenser for kunder

[!include [banner](../includes/banner.md)]

Ved å angi en kredittgrense kan du spesifisere det maksimale beløpet for kreditt som settes for kundene dine. Hvis en kredittgrense er angitt, kontrolleres den automatisk når en bruker forsøker å oppdatere et dokument. En melding vises til brukeren hvis kredittgrensen overskrides. Denne artikkelen gir en oversikt over hvordan kredittgrenser fungerer, og svarer på følgende spørsmål:

-   Hvilke dokumenter og prosesser kan jeg sjekke kredittgrenser for?

-   Hvor konfigurerer jeg måten kundens gjenværende kreditt beregnes på?

-   Hvor brukes informasjon om kundens gjenværende kreditt?

-   Hvor spesifiserer jeg om identifikasjon er nødvendig for at kreditt skal økes til en kunde, og også kredittgrenseverdien som krever identifikasjon?

-   Hvor spesifiserer jeg om det skal vises en advarsel eller feil hvis kredittgrensen overskrides?

-   Hvordan spesifiserer jeg kredittgrensen for en bestemt kunde?

-   Hvordan kontrollerer jeg kredittgrenser manuelt på salgsordrer?

**Hvilke dokumenter og prosesser kan jeg sjekke kredittgrenser for?**

Bruk skjemaet for **Mottakerparametere** for å spesifisere hvilke dokumenter som det skal sjekkes kredittgrenser for. Du må være medlem av Systemadministrator (-SYSADMIN-)-sikkerhetsrollen for å gjøre endringer i dette skjemaet. Du kan sjekke kredittgrenser for følgende dokumenter og prosesser:

-   Fakturaer for salgsordrer, når du legger inn fakturaene

-   Pakksedler for salgsordrer, når du oppdaterer pakksedler

-   Salgsordre, når du legger til linjer i skjemaet **Salgsordre**

-   Salgsordrer, når de er opprettet gjennom en tjeneste

-   Gratis tekstfakturaer, når du legger inn fakturaene

Kredittgrenser blir automatisk sjekket hvis en av følgende alternativer er angitt:

-   I skjemaet **Parametere for kundefordringer**, vil **Kredittgrensetype**-feltet settes til alt annet enn **Ingen**. Kredittgrenser kontrolleres for alle kunder.

-   I skjemaet **Parametere for kundefordringer**, er **Kredittgrensetype**-feltetsatt til **Ingen** men **Obligatorisk kredittgrense** er valgt for en kunde i skjemaet **Kunder**. Kredittgrenser sjekkes kun for bestemte kunder.

For å sjekke kredittgrenser for følgende dokumenter, må du angi flere innstillinger.

|    Dokument                                    |    Tilleggsinnstilling                                                                                                             |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|    Gratis tekstfaktura                         |    I skjemaet Parametere for kundefordringer, i kredittvurderingsområdet, velg Sjekk kredittgrense for gratis tekstfaktura.     |
|    Salgsordre (manuelt inntastet)            |    I skjemaet Parametere for kundefordringer, i kredittvurderingsområdet, velg Sjekk kredittgrense for salgsordrer.           |
|    Salgsordre (elektronisk mottatt)     |    I skjemaet Parametere for kundefordringer, i AIF-området, velg Sjekk kredittgrense for salgsordrer.                     |

**Hvor konfigurerer jeg måten en kundes gjenværende kreditt beregnes på?**

Du kan konfigurere Dynamics 365 til å beregne kundens gjenstående kreditt på en av følgende måter:

-   Sammenlign kredittgrensen mot kundesaldoen.

-   Sammenlign kredittgrensen mot kundesaldoen og pakkseddelbeløpene.

-   Sammenlign kredittgrensen mot kundesaldoen og all åpen transaksjonsaktivitet. Dette inkluderer pakkseddelbeløp og salgsordrebeløp.

Bruk skjemaet **Parametere for kundefordringer** for å spesifisere informasjonen å sammenligne med. Du må være medlem av Systemadministrator (-SYSADMIN-)-sikkerhetsrollen for å gjøre endringer i dette skjemaet. I feltet **Kredittgrensetype** velg om du skal utføre kredittgrensesjekk og hvilken transaksjonsinformasjon som skal inkluderes når kredittgrensen er sjekket. Velge fra følgende valg:

-   **Ingen** – Ikke sjekk kredittgrenser. Du kan overstyre dette alternativet for en spesifikk kunde ved å huke av avmerkingsboksen **Obligatorisk kredittsjekk** i skjemaet **Kunder**. Hvis du gjør dette sjekkes kredittgrensen mot kundesaldoen.

-   **Saldo** - Kredittgrensen kontrolleres mot kundesaldoen.

-   **Saldo + følgeseddel eller produktkvittering** – Kredittgrensen kontrolleres mot kundesaldoen og leveranser.

-   **Saldo+Alt** - Kredittgrensen kontrolleres mot kundesaldoen, leveranser og åpne ordrer.

**Hvor brukes informasjon om kundens gjenværende kreditt?**

Informasjon om en kundes saldo og gjenværende kredittbeløp kalkuleres og lagres når du oppretter et aldrende øyeblikksbilde, og vises i **Samlinger**-skjemaet. Belpene som vises i **Samlinger**-skjemaet kan ikke inkludere all transaksjonsaktivitet før et nytt eldre øyeblikksbilde er opprettet. Hvis du vil ha mer informasjon, kan du se [Samlinger og kreditt i kundefordringer](https://technet.microsoft.com/library/hh209221.aspx).

Avhengig av dokumentene som er valgt, beregnes informasjon om kundens saldo og gjenværende kredittbeløp når salgsordrer, pakksedler og kundefakturaer oppdateres. Hvis mengden av dokumentet du arbeider med ville føre til at kredittgrensen overskrides, vises en melding.

**Hvor spesifiserer jeg om identifikasjon er nødvendig for at kreditt skal økes til en kunde, og også kredittgrensen som krever identifikasjon?**

Bruk skjemaet **Parametere for kundefordringer** for å angi om det kreves identifikasjon og grenseverdien for kredittbeløp som krever identifikasjon.
Du må være medlem av Systemadministrator (-SYSADMIN-)-sikkerhetsrollen for å gjøre endringer i dette skjemaet.

|    Felt                                    |    beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Krev identifikasjon med kreditt     |    Velg typen identifikasjon som må angis for kunder, som din juridiske enhet øker kreditt for. Alternativet du velger i dette feltet, bestemmer når og hvilken type informasjon som kreves i offentlig ustedt identifikasjonsfelt i kundeskjemaet:      Nei – ikke offentlig utstedt identfikasjon     identifikasjon kreves uavhgengig av kundens gredittgrense.     Ja – Et       offentlig utstedt lisensnummer og andre offentlig utstedte identifikasjoner er nødvendig hvis kundens kredittgrense er høyere enn        eller lik null.     Minimumsgrense – Et          offentlig utstedt lisensnummer eller andre offentlig ustedte identifikasjoner er nødvendig hvis kundes kredittgrense er høyere enn       eller lik grensen som du skriver inn i Grensefeltet i dette     skjemaet.        |
|    Grense                                    |    Skriv inn kredittgrense    der et offentlig utstedt lisensnummer eller annen identifikasjon er nødvendig for   kundene.    For eksempel, skriv inn 2000 for å kreve at et     identifikasjonsnummer, slik som førerkortnummer, må skrives inn for kunder som har en kredittgrense på 2000 eller høyere.    Feltet er tilgjengelig hvis du valgte Minimumsgrense i nødvendig identfikasjon med kredittfelt.                                                                                                                                                                                                                                                                                                                                                                                                                                         |

**Hvor spesifiserer jeg om det skal vises en advarsel eller feil hvis kredittgrensen overskrides?**

Bruk **Parametere for kundefordringer**-skjemaet for å spesifisere om det skal vises en advarsel eller feil hvis kredittgrensen overskrides. Denne advarselen eller feilen vises når en bruker skriver inn eller legger inn informasjon, eller det er inkludert i en logg hvis dokumentene behandles av en elektronisk tjeneste. Du må være medlem av Systemadministrator (-SYSADMIN-)-sikkerhetsrollen for å gjøre endringer i dette skjemaet.

|    Felt                                                               |    beskrivelse                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Melding ved overskridelse av kredittgrense (i kredittvurderingsområdet)     |    Velg hvordan meldinger om kredittgrenser som overskrides vises for brukere. Velg mellom følgende alternativer:    Feil – en       feilmelding vises. Dette stopper vanligvis nåværende operasjon og      konflikten må løses før prosessen kan fortsette.     Advarsel – En      advarselmelding vises, men prosessen kan fortsette.                     |
|    Melding ved overskridelse av kredittgrense (i AIF-området)               |    Velg hvordan meldinger om kredittgrenser som overskrides leveres i en logg. Velg mellom følgende alternativer:    Feil – en       feilmelding vises i unntaksskjemaet, og      ddokumentet vil ikke behandles før feilen er løst.     Advarsel – En      advarselmelding vises i unntaksskjemaet, men     prosessen kan fortsette.        |

**Hvordan spesifiserer jeg kredittgrensebeløpet for en bestemt kunde?**

Bruk skjemaet **Kunder** for å spesifisere kredittgrensebeløpet for en bestemt kunde. Du må være medlem av en sikkerhetsrolle som har vedlikehold av kundemaster (CustCustomersMaintain)-ansvar tildelt for å gjøre endringer i dette skjemaet.

1.  Klikk **Kunder** \> **Felles** \> **Kunder** \> **Alle kunder**. Dobbeltklikk en kundekonto.

2.  I skjemaet **Kunder** på Handlings-ruten, klikk **Rediger**.

3.  Skriv inn et valutabeløp i feltet **Kredittgrense**. Denne verdien må være høyere enn null (0), og vil bli brukt som kredittgrensebeløp.

4.  Hvis det er påkrevd, skriv inn et lisensnummer eller annen offentlig utstedt identifikasjon i **Offentlig identfikasjon**-feltet.

> [!NOTE]
> I skjemaet **Parametere for kundefordringer**, er en kredittgrensetype typisk valgt. Men hvis kredittgrensetype er satt til **Ingen**, må du velge avmerkingsboksen **Obligatorisk kredittgrense** i skjemaet **Kunder** for å kunne sjekke kundens kredittgrense mot kundens saldo. For mer informasjon om kredittgrense typer, se "Hvilke dokumenter og prosesser kan jeg sjekke kredittgrenser for?" i dette emnet. 

**Hvordan sjekker jeg kredittgrenser manuelt for salgsordrer?**

Noen ganger må du kanskje manuelt sjekke kundens kredittgrense. For eksempel kan du manuelt sjekke kundens kredittgrense før du begynner å legge inn en salgsordre. Du kan bruke skjemaet **Salgsordre** for å manuelt sjekke kredittgrenser. Du må være medlem av en sikkerhetsrolle som har vedlikehold av salgsordre (SalesOrderMaintain)-ansvar tildelt for å gjøre endringer i dette skjemaet.

1.  Klikk **Salg og markedsføring** \> **Vanlig** \> **Salgsordrer** \> **Alle salgsordrer**. Dobbeltklikk en salgsordre.

2.  I skjemaet **Salgsordre** i Handlingsvinduet, på **Administrer**-kategorien, klikk **Sjekk kredittgrense**.
