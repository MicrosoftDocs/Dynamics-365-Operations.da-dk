---
title: Politikker for lagerstedsarbejde
description: Lagerstedets arbejdspolitikker kontrollerer, om lagerstedsarbejde er oprettet af lagerprocesser i produktion, ud fra arbejdsordretype, lagerlokation og produkt.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ec7dd3b91851729e866bc90ca85a118839f9d71d
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="warehouse-work-policies"></a>Politikker for lagerstedsarbejde

[!include[banner](../includes/banner.md)]


Lagerstedets arbejdspolitikker i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition kontrollerer, om lagerstedsarbejde er oprettet af lagerprocesser i produktion, ud fra arbejdsordretype, lagerlokation og produkt.

Denne arbejdspolitik kontrollerer, om lagerstedets arbejde er oprettet for lagerprocesser i produktion. Du kan angive arbejdspolitikken ved hjælp af en kombination af **arbejdsordretyper**, en **lagerlokation** og et **produkt**. Produkt L0101 rapporteres f.eks. som afsluttet til outputlokalitet 001. Den færdige vare forbruges senere i en anden produktionsordre på outputlokalitet 001. I dette tilfælde kan du oprette en arbejdspolitik for at forhindre, at der oprettes arbejde for færdige varer, når du rapporterer produkt L0101 færdig til outputlokalitet 001. Arbejdspolitikken er en enkelt enhed, der kan beskrives med følgende oplysninger:

-   **Navn på arbejdspolitik**(den entydige identifikator for arbejdspolitikken)
-   **Arbejdsordretyper** og **Metode til oprettelse af arbejde**
-   **Lagerlokationer**
-   **Produkter**

## <a name="work-order-types"></a>Arbejdsordretyper
Du kan vælge mellem følgende arbejdsordretyper:

-   Færdige varer, læg på lager
-   Samprodukt og biprodukt, læg på lager
-   Råvarepluk

Feltet **Metode til oprettelse af arbejde** har værdien **Aldrig**. Denne værdi angiver, at arbejdspolitikken forhindrer lagerstedsarbejde i at blive oprettet for den valgte arbejdsordretype.

## <a name="inventory-locations"></a>Lagerlokationer
Du kan vælge en lokation, der vedrører arbejdspolitikken. Hvis ingen lokation er knyttet til en arbejdspolitik, gælder den ikke for alle processer. På siden **Lokationer** kan du også vælge eller annullere valget af arbejdspolitikken for en bestemt lokation.

## <a name="products"></a>Produkter
Du kan vælge et produkt, der vedrører arbejdspolitikken. Du kan anvende arbejdspolitikken på alle produkter eller udvalgte produkter.

## <a name="example"></a>Eksempel
I følgende eksempel er der to produktionsordrer, PRD-001 og PRD-00*2*. Produktionsordre PRD-001 er en handling, der hedder **Assembly**, hvor produktet SC1 færdigmeldes på lokation O1. Produktionsordre PRD-002 er en handling, der hedder **Painting** og forbruger produkt SC1 fra lokation O1. Produktionsordren PRD-002 forbruger også råvare RM1 fra lokation O1. RM1 gemmes i lagerlokation BULK-001 og vil blive plukket til lokation O1 af lagerstedets arbejde til råvareplukning. Plukkearbejdet genereres, når produktionen PRD-002 frigives. 

