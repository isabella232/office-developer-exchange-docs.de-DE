---
title: Erstellen von Transport-Agents für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d291ab78-7cdd-4dbe-a5f4-9dc8e9650a33
description: Hier finden Sie Informationen zum Erstellen von benutzerdefinierten Transport-Agents für Exchange 2013 und die Systemanforderungen für das Erstellen eines benutzerdefinierten Agents.
ms.openlocfilehash: 6146e37c44441bed1d30d08f71ede255dba26440
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757177"
---
# <a name="creating-transport-agents-for-exchange-2013"></a><span data-ttu-id="f4d16-103">Erstellen von Transport-Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="f4d16-103">Creating transport agents for Exchange 2013</span></span>

<span data-ttu-id="f4d16-104">Hier finden Sie Informationen zum Erstellen von benutzerdefinierten Transport-Agents für Exchange 2013 und die Systemanforderungen für das Erstellen eines benutzerdefinierten Agents.</span><span class="sxs-lookup"><span data-stu-id="f4d16-104">Find information about how to create custom transport agents for Exchange 2013, and the system requirements for creating a custom agent.</span></span>
  
<span data-ttu-id="f4d16-105">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="f4d16-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="f4d16-106">Exchange Server 2013 enthält mehrere Transport-Agents, die Sie verwenden können, um Nachrichten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f4d16-106">Exchange Server 2013 includes several transport agents that you can use to process messages.</span></span> <span data-ttu-id="f4d16-107">Die Assemblys, die im Lieferumfang von Exchange verwenden, können Sie Ihre eigenen benutzerdefinierten Agents zur Ausführung bestimmter Aufgaben entsprechend den Anforderungen Ihrer Organisation erstellen.</span><span class="sxs-lookup"><span data-stu-id="f4d16-107">By using the assemblies that come with Exchange, you can create your own custom agents to perform specific tasks according to the needs of your organization.</span></span> <span data-ttu-id="f4d16-108">Beispielsweise können Sie einen SmtpReceiveAgent Transport-Agent auf Intercept-Nachrichten, die über den SMTP-Protokoll und Prozess die Nachricht an das Format des Textkörpers vorformatierten Text enthalten konvertieren empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="f4d16-108">For example, you can use an SmtpReceiveAgent transport agent to intercept messages that are received via the SMTP protocol and process the message to convert the format of the body to contain preformatted text.</span></span> <span data-ttu-id="f4d16-109">Einen Transport-Agent RoutingAgent können Sie die Nachrichten protokolliert, die über den Server auf Route auf einen anderen Server übergeben.</span><span class="sxs-lookup"><span data-stu-id="f4d16-109">You can use a RoutingAgent transport agent to log the messages that pass through the server on route to another server.</span></span> <span data-ttu-id="f4d16-110">Sie können auch komplexere erstellen Features, die mehr als eine Art von Agent verwenden.</span><span class="sxs-lookup"><span data-stu-id="f4d16-110">You can also create more complex features that make use of more than one type of agent.</span></span> <span data-ttu-id="f4d16-111">Um eine antivirus-Agent zu erstellen, können Sie beispielsweise eine SmtpReceiveAgent und einen Agent RoutingAgent implementieren.</span><span class="sxs-lookup"><span data-stu-id="f4d16-111">For example, to create an antivirus agent, you can implement an SmtpReceiveAgent and a RoutingAgent agent.</span></span> <span data-ttu-id="f4d16-112">Wenn Sie eine Komponente in Ihrem Netzwerk, die das SMTP-Protokoll nicht unterstützt verfügen, können Sie einen DeliveryAgent Transport-Agent, die Kommunikation zwischen dem Exchange-Server und Ihre externe Komponente zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="f4d16-112">If you have a component on your network that does not support the SMTP protocol, you can use a DeliveryAgent transport agent to handle the communication between your Exchange server and your external component.</span></span> 
  
<span data-ttu-id="f4d16-113">Dieser Artikel enthält Informationen zu den erforderlichen Komponenten für und Aufgaben beim Erstellen Ihrer eigenen Transport-Agents.</span><span class="sxs-lookup"><span data-stu-id="f4d16-113">This article provides information about the prerequisites for and tasks involved in creating your own transport agent.</span></span> <span data-ttu-id="f4d16-114">Informationen zum Erstellen von bestimmten Transport-Agents finden Sie unter [erstellen einen RoutingAgent Transport-Agent für Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md), [Erstellen eines SmtpReceiveAgent Transport-Agents für Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)und erstellen einen Transport-Agent DeliveryAgent [für Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md).</span><span class="sxs-lookup"><span data-stu-id="f4d16-114">For information about creating specific transport agents, see [Create a RoutingAgent transport agent for Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md), [Create an SmtpReceiveAgent transport agent for Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md), and [Create a DeliveryAgent transport agent for Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md).</span></span>
  
