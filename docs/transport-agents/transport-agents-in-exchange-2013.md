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
ms.openlocfilehash: 62fb259672c47242a57b939deb4887e1e5519e2a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461758"
---
# <a name="transport-agents-in-exchange"></a><span data-ttu-id="a5cc6-103">Transport-Agents in Exchange</span><span class="sxs-lookup"><span data-stu-id="a5cc6-103">Transport agents in Exchange</span></span>
  
<span data-ttu-id="a5cc6-104">Exchange 2013 enthält eine Bibliothek mit Klassen, die die Erweiterung des Exchange-Transportverhaltens unterstützen und das Lesen, schreiben und Konvertieren von Inhaltstypen ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a5cc6-104">Exchange 2013 provides a library of classes that support the extension of the Exchange transport behavior and enable the reading, writing, and converting of content types.</span></span> <span data-ttu-id="a5cc6-105">Sie können diese Klassen verwenden, um Exchange-Transportanwendungen zu erstellen, die Nachrichten in der Transportpipeline schreiben, lesen und verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="a5cc6-105">You can use these classes to create Exchange transport applications that read, write, and process messages in the transport pipeline.</span></span>
  
## <a name="what-you-need-to-know-about-transport-agents"></a><span data-ttu-id="a5cc6-106">Was Sie über Transport-Agents wissen müssen</span><span class="sxs-lookup"><span data-stu-id="a5cc6-106">What you need to know about transport agents</span></span>

|<span data-ttu-id="a5cc6-107">Wenn Sie sich Fragen, über...</span><span class="sxs-lookup"><span data-stu-id="a5cc6-107">If you're wondering about…</span></span>|<span data-ttu-id="a5cc6-108">Lesen Sie diesen Artikel</span><span class="sxs-lookup"><span data-stu-id="a5cc6-108">Read this</span></span>|
|:-----|:-----|
|<span data-ttu-id="a5cc6-109">Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="a5cc6-109">Availability</span></span>  <br/> |<span data-ttu-id="a5cc6-110">Transport-Agents stehen in Exchange-Versionen ab Exchange 2007 zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a5cc6-110">Transport agents are available in versions of Exchange starting with Exchange 2007.</span></span> <span data-ttu-id="a5cc6-111">Transport-Agents werden in Office 365 oder Exchange Online nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a5cc6-111">Transport agents are not supported in Office 365 or Exchange Online.</span></span>  <br/> |
|<span data-ttu-id="a5cc6-112">Remoteverwendung</span><span class="sxs-lookup"><span data-stu-id="a5cc6-112">Remote usage</span></span>  <br/> |<span data-ttu-id="a5cc6-113">Transport-Agents werden auf dem Exchange-Server ausgeführt, und Remotezugriff wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a5cc6-113">Transport agents run on the Exchange server and do not support remote usage.</span></span>  <br/> |
|<span data-ttu-id="a5cc6-114">Unterstützte Sprachen</span><span class="sxs-lookup"><span data-stu-id="a5cc6-114">Languages supported</span></span>  <br/> |<span data-ttu-id="a5cc6-115">Sie können eine beliebige .NET Framework-Sprache für die Arbeit mit Transport-Agents verwenden.</span><span class="sxs-lookup"><span data-stu-id="a5cc6-115">You can use any .NET Framework language to work with transport agents.</span></span>  <br/> |
|<span data-ttu-id="a5cc6-116">Verfügbare Test- und Debuggingtools</span><span class="sxs-lookup"><span data-stu-id="a5cc6-116">Available test and debug tools</span></span>  <br/> |<span data-ttu-id="a5cc6-117">Verwenden Sie Visual Studio ab Version Visual Studio 2012, um Transport-Agents zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="a5cc6-117">Use versions of Visual Studio starting with Visual Studio 2012 to debug transport agents.</span></span>  <br/> |
|<span data-ttu-id="a5cc6-118">Methoden für die Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="a5cc6-118">Deployment methods</span></span>  <br/> |<span data-ttu-id="a5cc6-119">Sie können Transport-Agentanwendungen mithilfe eines [Exchange Management Shell](../management/exchange-management-shell.md)-Skripts installieren.</span><span class="sxs-lookup"><span data-stu-id="a5cc6-119">You can install transport agent applications by using an [Exchange Management Shell](../management/exchange-management-shell.md) script.</span></span>  <br/> |
   
## <a name="in-this-section"></a><span data-ttu-id="a5cc6-120">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="a5cc6-120">In this section</span></span>

- [<span data-ttu-id="a5cc6-121">Neue und aktualisierte Transport-Agent-APIs in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="a5cc6-121">New and updated transport agent APIs in Exchange 2013</span></span>](new-and-updated-transport-agent-apis-in-exchange-2013.md)
    
- [<span data-ttu-id="a5cc6-122">Codebeispiele für Transport-Agent für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="a5cc6-122">Transport agent code samples for Exchange 2013</span></span>](transport-agent-code-samples-for-exchange-2013.md)
    
- [<span data-ttu-id="a5cc6-123">Transport-Agent-Konzepte in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="a5cc6-123">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)
    
- [<span data-ttu-id="a5cc6-124">Lesen und Ändern von Nachrichten in der Exchange 2013 Transportpipeline</span><span class="sxs-lookup"><span data-stu-id="a5cc6-124">Reading and modifying messages in the Exchange 2013 transport pipeline</span></span>](reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline.md)
    
- [<span data-ttu-id="a5cc6-125">Erstellen von Transport-Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="a5cc6-125">Creating transport agents for Exchange 2013</span></span>](creating-transport-agents-for-exchange-2013.md)
    
- [<span data-ttu-id="a5cc6-126">Transport-Agent-Referenz für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="a5cc6-126">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
    
## <a name="see-also"></a><span data-ttu-id="a5cc6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5cc6-127">See also</span></span>

- [<span data-ttu-id="a5cc6-128">Exchange Online- und Exchange-Entwicklung</span><span class="sxs-lookup"><span data-stu-id="a5cc6-128">Exchange Online and Exchange development</span></span>](../exchange-server-development.md)    
- [<span data-ttu-id="a5cc6-129">Erkunden von EWS Managed API, EWS und Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="a5cc6-129">Explore the EWS Managed API, EWS, and web services in Exchange</span></span>](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)   
- [<span data-ttu-id="a5cc6-130">Sicherung und Wiederherstellung für Exchange</span><span class="sxs-lookup"><span data-stu-id="a5cc6-130">Backup and restore for Exchange</span></span>](../backup-restore/backup-and-restore-for-exchange-2013.md) 
    

