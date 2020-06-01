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
# <a name="creating-transport-agents-for-exchange-2013"></a>Erstellen von Transport-Agents für Exchange 2013

Hier finden Sie Informationen zum Erstellen benutzerdefinierter Transport-Agents für Exchange 2013 und die Systemanforderungen zum Erstellen eines benutzerdefinierten Agents.
  
**Gilt für:** Exchange Server 2013
  
Exchange Server 2013 enthält mehrere Transport-Agents, die Sie zum Verarbeiten von Nachrichten verwenden können. Mithilfe der Assemblys, die mit Exchange geliefert werden, können Sie eigene benutzerdefinierte Agents erstellen, um bestimmte Aufgaben entsprechend den Anforderungen Ihrer Organisation auszuführen. Beispielsweise können Sie einen SmtpReceiveAgent-Transport-Agent zum Abfangen von Nachrichten verwenden, die über das SMTP-Protokoll empfangen werden, und die Nachricht verarbeiten, um das Format des Texts in vorformatierten Text zu konvertieren. Sie können einen Routing Agent-Transport-Agent verwenden, um die Nachrichten zu protokollieren, die den Server auf der Route an einen anderen Server durchlaufen. Sie können auch komplexere Features erstellen, die mehr als einen Agenttyp verwenden. Um beispielsweise einen Antivirus-Agent zu erstellen, können Sie ein SmtpReceiveAgent und einen Routing Agent-Agent implementieren. Wenn Sie über eine Komponente in Ihrem Netzwerk verfügen, die das SMTP-Protokoll nicht unterstützt, können Sie einen DeliveryAgent-Transport-Agent verwenden, um die Kommunikation zwischen Ihrem Exchange-Server und ihrer externen Komponente zu verarbeiten. 
  
Dieser Artikel enthält Informationen zu den Voraussetzungen für und Aufgaben beim Erstellen Ihres eigenen Transport-Agents. Informationen zum Erstellen bestimmter Transport-Agents finden Sie unter [Erstellen eines Routing Agent-Transport-Agents für Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md), [Erstellen eines SmtpReceiveAgent-Transport-Agents für Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)und [Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md).
  
## <a name="prerequisites-for-creating-a-transport-agent"></a>Voraussetzungen für die Erstellung eines Transport-Agents
<a name="bk_prerequisites"> </a>

Die folgenden Voraussetzungen müssen erfüllt sein, um einen Transport-Agent zu implementieren:
  
- Ein Computer mit Exchange 2013, der den Front-End-Transportdienst auf einem Client Zugriffs-oder Edge-Transport-Server ausführt, oder der Transport Dienst auf einem Postfachserver. Informationen zur Architektur der Serverrolle in Exchange 2013 finden Sie unter [Transport-Agent-Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md).
    
- Die folgenden Assemblys für die Transport-Agent-Klassen:
    
  - Microsoft. Exchange. Data. dll
    
  - Microsoft. Exchange. Data. Common. dll
    
  - Microsoft. Exchange. Transport. dll
    
- Die .NET Framework 4.5
    
Außerdem wird empfohlen, Visual Studio 2012 zu installieren. Sie können Transport-Agents implementieren, indem Sie entweder Visual Basic .net oder C# verwenden.
  
## <a name="referencing-the-assemblies"></a>Verweisen auf die Assemblys
<a name="bk_ReferenceAssemblies"> </a>

Exchange 2013 enthält eine Bibliothek mit Klassen, die die Erweiterung des Exchange-Transportverhaltens unterstützen. Für diese Klassen ist die .NET Framework 4.5 erforderlich. Sie können Transport-Agents basierend auf diesen Klassen mithilfe von Visual Studio 2012 implementieren.
  
Das Exchange 2013 Installationsprogramm installiert Assemblys, die für die Entwicklung von Transport-Agents verwendet werden, und registriert Sie im globaler Assemblycache (Global Assembly Cache, GAC). Um mit der Implementierung eines Transport-Agents zu beginnen, erstellen Sie einen Verweis auf die Microsoft. Exchange. Data. Transport-Assembly in einem Klassenbibliotheksprojekt.
  
