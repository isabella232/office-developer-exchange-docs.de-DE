---
title: Erstellen von Transport-Agents für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d291ab78-7cdd-4dbe-a5f4-9dc8e9650a33
description: Hier finden Sie Informationen zum Erstellen von benutzerdefinierten Transport-Agents für Exchange 2013 und zu den Systemanforderungen zum Erstellen eines benutzerdefinierten Agents.
ms.openlocfilehash: ea5ae1fab85fde781cb365a21b7a40ccd52955b3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520955"
---
# <a name="creating-transport-agents-for-exchange-2013"></a>Erstellen von Transport-Agents für Exchange 2013

Hier finden Sie Informationen zum Erstellen von benutzerdefinierten Transport-Agents für Exchange 2013 und zu den Systemanforderungen zum Erstellen eines benutzerdefinierten Agents.
  
**Gilt für:** Exchange Server 2013
  
Exchange Server 2013 enthält mehrere Transport-Agents, die Sie zum Verarbeiten von Nachrichten verwenden können. Mithilfe der Assemblys, die in Exchange enthalten sind, können Sie eigene benutzerdefinierte Agents erstellen, um bestimmte Aufgaben gemäß den Anforderungen Ihrer Organisation auszuführen. Sie können z. B. einen SmtpReceiveAgent-Transport-Agent verwenden, um Nachrichten abzufangen, die über das SMTP-Protokoll empfangen werden, und die Nachricht verarbeiten, um das Format des Textkörpers in vorformatierten Text zu konvertieren. Sie können einen RoutingAgent-Transport-Agent verwenden, um die Nachrichten zu protokollieren, die den Server auf dem Weg zu einem anderen Server passieren. Sie können auch komplexere Features erstellen, die mehr als einen Agenttyp verwenden. Um beispielsweise einen Antiviren-Agent zu erstellen, können Sie einen SmtpReceiveAgent und einen RoutingAgent-Agent implementieren. Wenn Sie in Ihrem Netzwerk über eine Komponente verfügen, die das SMTP-Protokoll nicht unterstützt, können Sie einen DeliveryAgent-Transport-Agent verwenden, um die Kommunikation zwischen Ihrem Exchange-Server und Ihrer externen Komponente zu verarbeiten. 
  
