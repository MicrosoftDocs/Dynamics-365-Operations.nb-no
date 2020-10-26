---
title: Definere lean-planleggingsgrupper
description: Lean-planleggingsgrupper defineres for å gruppere og skille produkter i kanban-planleggingen.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9ad470d81d94a0af1c4c4dc6c5072354cfd96d2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975854"
---
# <a name="define-lean-schedule-groups"></a>Definere lean-planleggingsgrupper

[!include [banner](../../includes/banner.md)]

Lean-planleggingsgrupper defineres for å gruppere og skille produkter i kanban-planleggingen. Grupperingen kan utføres som generisk tilknytning per firma eller spesifikk for en arbeidscelle. Hver gruppe har en fargekode tilordnet for visuell indikasjon på listesiden for kanban-planlegging. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.


## <a name="define-lean-scheduling-group"></a>Definere lean-planleggingsgruppe
1. Gå til Behandling av produktinformasjon > Lean manufacturing > Lean-planleggingsgrupper.
2. Klikk Ny.
3. Skriv inn en verdi i feltet Tidsplangruppe.
    * En planleggingsgruppegruppe kan defineres som global gruppe eller spesifikk for en arbeidscelle. I dette enkle eksemplet definerer vi en global gruppe, og arbeidscellen beholdes tom. Innstillingene for denne gruppen gjelder for alle arbeidsceller som ikke har bestemte planleggingsgrupper.  
4. Velg en farge fra fargevalget.
    * Fargene brukes til å utheve jobbene på listesiden for Kanban-tidsplan eller Kanban-prosesstavlen.  
5. Merk den valgte raden i listen.
6. Klikk koblingen i den valgte raden i listen.

## <a name="associate-product"></a>Tilknytte produkt
1. Tilknytte et bestemt produkt
    * Produkter kan knyttes til lean-planleggingsgrupper på to måter. Enten som et bestemt produkt (varerelasjonstype = vare) eller som en del av en varefordelingsnøkkel (varerelasjonstype = gruppe).    
2. Velg Vare i feltet Type varerelasjon
3. Skriv inn en verdi i Varenummer-feltet.
4. Angi et tall i feltet Produksjonsforhold.
    * Standard produksjonsforhold er 1, som betyr at de tilknyttede produktene forbruker nøyaktig den kapasiteten som er angitt i prosessaktivitetene for produksjonsflytene. Produksjonsforhold > 1 definerer en høyere ressursforbruk, Produksjonsforhold < 1 definerer en lavere ressursforbruk. Forholdet brukes i kostnadsberegningen og i beregningen av Kanban-jobbforbruket.  

## <a name="associate-item-allocation-key"></a>Tilknytte varefordelingsnøkkel
1. Tilknytte en varefordelingsnøkkel
    * Legg til en tilknytning i en varetildelingsnøkkel ved hjelp av varerelasjonstypen Gruppe.   Legg merke til at for denne prosessen må du ha en en varefordelingsnøkkel for prognose definert i dataene.  
2. Velg Gruppe i feltet Type varerelasjon
3. Klikk rullegardinknappen i feltet Varefordelingsnøkkel for å åpne oppslaget.
4. Klikk koblingen i den valgte raden i listen.

