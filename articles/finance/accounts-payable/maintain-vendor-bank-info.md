---
title: Vedligeholde kreditors bankkontooplysninger
description: Kreditorer kan bruge funktionen Leverandørsamarbejde til at vedligeholde deres bankkontooplysninger. Dette emne forklarer, hvordan du tilføjer og vedligeholder bankoplysninger for kreditorer, som du samarbejder med.
author: v-kiarnd
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 26181
ms.assetid: 10f56dea-ea2d-48ea-9622-4ef715eb1179
ms.search.region: USA
ms.search.industry: Public sector
ms.author: brpotter
ms.search.validFrom: 2011-01-14
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1221b8da59d16746f4ba5cccb900e34c8a25f358
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018247"
---
# <a name="maintain-vendor-bank-account-information"></a>Vedligeholde kreditors bankkontooplysninger

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Kreditorer kan bruge funktionen Leverandørsamarbejde til at vedligeholde deres bankkontooplysninger. Dette emne forklarer, hvordan du tilføjer og vedligeholder bankoplysninger for kreditorer, som du samarbejder med.

Når du har givet adgang til kreditorer, kan de tilføje oplysninger om nye bankkonti. Du kan derefter gennemse disse oplysninger og fuldføre den forudgående notabehandling, så de nye konti bruges til betalinger til disse kreditorer.

Du kan vedligeholde kreditorkontoen i arbejdsområdet **Kreditoroplysninger**. Der vælger kreditorerne **Flere detaljer** og derefter **Bankkonti** på rullelisten. Hvis du vil tilføje en ny bankkonto, skal du vælge **Tilføj** over bankkontogitteret. I den viste dialogboks **Ny** kan du angive følgende oplysninger:

- Pengeinstitutkonto
- Banknavn
- Bankkontonummer
- Bankregistreringsnummer
- Ikrafttrædelsesdato
- Udløbsdato
- Kommentarer (valgfrit)

Hvis den juridiske enhed ligger uden for USA, indeholder dialogboksen også felter til SWIFT-koden og IBAN (International Bank Account Number).

Hvis der er dokumenter med relation til den specifikke certificering, kan du tilknytte dem ved at vælge **Dokument**.

Bankoplysninger, som kreditorer indtaster på siden, viser **Kreditor** som kilden. Du kan også angive bankkontooplysninger på en kreditors vegne. Disse oplysninger vises her, og **Debitor** vises som kilde. Du kan finde flere oplysninger i [Oprette en kreditors bankkonto](../../supply-chain/procurement/tasks/create-vendor-bank-account.md).

Når en konto er blevet tilføjet, kan kreditorer redigere deres banks ikrafttrædelses- og udløbsdatoer efter behov.

## <a name="vendor-collaboration-generated-bank-changes-page"></a>Side for bankændringer, der genereres af kreditorsamarbejde

Når kreditorer har opdateret deres bankoplysninger, kan disse oplysninger ses på den nye side **Bankændringer, der genereres i kreditorsamarbejde**, som er tilgængelige under **Kreditor \> Forespørgsler \> Kreditorrapporter**. Som standard vises alle nyligt angivne eller ændrede bankposter. Kreditorassistenten kan få vist ændringerne og køre kontooplysningerne via notabehandlingen for at validere dem. Når denne proces er fuldført, og den primære betalingsmåde er blevet opdateret manuelt, kan den bankkonto, der vises på siden **Bankændringer, der genereres af kreditorsamarbejde** vælges og markeres som gennemset. Denne handling fjerner kontoen fra standardlisten.

Hvis du vil have vist alle de ændringer, der er foretaget i en kreditors bankoplysninger, kan du ændre filtrene for at få vist siden efter kreditorkonto, interval for ikrafttrædelsesdato,, og om ændringerne er blevet gennemset.
