---
title: eDiscovery in EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3128419f-dd5f-46d2-bb0d-0940738d0bb6
description: Informationen Sie zu eDiscovery in EWS in Exchange.
ms.openlocfilehash: 6491fdd9f2246870a89bfa89bf7d97b972d67c92
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756823"
---
# <a name="ediscovery-in-ews-in-exchange"></a><span data-ttu-id="a8248-103">eDiscovery in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="a8248-103">eDiscovery in EWS in Exchange</span></span>

<span data-ttu-id="a8248-104">Informationen Sie zu eDiscovery in EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="a8248-104">Learn about eDiscovery in EWS in Exchange.</span></span>
  
<span data-ttu-id="a8248-105">eDiscovery ist ein Verbundpartner Query-Webdienst, der externe Anwendungen, die zum Ausführen von Abfragen von Exchange-Daten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="a8248-105">eDiscovery is a federated query web service that enables external applications to perform queries of Exchange data.</span></span>
  
<span data-ttu-id="a8248-106">Ermittlung besteht aus mehreren Phasen, einschließlich identifizieren und Beibehalten von wichtigen Daten, culling nach unten und Überprüfen der Daten und Daten in gerichtlichen erzeugt.</span><span class="sxs-lookup"><span data-stu-id="a8248-106">Discovery consists of several phases, including identifying and preserving key data, culling down and reviewing the data, and producing data in court.</span></span> <span data-ttu-id="a8248-107">eDiscovery-Abfragen erleichtern den Suchprozess durch Bereitstellen eines einzelnen Discovery Workflows über Exchange und SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a8248-107">eDiscovery queries facilitate the discovery process by providing a single discovery workflow across Exchange and SharePoint.</span></span>
  
## <a name="ediscovery-operations"></a><span data-ttu-id="a8248-108">eDiscovery-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="a8248-108">eDiscovery operations</span></span>

<span data-ttu-id="a8248-109">EDiscovery-Funktionalität, die vom Exchange-Webdienste verfügbar gemacht wird ist über Vorgänge eingeführt in Exchange Online, Exchange Online als Teil von Office 365 und Exchange beginnend mit Exchange 2013-Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a8248-109">The eDiscovery functionality that is exposed by EWS is available via operations introduced in Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2013.</span></span> 
  
<span data-ttu-id="a8248-110">**In Tabelle 1. Neue Vorgänge für eDiscovery**</span><span class="sxs-lookup"><span data-stu-id="a8248-110">**Table 1. New operations for eDiscovery**</span></span>

|<span data-ttu-id="a8248-111">**Name des Vorgangs**</span><span class="sxs-lookup"><span data-stu-id="a8248-111">**Operation name**</span></span>|<span data-ttu-id="a8248-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a8248-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8248-113">GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8248-113">GetDiscoverySearchConfiguration</span></span>](http://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |<span data-ttu-id="a8248-114">Ruft die Konfigurationsinformationen für Compliance-Archive, gespeicherte Discovery-Suche und die Postfächer, die für die Ermittlung Suche aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="a8248-114">Gets configuration information for in-place holds, saved discovery searches, and the mailboxes that are enabled for discovery search.</span></span>  <br/> |
|[<span data-ttu-id="a8248-115">GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="a8248-115">GetHoldOnMailboxes</span></span>](http://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |<span data-ttu-id="a8248-116">Ruft den Status einer abfragebasierte Aufbewahrung, die mit der [SetHoldOnMailboxes-Vorgang](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a8248-116">Gets the status of a query-based hold, which is set by using the [SetHoldOnMailboxes operation](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx).</span></span>  <br/> |
|[<span data-ttu-id="a8248-117">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="a8248-117">GetNonIndexableItemDetails</span></span>](http://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |<span data-ttu-id="a8248-118">Ruft die Details zu den Elementen, die nicht indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="a8248-118">Retrieves details about items that cannot be indexed.</span></span> <span data-ttu-id="a8248-119">Dies umfasst, jedoch ist nicht beschränkt auf, die Element-ID, ein Fehlercode, eine fehlerbeschreibung, wenn versucht wurde, das Element und zusätzliche Informationen zur Datei zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="a8248-119">This includes, but is not limited to, the item identifier, an error code, an error description, when an attempt was made to index the item, and additional information about the file.</span></span>  <br/> |
|[<span data-ttu-id="a8248-120">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="a8248-120">GetNonIndexableItemStatistics</span></span>](http://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |<span data-ttu-id="a8248-121">Ruft die Anzahl der Elemente, die in einem Postfach nicht indiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a8248-121">Retrieves the count of items that cannot be indexed in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a8248-122">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="a8248-122">GetSearchableMailboxes</span></span>](http://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |<span data-ttu-id="a8248-123">Ruft einer Liste der Postfächer, die der Client verfügt über die Berechtigung zum Durchsuchen oder zum Ausführen von eDiscovery auf.</span><span class="sxs-lookup"><span data-stu-id="a8248-123">Gets a list of mailboxes that the client has permission to search or perform eDiscovery on.</span></span>  <br/> |
|[<span data-ttu-id="a8248-124">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="a8248-124">SearchMailboxes</span></span>](http://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |<span data-ttu-id="a8248-125">Sucht nach Elementen in bestimmte Postfächer, die von Abfrageschlüsselwörtern entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a8248-125">Searches for items in specific mailboxes that match query keywords.</span></span>  <br/> |
|[<span data-ttu-id="a8248-126">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="a8248-126">SetHoldOnMailboxes</span></span>](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |<span data-ttu-id="a8248-127">Legt ein abfragebasiertes enthalten Elemente.</span><span class="sxs-lookup"><span data-stu-id="a8248-127">Sets a query-based hold on items.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8248-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8248-128">See also</span></span>

- [<span data-ttu-id="a8248-129">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="a8248-129">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="a8248-130">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="a8248-130">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    
- [<span data-ttu-id="a8248-131">Übersicht über den EWS-Cliententwurf für Exchange</span><span class="sxs-lookup"><span data-stu-id="a8248-131">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    