## <a name="implementing-a-transport-agent"></a>Implementieren eines Transport-Agents
<a name="bk_implementationExample"> </a>

Das folgende Beispiel zeigt eine minimale Implementierung von Klassen, die von der [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) -und der [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) -Klasse abgeleitet werden. 
  
> [!CAUTION]
> Wenn mehrere Transport-Agents installiert und für dasselbe Ereignis registriert wurden, werden alle Agents aufgerufen, selbst wenn ein Agent alle Empfänger aus einem e-Mail-Element entfernt. > um nicht behandelte Fehler oder unvorhersehbares Verhalten zu vermeiden, sollte der Transport-Agent Fälle behandeln, in denen die Empfängeranzahl für ein e-Mail-Element gleich NULL ist. 
  
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

Nachdem Sie den Agent in eine DLL kompiliert haben, müssen Sie den Agent auf Ihrem Exchange-Entwicklungsserver installieren und aktivieren. Verwenden Sie im Exchange-Verwaltungsshell das Cmdlet [install-Transport Agent](https://technet.microsoft.com/library/aa997998.aspx) , um den Agent zu installieren, und das Cmdlet [enable-Transport Agent](https://technet.microsoft.com/library/bb124921.aspx) , um den Agent zu aktivieren. Informationen zur Verwendung des Exchange-Verwaltungsshell finden Sie unter [Exchange Server PowerShell (Exchange-Verwaltungsshell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).
  
> [!CAUTION]
> Transport-Agents haben Vollzugriff auf alle gefundenen E-Mails. Exchange 2013 schränkt das Verhalten eines Transport-Agents nicht ein. Transport-Agents, die instabil sind oder Sicherheitsmängel enthalten, können sich auf die Stabilität und Sicherheit von Exchange 2013 auswirken. Daher sollten Sie nur Transport-Agents installieren, die vollständig vertrauenswürdig sind und vollständig getestet wurden. 
  
Wenn Sie das Cmdlet **install-Transport Agent** verwenden, um einen Agent zu installieren, behält die Exchange-Verwaltungsshell eine Sperre für die Assembly bei. Wenn Sie die Sperre für die Assembly freigeben möchten, müssen Sie die Instanz der Exchange-Verwaltungsshell schließen, die Sie zum Installieren des Agents verwendet haben. Sie können die Assembly erst aktualisieren, wenn Sie die Sperre freigeben. 
  
Im folgenden Beispiel wird gezeigt, wie Sie mithilfe der Exchange-Verwaltungsshell einen Agent mit dem Namen myagent mithilfe einer von [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) namens myagents. MyAgentFactory abgeleiteten Klasse installieren und aktivieren. 
  
 `Install-TransportAgent -Name "MyCustomAgent" -TransportAgentFactory "MyAgents.MyAgentFactory" -AssemblyPath "C:\myagents\MyAgent.dll"`
  
In diesem Beispiel wird der Agent MyCustomAgent auf dem Server benannt, auf dem der Agent installiert ist. Im folgenden Beispiel wird gezeigt, wie der Agent mit dem Namen MyCustomAgent aktiviert wird.
  
 `Enable-TransportAgent -Name "MyCustomAgent"`
  
Um einen Transport-Agent im Front-End-Transport-Dienst auf einem Client Zugriffsserver zu verwalten, fügen Sie dem Befehl den folgenden Wert hinzu: `-TransportService FrontEnd` . Um beispielsweise die Transport-Agents im Front-End-Transport-Dienst anzuzeigen, führen Sie den folgenden Befehl aus.
  
 `Get-TransportAgent -TransportService FrontEnd`
  
Weitere Informationen zum Installieren, aktivieren und Verwalten Ihres Agents finden Sie unter [Manage Transport Agents](https://technet.microsoft.com/library/bb125175%28v=exchg.150%29.aspx).
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts
<a name="bk_inthissection"> </a>

- [Erstellen eines Routing Agent-Transport-Agents für Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)
    
- [Erstellen eines SmtpReceiveAgent-Transport-Agents für Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)
    
- [Erstellen eines DeliveryAgent-Transport-Agents für Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    
## <a name="see-also"></a>Siehe auch

- [Transport-Agent-Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)   
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)
    

