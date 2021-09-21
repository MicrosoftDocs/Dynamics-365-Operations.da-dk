---
title: Antal er ikke gyldigt ved registrering af indgående ordrer
description: "Hvis det antal, der er angivet for nummerplade, overstiger det antal, der stadig skal modtages, får du vist fejlmeddelelsen: 'Antallet er ikke gyldigt.'"
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
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475944"
---
# <a name="license-plate-quantity-is-not-valid-when-registering-inbound-orders"></a>Id-antallet er ikke gyldigt ved registrering af indgående ordrer

## <a name="symptoms"></a>Symptomer

Når du registrerer indgående ordrer, får du vist følgende fejlmeddelelse:

> Antallet er ugyldigt.

Hvis feltet **Politik for nummerpladegruppering** er indstillet til *Brugerdefineret* for et menupunkt på en mobilenhed, som bruges til at registrere indgående ordrer, får du vist en fejlmeddelelse ("Antallet er ikke gyldigt"), og du kan ikke fuldføre registreringen.

## <a name="cause"></a>Årsag

Når *Brugerdefineret* bruges som nummerpladegrupperingspolitik, opdeles den indgående lagerbeholdning i separate nummerplader, som angivet af enhedsseriegruppen. Hvis der bruges batch- eller serienumre til at spore den vare, der modtages, skal antallene for hver batch eller serie angives pr. nummerplade, der registreres. Hvis det antal, der er angivet for nummerplade, overstiger det antal, der stadig skal modtages for de aktuelle dimensioner, får du vist denne fejlmeddelelse.

## <a name="resolution"></a>Løsning

Når du registrerer en vare ved hjælp af menupunktet på en mobilenhed, hvor feltet **Politik for nummerpladegruppering** er angivet til *Brugerdefineret*, kan systemet kræve, at du bekræfter eller angiver nummerpladenumre, batchnumre eller serienumre.

På siden til bekræftelse af nummerplade vil systemet vise det antal, der er tildelt den aktuelle nummerplade. På batch- eller seriebekræftelsessiderne viser systemet det antal, der stadig skal modtages på den aktuelle nummerplade. Der findes også et felt, hvor du kan angive det antal, der skal registreres for denne kombination af nummerplade og batch- eller serienummer. Hvis det er tilfældet, skal du sikre dig, at det antal, der registreres for nummerpladen, ikke overstiger det antal, der stadig skal modtages.

Hvis der genereres for mange nummerplader ved indgående ordreregistrering, kan værdien i feltet **Politik for nummerpladegruppering** ændres til *Nummerpladegruppering*, og derfor kan der tildeles en ny enhedsseriegruppe til varen, eller indstillingen af **Nummerpladegruppering** for enhedsseriegruppen kan deaktiveres.