## <a name="prerequisites-for-creating-a-transport-agent"></a><span data-ttu-id="f4d16-115">Voraussetzungen für die Erstellung von Transport-agent</span><span class="sxs-lookup"><span data-stu-id="f4d16-115">Prerequisites for creating a transport agent</span></span>
<span data-ttu-id="f4d16-116"><a name="bk_prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="f4d16-116"></span></span>

<span data-ttu-id="f4d16-117">Im folgenden sind die erforderlichen Komponenten, die Sie benötigen, um einen Transport-Agent zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="f4d16-117">The following are the prerequisites that you need in order to implement a transport agent:</span></span>
  
- <span data-ttu-id="f4d16-118">Einen Computer unter Exchange 2013, die der Front-End-Transport-Dienst auf einem Clientzugriffsserver oder Edge-Transport-Server oder den Transportdienst auf einem Postfachserver ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4d16-118">A computer running Exchange 2013 that is running the Front End Transport service on a Client Access or Edge Transport server, or the Transport service on a Mailbox server.</span></span> <span data-ttu-id="f4d16-119">Informationen über die Rolle Serverarchitektur in Exchange 2013 finden Sie unter [Transport-Agent Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md).</span><span class="sxs-lookup"><span data-stu-id="f4d16-119">For information about the server role architecture in Exchange 2013, see [Transport agent concepts in Exchange 2013](transport-agent-concepts-in-exchange-2013.md).</span></span>
    
- <span data-ttu-id="f4d16-120">Die folgenden Assemblys für die Transport-Agent-Klassen:</span><span class="sxs-lookup"><span data-stu-id="f4d16-120">The following assemblies for the transport agent classes:</span></span>
    
  - <span data-ttu-id="f4d16-121">Microsoft.Exchange.Data.dll</span><span class="sxs-lookup"><span data-stu-id="f4d16-121">Microsoft.Exchange.Data.dll</span></span>
    
  - <span data-ttu-id="f4d16-122">Microsoft.Exchange.Data.Common.dll</span><span class="sxs-lookup"><span data-stu-id="f4d16-122">Microsoft.Exchange.Data.Common.dll</span></span>
    
  - <span data-ttu-id="f4d16-123">Microsoft.Exchange.Transport.dll</span><span class="sxs-lookup"><span data-stu-id="f4d16-123">Microsoft.Exchange.Transport.dll</span></span>
    
- <span data-ttu-id="f4d16-124">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="f4d16-124">The .NET Framework 4.5</span></span>
    
<span data-ttu-id="f4d16-125">Außerdem wird empfohlen, dass die Installation von Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="f4d16-125">We also recommend that you install Visual Studio 2012.</span></span> <span data-ttu-id="f4d16-126">Transport-Agents können Sie mithilfe von Visual Basic .NET oder Visual c# implementieren.</span><span class="sxs-lookup"><span data-stu-id="f4d16-126">You can implement transport agents by using either Visual Basic .NET or C#.</span></span>
  
## <a name="referencing-the-assemblies"></a><span data-ttu-id="f4d16-127">Verweisen auf die Assemblys</span><span class="sxs-lookup"><span data-stu-id="f4d16-127">Referencing the assemblies</span></span>
<span data-ttu-id="f4d16-128"><a name="bk_ReferenceAssemblies"> </a></span><span class="sxs-lookup"><span data-stu-id="f4d16-128"></span></span>

<span data-ttu-id="f4d16-129">Exchange 2013 bietet eine Bibliothek mit Klassen, die die Erweiterung der Exchange-Transport-Verhalten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f4d16-129">Exchange 2013 provides a library of classes that support the extension of Exchange transport behavior.</span></span> <span data-ttu-id="f4d16-130">Diese Klassen ist .NET Framework 4.5 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f4d16-130">These classes require the .NET Framework 4.5.</span></span> <span data-ttu-id="f4d16-131">Sie können Transport-Agents mithilfe von Visual Studio 2012 basierend auf diesen Klassen implementieren.</span><span class="sxs-lookup"><span data-stu-id="f4d16-131">You can implement transport agents based on these classes by using Visual Studio 2012.</span></span>
  
<span data-ttu-id="f4d16-132">Der Exchange 2013-Installer installiert Assemblys, die für die Entwicklung von Transport-Agent verwendet werden und registriert diese im globalen Assemblycache (GAC).</span><span class="sxs-lookup"><span data-stu-id="f4d16-132">The Exchange 2013 installer installs assemblies that are used for transport agent development and registers them in the global assembly cache (GAC).</span></span> <span data-ttu-id="f4d16-133">Um einen Transport-Agent implementieren zu beginnen, erstellen Sie einen Verweis auf die Assembly Microsoft.Exchange.Data.Transport in ein Klassenbibliotheksprojekt.</span><span class="sxs-lookup"><span data-stu-id="f4d16-133">To begin implementing a transport agent, create a reference to the Microsoft.Exchange.Data.Transport assembly in a class library project.</span></span>
  
