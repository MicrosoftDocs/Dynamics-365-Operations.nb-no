---
title: Du kan ikke bekrefte en forsendelse fordi varer ikke har blitt plukket
description: Du kan ikke bekrefte en forsendelse fordi varer ikke har blitt plukket
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7b57d3151852c9a2880185b7d9414e4246b7efb6429fcfce04c7cdae4ee00e37
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760930"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>Du kan ikke bekrefte en forsendelse fordi varer ikke har blitt plukket

Feilkode: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Symptomer

Når du prøver å bekrefte en forsendelse, viser systemet følgende feilmelding:

> Noen av varene som trengs for lasten %1, har ennå ikke blitt plukket og flyttet til den endelige forsendelseslokasjonen.

Derfor kan du ikke bekrefte forsendelsen for belastningen.

## <a name="cause"></a>Årsak

Belastningen eller forsendelsen kan ikke bekreftes i gjeldende tilstand, fordi det kan hende at én av følgende betingelser finnes:

- Det relaterte arbeidet er ennå ikke plukket og flyttet til den endelige forsendelseslokasjonen.
- Det plukkede arbeidsantallet samsvarer ikke med det opprettede arbeidsantallet på belastningslinjen.
- Lokasjonsdirektivet er konfigurert med emballasjelokasjon som den endelige forsendelseslokasjonen ved bruk av bølgemalcontainerbruk.

## <a name="resolution"></a>Løsning

Lasten eller forsendelsen er for øyeblikket i en tilstand der forsendelsesbekreftelsen mislykkes. Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:

- Gå gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.
- Avbryt arbeids-IDene som er opprettet med emballasjelokasjonen som endelig forsendelseslokasjon, konfigurer lokasjonsdirektivet på nytt, og slett lasten på nytt.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Gå gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer

Bruk følgende fremgangsmåte til å g gjennom lastlinjene, og kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg belastningen som forsendelsen ikke kan bekreftes for.
1. I hurtigfanen **Lastlinjer** velger du lastlinjen.
1. Legg merke til verdien i feltet **Antall for arbeid opprettet**.
1. I handlingsruten, i fanen **Laster** i gruppen **Relatert informasjon**, velger du **Arbeid**.
1. Kontroller at arbeidet er fullført på det endelige forsendelsesstedet, og at det plukkede arbeidsantallet samsvarer med det opprettede arbeidsantallet på belastningslinjen.
1. Gjenta denne fremgangsmåten for alle belastningslinjer for å være sikker på at alle kriteriene er oppfylt.

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a>Avbryt arbeids-IDene som er opprettet med emballasjelokasjonen som endelig forsendelseslokasjon, konfigurer lokasjonsdirektivet på nytt, og slett lasten på nytt

Bruk fremgangsmåten nedenfor til å avbryte arbeids-IDene som har emballasjelokasjonen som endelig plasseringslokasjon med automatisert containerbruk på plass.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Rydd opp \> Avbryt arbeid**.
1. Dialogboksen **Avbryt arbeid** åpnes. Angi IDen for arbeidet du vil avbryte, i **Arbeids-ID**-feltet. Den valgte arbeids-IDen må ha **Arbeidsstatus**-verdien *Åpen*, *Pågår*, *Avbrutt*, *Kombinert* eller *Lukket*.
1. Velg **OK**.
1. Velg **Ja** for å bekrefte at du vil avbryte arbeidet.
1. Gjenta denne fremgangsmåten for de andre arbeids-IDene etter behov.

For mer informasjon, se [Avbryte lagerarbeid for unntaksbehandling](../../warehousing/cancel-warehouse-work.md).

Bruk fremgangsmåten nedenfor til å konfigurere lokasjonsdirektivet på nytt, slik at det ikke bruker emballasjelokasjonen som endelig forsendelseslokasjon når automatisert containerbruk er definert for bølgemalen.

1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.
1. Velg *Salgsordrer* i feltet **Arbeidsordretype**.
1. Velg lokasjonsdirektivet du bruker for automatisert containerbruk.
1. I **Lokasjonsdirektivhandlinger**-hurtigfaneverktøylinjen velger du **Rediger spørring**.
1. I dialogboksen for Power Query-redigering, i fanen **Område**, finner du raden der **Felt** er satt til *Lokasjonsprofil*, og kontroller at **Kriterier**-feltet for denne raden ikke er satt til en lokasjonsprofil som har **Lokasjonstype** *Emballasje*. Juster **Kriterier**-feltet for å rette den endelige plasserte lokasjonen.

Bruk fremgangsmåten nedenfor til å slette belastningen på nytt og opprette arbeids-IDer med riktig endelig forsendelseslokasjon.

1. Gå til **Lagerstyring \> Laster \> Arbeidsområde for lastplanlegging**.
1. I **Last**-delen finner du lasten som må frigis.
1. I delen **Laster** velger du **Frigi \> Frigi til lager** for å frigi den valgte lasten til lageret.
1. Gjenta denne fremgangsmåten for de andre lastene etter behov.
