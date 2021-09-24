---
title: Erstellen eines SmtpReceiveAgent-Transport-Agents für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cdc7c462-74a7-49d6-95b2-155d783840e9
description: Erfahren Sie, wie Sie einen benutzerdefinierten SmtpReceiveAgent-Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
ms.openlocfilehash: a441f93113798c10421e9073e266c28fd87bca8d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513031"
---
# <a name="create-an-smtpreceiveagent-transport-agent-for-exchange-2013"></a>Erstellen eines SmtpReceiveAgent-Transport-Agents für Exchange 2013

Erfahren Sie, wie Sie einen benutzerdefinierten SmtpReceiveAgent-Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
  
**Gilt für:** Exchange Server 2013
  
Verwandte Codeausschnitte und Beispiel-Apps:

- [Exchange 2013: Erstellen eines Transport-Agents für die Textkonvertierung](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)
  
Mit den Klassen [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) und [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) können Sie das Verhalten des Front-End-Transportdiensts auf einem Clientzugriffsserver oder den Transportdienst auf einem Postfachserver erweitern. Sie können diese Klassen verwenden, um Transport-Agents zu implementieren, die darauf ausgelegt sind, auf Nachrichten zu reagieren, die in Ihrer Organisation eingehen. 
  
Die [Klassen SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) und [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) enthalten die ereignisse, die in der folgenden Tabelle aufgeführt sind. 
  
**Tabelle 1. SmtpReceiveAgent-Klassenereignisse**

|Document.SelectionChanged **-Ereignis**|**Beschreibung**|
|:-----|:-----|
|[OnAuthCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnAuthCommand.aspx) <br/> |Verwenden Sie dies, wenn ihr Agent Informationen benötigt, die nur im SMTP **AUTH-Befehl** bereitgestellt werden, z. B. ein Agent, der Versuche zur Übermittlung einer Nachricht basierend auf dem Typ der verwendeten Authentifizierungsmethode akzeptiert oder ablehnt.  <br/> |
|[OnConnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnConnect.aspx) <br/> |Verwenden Sie dies, wenn Ihr Agent Informationen benötigt, die nur bereitgestellt werden, wenn eine Verbindung über SMTP mit dem Front-End-Transportdienst geöffnet wird, z. B. ein Agent, der eine Aktion basierend auf der Adresse oder Domäne des SMTP-Remoteservers ausführt.  <br/> |
|[OnDataCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDataCommand.aspx) <br/> |Verwenden Sie dieses Ereignis, wenn Ihr Agent Informationen benötigt, die im **SMTP-DATENbefehl** angegeben sind.  <br/> |
|[OnDisconnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDisconnect.aspx) <br/> |Verwenden Sie dies, wenn Ihr Agent Informationen benötigt, die zum Zeitpunkt der Trennung verfügbar sind, z. B. das aktuelle Datum und die aktuelle Uhrzeit, um Zeitberechnungen durchzuführen.  <br/> |
|[OnEhloCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEhloCommand.aspx) <br/> |Verwenden Sie dies, wenn Ihr Agent Informationen benötigt, die im **SMTP-EHLO-Befehl** bereitgestellt werden. Beispielsweise, wenn Ihr Agent Nachrichten basierend auf der im **EHLO-Befehl** angegebenen Identität akzeptiert oder ablehnt.  <br/> |
|[OnEndOfAuthentication](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfAuthentication.aspx) <br/> |Verwenden Sie dies, wenn Ihr Agent Informationen benötigt, die verfügbar sind, nachdem der Remoteserver den Authentifizierungsprozess abgeschlossen hat. Beispielsweise für einen Agent, der eine Aktion für eine Nachricht basierend auf den Authentifizierungsinformationen durchführt, die vom REMOTE-SMTP-Server oder -Client bereitgestellt werden.  <br/> |
|[OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) <br/> |Verwenden Sie dies, wenn Ihr Agent eine Aktion basierend auf den in der Nachricht verfügbaren Daten ausführen muss. Dieses Ereignis wird nicht im Front-End-Transport-Dienst ausgelöst. Wenn Ihr Transport-Agent dieses Ereignis verwenden muss, müssen Sie es auf einem Postfachserver installieren.  <br/> |
|[OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) <br/> |Verwenden Sie dies, wenn ihr Agent eine Aktion basierend auf Informationen ausführen muss, die in den Kopfzeilen der gesendeten Nachricht verfügbar sind.  <br/> |
   
## <a name="creating-a-custom-smtpreceiveagent-transport-agent"></a>Erstellen eines benutzerdefinierten SmtpReceiveAgent-Transport-Agents

Im folgenden Verfahren wird beschrieben, wie Sie einen benutzerdefinierten SmtpReceiveAgent-Transport-Agent erstellen. 
  
### <a name="to-create-the-transport-agent"></a>So erstellen Sie den Transport-Agent

1. Fügen Sie Verweise auf die Namespaces hinzu.
    
   ```cs
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Smtp;
      using Microsoft.Exchange.Data.Transport.Email;
      using Microsoft.Exchange.Data.TextConverters;
  
   ```

   Sie finden diese Namespaces auf Ihrem Exchange 2013-Server. Wenn Sie einen Verweis auf diese Namespaces hinzufügen, haben Sie Zugriff auf die [SmtpReceiveAgent-Member](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) sowie auf andere Klassen, die im [Beispiel Exchange 2013: Erstellen eines Transport-Agent-Beispiels für die Textkonvertierung](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) verwendet werden. 
    
2. Implementieren Sie die abgeleitete Klasse für die [SmtpReceiveAgentFactory-Klasse.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) 
    
   ```cs
      public class BodyConversionFactory : SmtpReceiveAgentFactory
      {
          /// <summary>
          /// Create a new BodyConversion
          /// </summary>
          /// <param name="server">Exchange server</param>
          /// <returns>A new BodyConversion</returns>
          public override SmtpReceiveAgent CreateAgent(SmtpServer server)
          {
              return new BodyConversion();
          }
      }
  
   ```

   Dieser Code instanziiert die abgeleitete Klasse und überschreibt die **CreateAgent-Methode,** um eine Instanz des neuen benutzerdefinierten Agents zu erstellen. 
    
3. Definieren Sie Ihren Agent.
    
   ```cs
     public class BodyConversion : SmtpReceiveAgent
      {
          // Your custom code goes here
          /// <summary>
          /// The constructor registers an end of data event handler.
          /// </summary>
          public BodyConversion()
          {
              Debug.WriteLine("[BodyConversion] Agent constructor");
              this.OnEndOfData += new EndOfDataEventHandler(this.OnEndOfDataHandler);
          }
      }
  
   ```

   Nachdem Sie die Agentklasse definiert haben, können Sie Ihre benutzerdefinierten Funktionen hinzufügen. In diesem Beispiel wird das [OnEndOfData-Ereignis](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) an den benutzerdefinierten Ereignishandler umgeleitet. 
    
## <a name="see-also"></a>Siehe auch

- [Transport-Agent-Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)    
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)    
- [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
    

