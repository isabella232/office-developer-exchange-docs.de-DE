---
title: Erstellen von Transport-Agents für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d291ab78-7cdd-4dbe-a5f4-9dc8e9650a33
description: Hier finden Sie Informationen zum Erstellen benutzerdefinierter Transport-Agents für Exchange 2013 und die Systemanforderungen zum Erstellen eines benutzerdefinierten Agents.
ms.openlocfilehash: cb1cd180817524fe29a100a48d90444c75a77510
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462374"
---
# <a name="creating-transport-agents-for-exchange-2013"></a><span data-ttu-id="82ddc-103">Erstellen von Transport-Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="82ddc-103">Creating transport agents for Exchange 2013</span></span>

<span data-ttu-id="82ddc-104">Hier finden Sie Informationen zum Erstellen benutzerdefinierter Transport-Agents für Exchange 2013 und die Systemanforderungen zum Erstellen eines benutzerdefinierten Agents.</span><span class="sxs-lookup"><span data-stu-id="82ddc-104">Find information about how to create custom transport agents for Exchange 2013, and the system requirements for creating a custom agent.</span></span>
  
<span data-ttu-id="82ddc-105">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="82ddc-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="82ddc-106">Exchange Server 2013 enthält mehrere Transport-Agents, die Sie zum Verarbeiten von Nachrichten verwenden können.</span><span class="sxs-lookup"><span data-stu-id="82ddc-106">Exchange Server 2013 includes several transport agents that you can use to process messages.</span></span> <span data-ttu-id="82ddc-107">Mithilfe der Assemblys, die mit Exchange geliefert werden, können Sie eigene benutzerdefinierte Agents erstellen, um bestimmte Aufgaben entsprechend den Anforderungen Ihrer Organisation auszuführen.</span><span class="sxs-lookup"><span data-stu-id="82ddc-107">By using the assemblies that come with Exchange, you can create your own custom agents to perform specific tasks according to the needs of your organization.</span></span> <span data-ttu-id="82ddc-108">Beispielsweise können Sie einen SmtpReceiveAgent-Transport-Agent zum Abfangen von Nachrichten verwenden, die über das SMTP-Protokoll empfangen werden, und die Nachricht verarbeiten, um das Format des Texts in vorformatierten Text zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="82ddc-108">For example, you can use an SmtpReceiveAgent transport agent to intercept messages that are received via the SMTP protocol and process the message to convert the format of the body to contain preformatted text.</span></span> <span data-ttu-id="82ddc-109">Sie können einen Routing Agent-Transport-Agent verwenden, um die Nachrichten zu protokollieren, die den Server auf der Route an einen anderen Server durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="82ddc-109">You can use a RoutingAgent transport agent to log the messages that pass through the server on route to another server.</span></span> <span data-ttu-id="82ddc-110">Sie können auch komplexere Features erstellen, die mehr als einen Agenttyp verwenden.</span><span class="sxs-lookup"><span data-stu-id="82ddc-110">You can also create more complex features that make use of more than one type of agent.</span></span> <span data-ttu-id="82ddc-111">Um beispielsweise einen Antivirus-Agent zu erstellen, können Sie ein SmtpReceiveAgent und einen Routing Agent-Agent implementieren.</span><span class="sxs-lookup"><span data-stu-id="82ddc-111">For example, to create an antivirus agent, you can implement an SmtpReceiveAgent and a RoutingAgent agent.</span></span> <span data-ttu-id="82ddc-112">Wenn Sie über eine Komponente in Ihrem Netzwerk verfügen, die das SMTP-Protokoll nicht unterstützt, können Sie einen DeliveryAgent-Transport-Agent verwenden, um die Kommunikation zwischen Ihrem Exchange-Server und ihrer externen Komponente zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="82ddc-112">If you have a component on your network that does not support the SMTP protocol, you can use a DeliveryAgent transport agent to handle the communication between your Exchange server and your external component.</span></span> 
  
