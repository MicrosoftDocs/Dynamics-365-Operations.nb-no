---
title: Antall er ugyldig ved registrering av innkommende ordrer
description: Hvis antallet som er tildelt for et nummerskilt, overskrider antallet som fortsatt må mottas, får du feilmeldingen. "Antallet er ikke gyldig."
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5099b320447bf59c72f5017564ea660f19c690a5
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477240"
---
# <a name="license-plate-quantity-is-not-valid-when-registering-inbound-orders"></a>Nummerskiltkvantum er ugyldig ved registrering av innkommende ordrer

## <a name="symptoms"></a>Symptomer

Når du registrerer innkommende ordrer, kan du motta følgende feilmelding:

> Antallet er ikke gyldig.

Hvis feltet **Grupperingspolicy for nummerskilt** er satt til *Brukerdefinert* for et menyelement på en mobilenhet som brukes til å registrere innkommende ordrer, får du denne feilmeldingen, og du kan ikke fullføre registreringen.

## <a name="cause"></a>Årsak

Når *Brukerdefinert* brukes som en grupperingspolicy for nummerskilt, deler systemet det innkommende lageret i separate nummerskilt, som angitt av enhetsseriegruppen. Hvis parti- eller serienumre brukes til å spore varen som mottas, må antallene i hvert parti eller hver serie angis per nummerskilt som er registrert. Hvis antallet som er angitt for et nummerskilt, overskrider antallet som fortsatt må mottas for gjeldende dimensjoner, får du feilmeldingen.

## <a name="resolution"></a>Løsning

Når du registrerer en vare ved hjelp av et menyelement for mobilenhet der feltet **Grupperingspolicy for nummerskilt** er satt til *Brukerdefinert*, kan systemet kreve at du bekrefter eller angir numre på nummerskilt, partinumre eller serienumre.

På bekreftelsessiden for nummerskiltet viser systemet antallet som er tilordnet for gjeldende nummerskilt. På parti- eller seriebekreftelsessidene vil systemet vise antallet som fortsatt må mottas på gjeldende numerskilt. Det inkluderer også et felt der du kan angi antallet som skal registreres for denne kombinasjonen av nummerskilt og parti- eller serienummer. I så fall må du sørge for at antallet som blir registrert for nummerskiltet, ikke overskrider antallet som fortsatt må mottas.

Hvis det genereres for mange lisensavtaler ved innkommende ordreregistrering, kan verdien i feltet **Grupperingspolicy for numerskilt** endres til *Gruppering av nummerskilt*, en ny enhetssekvensgruppe kan tilordnes varen, eller alternativet **Gruppering av nummerskilt** for enhetssekvensgruppen kan deaktiveres.
