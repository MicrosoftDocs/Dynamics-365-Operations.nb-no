---
title: "Samarbeide med leverandører ved hjelp av leverandørportalen"
description: "Dette emnet forklarer hvordan innkjøpsagenter kan bruke leverandørportalen til å samarbeide med eksterne leverandører under bekreftelse av bestillinger. Denne informasjonen i dette emnet gjelder bare for februar 2016- &amp; mai 2016-versjonene av Dynamics AX."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2fa152c5586a1122a109762780d23fd8c2240702
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="collaborate-with-vendors-by-using-the-vendor-portal"></a>Samarbeide med leverandører ved hjelp av leverandørportalen

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan innkjøpsagenter kan bruke leverandørportalen til å samarbeide med eksterne leverandører under bekreftelse av bestillinger. Denne informasjonen i dette emnet gjelder bare for februar 2016- &amp; mai 2016-versjonene av Dynamics AX.

Informasjonen i dette emnet gjelder bare for februar 2016- og mai 2016-versjonene av Dynamics AX. Funksjonen for leverandørportal er erstattet med utvidede leverandørsamarbeidsfunksjoner i Dynamics 365 Operations versjon 1611. Hvis du vil ha mer informasjon om den nye leverandørsamarbeidsfunksjonen, kan du se [Bruke leverandørsamarbeid til å arbeide med eksterne leverandører](vendor-collaboration-work-external-vendors.md).  

Leverandørportalen er utformet for leverandører som ikke har EDI-integrasjon (utveksling av elektroniske data) med Microsoft Dynamics AX for å utveksle bestillingsinformasjon. Med portalen kan innkjøpsagenter sende en bestilling til leverandøren og deretter motta et bekreftet eller avvist svar direkte i Dynamics AX.  

Prosessen kan konfigureres slik at en bekreftelse fra leverandøren automatisk bekrefter ordren. I dette tilfellet er oppfølging bare nødvendig av og til, når en ordre er avvist, eller hvis leverandørbekreftelse er registrert som et svar, men statusen for bestillingen ikke blir oppdatert til **Bekreftet** på grunn av et problem i bekreftelsesprosessen.

## <a name="po-confirmation-and-rejection"></a>Bekreftelse av og avslag på bestilling
Bestillinger klargjøres i Dynamics AX. Når du har en bestilling som har statusen **Godkjent**, sender du den til leverandøren ved å generere en forespørsel om bekreftelse. Hvis du vil trekke leverandørens oppmerksomhet til en ny bestilling, kan du også bruke utskriftsbehandlingssystemet til å sende bestillingen via e-post. Bestillingen vises i leverandørportalen med et alternativ som leverandøren kan bruke til å bekrefte eller avvise den. Leverandøren kan også legge til merknader for å formidle informasjon, for eksempel endringer i bestillingen.  

I leverandørportalen kan leverandøren se ordrelinjer. Disse linjene inkluderer informasjon som eksternt produktnummer, dimensjoner, prisinformasjon, antall, leveringsdato og leveringsadresse. Leverandøren kan generere en rapport som viser bestillingsinformasjon, i tillegg til totalprisen. Tillegg som er relevante for leverandøren, vises hvis leverandøren klikker **Tillegg**-knappen i overskriften eller på linjene. Leverandører kan importere bestillingsinformasjon til sine egne systemer ved hjelp av den **Eksporter til Excel** funksjonalitet.  

Tabellen nedenfor viser den vanlige utvekslingen av informasjon, avhengig av hvordan leverandøren svarer når du sender dem en bestilling for bekreftelse.

| Type svar                                                                                                  | Resultat                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Leverandøren bekrefter ordren. Systemet er konfigurert til automatisk å bekrefte bestillinger når leverandøren bekrefter.    | Statusen for ordren oppdateres til **Bekreftet**. Hvis noe forhindrer at ordren blir oppdatert, registreres likevel leverandørsvaret som **Bekreftet**, men statusen for bestillingen blir værende **Til ekstern vurdering**.                                                                       |
| Leverandøren bekrefter ordren. Systemet er ikke konfigurert til automatisk å bekrefte bestillinger når leverandøren bekrefter. | Leverandørsvaret registreres som **Bekreftet**, men statusen for bestillingen blir værende **Til ekstern vurdering**.                                                                                                                                                                                      |
| Leverandøren avviser ordren.                                                                                     | Leverandørsvaret registreres som **Avvist**, og statusen for bestillingen blir værende **Til ekstern vurdering**. Avvisningen mottas sammen med årsaken og et forslag til endring, for eksempel en alternativ leveringsdato. Du kan oppdatere bestillingen og deretter sende en ny versjon for bekreftelse. |

## <a name="changes-to-a-po"></a>Endringer i en bestilling
Når du må endre en bestilling som allerede er bekreftet, kan du sende en ny bestilling til leverandøren via leverandørportalen. Den nye bestillingen har et versjonssuffiks til å angi at det er en endret versjon av en bestilling som tidligere ble formidlet. Leverandører kan spore loggen for hver ordre på leverandørportalen. Den tidligere bekreftede versjonen av bestillingen forblir i listen over bekreftede bestillinger til den nye bestillingen er bekreftet.  

Når du avbryter en bestilling, endres statusen tilbake til **Godkjent**. Du må sende bestillingen tilbake til leverandøren via leverandørportalen, slik at leverandøren kan bekrefte eller avvise annulleringen. Når annulleringen er bekreftet, vises bestillingen i leverandørens liste over bekreftede bestillinger som **Annullert**.

## <a name="versions-status-transitions-and-change-management"></a>Versjoner, statusoverganger og endringshåndtering
Når en bestilling er sendt til leverandøren, registreres den i systemet som en bestemt versjon av bestillingen, og statusen endres fra **Godkjent** til **Til ekstern vurdering**. Hvis bestillingen endres senere, opprettes en ny versjon av bestillingen, og statusen går tilbake til **Godkjent** (eller **Utkast** gvis endringsadministrasjon er aktivert).  