<span data-ttu-id="82ddc-113">Dieser Artikel enthält Informationen zu den Voraussetzungen für und Aufgaben beim Erstellen Ihres eigenen Transport-Agents.</span><span class="sxs-lookup"><span data-stu-id="82ddc-113">This article provides information about the prerequisites for and tasks involved in creating your own transport agent.</span></span> <span data-ttu-id="82ddc-114">Informationen zum Erstellen bestimmter Transport-Agents finden Sie unter [Erstellen eines Routing Agent-Transport-Agents für Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md), [Erstellen eines SmtpReceiveAgent-Transport-Agents für Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)und [Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md).</span><span class="sxs-lookup"><span data-stu-id="82ddc-114">For information about creating specific transport agents, see [Create a RoutingAgent transport agent for Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md), [Create an SmtpReceiveAgent transport agent for Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md), and [Create a DeliveryAgent transport agent for Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md).</span></span>
  
## <a name="prerequisites-for-creating-a-transport-agent"></a><span data-ttu-id="82ddc-115">Voraussetzungen für die Erstellung eines Transport-Agents</span><span class="sxs-lookup"><span data-stu-id="82ddc-115">Prerequisites for creating a transport agent</span></span>
<span data-ttu-id="82ddc-116"><a name="bk_prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="82ddc-116"><a name="bk_prerequisites"> </a></span></span>

<span data-ttu-id="82ddc-117">Die folgenden Voraussetzungen müssen erfüllt sein, um einen Transport-Agent zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="82ddc-117">The following are the prerequisites that you need in order to implement a transport agent:</span></span>
  
- <span data-ttu-id="82ddc-118">Ein Computer mit Exchange 2013, der den Front-End-Transportdienst auf einem Client Zugriffs-oder Edge-Transport-Server ausführt, oder der Transport Dienst auf einem Postfachserver.</span><span class="sxs-lookup"><span data-stu-id="82ddc-118">A computer running Exchange 2013 that is running the Front End Transport service on a Client Access or Edge Transport server, or the Transport service on a Mailbox server.</span></span> <span data-ttu-id="82ddc-119">Informationen zur Architektur der Serverrolle in Exchange 2013 finden Sie unter [Transport-Agent-Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md).</span><span class="sxs-lookup"><span data-stu-id="82ddc-119">For information about the server role architecture in Exchange 2013, see [Transport agent concepts in Exchange 2013](transport-agent-concepts-in-exchange-2013.md).</span></span>
    
- <span data-ttu-id="82ddc-120">Die folgenden Assemblys für die Transport-Agent-Klassen:</span><span class="sxs-lookup"><span data-stu-id="82ddc-120">The following assemblies for the transport agent classes:</span></span>
    
  - <span data-ttu-id="82ddc-121">Microsoft. Exchange. Data. dll</span><span class="sxs-lookup"><span data-stu-id="82ddc-121">Microsoft.Exchange.Data.dll</span></span>
    
  - <span data-ttu-id="82ddc-122">Microsoft. Exchange. Data. Common. dll</span><span class="sxs-lookup"><span data-stu-id="82ddc-122">Microsoft.Exchange.Data.Common.dll</span></span>
    
  - <span data-ttu-id="82ddc-123">Microsoft. Exchange. Transport. dll</span><span class="sxs-lookup"><span data-stu-id="82ddc-123">Microsoft.Exchange.Transport.dll</span></span>
    
- <span data-ttu-id="82ddc-124">Die .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="82ddc-124">The .NET Framework 4.5</span></span>
    
<span data-ttu-id="82ddc-125">Außerdem wird empfohlen, Visual Studio 2012 zu installieren.</span><span class="sxs-lookup"><span data-stu-id="82ddc-125">We also recommend that you install Visual Studio 2012.</span></span> <span data-ttu-id="82ddc-126">Sie können Transport-Agents implementieren, indem Sie entweder Visual Basic .net oder C# verwenden.</span><span class="sxs-lookup"><span data-stu-id="82ddc-126">You can implement transport agents by using either Visual Basic .NET or C#.</span></span>
  
## <a name="referencing-the-assemblies"></a><span data-ttu-id="82ddc-127">Verweisen auf die Assemblys</span><span class="sxs-lookup"><span data-stu-id="82ddc-127">Referencing the assemblies</span></span>
<span data-ttu-id="82ddc-128"><a name="bk_ReferenceAssemblies"> </a></span><span class="sxs-lookup"><span data-stu-id="82ddc-128"><a name="bk_ReferenceAssemblies"> </a></span></span>

