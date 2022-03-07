---
title: Konfigurer nettbutikker
description: Denne artikkelen inneholder koblinger til emner som hjelper deg med sentral konfigurasjon og administrasjon av en nettbutikk.
author: kfend
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.custom: 31541
ms.assetid: 7a25f9b4-a0bb-4e8c-95c0-c0799ec0620d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e5bff9986467b79beb68e9274d3c554fe10c9cbb
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781835"
---
# <a name="configure-online-stores"></a>Konfigurer nettbutikker

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder koblinger til emner som hjelper deg med sentral konfigurasjon og administrasjon av en nettbutikk.

Emnene som er oppført i tabellen nedenfor, er til hjelp når du skal konfigurere Commerce-komponenter og nettbutikken i klienten.

## <a name="configure-an-online-store"></a>Konfigurere en nettbutikk

| Oppgave                                                | Detaljer                                                                                                                                                                                                                                                                                                                                                   | Emner                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konfigurer komponenter.                        | Definer og vedlikehold informasjon om handelsoperasjoner. Denne informasjonen inkluderer butikker, avgifter, produkter, gavekort, kampanjer og rabatter.                                                                                                                                                                                                          | [Konfigurere og vedlikeholde Retail](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-retail) (TechNet-innhold for Microsoft Dynamics AX 2012)                                                                                                                                                                                                                                                                                          |
| Konfigurer et navigasjonshierarki for kanal.    | Opprett et navigasjonskategorihierarki for en kanal for å definere en kategoristruktur for produkter du tilbyr gjennom en nettbutikk. Du kan definere kategorihierarkiet og deretter tilordne produkter, produktattributtgrupper og attributtverdier til kategoriene. Deretter tilordner du kategorihierarkiet til en nettbutikk.                            | [Angi et handelshierarki](/dynamicsax-2012/appuser-itpro/set-up-a-retail-hierarchy)</br> (TechNet-innhold for AX 2012)</br> [Definere attributter og attributtyper](/dynamicsax-2012/appuser-itpro/set-up-attributes-and-attribute-types) (TechNet-innhold for AX 2012)</br> [Definere attributtgrupper for detaljhandel](/dynamicsax-2012/appuser-itpro/set-up-retail-attribute-groups) (TechNet-innhold for AX 2012) |
| Legg til nettbutikken i organisasjonshierarkiet. | Før du kan tilordne produktsortimenter eller fullføre ordrer for nettbutikken som du opprettet, eller generere rapporter som inneholder informasjon fra denne nettbutikken, må du tilordne butikken til en eller flere organisasjonshierarkier. Du må minst tilordne nettbutikken til et organisasjonshierarki som inneholder produktsortimenter. | [Definere en nettbutikk](/dynamicsax-2012/appuser-itpro/set-up-an-online-store) (TechNet-innhold for AX 2012)                                                                                                                                                                                                                                                                                                     |
| Legg til leveringsmåter for nettbutikken.          | Velg leveringsmetodene nettbutikken tilbyr.                                                                                                                                                                                                                                                                                                 | [Definere en nettbutikk](/dynamicsax-2012/appuser-itpro/set-up-an-online-store) (TechNet-innhold for Microsoft AX 2012)                                                                                                                                                                                                                                                                                                     |
| Tilordne attributter, og legg til metadata.                   | Velg alternativene som angir hvordan attributtene for hver kategori eller hvert kanalprodukt skal virke i nettbutikken på Microsoft SharePoint-området.                                                                                                                                                                                              | [Definere en nettbutikk](/dynamicsax-2012/appuser-itpro/set-up-an-online-store) (TechNet-innhold for AX 2012)                                                                                                                                                                                                                                                                                                     |

## <a name="configure-online-store-products"></a>Konfigurer produkter for nettbutikk

| Oppgave                                 | Detaljer                                                                                                                                           | Emner                                                                                                                                                                                                                                                                            |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Legg til sortimenter for nettbutikken. | Legg til sortimenter som inneholder produktene du tilbyr i en nettbutikk.                                                                  | [Definere en nettbutikk](/dynamicsax-2012/appuser-itpro/set-up-an-online-store) (TechNet-innhold for AX 2012)                                                                                                                                              |
| Administrer kataloger.                     | Bruk produktkataloger til å identifisere produktene du vil tilby i butikkene.                                                              | [Hovedoppgaver: Opprette detaljhandelsproduktkataloger](/dynamicsax-2012/appuser-itpro/key-tasks-create-retail-product-catalogs) (TechNet-innhold for AX 2012)                                                                                                                           |
| Administrer priser.                       | Opprett og bruk prisgrupper, som er den sentrale koblingen mellom priser og rabatter, og kanaler, kataloger, tilknytninger og lojalitetsprogrammer. | [Definere prissetting ved hjelp av prisgrupper](/dynamicsax-2012/appuser-itpro/setting-up-prices-using-price-groups) (TechNet-innhold for AX 2012)</br> [Definere avgifter](/dynamicsax-2012/appuser-itpro/setting-up-taxes) (TechNet-innhold for AX 2012) |
| Behandle rabatter.                    | Definer og administrer prisjusteringer og fire typer rabatter.                                                                                  | [Konfigurere prisjusteringer og rabatter](/dynamicsax-2012/appuser-itpro/setting-up-price-adjustments-and-discounts) (TechNet-innhold for AX 2012)                                                                                                                          |
| Behandle forsendelseskostnader.             | Definer og behandle forsendelseskostnadene som er spesifikke for nettbutikken.                                                                     | [Definere forsendelseskostnader for nettbutikker](/dynamicsax-2012/appuser-itpro/set-up-shipping-charges-for-online-stores) (TechNet-innhold for AX 2012)                                                                                                                           |
| Behandle leveringsmåter.            | Behandle leveringsmåter som tilbys i nettbutikken.                                                                                        | [Definere leveringsmåter](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) (TechNet-innhold for AX 2012)                                                                                                                                            |

## <a name="set-up-data-exchange-between-commerce-and-the-online-store"></a>Definere datautveksling mellom Commerce og nettbutikken

| Oppgave                                 | Detaljer                                                                                                                               | Emner                                                                                                                                                                                                                                                                                  |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Definer profiler for kanalintegrering. | Profiler gjør at komponentene kan kommunisere med hverandre. Definer profiler før du konfigurerer innstillinger for datautveksling. | [Definere en Real-time Service-profil](/dynamicsax-2012/appuser-itpro/set-up-a-real-time-service-profile) (TechNet-innhold for AX 2012)</br> [Definere en kanalprofil](/dynamicsax-2012/appuser-itpro/set-up-a-channel-profile) (TechNet-innhold for AX 2012) |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]