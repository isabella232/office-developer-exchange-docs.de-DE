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
# <a name="creating-transport-agents-for-exchange-2013"></a>Erstellen von Transport-Agents für Exchange 2013

Hier finden Sie Informationen zum Erstellen von benutzerdefinierten Transport-Agents für Exchange 2013 und die Systemanforderungen für das Erstellen eines benutzerdefinierten Agents.
  
**Gilt für:** Exchange Server 2013
  
Exchange Server 2013 enthält mehrere Transport-Agents, die Sie verwenden können, um Nachrichten zu verarbeiten. Die Assemblys, die im Lieferumfang von Exchange verwenden, können Sie Ihre eigenen benutzerdefinierten Agents zur Ausführung bestimmter Aufgaben entsprechend den Anforderungen Ihrer Organisation erstellen. Beispielsweise können Sie einen SmtpReceiveAgent Transport-Agent auf Intercept-Nachrichten, die über den SMTP-Protokoll und Prozess die Nachricht an das Format des Textkörpers vorformatierten Text enthalten konvertieren empfangen werden. Einen Transport-Agent RoutingAgent können Sie die Nachrichten protokolliert, die über den Server auf Route auf einen anderen Server übergeben. Sie können auch komplexere erstellen Features, die mehr als eine Art von Agent verwenden. Um eine antivirus-Agent zu erstellen, können Sie beispielsweise eine SmtpReceiveAgent und einen Agent RoutingAgent implementieren. Wenn Sie eine Komponente in Ihrem Netzwerk, die das SMTP-Protokoll nicht unterstützt verfügen, können Sie einen DeliveryAgent Transport-Agent, die Kommunikation zwischen dem Exchange-Server und Ihre externe Komponente zu behandeln. 
  
Dieser Artikel enthält Informationen zu den erforderlichen Komponenten für und Aufgaben beim Erstellen Ihrer eigenen Transport-Agents. Informationen zum Erstellen von bestimmten Transport-Agents finden Sie unter [erstellen einen RoutingAgent Transport-Agent für Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md), [Erstellen eines SmtpReceiveAgent Transport-Agents für Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)und erstellen einen Transport-Agent DeliveryAgent [für Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md).
  
## <a name="prerequisites-for-creating-a-transport-agent"></a>Voraussetzungen für die Erstellung von Transport-agent
<a name="bk_prerequisites"> </a>

Im folgenden sind die erforderlichen Komponenten, die Sie benötigen, um einen Transport-Agent zu implementieren:
  
- Einen Computer unter Exchange 2013, die der Front-End-Transport-Dienst auf einem Clientzugriffsserver oder Edge-Transport-Server oder den Transportdienst auf einem Postfachserver ausgeführt wird. Informationen über die Rolle Serverarchitektur in Exchange 2013 finden Sie unter [Transport-Agent Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md).
    
- Die folgenden Assemblys für die Transport-Agent-Klassen:
    
  - Microsoft.Exchange.Data.dll
    
  - Microsoft.Exchange.Data.Common.dll
    
  - Microsoft.Exchange.Transport.dll
    
- .NET Framework 4.5
    
Außerdem wird empfohlen, dass die Installation von Visual Studio 2012. Transport-Agents können Sie mithilfe von Visual Basic .NET oder Visual c# implementieren.
  
## <a name="referencing-the-assemblies"></a>Verweisen auf die Assemblys
<a name="bk_ReferenceAssemblies"> </a>

Exchange 2013 bietet eine Bibliothek mit Klassen, die die Erweiterung der Exchange-Transport-Verhalten zu unterstützen. Diese Klassen ist .NET Framework 4.5 erforderlich. Sie können Transport-Agents mithilfe von Visual Studio 2012 basierend auf diesen Klassen implementieren.
  
Der Exchange 2013-Installer installiert Assemblys, die für die Entwicklung von Transport-Agent verwendet werden und registriert diese im globalen Assemblycache (GAC). Um einen Transport-Agent implementieren zu beginnen, erstellen Sie einen Verweis auf die Assembly Microsoft.Exchange.Data.Transport in ein Klassenbibliotheksprojekt.
  