<span data-ttu-id="82ddc-129">Exchange 2013 enthält eine Bibliothek mit Klassen, die die Erweiterung des Exchange-Transportverhaltens unterstützen.</span><span class="sxs-lookup"><span data-stu-id="82ddc-129">Exchange 2013 provides a library of classes that support the extension of Exchange transport behavior.</span></span> <span data-ttu-id="82ddc-130">Für diese Klassen ist die .NET Framework 4.5 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="82ddc-130">These classes require the .NET Framework 4.5.</span></span> <span data-ttu-id="82ddc-131">Sie können Transport-Agents basierend auf diesen Klassen mithilfe von Visual Studio 2012 implementieren.</span><span class="sxs-lookup"><span data-stu-id="82ddc-131">You can implement transport agents based on these classes by using Visual Studio 2012.</span></span>
  
<span data-ttu-id="82ddc-132">Das Exchange 2013 Installationsprogramm installiert Assemblys, die für die Entwicklung von Transport-Agents verwendet werden, und registriert Sie im globaler Assemblycache (Global Assembly Cache, GAC).</span><span class="sxs-lookup"><span data-stu-id="82ddc-132">The Exchange 2013 installer installs assemblies that are used for transport agent development and registers them in the global assembly cache (GAC).</span></span> <span data-ttu-id="82ddc-133">Um mit der Implementierung eines Transport-Agents zu beginnen, erstellen Sie einen Verweis auf die Microsoft. Exchange. Data. Transport-Assembly in einem Klassenbibliotheksprojekt.</span><span class="sxs-lookup"><span data-stu-id="82ddc-133">To begin implementing a transport agent, create a reference to the Microsoft.Exchange.Data.Transport assembly in a class library project.</span></span>
  
## <a name="implementing-a-transport-agent"></a><span data-ttu-id="82ddc-134">Implementieren eines Transport-Agents</span><span class="sxs-lookup"><span data-stu-id="82ddc-134">Implementing a transport agent</span></span>
<span data-ttu-id="82ddc-135"><a name="bk_implementationExample"> </a></span><span class="sxs-lookup"><span data-stu-id="82ddc-135"><a name="bk_implementationExample"> </a></span></span>

<span data-ttu-id="82ddc-136">Das folgende Beispiel zeigt eine minimale Implementierung von Klassen, die von der [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) -und der [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) -Klasse abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="82ddc-136">The following example shows a minimal implementation of classes that derive from the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="82ddc-137">Wenn mehrere Transport-Agents installiert und für dasselbe Ereignis registriert wurden, werden alle Agents aufgerufen, selbst wenn ein Agent alle Empfänger aus einem e-Mail-Element entfernt.</span><span class="sxs-lookup"><span data-stu-id="82ddc-137">If multiple transport agents are installed and registered for the same event, all agents will be invoked, even if one agent removes all the recipients from a mail item.</span></span> <span data-ttu-id="82ddc-138">> um nicht behandelte Fehler oder unvorhersehbares Verhalten zu vermeiden, sollte der Transport-Agent Fälle behandeln, in denen die Empfängeranzahl für ein e-Mail-Element gleich NULL ist.</span><span class="sxs-lookup"><span data-stu-id="82ddc-138">> To avoid unhandled errors or unpredictable behavior, your transport agent should handle cases in which the recipient count on a mail item is equal to zero.</span></span> 
  
```cs
using System;
using System.Collections.Generic;
using System.Text;
using Microsoft.Exchange.Data.Transport;
using Microsoft.Exchange.Data.Transport.Smtp;
namespace MyAgents
{
    public sealed class MyAgentFactory : SmtpReceiveAgentFactory
    {
        public override SmtpReceiveAgent CreateAgent(SmtpServer server)
        {
            return new MyAgent();
        }
    }
    public class MyAgent : SmtpReceiveAgent
    {
        public MyAgent()
        {
            this.OnEndOfData += new EndOfDataEventHandler(MyEndOfDataHandler);
        }
        private void MyEndOfDataHandler (ReceiveMessageEventSource source, EndOfDataEventArgs e)
        {
            // The following line appends text to the subject of the message that caused the event.
            e.MailItem.Message.Subject += " - this text appended by MyAgent";
        }
    }
}
```

