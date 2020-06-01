---
title: Erstellen eines SmtpReceiveAgent-Transport-Agents für Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cdc7c462-74a7-49d6-95b2-155d783840e9
description: Erfahren Sie, wie Sie einen benutzerdefinierten SmtpReceiveAgent-Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
ms.openlocfilehash: 5ba021d02849ffc7e125029f0fd18ebf14c3f8da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459139"
---
# <a name="create-an-smtpreceiveagent-transport-agent-for-exchange-2013"></a>Erstellen eines SmtpReceiveAgent-Transport-Agents für Exchange 2013

Erfahren Sie, wie Sie einen benutzerdefinierten SmtpReceiveAgent-Transport-Agent für die Verwendung mit Exchange 2013 erstellen.
  
**Gilt für:** Exchange Server 2013
  
Zugehörige Codeausschnitte und Beispiel-apps:

- [Exchange 2013: Erstellen eines Transport-Agents für die Text Konvertierung](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)
  
Mit der [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) -und der [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) -Klasse können Sie das Verhalten des Front-End-Transportdiensts auf einem Client Zugriffsserver oder dem Transportdienst auf einem Postfachserver erweitern. Sie können diese Klassen verwenden, um Transport-Agents zu implementieren, die darauf ausgelegt sind, auf Nachrichten zu reagieren, wenn Sie in Ihrer Organisation eingehen. 
  
Die [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) -und [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) -Klassen umfassen die in der folgenden Tabelle aufgeführten Ereignisse. 
  
**Tabelle 1. Ereignisse der SmtpReceiveAgent-Klasse**

|**Event**|**Beschreibung**|
|:-----|:-----|
|[OnAuthCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnAuthCommand.aspx) <br/> |Verwenden Sie diese Methode, wenn Ihr Agent Informationen benötigt, die nur im SMTP- **Authentifizierungs** Befehl bereitgestellt werden, beispielsweise ein Agent, der versucht, eine Nachricht basierend auf dem Typ der verwendeten Authentifizierungsmethode zu übertragen oder abzulehnen.  <br/> |
|[OnConnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnConnect.aspx) <br/> |Wird verwendet, wenn Ihr Agent Informationen benötigt, die nur beim Öffnen einer Verbindung über SMTP für den Front-End-Transport-Dienst bereitgestellt werden, beispielsweise ein Agent, der eine Aktion basierend auf der Adresse oder Domäne des SMTP-Remoteservers ausführt.  <br/> |
|[OnDataCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDataCommand.aspx) <br/> |Verwenden Sie dieses Ereignis, wenn Ihr Agent Informationen benötigt, die im SMTP-Befehl **Data** bereitgestellt werden.  <br/> |
|[OnDisconnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDisconnect.aspx) <br/> |Verwenden Sie diese Aktion, wenn Ihr Agent Informationen benötigt, die zum Zeitpunkt der Verbindungstrennung zur Verfügung stehen, beispielsweise das aktuelle Datum und die Uhrzeit, um Zeitberechnungen durchzuführen.  <br/> |
|[OnEhloCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEhloCommand.aspx) <br/> |Verwenden Sie diese Funktion, wenn Ihr Agent Informationen benötigt, die im SMTP-Befehl **EHLO** bereitgestellt werden. Wenn Ihr Agent beispielsweise Nachrichten annimmt oder ablehnt, basierend auf der im Befehl **EHLO** angegebenen Identität.  <br/> |
|[OnEndOfAuthentication](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfAuthentication.aspx) <br/> |Verwenden Sie dieses Verfahren, wenn Ihr Agent Informationen benötigt, die nach Abschluss des Authentifizierungsprozesses durch den Remoteserver verfügbar sind. beispielsweise für einen Agent, der eine Aktion für eine Nachricht basierend auf den vom Remote-SMTP-Server oder-Client bereitgestellten Authentifizierungsinformationen ausführt.  <br/> |
|[OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) <br/> |Wird verwendet, wenn Ihr Agent eine Aktion basierend auf Daten ausführen muss, die in der Nachricht zur Verfügung stehen. Dieses Ereignis wird nicht für den Front-End-Transport-Dienst ausgelöst. Wenn Ihr Transport-Agent dieses Ereignis verwenden muss, müssen Sie es auf einem Postfachserver installieren.  <br/> |
|[OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) <br/> |Wird verwendet, wenn Ihr Agent eine Aktion basierend auf Informationen ausführen muss, die in den Kopfzeilen der übermittelten Nachricht verfügbar sind.  <br/> |
   
## <a name="creating-a-custom-smtpreceiveagent-transport-agent"></a>Erstellen eines benutzerdefinierten SmtpReceiveAgent-Transport-Agents

Im folgenden Verfahren wird beschrieben, wie ein benutzerdefinierter SmtpReceiveAgent-Transport-Agent erstellt wird. 
  
### <a name="to-create-the-transport-agent"></a>So erstellen Sie den Transport-Agent

1. Fügen Sie Verweise auf die Namespaces hinzu.
    
   ```cs
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Smtp;
      using Microsoft.Exchange.Data.Transport.Email;
      using Microsoft.Exchange.Data.TextConverters;
  
   ```

   Sie können diese Namespaces auf Ihrem Exchange 2013 Server finden. Wenn Sie einen Verweis auf diese Namespaces hinzufügen, haben Sie Zugriff auf die [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) -Member sowie auf andere Klassen, die im [Exchange 2013: Beispiel zum Erstellen eines Body Conversion Transport-Agents](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) verwendet werden. 
    
2. Implementieren Sie die abgeleitete Klasse für die [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) -Klasse. 
    
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

   Mit diesem Code wird die abgeleitete Klasse instanziiert und die **createagent** -Methode überschrieben, um eine Instanz des neuen benutzerdefinierten Agents zu erstellen. 
    
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

   Nachdem Sie die agentklasse definiert haben, können Sie Ihre benutzerdefinierte Funktionalität hinzufügen. In diesem Beispiel wird das [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) -Ereignis an Ihren benutzerdefinierten Ereignishandler umgeleitet. 
    
## <a name="see-also"></a>Siehe auch

- [Transport-Agent-Konzepte in Exchange 2013](transport-agent-concepts-in-exchange-2013.md)    
- [Transport-Agent-Referenz für Exchange 2013](transport-agent-reference-for-exchange-2013.md)    
- [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)    
- [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
    

