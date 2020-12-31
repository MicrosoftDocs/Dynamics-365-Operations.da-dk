---
title: Konfigurere ER-destinationer
description: Denne procedure viser, hvordan du konfigurerer og bruger forskellige destinationer for outputkomponenter for elektronisk rapportering (ER), f.eks. en mappe eller en fil.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0073033454c7d3054496fe4c38cdb3cff71d8755
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681871"
---
# <a name="er-configure-destinations"></a>Konfigurere ER-destinationer

[!include [banner](../../includes/banner.md)]

Denne procedure viser, hvordan du konfigurerer og bruger forskellige destinationer for outputkomponenter for elektronisk rapportering (ER), f.eks. en mappe eller en fil. Det demodatafirma, der bruges til at oprette denne procedure, er DEMF. Tyskland er landet\området for den juridiske enheds primære adresse, men du kan også bruge enhver juridisk enhed til denne procedure. 

Det format, der bruges i dette eksempel, er ISO20022-kreditoverførsel, men du kan bruge ethvert format, du allerede har importeret. Bemærk, at denne procedure er et eksempel på en destination af en enkelt fil og en enkelt destination. Flere oplysninger om styring af destinationer for elektronisk rapportering findes i Dynamics 365 Finance Hjælp.

1. Gå til Virksomhedsadministration > Elektronisk rapportering > Destination for elektronisk rapportering.
2. Klik på ny for at oprette et nyt sæt destinationer for et format.
3. Vælg et format, som du vil konfigurere destinationer for, i feltet Reference.
    * Hvis der ikke er en værdi at vælge, betyder det, at du ikke har importeret nogen konfiguration for elektronisk rapporteringsformat. Du skal importere en formatkonfiguration, før du konfigurerer destinationer.  
4. Klik på Ny for at oprette en ny fildestination.
    * Bemærk, at du kan oprette én fildestination for hver outputkomponent af samme format som f.eks. en mappe eller en fil. Du kan aktivere og deaktivere destinationer separat i indstillingerne.  
5. Angiv et brugervenligt navn til outputkomponenten i feltet navn.
    * Vi anbefaler, at du bruger meningsfulde navne såsom "Betalingsfil" eller "Kontrolrapport". Disse navne vises til brugerne ved konfigurationskørsel sammen med indstillingerne for destinationen.  
6. Vælg en fil eller mappe, der er specifik for formatet, i feltet Filnavn.
7. Klik på Indstillinger.
8. Vælg Ja i feltet Aktiveret.
    * Med afkrydsningsfeltet Aktiveret på hver fane kan du aktivere og deaktivere hver destination separat. I dette eksempel kan du aktivere afsendelse af en outputfil til en postmodtager, når filen er genereret.  
9. Klik på Rediger for at konfigurere mailmodtagere.
10. Klik på Tilføj.
11. Klik på Mail for udskriftsstyring.
12. Vælg en indstilling i feltet Mailkildetype.
    * Du kan vælge forskellige mailkildetyper, f.eks. en kunde eller en leverandør. Dette definerer den argumenttype, der returneres af formlen Kildekonto for mail. I formlen Kildekonto for mail, der er beskrevet i et trin nedenfor, kan du tilknytte en mailkilde. Vælg Kreditor, hvis formlen skal returnere en kreditorkonto. Brug Kreditor, hvis du benytter konfigurationseksemplet for ISO 20022-kreditoverførsel.  
13. Klik på knappen Bind mailkilde.
14. Angiv en dokumentspecifik reference til en partstype, du har valgt tidligere, i formlen.
    * I stedet for at skrive kan du finde en datakildenode, der repræsenterer partskontoen, og klikke på knappen Tilføj datakilde for at opdatere formlen. Hvis du f.eks. bruger konfigurationen ISO 20022 SEPA-kreditoverførsel, er den node, der repræsenterer en kreditorkonto, '$PaymentsForCoveringLetter'. Creditor.Identification.SourceID. Ellers skal du indtaste en strengværdi som f.eks. "DE-001" for at gemme en formel.  
15. Klik på Gem.
16. Luk siden.
17. Klik på Rediger for at konfigurere kontaktoplysninger for parten.
18. Vælg Ja i feltet Primær kontakt.
    * Du kan bruge forskellige indstillinger til at angive, hvilke kontakttype hos parten der skal bruges som en mailadresse for denne destination. Vi bruger en primær kontakt i dette eksempel.  
19. Klik på OK.
20. Klik på OK.
21. Skriv en værdi i feltet Emne.
22. Klik på OK.

