---
title: Utvide Talent med Power Apps og Power Automate
description: Denne artikkelen beskriver noen eksempler på scenarioer for utvidelsesmuligheter for Microsoft Dynamics 365 Human Resources som bruker Microsoft Power Apps og Microsoft Power Automate.
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5fe8ecd368bc63eed43c86053084ca67ef9beac6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859524"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Utvide med Power Apps og Power Automate


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Denne artikkelen beskriver noen eksempler på scenarioer for utvidelsesmuligheter for Microsoft Dynamics 365 Human Resources som bruker Microsoft Power Apps og Microsoft Power Automate. Du kan importere løsningspakken som er tilknyttet hvert eksempel, i ditt Power Apps-miljø. Du kan deretter bruke pakkene som retningslinjer eller som utgangspunkt til å implementere scenarioene som gjelder for organisasjonen din.

> [!IMPORTANT]
> Hvis du vil bruke malene og appene som er beskrevet i denne artikkelen, "som de er", må du teste dem å være sikker på at de dekker alle scenarioene som er spesifikke for implementeringen.

## <a name="prerequisites"></a>Forutsetninger

- Hvis du vil importere pakker, må brukerne ha **Miljøskaper**-tillatelsen.
- Hvis du vil eksportere eller importere apper, må brukerne ha en Power Apps Plan 2-lisens eller en Power Apps Plan 2-prøvelisens.

## <a name="integration-with-microsoft-365-power-automate"></a>Integrering med Microsoft 365, Power Automate

**Integrering med Microsoft 365**-appen kan brukes til å hente teaminformasjon for påloggede brukere fra Microsoft 365. Den refererer til arbeidere i Human Resources for å trekke ut identifikasjonstyper for ansatte. Ledere kan kontrollere utløpsdatoer for ansatt-ID-typer. De kan også sende en e-postpåminnelse hvis ansatt-ID-typen utløper. Power Automate integreres med Power Apps for å sende denne påminnelsen. Bekreftelse vil bli sendt tilbake til Power Apps fra Power Automate når påminnelsen sendes. Identifikasjonstyper omfatter førerkort, pass og andre godkjente former for ID.

Du kan utvide denne appen til andre scenarier. Du kan for eksempel bruke den til å vise ferieinformasjon for team, kalenderhendelser og teamspesifikke hendelser.

Du kan laste ned appen for **integrering med Microsoft 365, Power Automate** ved å gå til [Integrering med Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) i Microsoft Download Center.

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – SQL-tilkobling og kjøring

Malen **Power Automate – SQL-tilkobling og kjøring** kobler til Microsoft SQL Server og aktiverer SQL-spørringer som skal kjøres.

Selv om denne malen leser og oppdaterer SQL-tabeller, kan du utvide den og bruke den i andre scenarioer. Du kan for eksempel bruke den til å fylle ut en oppsamlingstabell i Dataverse med poster fra SQL Server og synkronisere oppsamlingstabellen jevnlig ved hjelp av en trinnvis push fra SQL Server.

Avansert spørring integreres med flyt for å muliggjøre datatransformering og trinnvis push.

For å laste ned malen **Power Automate – SQL-tilkobling og kjøring** kan du gå til [Power Automate – SQL-tilkobling og kjøring](https://go.microsoft.com/fwlink/?linkid=2081789) på Microsoft Download Center.

## <a name="additional-resources"></a>Tilleggsressurser

[Microsoft Power Platform](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
