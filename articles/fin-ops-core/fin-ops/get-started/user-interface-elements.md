---
title: Elementer i brukergrensesnitt
description: Dette emnet beskriver elementene i brukergrensesnittet som brukes i appen.
author: tlefor
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: ''
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 8087090b16ddbcf9586ae289c6ec7c1d23087422
ms.sourcegitcommit: c0929ebda9dfb7affe2a187336abf980ce2009a6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2020
ms.locfileid: "2994124"
---
# <a name="user-interface-elements"></a>Elementer i brukergrensesnitt

Dette emnet beskriver elementene i brukergrensesnittet som brukes i appen. Før brukere kan navigere i grensesnittet, er det viktig å kjenne navnene på og funksjonene for elementene som utgjør grensesnittet.

## <a name="overview"></a>Oversikt

- **Handlingsrute** - Feltet under navigasjonsfeltet. Her kan du velge kategorier for å endre poster som vises på siden. Du kan redigere og lagre postene her.  
- **Faktaboks** - Du kan se informasjon og følge aktivitetene for bestemte poster i denne ruten.  
- **Faktaboksrute** Her kan du bla gjennom forskjellige aspekter ved en post som skal vises i faktaboksen.  
- **Filtreringsrute** - På noen sider kan du velge **Vis filtre** for å åpne denne ruten. Den gir deg muligheten til å begrense resultatene som er synlige for deg på siden.  
- **Navigasjonsfelt** - Linjen øverst i grensesnittet. Den **inneholder Dynamics 365-portalen**, **søk**, **firmavelger**, **handlingssenter**, **innstillinger**, **hjelp og støtte** og brukerprofilen.  
- **Navigasjonsliste** - På noen sider kan du bla gjennom denne ruten for å finne en bestemt post. Når valgt, vil detaljene for posten vises på siden.  
- **Navigasjonsrute** - Ruten lengst til venstre. Herfra kan du finne en hvilken som helst side i produktet.  
- **Side** - Det sentrale fokuset i grensesnittet. Valg som gjøres på de andre grensesnittkomponentene, vil påvirke hvilke poster som vises her.  
- **Rute** - Ruten lengst til høyre. Denne vil åpnes i noen tilfeller når aspekter ved en post må endres og lagres.  
- **Kategori** - Når det refereres til handlingsruten, er det en meny med alternativer som vises når du velger et gitt alternativ i handlingsruten.  

![Bildet nedenfor viser plasseringen av disse elementene i grensesnittet.](media/user-interface-01.png)

## <a name="tabs-fields-and-sections"></a>Kategorier, felt og deler

En *kategori* er et valg som utføres på siden, og som åpner et annet aspekt av en post på samme side. Ofte vil den gi deg mulighet til å endre bestemte *felt*eller grensesnittelementer som tillater inntastede data. 

En *hurtigfane* er en kategori med den ekstra fordelen at flere kategorier kan være synlige samtidig. Du kan utvide en hurtigfane ved å velge pilen som peker nedover til høyre for den.

![Bildet nedenfor viser et eksempel på kategorier og hurtigfaner.](media/user-interface-02.png)

En *del* ligner på en kategori. Ordet "del" brukes ofte til å beskrive et hvilket som helst område på en side som organiserer en bestemt kategori med informasjon. I bildet nedenfor er Sammendrag, Ordrer og favoritter og Koblinger alle eksempler på deler.

![Bildet nedenfor viser et eksempel på kategorier og en del.](media/user-interface-03.png)

## <a name="dialog-boxes-and-drop-down-menus"></a>Dialogbokser og rullegardinmenyer

En *dialogboks* er en rute som åpnes når bestemte valg gjøres for å endre eller opprette en post. Dialogbokser inneholder felt som gir deg muligheten til å angi data som skrives inn. Noen ganger gir et gitt felt deg muligheten til å velge en pil som peker nedover, og som åpner en liste med alternativer du kan velge fra. Dette kalles en *rullegardinmeny*. I følgende bilde inneholder feltene **Type** og **Kundegruppe** alternativet for å åpne en rullegardinmeny.

![Bildet nedenfor viser et eksempel på en dialogboks.](media/user-interface-04.png)

I noen tilfeller vil en dialogboks åpnes nær en gitt knapp når du velger den. Dette kalles en *rullegardinboks*. I det følgende bildet ble **Per dato**-knappen valgt, som åpnet en rullegardinboks.

![Bildet nedenfor viser et eksempel på en rullegardinboks.](media/user-interface-05.png)

## <a name="notifications"></a>Varslinger

Enkelte endringer i objektene du har oppsyn med, vises som *varslinger*. Varslinger kan varsle deg når informasjonen til en bestemt kunde er endret, eller den kan varsle deg når systemet ikke kan godta inndata du har lagt til i bestemte felt. Du kan lære hvordan du tilpasser hva du mottar varslinger om, i [Oversikt over varsler](../get-started/alerts-overview.md).

Varsler vises på en rekke måter.
- **Funksjonsforklaring** – Dette vises ved siden av et felt, en kategori eller en annen knapp for å tilby en forklaring på hva funksjonen brukes til. 
- **Handlingssenter** - En boks som inneholder varslingen, vil vises ved siden av knappen Handlingssenter i navigasjonsfeltet. Du kan se detaljer om varslingen ved å velge **Handlingssenter**.  
- **Meldingsfelt**- Dette vises under handlingsruten.  

Det følgende bildet viser eksempler på slike varslingstyper.

![Det følgende bildet viser eksempler på varslinger.](media/user-interface-06.png)

- **Meldingsboks** - Denne vil vises over grensesnittet og må samhandles med før du kan fortsette å bruke produktet.  

![Bildet nedenfor viser et eksempel på en meldingsboks.](media/user-interface-07.png)

## <a name="toolbars-grids-and-lists"></a>Verktøylinjer, rutenett og lister

En *verktøylinje* inneholder verktøy, for eksempel muligheten til å legge til felt eller fjerne poster. Noen ganger vil det vises en verktøylinje på siden over et *rutenett*. Dette området, rutenettet, er et navn som er gitt til rader med poster med forskjellige datakolonner. Ikke alle rutenett har verktøylinjer over seg.

En *liste* er navnet på en samling med poster som du kan rulle gjennom. Du kan plassere disse postene på siden ved å velge dem. Ofte vil dette åpne et rutenett.

![Bildet nedenfor viser eksempler på verktøylinjer, rutenett og lister.](media/user-interface-08.png)