```vb
Imports System
Imports System.Collections.Generic
Imports System.Text
Imports Microsoft.Exchange.Data.Transport
Imports Microsoft.Exchange.Data.Transport.Smtp
Namespace MyAgents
    NotInheritable Class MyAgentFactory
        Inherits SmtpReceiveAgentFactory
        Public Overrides Function CreateAgent(ByVal server as SmtpServer) As SmtpReceiveAgent
            Return New MyAgent
        End Function
    End Class
    Public Class MyAgent
        Inherits SmtpReceiveAgent
        Private Sub MyEndOfDataHandler(ByVal source As ReceiveMessageEventSource, ByVal e As EndOfDataEventArgs) Handles Me.OnEndOfData
            ' The following line appends text to the subject of the message that caused the event.
            e.MailItem.Message.Subject &amp;= e.MailItem.Message.Subject + " - this text appended by MyAgent"
        End Sub
    End Class
End Namespace
```

## <a name="installing-and-enabling-an-agent"></a><span data-ttu-id="82ddc-139">Installieren und Aktivieren eines Agents</span><span class="sxs-lookup"><span data-stu-id="82ddc-139">Installing and enabling an agent</span></span>
<span data-ttu-id="82ddc-140"><a name="bk_InstallEnable"> </a></span><span class="sxs-lookup"><span data-stu-id="82ddc-140"><a name="bk_InstallEnable"> </a></span></span>