## <a name="implementing-a-transport-agent"></a><span data-ttu-id="f4d16-134">Implementieren einen Transport-agent</span><span class="sxs-lookup"><span data-stu-id="f4d16-134">Implementing a transport agent</span></span>
<span data-ttu-id="f4d16-135"><a name="bk_implementationExample"> </a></span><span class="sxs-lookup"><span data-stu-id="f4d16-135"></span></span>

<span data-ttu-id="f4d16-136">Das folgende Beispiel zeigt eine minimale Implementierung von Klassen, die von der [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) und [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) Klassen abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="f4d16-136">The following example shows a minimal implementation of classes that derive from the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="f4d16-137">Wenn mehrere Transport-Agents installiert und für dasselbe Ereignis registriert sind, werden alle Agents aufgerufen werden, selbst wenn ein Agent alle Empfänger einer e-Mail-Element entfernt.</span><span class="sxs-lookup"><span data-stu-id="f4d16-137">If multiple transport agents are installed and registered for the same event, all agents will be invoked, even if one agent removes all the recipients from a mail item.</span></span> <span data-ttu-id="f4d16-138">>, Um nicht behandelte Fehler oder unvorhersehbares Verhalten zu vermeiden, sollten Transport-Agent Fällen behandeln, in denen der Empfänger wird auf ein e-Mail-Element gleich NULL ist.</span><span class="sxs-lookup"><span data-stu-id="f4d16-138">> To avoid unhandled errors or unpredictable behavior, your transport agent should handle cases in which the recipient count on a mail item is equal to zero.</span></span> 
  
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

## <a name="installing-and-enabling-an-agent"></a><span data-ttu-id="f4d16-139">Installieren und aktivieren einen agent</span><span class="sxs-lookup"><span data-stu-id="f4d16-139">Installing and enabling an agent</span></span>
<span data-ttu-id="f4d16-140"><a name="bk_InstallEnable"> </a></span><span class="sxs-lookup"><span data-stu-id="f4d16-140"></span></span>

