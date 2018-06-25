---
title: Transport-Agents in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 36d63aa6-1b72-4670-b5c3-da685f3017cb
description: Hier finden Sie Informationen zu Transport-Agents in Exchange 2013.
ms.openlocfilehash: 1a28ae79e2a7e338ddd6cb1f6961dd14a980b56e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757203"
---
# <a name="transport-agents-in-exchange"></a><span data-ttu-id="ed8c4-103">Transport-Agents in Exchange</span><span class="sxs-lookup"><span data-stu-id="ed8c4-103">Transport agents in Exchange</span></span>
  
<span data-ttu-id="ed8c4-104">Exchange 2013 bietet eine Bibliothek mit Klassen, die Unterstützung der Erweiterungs für das Verhalten des Exchange-Transport, und aktivieren das Lesen, schreiben und Konvertieren von Inhaltstypen.</span><span class="sxs-lookup"><span data-stu-id="ed8c4-104">Exchange 2013 provides a library of classes that support the extension of the Exchange transport behavior and enable the reading, writing, and converting of content types.</span></span> <span data-ttu-id="ed8c4-105">Diese Klassen können Sie Exchange-Transport-Anwendungen erstellen, die lesen und schreiben sowie die Nachrichten in der Transportpipeline zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ed8c4-105">You can use these classes to create Exchange transport applications that read, write, and process messages in the transport pipeline.</span></span>
  
## <a name="what-you-need-to-know-about-transport-agents"></a><span data-ttu-id="ed8c4-106">Was Sie über Transport-Agents wissen müssen</span><span class="sxs-lookup"><span data-stu-id="ed8c4-106">What you need to know about transport agents</span></span>

|<span data-ttu-id="ed8c4-107">Wenn Sie wissen möchten, zu...</span><span class="sxs-lookup"><span data-stu-id="ed8c4-107">If you're wondering about…</span></span>|<span data-ttu-id="ed8c4-108">Lesen Sie diesen Artikel</span><span class="sxs-lookup"><span data-stu-id="ed8c4-108">Read this</span></span>|
|:-----|:-----|
|<span data-ttu-id="ed8c4-109">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="ed8c4-109">Availability</span></span>  <br/> |<span data-ttu-id="ed8c4-110">Transport-Agents sind in Exchange beginnend mit Exchange 2007-Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ed8c4-110">Transport agents are available in versions of Exchange starting with Exchange 2007.</span></span> <span data-ttu-id="ed8c4-111">Transport-Agents werden nicht in Office 365 oder Exchange Online unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed8c4-111">Transport agents are not supported in Office 365 or Exchange Online.</span></span>  <br/> |
|<span data-ttu-id="ed8c4-112">Remoteverwendung</span><span class="sxs-lookup"><span data-stu-id="ed8c4-112">Remote usage</span></span>  <br/> |<span data-ttu-id="ed8c4-113">Transport-Agents werden auf dem Exchange-Server ausgeführt, und Remotezugriff wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed8c4-113">Transport agents run on the Exchange server and do not support remote usage.</span></span>  <br/> |
|<span data-ttu-id="ed8c4-114">Unterstützte Sprachen</span><span class="sxs-lookup"><span data-stu-id="ed8c4-114">Languages supported</span></span>  <br/> |<span data-ttu-id="ed8c4-115">Sie können eine beliebige .NET Framework-Sprache für die Arbeit mit Transport-Agents verwenden.</span><span class="sxs-lookup"><span data-stu-id="ed8c4-115">You can use any .NET Framework language to work with transport agents.</span></span>  <br/> |
|<span data-ttu-id="ed8c4-116">Verfügbare Test- und Debuggingtools</span><span class="sxs-lookup"><span data-stu-id="ed8c4-116">Available test and debug tools</span></span>  <br/> |<span data-ttu-id="ed8c4-117">Verwenden Sie Visual Studio ab Version Visual Studio 2012, um Transport-Agents zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="ed8c4-117">Use versions of Visual Studio starting with Visual Studio 2012 to debug transport agents.</span></span>  <br/> |
|<span data-ttu-id="ed8c4-118">Methoden für die Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="ed8c4-118">Deployment methods</span></span>  <br/> |<span data-ttu-id="ed8c4-119">Sie können mithilfe eines Skripts für die [Exchange-Verwaltungsshell](../management/exchange-management-shell.md) Transport-Agent Applikationen installieren.</span><span class="sxs-lookup"><span data-stu-id="ed8c4-119">You can install transport agent applications by using an [Exchange Management Shell](../management/exchange-management-shell.md) script.</span></span>  <br/> |
   
## <a name="in-this-section"></a><span data-ttu-id="ed8c4-120">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="ed8c4-120">In this section</span></span>

- [<span data-ttu-id="ed8c4-121">Neue und aktualisierte Transport-Agent-APIs in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="ed8c4-121">New and updated transport agent APIs in Exchange 2013</span></span>](new-and-updated-transport-agent-apis-in-exchange-2013.md)
    
- [<span data-ttu-id="ed8c4-122">Transport-Agent-Codebeispiele für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="ed8c4-122">Transport agent code samples for Exchange 2013</span></span>](transport-agent-code-samples-for-exchange-2013.md)
    
- [<span data-ttu-id="ed8c4-123">Transport-Agent Konzepte in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="ed8c4-123">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)
    
- [<span data-ttu-id="ed8c4-124">Lesen und Ändern von Nachrichten in der Transportpipeline Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="ed8c4-124">Reading and modifying messages in the Exchange 2013 transport pipeline</span></span>](reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline.md)
    
- [<span data-ttu-id="ed8c4-125">Erstellen von Transport-Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="ed8c4-125">Creating transport agents for Exchange 2013</span></span>](creating-transport-agents-for-exchange-2013.md)
    
- [<span data-ttu-id="ed8c4-126">Transport-Agent-Referenz für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="ed8c4-126">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
    
## <a name="see-also"></a><span data-ttu-id="ed8c4-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed8c4-127">See also</span></span>

- [<span data-ttu-id="ed8c4-128">Exchange Online und Exchange-Entwicklung</span><span class="sxs-lookup"><span data-stu-id="ed8c4-128">Exchange Online and Exchange development</span></span>](../exchange-server-development.md)    
- [<span data-ttu-id="ed8c4-129">Erkunden von verwalteter EWS-API, EWS und Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="ed8c4-129">Explore the EWS Managed API, EWS, and web services in Exchange</span></span>](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)   
- [<span data-ttu-id="ed8c4-130">Sicherung und Wiederherstellung für Exchange</span><span class="sxs-lookup"><span data-stu-id="ed8c4-130">Backup and restore for Exchange</span></span>](../backup-restore/backup-and-restore-for-exchange-2013.md) 
    

