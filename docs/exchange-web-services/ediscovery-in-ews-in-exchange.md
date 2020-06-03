---
title: eDiscovery in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3128419f-dd5f-46d2-bb0d-0940738d0bb6
description: Erfahren Sie mehr über eDiscovery in EWS in Exchange.
ms.openlocfilehash: 48e3fdb3a2f21f7dcfcb7eed21b586e099b249a3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456094"
---
# <a name="ediscovery-in-ews-in-exchange"></a><span data-ttu-id="4e8db-103">eDiscovery in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="4e8db-103">eDiscovery in EWS in Exchange</span></span>

<span data-ttu-id="4e8db-104">Erfahren Sie mehr über eDiscovery in EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="4e8db-104">Learn about eDiscovery in EWS in Exchange.</span></span>
  
<span data-ttu-id="4e8db-105">eDiscovery ist ein Webdienst für die Verbund Abfrage, mit dem externe Anwendungen Abfragen von Exchange-Daten ausführen können.</span><span class="sxs-lookup"><span data-stu-id="4e8db-105">eDiscovery is a federated query web service that enables external applications to perform queries of Exchange data.</span></span>
  
<span data-ttu-id="4e8db-106">Die Ermittlung umfasst mehrere Phasen, darunter das identifizieren und beibehalten von Schlüsseldaten, das Ausmerzen und Überprüfen der Daten und das Erstellen von Daten vor Gericht.</span><span class="sxs-lookup"><span data-stu-id="4e8db-106">Discovery consists of several phases, including identifying and preserving key data, culling down and reviewing the data, and producing data in court.</span></span> <span data-ttu-id="4e8db-107">eDiscovery-Abfragen erleichtern den Ermittlungsprozess durch Bereitstellen eines einzelnen Discovery-Workflows in Exchange und SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4e8db-107">eDiscovery queries facilitate the discovery process by providing a single discovery workflow across Exchange and SharePoint.</span></span>
  
## <a name="ediscovery-operations"></a><span data-ttu-id="4e8db-108">eDiscovery-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="4e8db-108">eDiscovery operations</span></span>

<span data-ttu-id="4e8db-109">Die eDiscovery-Funktionalität, die von EWS verfügbar gemacht wird, ist über Vorgänge verfügbar, die in Exchange Online eingeführt werden, Exchange Online im Rahmen von Office 365 und Exchange-Versionen, die mit Exchange 2013 beginnen.</span><span class="sxs-lookup"><span data-stu-id="4e8db-109">The eDiscovery functionality that is exposed by EWS is available via operations introduced in Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2013.</span></span> 
  
<span data-ttu-id="4e8db-110">**Tabelle 1. Neue Vorgänge für eDiscovery**</span><span class="sxs-lookup"><span data-stu-id="4e8db-110">**Table 1. New operations for eDiscovery**</span></span>

|<span data-ttu-id="4e8db-111">**Name des Vorgangs**</span><span class="sxs-lookup"><span data-stu-id="4e8db-111">**Operation name**</span></span>|<span data-ttu-id="4e8db-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4e8db-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e8db-113">GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e8db-113">GetDiscoverySearchConfiguration</span></span>](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |<span data-ttu-id="4e8db-114">Ruft Konfigurationsinformationen für in-Place-Speicher, gespeicherte Ermittlungs suchen und die für die Ermittlungs Suche aktivierten Postfächer ab.</span><span class="sxs-lookup"><span data-stu-id="4e8db-114">Gets configuration information for in-place holds, saved discovery searches, and the mailboxes that are enabled for discovery search.</span></span>  <br/> |
|[<span data-ttu-id="4e8db-115">GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="4e8db-115">GetHoldOnMailboxes</span></span>](https://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |<span data-ttu-id="4e8db-116">Ruft den Status eines abfragebasierten haltebereichs ab, der mithilfe des [SetHoldOnMailboxes-Vorgangs](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx)festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4e8db-116">Gets the status of a query-based hold, which is set by using the [SetHoldOnMailboxes operation](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx).</span></span>  <br/> |
|[<span data-ttu-id="4e8db-117">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="4e8db-117">GetNonIndexableItemDetails</span></span>](https://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |<span data-ttu-id="4e8db-118">Ruft Details zu Elementen ab, die nicht indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="4e8db-118">Retrieves details about items that cannot be indexed.</span></span> <span data-ttu-id="4e8db-119">Dies umfasst, jedoch nicht auf die Element-ID, einen Fehlercode, eine Fehlerbeschreibung, bei dem Versuch, das Element zu indizieren, sowie zusätzliche Informationen zur Datei.</span><span class="sxs-lookup"><span data-stu-id="4e8db-119">This includes, but is not limited to, the item identifier, an error code, an error description, when an attempt was made to index the item, and additional information about the file.</span></span>  <br/> |
|[<span data-ttu-id="4e8db-120">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="4e8db-120">GetNonIndexableItemStatistics</span></span>](https://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |<span data-ttu-id="4e8db-121">Ruft die Anzahl der Elemente ab, die nicht in einem Postfach indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="4e8db-121">Retrieves the count of items that cannot be indexed in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="4e8db-122">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="4e8db-122">GetSearchableMailboxes</span></span>](https://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |<span data-ttu-id="4e8db-123">Ruft eine Liste von Postfächern ab, für die der Client über die Berechtigung zum Durchsuchen oder Ausführen von eDiscovery verfügt.</span><span class="sxs-lookup"><span data-stu-id="4e8db-123">Gets a list of mailboxes that the client has permission to search or perform eDiscovery on.</span></span>  <br/> |
|[<span data-ttu-id="4e8db-124">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="4e8db-124">SearchMailboxes</span></span>](https://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |<span data-ttu-id="4e8db-125">Sucht nach Elementen in bestimmten Postfächern, die Abfrageschlüsselwörtern entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4e8db-125">Searches for items in specific mailboxes that match query keywords.</span></span>  <br/> |
|[<span data-ttu-id="4e8db-126">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="4e8db-126">SetHoldOnMailboxes</span></span>](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |<span data-ttu-id="4e8db-127">Legt einen abfragebasierten Haltebereich für Elemente fest.</span><span class="sxs-lookup"><span data-stu-id="4e8db-127">Sets a query-based hold on items.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e8db-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e8db-128">See also</span></span>

- [<span data-ttu-id="4e8db-129">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="4e8db-129">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="4e8db-130">Verwenden von Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="4e8db-130">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    
- [<span data-ttu-id="4e8db-131">Übersicht über den EWS-Cliententwurf für Exchange</span><span class="sxs-lookup"><span data-stu-id="4e8db-131">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    

