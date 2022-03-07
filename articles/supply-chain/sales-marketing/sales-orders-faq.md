---
title: Ofte stillede spørgsmål om salgsordrer
description: Denne side omhandler ofte stillede spørgsmål, der vises, når der arbejdes med salgsordrer i Dynamics 365 Supply Chain Management.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d75022dcc476052040b16c9033cf5ff2a697ae6c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475895"
---
# <a name="sales-order-faqs"></a>Ofte stillede spørgsmål om Salgsordre

Denne side omhandler ofte stillede spørgsmål, der vises, når der arbejdes med salgsordrer i Dynamics 365 Supply Chain Management.

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Kan jeg knytte en indkøbsordre til en salgsordre for at opfylde efterspørgslen?

Du kan oprette en indkøbsordre ud fra en salgsordre. Du kan finde flere oplysninger i [Oprette en indkøbsordre fra en salgsordre](/dynamics365/supply-chain/sales-marketing/tasks/create-purchase-order-sales-order).

## <a name="can-i-cancel-or-delete-a-sales-order-or-return-order"></a>Kan jeg annullere eller slette en returordre eller salgsordre?

Du kan kun annullere salgsordrer og returordrer, der er i *Oprettet* tilstand. Du kan finde flere oplysninger under [Annullere en returordre](/dynamics365/supply-chain/service-management/cancel-return-order).

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Kan jeg gendanne en faktureret salgsordre, der er slettet?

Hvis en faktureret salgsordre blev slettet ved en fejl, kan du gendanne den eller se oplysningerne om den.

Gå til **Kundekonto \> Transaktioner \> Originalt dokument \> Vis detaljer**. Find den faktura, du leder efter, og vælg den for at få vist oplysninger om den. Disse oplysninger omfatter referencen til salgsordren. Du skulle også kunne få adgang til salgsordreoplysningerne fra den pågældende side.

## <a name="how-do-i-delete-orphaned-sales-order-records"></a>Hvordan kan jeg slette poster for tabte salgsordrer?

Hvis du vil rydde op i tabte salgsordreposter, skal du køre det periodiske job *Sletning af salgsordre* ved at gå til et af følgende steder:

- Salg og markering \> Periodiske opgaver \> Oprydning \> Slet salgsordrer
- Detail og handel \> Retail og Commerce IT \> Oprydning \> Slet salgsordrer

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Er det muligt at beregne provision på fakturaer, der allerede er bogført?

Supply Chain Management understøtter i øjeblikket ikke beregningen af provisioner for bogførte fakturaer.
