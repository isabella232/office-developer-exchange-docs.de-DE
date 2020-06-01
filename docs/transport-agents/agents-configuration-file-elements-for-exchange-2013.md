---
title: Elemente der Konfigurationsdatei der Agents für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Agents
api_type:
- schema
ms.assetid: 3047653b-d712-46c1-ae0a-73f3975f5e9d
description: Hier finden Sie Informationen zu den XML-Elementen in der Konfigurationsdatei Agents. config und fetagents. config in Exchange 2013.
ms.openlocfilehash: f19fe8316a78cef668db881e630562d3be8be64a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461569"
---
# <a name="agents-configuration-file-elements-for-exchange-2013"></a><span data-ttu-id="7fc6c-103">Elemente der Konfigurationsdatei der Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="7fc6c-103">Agents configuration file elements for Exchange 2013</span></span>

<span data-ttu-id="7fc6c-104">Hier finden Sie Informationen zu den XML-Elementen in der Konfigurationsdatei Agents. config und fetagents. config in Exchange 2013.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-104">Find information about the XML elements in the agents.config and fetagents.config configuration file in Exchange 2013.</span></span>
  
<span data-ttu-id="7fc6c-105">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="7fc6c-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="7fc6c-106">Wenn Sie die Client Zugriffs-oder Postfachserverrolle auf einem Exchange-Server installieren, erstellt das Installationsprogramm eine XML-Datei mit Konfigurationsinformationen zu Agents, die auf dem Server installiert sind.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-106">When you install the Client Access or the Mailbox server role on an Exchange server, the installer creates an XML file that contains configuration information about agents that are installed on the server.</span></span> <span data-ttu-id="7fc6c-107">Sie können nicht direkt in diese Datei schreiben.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-107">You cannot write directly to this file.</span></span> 
  
<span data-ttu-id="7fc6c-108">Der Front-End-Transport-Dienst wird auf Client Zugriffsservern ausgeführt und schreibt in eine Datei mit dem Namen "fetagents. config". Der Transportdienst und der postfachtransportdienst werden auf Postfachservern ausgeführt und in eine Datei mit dem Namen Agents. config geschrieben. Ein Computer, der über die Client Zugriffs-Serverrolle und die Postfachserverrolle verfügt, verfügt über eine Datei fetagents. config und eine Agents. config.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-108">The Front End Transport service runs on Client Access servers and writes to a file named fetagents.config. The Transport service and the Mailbox Transport service run on Mailbox servers, and write to a file named agents.config. A computer that has both the Client Access server role and the Mailbox server role will have both a fetagents.config and an agents.config file.</span></span> 
  