<span data-ttu-id="82ddc-141">Nachdem Sie den Agent in eine DLL kompiliert haben, müssen Sie den Agent auf Ihrem Exchange-Entwicklungsserver installieren und aktivieren.</span><span class="sxs-lookup"><span data-stu-id="82ddc-141">After you compile your agent to a DLL, you must install and enable the agent on your development Exchange server.</span></span> <span data-ttu-id="82ddc-142">Verwenden Sie im Exchange-Verwaltungsshell das Cmdlet [install-Transport Agent](https://technet.microsoft.com/library/aa997998.aspx) , um den Agent zu installieren, und das Cmdlet [enable-Transport Agent](https://technet.microsoft.com/library/bb124921.aspx) , um den Agent zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="82ddc-142">In the Exchange Management Shell, use the [Install-TransportAgent](https://technet.microsoft.com/library/aa997998.aspx) cmdlet to install your agent, and the [Enable-TransportAgent](https://technet.microsoft.com/library/bb124921.aspx) cmdlet to enable your agent.</span></span> <span data-ttu-id="82ddc-143">Informationen zur Verwendung des Exchange-Verwaltungsshell finden Sie unter [Exchange Server PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="82ddc-143">For information about how to use the Exchange Management Shell, see [Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).</span></span>
  
> [!CAUTION]
> <span data-ttu-id="82ddc-144">Transport-Agents haben Vollzugriff auf alle gefundenen E-Mails.</span><span class="sxs-lookup"><span data-stu-id="82ddc-144">Transport agents have full access to all email messages that they encounter.</span></span> <span data-ttu-id="82ddc-145">Exchange 2013 schränkt das Verhalten eines Transport-Agents nicht ein.</span><span class="sxs-lookup"><span data-stu-id="82ddc-145">Exchange 2013 does not restrict the behavior of a transport agent.</span></span> <span data-ttu-id="82ddc-146">Transport-Agents, die instabil sind oder Sicherheitsmängel enthalten, können sich auf die Stabilität und Sicherheit von Exchange 2013 auswirken.</span><span class="sxs-lookup"><span data-stu-id="82ddc-146">Transport agents that are unstable or that contain security flaws might affect the stability and security of Exchange 2013.</span></span> <span data-ttu-id="82ddc-147">Daher sollten Sie nur Transport-Agents installieren, die vollständig vertrauenswürdig sind und vollständig getestet wurden.</span><span class="sxs-lookup"><span data-stu-id="82ddc-147">Therefore, you should only install transport agents that you fully trust and that have been fully tested.</span></span> 
  
<span data-ttu-id="82ddc-148">Wenn Sie das Cmdlet **install-Transport Agent** verwenden, um einen Agent zu installieren, behält die Exchange-Verwaltungsshell eine Sperre für die Assembly bei.</span><span class="sxs-lookup"><span data-stu-id="82ddc-148">When you use the **Install-TransportAgent** cmdlet to install an agent, the Exchange Management Shell keeps a lock on the assembly.</span></span> <span data-ttu-id="82ddc-149">Wenn Sie die Sperre für die Assembly freigeben möchten, müssen Sie die Instanz der Exchange-Verwaltungsshell schließen, die Sie zum Installieren des Agents verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="82ddc-149">To release the lock on the assembly, you must close the instance of the Exchange Management Shell that you used to install the agent.</span></span> <span data-ttu-id="82ddc-150">Sie können die Assembly erst aktualisieren, wenn Sie die Sperre freigeben.</span><span class="sxs-lookup"><span data-stu-id="82ddc-150">You will be unable to update the assembly until you release the lock.</span></span> 
  
<span data-ttu-id="82ddc-151">Im folgenden Beispiel wird gezeigt, wie Sie mithilfe der Exchange-Verwaltungsshell einen Agent mit dem Namen myagent mithilfe einer von [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) namens myagents. MyAgentFactory abgeleiteten Klasse installieren und aktivieren.</span><span class="sxs-lookup"><span data-stu-id="82ddc-151">The following example shows how to use the Exchange Management Shell to install and enable an agent named MyAgent by using a class derived from [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) named MyAgents.MyAgentFactory.</span></span> 
  
 `Install-TransportAgent -Name "MyCustomAgent" -TransportAgentFactory "MyAgents.MyAgentFactory" -AssemblyPath "C:\myagents\MyAgent.dll"`
  
<span data-ttu-id="82ddc-152">In diesem Beispiel wird der Agent MyCustomAgent auf dem Server benannt, auf dem der Agent installiert ist.</span><span class="sxs-lookup"><span data-stu-id="82ddc-152">This example names the agent MyCustomAgent on the server on which the agent is installed.</span></span> <span data-ttu-id="82ddc-153">Im folgenden Beispiel wird gezeigt, wie der Agent mit dem Namen MyCustomAgent aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="82ddc-153">The following example shows how to enable the agent named MyCustomAgent.</span></span>
  
 `Enable-TransportAgent -Name "MyCustomAgent"`
  
<span data-ttu-id="82ddc-154">Um einen Transport-Agent im Front-End-Transport-Dienst auf einem Client Zugriffsserver zu verwalten, fügen Sie dem Befehl den folgenden Wert hinzu: `-TransportService FrontEnd` .</span><span class="sxs-lookup"><span data-stu-id="82ddc-154">To manage a transport agent in the Front End Transport service on a Client Access server, add the following value to the command:  `-TransportService FrontEnd`.</span></span> <span data-ttu-id="82ddc-155">Um beispielsweise die Transport-Agents im Front-End-Transport-Dienst anzuzeigen, führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="82ddc-155">For example, to view the transport agents in the Front End Transport service, run the following command.</span></span>
  
 `Get-TransportAgent -TransportService FrontEnd`
  
<span data-ttu-id="82ddc-156">Weitere Informationen zum Installieren, aktivieren und Verwalten Ihres Agents finden Sie unter [Manage Transport Agents](https://technet.microsoft.com/library/bb125175%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="82ddc-156">For more information about installing, enabling, and managing your agent, see [Manage Transport Agents](https://technet.microsoft.com/library/bb125175%28v=exchg.150%29.aspx).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="82ddc-157">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="82ddc-157">In this section</span></span>
<span data-ttu-id="82ddc-158"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="82ddc-158"><a name="bk_inthissection"> </a></span></span>

- [<span data-ttu-id="82ddc-159">Erstellen eines Routing Agent-Transport-Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="82ddc-159">Create a RoutingAgent transport agent for Exchange 2013</span></span>](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)
    
- [<span data-ttu-id="82ddc-160">Erstellen eines SmtpReceiveAgent-Transport-Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="82ddc-160">Create an SmtpReceiveAgent transport agent for Exchange 2013</span></span>](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)
    
- [<span data-ttu-id="82ddc-161">Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="82ddc-161">Create a DeliveryAgent transport agent for Exchange 2013</span></span>](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    
## <a name="see-also"></a><span data-ttu-id="82ddc-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82ddc-162">See also</span></span>

- [<span data-ttu-id="82ddc-163">Transport-Agent-Konzepte in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="82ddc-163">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)   
- [<span data-ttu-id="82ddc-164">Transport-Agent-Referenz für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="82ddc-164">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
    