<span data-ttu-id="f4d16-141">Nachdem Sie den Agent in eine DLL kompiliert haben, müssen Sie installieren und Aktivieren des-Agenten auf dem Entwicklungsserver Exchange.</span><span class="sxs-lookup"><span data-stu-id="f4d16-141">After you compile your agent to a DLL, you must install and enable the agent on your development Exchange server.</span></span> <span data-ttu-id="f4d16-142">Verwenden Sie in der Exchange-Verwaltungsshell das Cmdlet [Install-TransportAgent](http://technet.microsoft.com/de-de/library/aa997998.aspx) So installieren Sie den Agent und das Cmdlet [Enable-TransportAgent](http://technet.microsoft.com/de-de/library/bb124921.aspx) , um Ihre Agent zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f4d16-142">In the Exchange Management Shell, use the [Install-TransportAgent](http://technet.microsoft.com/de-de/library/aa997998.aspx) cmdlet to install your agent, and the [Enable-TransportAgent](http://technet.microsoft.com/de-de/library/bb124921.aspx) cmdlet to enable your agent.</span></span> <span data-ttu-id="f4d16-143">Informationen dazu, wie Sie mithilfe der Exchange-Verwaltungsshell finden Sie unter [Exchange Server-PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/de-de/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="f4d16-143">For information about how to use the Exchange Management Shell, see [Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/de-de/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).</span></span>
  
> [!CAUTION]
> <span data-ttu-id="f4d16-144">Transport-Agents haben vollen Zugriff auf alle e-Mail-Nachrichten, mit denen sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f4d16-144">Transport agents have full access to all email messages that they encounter.</span></span> <span data-ttu-id="f4d16-145">Exchange 2013 schränkt das Verhalten eines Transport-Agents nicht ein.</span><span class="sxs-lookup"><span data-stu-id="f4d16-145">Exchange 2013 does not restrict the behavior of a transport agent.</span></span> <span data-ttu-id="f4d16-146">Transport-Agents, sind instabil oder Sicherheitsfehler enthalten, können sich auf die Stabilität und Sicherheit von Exchange 2013 auswirken.</span><span class="sxs-lookup"><span data-stu-id="f4d16-146">Transport agents that are unstable or that contain security flaws might affect the stability and security of Exchange 2013.</span></span> <span data-ttu-id="f4d16-147">Aus diesem Grund sollten Sie nur installieren Transport-Agents, die Sie als vertrauenswürdig einstufen und, vollständig getestet wurden.</span><span class="sxs-lookup"><span data-stu-id="f4d16-147">Therefore, you should only install transport agents that you fully trust and that have been fully tested.</span></span> 
  
<span data-ttu-id="f4d16-148">Wenn Sie das Cmdlet **Install-TransportAgent** verwenden, um einen Agent installieren, behält die Exchange-Verwaltungsshell eine Sperre auf die Assembly.</span><span class="sxs-lookup"><span data-stu-id="f4d16-148">When you use the **Install-TransportAgent** cmdlet to install an agent, the Exchange Management Shell keeps a lock on the assembly.</span></span> <span data-ttu-id="f4d16-149">Um die Sperre für die Assembly, müssen Sie die Instanz von der Exchange-Verwaltungsshell schließen, die Sie zum Installieren des Agents verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4d16-149">To release the lock on the assembly, you must close the instance of the Exchange Management Shell that you used to install the agent.</span></span> <span data-ttu-id="f4d16-150">Sie können die Assembly aktualisieren, bis die Sperre aufheben.</span><span class="sxs-lookup"><span data-stu-id="f4d16-150">You will be unable to update the assembly until you release the lock.</span></span> 
  
<span data-ttu-id="f4d16-151">Im folgenden Beispiel wird veranschaulicht, wie mithilfe der Exchange-Verwaltungsshell zum Installieren und aktivieren einen Agent, der mit dem Namen MyAgent mithilfe einer von [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) mit dem Namen MyAgents.MyAgentFactory abgeleiteten Klasse.</span><span class="sxs-lookup"><span data-stu-id="f4d16-151">The following example shows how to use the Exchange Management Shell to install and enable an agent named MyAgent by using a class derived from [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) named MyAgents.MyAgentFactory.</span></span> 
  
 `Install-TransportAgent -Name "MyCustomAgent" -TransportAgentFactory "MyAgents.MyAgentFactory" -AssemblyPath "C:\myagents\MyAgent.dll"`
  
<span data-ttu-id="f4d16-152">In diesem Beispiel wird den Namen des MyCustomAgent-Agents auf dem Server, auf dem der Agent installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f4d16-152">This example names the agent MyCustomAgent on the server on which the agent is installed.</span></span> <span data-ttu-id="f4d16-153">Im folgenden Beispiel wird gezeigt, wie den MyCustomAgent-Agent zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f4d16-153">The following example shows how to enable the agent named MyCustomAgent.</span></span>
  
 `Enable-TransportAgent -Name "MyCustomAgent"`
  
<span data-ttu-id="f4d16-154">Um einen Transport-Agent im Front-End-Transport-Dienst auf einem Clientzugriffsserver zu verwalten, fügen Sie den folgenden Wert an den Befehl: `-TransportService FrontEnd`.</span><span class="sxs-lookup"><span data-stu-id="f4d16-154">To manage a transport agent in the Front End Transport service on a Client Access server, add the following value to the command:  `-TransportService FrontEnd`.</span></span> <span data-ttu-id="f4d16-155">Angenommen, um die Transport-Agents in der Front-End-Transport-Dienst anzuzeigen, führen Sie den folgenden Befehl an.</span><span class="sxs-lookup"><span data-stu-id="f4d16-155">For example, to view the transport agents in the Front End Transport service, run the following command.</span></span>
  
 `Get-TransportAgent -TransportService FrontEnd`
  
<span data-ttu-id="f4d16-156">Weitere Informationen zum Installieren aktivieren und Verwalten des Agents finden Sie unter [Transport-Agents verwalten](http://technet.microsoft.com/de-de/library/bb125175%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f4d16-156">For more information about installing, enabling, and managing your agent, see [Manage Transport Agents](http://technet.microsoft.com/de-de/library/bb125175%28v=exchg.150%29.aspx).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="f4d16-157">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="f4d16-157">In this section</span></span>
<span data-ttu-id="f4d16-158"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="f4d16-158"></span></span>

- [<span data-ttu-id="f4d16-159">Erstellen eines RoutingAgent-Transport-Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="f4d16-159">Create a RoutingAgent transport agent for Exchange 2013</span></span>](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)
    
- [<span data-ttu-id="f4d16-160">Erstellen eines SmtpReceiveAgent Transport-Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="f4d16-160">Create an SmtpReceiveAgent transport agent for Exchange 2013</span></span>](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)
    
- [<span data-ttu-id="f4d16-161">Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="f4d16-161">Create a DeliveryAgent transport agent for Exchange 2013</span></span>](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    
## <a name="see-also"></a><span data-ttu-id="f4d16-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4d16-162">See also</span></span>

- [<span data-ttu-id="f4d16-163">Transport-Agent Konzepte in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="f4d16-163">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)   
- [<span data-ttu-id="f4d16-164">Transport-Agent-Referenz für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="f4d16-164">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
    