[![Politikker for lagerstedsarbejde](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png) 

Når du skal konfigurere lagerstedets arbejdspolitik for dette scenario, skal du overveje følgende oplysninger:

-   Lagerstedets arbejde for færdigvarer, der lægges på lager, er ikke påkrævet, når du færdigmelder produkt SC1 fra produktionsordre PRD-001 til lokation O1. Dette skyldes, at **Painting**-operation for produktionsordre PRD-002 forbruger SC1 på samme lokation.
-   Lagerstedsarbejde til plukning af råvarer kræves for at flytte råvare RM1 fra lagerlokation BULK-001 til lokation O1.

Her er et eksempel på den politik for arbejde, du har angivet, ud fra disse overvejelser.

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
|**Navn på arbejdspolitik**<br>                 |**Arbejdsordretyper**<br>                               |
| Læg ikke på lager 01     `                    |- Færdige varer, læg på lager<br>                           |
|                                         |**Lokationer**<br>                                      |
|                                         |- O1   |                                               |
|                                         |**Produkter** <br>                                      |
|                                         |- SC1                                                  |

Følgende procedurer indeholder trinvise instruktioner om, hvordan du konfigurerer arbejdspolitikken for lagersted i dette scenario. En eksempelopsætning, der viser, hvordan du færdigmelder en produktionsordre til en lokation, der ikke er id-kontrolleret, beskrives også.

## <a name="set-up-a-warehouse-work-policy"></a>Konfigurere en arbejdspolitik for lagersted
Lagerstedsprocesser omfatter ikke altid lagerstedsarbejde. Ved at definere en arbejdspolitik kan du forhindre oprettelse af arbejde med pluk af råmaterialer og placering af færdigvarer på lager for en række produkter på bestemte lokationer. Demodatafirmaet USMF bruges til at oprette denne procedure. 

TRIN (21)

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| 1  | Gå til Lagerstyring &gt; Konfiguration &gt; Arbejde &gt; Arbejdspolitikker.        |
| 2  | Klik på Ny.                                                                 |
| 3  | Skriv 'Ikke læg-på-lager-arbejde' i navnefeltet Arbejdspolitik.                    |
| 4  | Klik på Gem.                                                                |
| 5  | Klik på Tilføj.                                                                 |
| 6  | Markér den valgte række på listen.                                        |
| 7  | Vælg 'Færdige varer lægges på lager' i feltet Arbejdsordretype.            |
| 8  | Klik på Tilføj.                                                                 |
| 9  | Markér den valgte række på listen.                                        |
| 10. | Vælg 'Samprodukter eller biprodukter, der er lagt på lager' i feltet Arbejdsordretype. |
| 11. | Udvid sektionen Lagerlokationer.                                    |
| 12. | Klik på Tilføj.                                                                 |
| 13 | Markér den valgte række på listen.                                        |
| 14. | Indtast '51' på lagerstedslisten.                                         |
| 15. | Indtast eller vælg '001' i feltet Lokation.                              |
| 16. | Udvid afsnittet Produkter.                                               |
| 17. | Vælg 'Valgt' i feltet Produktvalg.                         |
| 18. | Klik på Tilføj.                                                                 |
| 19. | Markér den valgte række på listen.                                        |
| 20. | Indtast eller vælg 'L0101' i feltet Varenummer.                         |
| 21. | Klik på Gem.                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Færdigmelde en produktionsordre til en lokation, der ikke er id-kontrolleret
Denne procedure viser et eksempel på færdigmelding til en lokation, der ikke er id-kontrolleret. En relevant arbejdspolitik er en forudsætning for denne opgave. Foregående procedure viser konfigurationen af arbejdspolitikken. 

TRIN (25)

<table>
<tbody>
<tr>
<td colspan="3"><strong>Underopgave: Konfigurere en outputlokation.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Gå til Virksomhedsadministration &gt; Ressourcer &gt; Ressourcegrupper.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Vælg ressourcegruppen '5102' på listen.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Klik på Rediger.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Indtast '51' i feltet Lagersted for udlagring.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Indtast '001' i feltet Udlagringslokation.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Lokationen 001 er ikke en id-kontrolleret lokation. Du kan kun konfigurere en outputplacering uden id-kontrol, hvis der findes en gyldig arbejdspolitik for lokationen.</td>
</tr>
<tr>
<td colspan="3"><strong>Underopgave: Oprette en produktionsordre og rapportere den som færdig.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Luk siden.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Gå til Produktionsstyring &gt; Produktionsordrer &gt; Alle produktionsordrer.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Klik på Ny produktionsordre.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Indtast 'L0101' i feltet Varenummer.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Klik på Opret.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Klik på Produktionsordre i handlingsruden.</td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td>Klik på Forkalkulation.</td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td>Klik på OK.</td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td>Klik på Start.</td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td>Klik på fanen Generelt.</td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td>Vælg "Aldrig" i feltet Automatisk styklisteforbrug.</td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td>Klik på OK.</td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td>Klik på Færdigmeld.</td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td>Klik på fanen Generelt.</td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td>Vælg Ja i feltet Accepter fejl.</td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td>Klik på OK.</td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td>Klik på Lagersted i handlingsruden.</td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td>Klik på Arbejdsdetaljer.</td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td>Når produktionsordren er færdigmeldt, oprettes der intet arbejde for læg-på-lager. Dette skyldes, at der er defineret en arbejdspolitik, som forhindrer, at der genereres arbejde, når produktet L0101 rapporteres som færdigt på lokation 001.</td>
</tr>
</tbody>
</table>