Dieser Artikel enthält Informationen zu den Voraussetzungen und Aufgaben, die bei der Erstellung Ihres eigenen Transport-Agents erforderlich sind. Informationen zum Erstellen bestimmter Transport-Agents finden Sie unter [Erstellen eines RoutingAgent-Transport-Agents für Exchange 2013,](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md) [Erstellen eines SmtpReceiveAgent-Transport-Agents für Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)und [Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013.](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
  
## <a name="prerequisites-for-creating-a-transport-agent"></a>Voraussetzungen für die Erstellung eines Transport-Agents
<a name="bk_prerequisites"> </a>

Im Folgenden sind die Voraussetzungen aufgeführt, die Sie zum Implementieren eines Transport-Agents benötigen:
  
- Ein Computer mit Exchange 2013, auf dem der Front-End-Transport-Dienst auf einem Clientzugriffs- oder Edge-Transport-Server oder der Transportdienst auf einem Postfachserver ausgeführt wird. Informationen zur Serverrollenarchitektur in Exchange 2013 finden Sie unter [Transport-Agent-Konzepte in Exchange 2013.](transport-agent-concepts-in-exchange-2013.md)
    
- Die folgenden Assemblys für die Transport-Agent-Klassen:
    
  - Microsoft.Exchange.Data.dll
    
  - Microsoft.Exchange.Data.Common.dll
    
  - Microsoft.Exchange.Transport.dll
    
- Die .NET Framework 4.5
    
Es wird auch empfohlen, Visual Studio 2012 zu installieren. Sie können Transport-Agents mithilfe von Visual Basic .NET oder C# implementieren.
  
## <a name="referencing-the-assemblies"></a>Verweisen auf die Assemblys
<a name="bk_ReferenceAssemblies"> </a>

Exchange 2013 bietet eine Bibliothek von Klassen, die die Erweiterung von Exchange Transportverhalten unterstützen. Diese Klassen erfordern die .NET Framework 4.5. Sie können Transport-Agents basierend auf diesen Klassen mit Visual Studio 2012 implementieren.
  
Das Installationsprogramm Exchange 2013 installiert Assemblys, die für die Entwicklung von Transport-Agents verwendet werden, und registriert sie im globalen Assemblycache (Global Assembly Cache, GAC). Um mit der Implementierung eines Transport-Agents zu beginnen, erstellen Sie einen Verweis auf Microsoft. Exchange. Data.Transport-Assembly in einem Klassenbibliotheksprojekt.
  
## <a name="implementing-a-transport-agent"></a>Implementieren eines Transport-Agents
<a name="bk_implementationExample"> </a>

Das folgende Beispiel zeigt eine minimale Implementierung von Klassen, die von den [Klassen SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) und [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) abgeleitet sind. 
  
> [!CAUTION]
> Wenn mehrere Transport-Agents installiert und für dasselbe Ereignis registriert sind, werden alle Agents aufgerufen, auch wenn ein Agent alle Empfänger aus einem E-Mail-Element entfernt. > Um unbehandelte Fehler oder unvorhersehbares Verhalten zu vermeiden, sollte Ihr Transport-Agent Fälle verarbeiten, in denen die Empfängeranzahl für ein E-Mail-Element gleich Null ist. 
  
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

## <a name="installing-and-enabling-an-agent"></a>Installieren und Aktivieren eines Agents
<a name="bk_InstallEnable"> </a>

Nachdem Sie den Agent in eine DLL kompiliert haben, müssen Sie den Agent auf dem Entwicklungsserver Exchange installieren und aktivieren. Verwenden Sie in der Exchange Verwaltungsshell das Cmdlet ["Install-TransportAgent",](https://technet.microsoft.com/library/aa997998.aspx) um den Agent zu installieren, und das Cmdlet ["Enable-TransportAgent",](https://technet.microsoft.com/library/bb124921.aspx) um den Agent zu aktivieren. Informationen zur Verwendung der Exchange-Verwaltungsshell finden Sie unter [Exchange Server PowerShell (Exchange-Verwaltungsshell).](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
  
> [!CAUTION]
> Transport-Agents haben Vollzugriff auf alle gefundenen E-Mails. Exchange 2013 schränkt das Verhalten eines Transport-Agents nicht ein. Transport-Agents, die instabil sind oder Sicherheitsfehler enthalten, können sich auf die Stabilität und Sicherheit von Exchange 2013 auswirken. Daher sollten Sie nur Transport-Agents installieren, denen Sie voll vertrauenswürdig sind und die vollständig getestet wurden. 
  
Wenn Sie das Cmdlet **"Install-TransportAgent"** zum Installieren eines Agents verwenden, behält die Exchange Verwaltungsshell eine Sperre für die Assembly bei. Um die Sperre für die Assembly aufzuheben, müssen Sie die Instanz der Exchange Verwaltungsshell schließen, die Sie zum Installieren des Agents verwendet haben. Sie können die Assembly erst aktualisieren, wenn Sie die Sperre aufgehoben haben. 
  
Das folgende Beispiel zeigt, wie Sie die Exchange-Verwaltungsshell verwenden, um einen Agent namens MyAgent mithilfe einer von [SmtpReceiveAgentFactory abgeleiteten](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) Klasse namens MyAgents.MyAgentFactory zu installieren und zu aktivieren. 
  
 `Install-TransportAgent -Name "MyCustomAgent" -TransportAgentFactory "MyAgents.MyAgentFactory" -AssemblyPath "C:\myagents\MyAgent.dll"`
  
In diesem Beispiel wird der Agent MyCustomAgent auf dem Server bezeichnet, auf dem der Agent installiert ist. Das folgende Beispiel zeigt, wie der Agent mit dem Namen MyCustomAgent aktiviert wird.
  
 `Enable-TransportAgent -Name "MyCustomAgent"`
  
Um einen Transport-Agent im Front-End-Transport-Dienst auf einem Clientzugriffsserver zu verwalten, fügen Sie dem Befehl den folgenden Wert hinzu:  `-TransportService FrontEnd` . Führen Sie beispielsweise den folgenden Befehl aus, um die Transport-Agents im Front-End-Transportdienst anzuzeigen.
  
 `Get-TransportAgent -TransportService FrontEnd`
  
Weitere Informationen zum Installieren, Aktivieren und Verwalten Ihres Agents finden Sie unter [Verwalten von Transport-Agents.](https://technet.microsoft.com/library/bb125175%28v=exchg.150%29.aspx)
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [Erstellen eines RoutingAgent-Transport-Agents für Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)
    
- [Erstellen eines SmtpReceiveAgent-Transport-Agents für Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)
    
- [Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    
## <a name="see-also"></a>Siehe auch

- [Transport-Agent-Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)   
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)
    