Tabellen nedenfor viser et eksempel på endringene i status og versjon som en bestilling kan gå gjennom.

| Handling                                                   | Status og versjon                                                                                    |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Den første versjonen av Bestillingen opprettes i Dynamics AX. | Statusen er **Godkjent**.                                                                           |
| Bestillingen er sendt til leverandørportalen.                     | En versjon er registrert på leverandørportalen, og statusen endres til **Til ekstern vurdering**.    |
| Du kan gjøre noen endringer som kreves av leverandøren.  | Statusen endres tilbake til **Godkjent**.                                                            |
| Du sender den nye versjonen av bestillingen til leverdnaørportalen. | En ny versjon er registrert på leverandørportalen, og statusen endres til **Til ekstern vurdering**. |
| Leverandøren godkjenner den nye versjonen av bestillingen.           | Statusen endres til **Bekreftet**.                                                                |

Hvis du vil se hvilke versjoner av bestillingen som er sendt til leverandøren og svarene fra leverandøren, klikker du **Journaler** &gt; **Forespørsler om bekreftelse** fra bestillingen.  

Bestillinger som er sendt til leverandøren for svar og har statusen **Til ekstern vurdering**, vises enten i listen **Bestillingene er sendt til leverandørportalen. Venter på svar.** ekker **Bestillingene er sendt til leverandørportalen. Svaret krever handling.**. Når du endrer en ordre som er sendt til leverandøren, slik at endres statusen tilbake til **Godkjent**, vises ikke ordren lenger i disse listene. For å se om det allerede er et svar på ordren fra leverandøren, kan du klikke **Journaler** &gt; **Forespørsler om bekreftelse**.  

Leverandører trenger ikke bekrefte bestillingen på leverandørportalen. De kan også sende en e-postmelding eller formidle at de godtar en bestilling via andre kanaler. Deretter kan du bekrefte ordren manuelt i Dynamics AX. I så fall får du en advarsel om at ordren blir bekreftet, selv om det ikke finnes noe svar fra leverandøren. Bestillingen vil vises i bekreftelsesloggen på leverandørportalen som en åpen bekreftet ordre som ikke har noen svar. I tillegg vil ikke leverandøren lenger ha muligheten til å bekrefte eller avvise bestillingen.  

**Obs!** Versjonen av bestillingen som er tilgjengelig for andre prosesser i Dynamics AX, er alltid den nyeste versjonen, selv om denne versjonen ennå ikke er registrert.

### <a name="change-management"></a>Endringsbehandling

Hvis du har aktivert endringsadministrasjon for en bestilling, går bestillingen gjennom en godkjenningsarbeidsflyt når den får statusen **Godkjent**. Denne prosessen er ikke synlig for leverandøren.  

Når endringsadministrasjon er aktivert for en bestilling, registreres versjonen når bestillingen er godkjent, ikke når bestillingen sendes til leverandøren eller bekreftes.  

Tabellen nedenfor viser et eksempel på endringene i status og versjon som en bestilling kan gå gjennom når endringsadministrasjon er aktivert:


|                                                    Handling                                                     |                                                                                                                                                                                                                      Status og versjon                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                           Den første versjonen av Bestillingen opprettes i Dynamics AX.                            |                                                                                                                                                                                                            Statusen er <strong>Utkast</strong>.                                                                                                                                                                                                             |
| Bestillingen sendes til godkjenningsprosessen. (Dette er en intern prosess som leverandøren ikke er involvert i.) |                                                                                                                        Statusen endres fra <strong>Utkast</strong> til <strong>Til vurdering</strong> til <strong>Godkjenning</strong> hvis bestillingen ikke avvises under godkjenningsprosessen. Den godkjente bestillingen registreres som en versjon.                                                                                                                        |
|                                      Bestillingen er sendt til leverandørportalen                                      |                                                                                                                                                                      Versjonen registreres på leverandørportalen, og statusen endres til <strong>Til ekstern vurdering</strong>.                                                                                                                                                                       |
|                            Du kan gjøre noen endringer som kreves av leverandøren.                            |                                                                                                                                                                                                    Statusen endres tilbake til <strong>Utkast</strong>.                                                                                                                                                                                                     |
|                              Bestillingen sendes til godkjenningsprosessen på nytt.                               | Statusen endres fra <strong>Utkast</strong> til <strong>Til vurdering</strong> til <strong>Godkjenning</strong> hvis bestillingen ikke avvises under godkjenningsprosessen. Systemet kan også konfigureres slik at spesifikke endringer i felter ikke krever ny godkjenning. I dette tilfellet endres statusen først til <strong>Utkast</strong> og oppdateres deretter automatisk til <strong>Godkjent</strong>. Den godkjente bestillingen registreres som en ny versjon. |
|                           Du sender den nye versjonen av bestillingen til leverdnaørportalen.                            |                                                                                                                                                                    Den nye versjonen registreres på leverandørportalen, og statusen endres til <strong>Til ekstern vurdering</strong>.                                                                                                                                                                     |
|                                Leverandøren godkjenner den nye versjonen av bestillingen.                                 |                                                                                                                                                     Statusen endres til <strong>Bekreftet</strong>, enten automatisk eller når du mottar svaret fra leverandøren og deretter bekrefter bestillingen.                                                                                                                                                     |

<a name="additional-resources"></a>Tilleggsressurser
--------

[Konfigurering av sikkerhet for brukere av leverandørsamarbeid](configure-security-vendor-portal-users.md)

[Arbeidsområde for leverandørsamarbeidsfakturering](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md)




