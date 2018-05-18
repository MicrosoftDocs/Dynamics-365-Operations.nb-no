---
title: Konfigurere en nettbutikk
description: Denne artikkelen inneholder koblinger til emner som hjelper deg med sentral konfigurasjon og administrasjon av en nettbutikk.
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 31541
ms.assetid: 7a25f9b4-a0bb-4e8c-95c0-c0799ec0620d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d87430ad92e60b7037b1ce4d2fbac7920322f0fb
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="configure-an-online-store"></a>Konfigurere en nettbutikk

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder koblinger til emner som hjelper deg med sentral konfigurasjon og administrasjon av en nettbutikk.

Emnene som er oppført i tabellen nedenfor, er til hjelp når du skal konfigurere Retail-komponenter og nettbutikken for detaljhandel i klienten.

## <a name="configure-an-online-store"></a>Konfigurere en nettbutikk

| Oppgave                                                | Detaljer                                                                                                                                                                                                                                                                                                                                                   | Emner                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konfigurer Retail-komponenter.                        | Definer og vedlikehold informasjon om detaljhandelsoperasjoner. Denne informasjonen inkluderer butikker, avgifter, produkter, gavekort, kampanjer og rabatter.                                                                                                                                                                                                          | [Konfigurere og vedlikeholde Retail](https://technet.microsoft.com/en-us/library/hh597201.aspx) (TechNet-innhold for Microsoft Dynamics AX 2012)                                                                                                                                                                                                                                                                                          |
| Konfigurer et navigasjonshierarki for detaljhandelskanal.    | Opprett et navigasjonskategorihierarki for en detaljhandelskanal for å definere en kategoristruktur for produkter du tilbyr gjennom en nettbutikk. Du kan definere kategorihierarkiet og deretter tilordne produkter, produktattributtgrupper og attributtverdier til kategoriene. Deretter tilordner du kategorihierarkiet til en nettbutikk.                            | [Angi et handelshierarki](https://technet.microsoft.com/en-us/library/hh580593.aspx) (TechNet-innhold for AX 2012) [Definere attributter og attributtyper](https://technet.microsoft.com/en-us/library/hh227548.aspx) (TechNet-innhold for AX 2012) [Definere attributtgrupper for detaljhandel](https://technet.microsoft.com/en-us/library/jj728713.aspx) (TechNet-innhold for AX 2012) |
| Legg til nettbutikken i organisasjonshierarkiet. | Før du kan tilordne produktsortimenter eller fullføre ordrer for nettbutikken som du opprettet, eller generere rapporter som inneholder informasjon fra denne nettbutikken, må du tilordne butikken til en eller flere organisasjonshierarkier. Du må minst tilordne nettbutikken til et organisasjonshierarki som inneholder produktsortimenter. | [Definere en nettbutikk](https://technet.microsoft.com/en-us/library/jj682095.aspx) (TechNet-innhold for AX 2012)                                                                                                                                                                                                                                                                                                     |
| Legg til leveringsmåter for nettbutikken.          | Velg leveringsmetodene nettbutikken tilbyr.                                                                                                                                                                                                                                                                                                 | [Definere en nettbutikk](https://technet.microsoft.com/en-us/library/jj682095.aspx) (TechNet-innhold for Microsoft AX 2012)                                                                                                                                                                                                                                                                                                     |
| Tilordne attributter, og legg til metadata.                   | Velg alternativene som angir hvordan attributtene for hver kategori eller hvert kanalprodukt skal virke i nettbutikken på Microsoft SharePoint-området.                                                                                                                                                                                              | [Definere en nettbutikk](https://technet.microsoft.com/en-us/library/jj682095.aspx) (TechNet-innhold for AX 2012)                                                                                                                                                                                                                                                                                                     |

## <a name="configure-online-store-products"></a>Konfigurer produkter for nettbutikk

| Oppgave                                 | Detaljer                                                                                                                                           | Emner                                                                                                                                                                                                                                                                            |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Legg til sortimenter for nettbutikken. | Legg til sortimenter som inneholder produktene du tilbyr i en nettbutikk.                                                                  | [Definere en nettbutikk](https://technet.microsoft.com/en-us/library/jj682095.aspx) (TechNet-innhold for AX 2012)                                                                                                                                              |
| Administrer kataloger.                     | Bruk produktkataloger til å identifisere produktene du vil tilby i butikkene.                                                              | [Hovedoppgaver: Opprette detaljhandelsproduktkataloger](https://technet.microsoft.com/en-us/library/jj728712.aspx) (TechNet-innhold for AX 2012)                                                                                                                           |
| Administrer priser.                       | Opprett og bruk prisgrupper, som er den sentrale koblingen mellom priser og rabatter, og kanaler, kataloger, tilknytninger og lojalitetsprogrammer. | [Definere prissetting ved hjelp av prisgrupper](https://technet.microsoft.com/en-us/library/hh597169.aspx) (TechNet-innhold for AX 2012) [Definere avgifter](https://technet.microsoft.com/en-us/library/hh580571.aspx) (TechNet-innhold for AX 2012) |
| Behandle rabatter.                    | Definer og administrer prisjusteringer og fire typer rabatter.                                                                                  | [Konfigurere prisjusteringer og rabatter](https://technet.microsoft.com/en-us/library/hh597114.aspx) (TechNet-innhold for AX 2012)                                                                                                                          |
| Behandle forsendelseskostnader.             | Definer og behandle forsendelseskostnadene som er spesifikke for nettbutikken.                                                                     | [Definere forsendelseskostnader for nettbutikker](https://technet.microsoft.com/en-us/library/jj728714.aspx) (TechNet-innhold for AX 2012)                                                                                                                           |
| Behandle leveringsmåter.            | Behandle leveringsmåter som tilbys i nettbutikken.                                                                                        | [Definere leveringsmåter](https://technet.microsoft.com/en-us/library/jj728719.aspx) (TechNet-innhold for AX 2012)                                                                                                                                            |

## <a name="set-up-data-exchange-between-microsoft-dynamics-365-for-retail-and-the-online-store"></a>Definere datautveksling mellom Microsoft Dynamics 365 for Retail og nettbutikken

| Oppgave                                 | Detaljer                                                                                                                               | Emner                                                                                                                                                                                                                                                                                  |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Definer profiler for kanalintegrering. | Profiler gjør at komponentene i Retail kan kommunisere med hverandre. Definer profiler før du konfigurerer innstillinger for datautveksling. | [Definere en Real-time Service-profil](https://technet.microsoft.com/en-us/library/hh580631.aspx) (TechNet-innhold for AX 2012) [Definere en kanalprofil](https://technet.microsoft.com/en-us/library/jj677402.aspx) (TechNet-innhold for AX 2012) |