## <a name="implementing-a-transport-agent"></a>Implementieren einen Transport-agent
<a name="bk_implementationExample"> </a>

Das folgende Beispiel zeigt eine minimale Implementierung von Klassen, die von der [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) und [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) Klassen abgeleitet werden. 
  
> [!CAUTION]
> Wenn mehrere Transport-Agents installiert und für dasselbe Ereignis registriert sind, werden alle Agents aufgerufen werden, selbst wenn ein Agent alle Empfänger einer e-Mail-Element entfernt. >, Um nicht behandelte Fehler oder unvorhersehbares Verhalten zu vermeiden, sollten Transport-Agent Fällen behandeln, in denen der Empfänger wird auf ein e-Mail-Element gleich NULL ist. 
  
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

## <a name="installing-and-enabling-an-agent"></a>Installieren und aktivieren einen agent
<a name="bk_InstallEnable"> </a>

Nachdem Sie den Agent in eine DLL kompiliert haben, müssen Sie installieren und Aktivieren des-Agenten auf dem Entwicklungsserver Exchange. Verwenden Sie in der Exchange-Verwaltungsshell das Cmdlet [Install-TransportAgent](http://technet.microsoft.com/en-us/library/aa997998.aspx) So installieren Sie den Agent und das Cmdlet [Enable-TransportAgent](http://technet.microsoft.com/en-us/library/bb124921.aspx) , um Ihre Agent zu aktivieren. Informationen dazu, wie Sie mithilfe der Exchange-Verwaltungsshell finden Sie unter [Exchange Server-PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).
  
> [!CAUTION]
> Transport-Agents haben vollen Zugriff auf alle e-Mail-Nachrichten, mit denen sie arbeiten. Exchange 2013 schränkt das Verhalten eines Transport-Agents nicht ein. Transport-Agents, sind instabil oder Sicherheitsfehler enthalten, können sich auf die Stabilität und Sicherheit von Exchange 2013 auswirken. Aus diesem Grund sollten Sie nur installieren Transport-Agents, die Sie als vertrauenswürdig einstufen und, vollständig getestet wurden. 
  
Wenn Sie das Cmdlet **Install-TransportAgent** verwenden, um einen Agent installieren, behält die Exchange-Verwaltungsshell eine Sperre auf die Assembly. Um die Sperre für die Assembly, müssen Sie die Instanz von der Exchange-Verwaltungsshell schließen, die Sie zum Installieren des Agents verwendet. Sie können die Assembly aktualisieren, bis die Sperre aufheben. 
  
Im folgenden Beispiel wird veranschaulicht, wie mithilfe der Exchange-Verwaltungsshell zum Installieren und aktivieren einen Agent, der mit dem Namen MyAgent mithilfe einer von [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) mit dem Namen MyAgents.MyAgentFactory abgeleiteten Klasse. 
  
 `Install-TransportAgent -Name "MyCustomAgent" -TransportAgentFactory "MyAgents.MyAgentFactory" -AssemblyPath "C:\myagents\MyAgent.dll"`
  
In diesem Beispiel wird den Namen des MyCustomAgent-Agents auf dem Server, auf dem der Agent installiert ist. Im folgenden Beispiel wird gezeigt, wie den MyCustomAgent-Agent zu aktivieren.
  
 `Enable-TransportAgent -Name "MyCustomAgent"`
  
Um einen Transport-Agent im Front-End-Transport-Dienst auf einem Clientzugriffsserver zu verwalten, fügen Sie den folgenden Wert an den Befehl: `-TransportService FrontEnd`. Angenommen, um die Transport-Agents in der Front-End-Transport-Dienst anzuzeigen, führen Sie den folgenden Befehl an.
  
 `Get-TransportAgent -TransportService FrontEnd`
  
Weitere Informationen zum Installieren aktivieren und Verwalten des Agents finden Sie unter [Transport-Agents verwalten](http://technet.microsoft.com/en-us/library/bb125175%28v=exchg.150%29.aspx).
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [Erstellen eines RoutingAgent-Transport-Agents für Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)
    
- [Erstellen eines SmtpReceiveAgent Transport-Agents für Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)
    
- [Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    
## <a name="see-also"></a>Siehe auch

- [Transport-Agent Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)   
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)
    