<span data-ttu-id="7fc6c-109">Die einzige unterstützte Möglichkeit, in diese Dateien zu schreiben, ist die Verwendung der Transport-Agent-Cmdlets im Exchange-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-109">The only supported way to write to these files is by using the transport agent cmdlets in the Exchange Management Shell.</span></span> <span data-ttu-id="7fc6c-110">Informationen zu den Transport-Agent-Cmdlets finden Sie unter [Nachrichtenfluss-Cmdlets](https://technet.microsoft.com/library/aa998553%28v=exchg.150%29.aspx) auf TechNet.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-110">For information about the transport agent cmdlets, see [Mail Flow Cmdlets](https://technet.microsoft.com/library/aa998553%28v=exchg.150%29.aspx) on TechNet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7fc6c-111">Um zwischen Agents zu unterscheiden, die den Front-End-Transport-Dienst auf dem Client Zugriffsserver und den Transportdienst auf dem Postfachserver erweitern, verfügen Transport-Agent-Cmdlets über einen _Transportservice_ -Parameter mit dem Wert "Hub" für den Transportdienst und "Frontend" für den Front-End-Transport-Dienst.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-111">To distinguish between agents that extend the Front End Transport service on the Client Access server and the Transport service on the Mailbox server, transport agent cmdlets have a  _TransportService_ parameter with a value of "Hub" for the Transport service and "FrontEnd" for the Front End Transport service.</span></span> 
  
<span data-ttu-id="7fc6c-112">Sie können die Datei Agents. config oder fetagents. config lesen, um das vorhanden sein von und Konfigurationsinformationen für einen oder mehrere Agents auf dem Server zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-112">You can read the agents.config or fetagents.config file to determine the presence of and configuration information for one or more agents on the server.</span></span> <span data-ttu-id="7fc6c-113">Diese Dokumentation enthält eine Referenz, die Sie verwenden können, um die Informationen in der Datei "Agents. config" oder in der fetagents. config zu lesen. Das Format für beide Dateien ist identisch.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-113">This documentation provides a reference that you can use to read the information in either the agents.config file or the fetagents.config. The format for both of these files is the same.</span></span> <span data-ttu-id="7fc6c-114">In dieser Dokumentation werden keine Informationen zum Schreiben in die Dateien bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-114">This documentation does not provide information about how to write to the files.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="7fc6c-115">Die Verwendung nicht unterstützter Methoden zum Schreiben in die Datei Agents. config oder fetagents. config kann zu unerwarteten Ergebnissen führen, einschließlich des Fehlers des Transportdiensts oder der Transport-Agents oder beider.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-115">Using unsupported methods to write to the agents.config file or fetagents.config can produce unexpected results, including failure of the transport service or transport agents, or both.</span></span> <span data-ttu-id="7fc6c-116">Schreiben Sie nicht direkt in eine dieser Dateien.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-116">Do not write directly to either of these files.</span></span> <span data-ttu-id="7fc6c-117">Die einzige unterstützte Methode zum Schreiben in diese Dateien ist die Verwendung der Cmdlets für den Exchange-Verwaltungsshell Transport-Agent.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-117">The only supported method for writing to these files is by using the Exchange Management Shell transport agent cmdlets.</span></span> 
  
## <a name="location-of-the-transport-agent-configuration-files"></a><span data-ttu-id="7fc6c-118">Speicherort der Transport-Agent-Konfigurationsdateien</span><span class="sxs-lookup"><span data-stu-id="7fc6c-118">Location of the transport agent configuration files</span></span>
<span data-ttu-id="7fc6c-119"><a name="bk_ConfigLoc"> </a></span><span class="sxs-lookup"><span data-stu-id="7fc6c-119"><a name="bk_ConfigLoc"> </a></span></span>

<span data-ttu-id="7fc6c-120">Wenn Sie Exchange 2013 installieren, erstellt das Installationsprogramm je nach installierter Serverrolle eine XML-Datei mit dem Namen "Agents. config. Template" oder "fetagents. config. Template" im \<ExchangeInstallFolder\> Ordner "\TransportRoles\Agents" (wobei \<ExchangeInstallFolder\> es sich um den Ordner handelt, in dem Sie Exchange 2013 installiert haben).</span><span class="sxs-lookup"><span data-stu-id="7fc6c-120">When you install Exchange 2013, the installer creates an XML file that is named either agents.config.template or fetagents.config.template, depending on the server role installed, in the \<ExchangeInstallFolder\>\TransportRoles\Agents folder (where \<ExchangeInstallFolder\> is the folder in which you installed Exchange 2013).</span></span> <span data-ttu-id="7fc6c-121">Wenn Sie die Client Zugriffs-Serverrolle installieren, kopiert Exchange 2013 die Datei fetagents. config. Template in fetagents. config. Wenn Sie die Postfachserverrolle installieren, kopiert Exchange 2013 die Datei Agents. config. Template in Agents. config. Exchange 2013 liest und schreibt diese Datei, wenn Sie die Transport-Agent-Konfiguration auf dem Server ändern.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-121">If you install the Client Access server role, Exchange 2013 copies the fetagents.config.template file to fetagents.config. If you install the Mailbox server role, Exchange 2013 copies the agents.config.template file to agents.config. Exchange 2013 reads and writes this file when you change the transport agents configuration on the server.</span></span>
  
## <a name="verifying-a-transport-agent-installation"></a><span data-ttu-id="7fc6c-122">Überprüfen der Installation eines Transport-Agents</span><span class="sxs-lookup"><span data-stu-id="7fc6c-122">Verifying a transport agent installation</span></span>
<span data-ttu-id="7fc6c-123"><a name="bk_verifyinstall"> </a></span><span class="sxs-lookup"><span data-stu-id="7fc6c-123"><a name="bk_verifyinstall"> </a></span></span>

<span data-ttu-id="7fc6c-124">Sie können die XML-Funktionen verwenden, die der .NET Framework zum Lesen und Validieren der XML-Datei "Agents. config" oder "fetagents. config" bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-124">You can use the XML capabilities that the .NET Framework provides to read and validate the agents.config or the fetagents.config XML file.</span></span> <span data-ttu-id="7fc6c-125">Zum Überprüfen der Installation und Konfiguration eines Transport-Agents lesen Sie den XML-Code in der Konfigurationsdatei, und suchen Sie nach dem [Agent](agent.md) -Element, das dem Transport-Agent entspricht.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-125">To verify the installation and configuration of a transport agent, read the XML in the configuration file and find the [agent](agent.md) element that corresponds to the transport agent.</span></span> <span data-ttu-id="7fc6c-126">Wenn kein **Agent** -Element für den bestimmten Transport-Agent vorhanden ist, ist der Transport-Agent nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-126">If an **agent** element for the specific transport agent does not exist, the transport agent is not installed.</span></span> <span data-ttu-id="7fc6c-127">Wenn der Transport-Agent installiert ist, können Sie die Attribute des **Agent** -Elements lesen, um die Konfiguration zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-127">If the transport agent is installed, you can read the attributes of the **agent** element to determine its configuration.</span></span> 
  
## <a name="configuration-file-element-hierarchy"></a><span data-ttu-id="7fc6c-128">Hierarchie der Konfigurationsdateielemente</span><span class="sxs-lookup"><span data-stu-id="7fc6c-128">Configuration file element hierarchy</span></span>
<span data-ttu-id="7fc6c-129"><a name="bk_elementref"> </a></span><span class="sxs-lookup"><span data-stu-id="7fc6c-129"><a name="bk_elementref"> </a></span></span>

<span data-ttu-id="7fc6c-130">Der folgende Code zeigt die Elementhierarchie in der XML-Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="7fc6c-130">The following code shows the element hierarchy in the configuration XML file.</span></span>
  
```XML
<configuration>
    <mexRuntime>
        <monitoring>
            <agentExecution/>
            <messageSnapshot/>
        </monitoring>
        <agentList>
            <agent/>
            <agent/>
            <agent />
        </agentList>
    </mexRuntim>
</configuration>
```

## <a name="in-this-section"></a><span data-ttu-id="7fc6c-131">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="7fc6c-131">In this section</span></span>
<span data-ttu-id="7fc6c-132"><a name="bk_elementreflist"> </a></span><span class="sxs-lookup"><span data-stu-id="7fc6c-132"><a name="bk_elementreflist"> </a></span></span>

- [<span data-ttu-id="7fc6c-133">Agent</span><span class="sxs-lookup"><span data-stu-id="7fc6c-133">agent</span></span>](agent.md)
    
- [<span data-ttu-id="7fc6c-134">agentExecution</span><span class="sxs-lookup"><span data-stu-id="7fc6c-134">agentExecution</span></span>](agentexecution.md)
    
- [<span data-ttu-id="7fc6c-135">Agentliste</span><span class="sxs-lookup"><span data-stu-id="7fc6c-135">agentList</span></span>](agentlist.md)
    
- [<span data-ttu-id="7fc6c-136">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="7fc6c-136">configuration</span></span>](configuration.md)
    
- [<span data-ttu-id="7fc6c-137">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="7fc6c-137">messageSnapshot</span></span>](messagesnapshot.md)
    
- [<span data-ttu-id="7fc6c-138">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="7fc6c-138">mexRuntime</span></span>](mexruntime.md)
    
- [<span data-ttu-id="7fc6c-139">Überwachung</span><span class="sxs-lookup"><span data-stu-id="7fc6c-139">monitoring</span></span>](monitoring.md)
    
## <a name="see-also"></a><span data-ttu-id="7fc6c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fc6c-140">See also</span></span>

- [<span data-ttu-id="7fc6c-141">Transport-Agents in Exchange</span><span class="sxs-lookup"><span data-stu-id="7fc6c-141">Transport agents in Exchange</span></span>](transport-agents-in-exchange-2013.md)
- [<span data-ttu-id="7fc6c-142">Transport-Agent-Konzepte in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="7fc6c-142">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)
- [<span data-ttu-id="7fc6c-143">Transport-Agent-Referenz für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="7fc6c-143">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
- [<span data-ttu-id="7fc6c-144">Namespaces des Transport-Agents in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="7fc6c-144">Transport agent namespaces in Exchange 2013</span></span>](transport-agent-namespaces-in-exchange-2013.md)
- [<span data-ttu-id="7fc6c-145">Cmdlets für den Nachrichtenfluss</span><span class="sxs-lookup"><span data-stu-id="7fc6c-145">Mail Flow Cmdlets</span></span>](https://docs.microsoft.com/powershell/exchange/?view=exchange-ps)
    

