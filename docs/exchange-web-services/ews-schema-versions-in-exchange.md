---
title: EWS-Schemaversionen in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d1ab6f9c-ea91-4022-830d-7f7b759e3935
description: Informationen Sie zu den EWS, Schema und Entwerfen Sie die Anwendung für die Arbeit mit es als auch die Features, die mit jeder Schemaversion verfügbar sind und wie das Schema auf die Exchange-Version-Dienst bezieht.
ms.openlocfilehash: dd8e85547666ba0bf3a1a38775260268594f2a8b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756844"
---
# <a name="ews-schema-versions-in-exchange"></a>EWS-Schemaversionen in Exchange

Informationen Sie zu den EWS, Schema und Entwerfen Sie die Anwendung für die Arbeit mit es als auch die Features, die mit jeder Schemaversion verfügbar sind und wie das Schema auf die Exchange-Version-Dienst bezieht.
  
Das EWS-Schema definiert die Datenstrukturen, die an gesendet und von Exchange zurückgegeben werden können. Jede neue Version von Exchange, die eine erhebliche Änderung an EWS-Funktionalität enthält, wird ein neues Schema enthalten. EWS und die EWS-Schema sind beide nach hinten, und in einigen Fällen forward kompatible - Clientanwendungen, die mit früheren Versionen von Exchange-Webdienste entwickelt funktioniert, in den meisten Fällen späteren Versionen von Exchange-Webdienste, und Anwendungen, die von späteren von Exchange-Webdienste Versionen ist funktionsfähig, wenn die gleiche Funktionalität wurde in einer früheren Version enthalten. In diesem Artikel helfen Ihnen das Verständnis der Rolle des EWS-Schemas, Schema Versioning, die Beziehung zwischen dem Schema und die Version Service Funktionsweise und Ihre Anwendung das Schema EWS entwickelt entwerfen. 
  
## <a name="role-of-the-ews-schema"></a>Rolle des EWS-Schemas

Das Schema EWS bewirkt Folgendes:
  
- Definiert die Featuregruppe, die an einen Client verfügbar ist. Ein Client kann die Liste der unterstützten Schemaversionen mithilfe des SOAP- [AutoErmittlungsdienst](autodiscover-for-exchange.md)abrufen. Der Client kann dann darauf zugreifen können, welche Features von bestimmen, da jede Schemaversion eine [EWS-Funktion festgelegt stellt](ews-schema-versions-in-exchange.md#bk_features). Jede neues Schema freigegeben für EWS enthält Entitäten Schema aus der vorherigen Version plus die Schemadefinitionen für neue Funktionen. Auf diese Weise unterstützt EWS-Anwendungen, die als eine frühere Version von Exchange-Webdienste Ziel.
    
- Enthält eine allgemeine Beschreibung des Vertrags API. Dieser Vertrag können Sie um die Datenstrukturen zu ermitteln, die an gesendet und Empfangen von Exchange werden kann.
    
- Bietet einen Mechanismus Versioning für zusenden. Der Exchange-Server enthält alle unterstützten EWS-Schemaversionen in dem virtuellen Verzeichnis. 
    
## <a name="designing-your-application-with-schema-version-in-mind"></a>Entwerfen der Anwendung mit der Schemaversion Beachten

Bedenken Sie folgende Punkte beachten Sie, wie Sie die Anwendung zum Arbeiten mit verschiedenen Versionen des EWS-Schemas entwerfen:
  
- Aktivieren Sie/deaktivieren Funktionen basierend auf die Schemaversion. Sie benötigen Clientfunktionen auf die Schemaversion und in einigen Fällen auf die Version des Diensts zuordnen möchten. Das folgende Beispiel gibt die Version des Schemas und der Dienst einen [PropertySet](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) anhand zurück. 
    
  ```cs
  private static PropertySet InitPropertySetByVersion(ExchangeService service)
  {
      PropertySet props;
      // The schema version to target to access the NormalizedBody property 
      // is Exchange2013 or later. The server version to target to access the 
      // NormalizedBody property on an email is 15 or later, which 
      // equates to Exchange 2013.
      if (service.RequestedServerVersion >= ExchangeVersion.Exchange2013 &amp;&amp;
          service.ServerInfo.MajorVersion >= 15)
      {
          props = new PropertySet(EmailMessageSchema.NormalizedBody);
      }
      else
      {
          props = new PropertySet(EmailMessageSchema.Body);
      }
      return props;
  }
  ```

- Version Ihrer Anforderungen mit der ältesten Version von der EWS-Schema, das die Funktionalität unterstützt, die Sie verwenden möchten. Dadurch wird den Client für eine größere Anzahl von potenziellen Exchange-Server gelten. Dies ist weniger wichtig, wenn Sie einen Server in Ihrem Unternehmen als Ziel eine Line-of-Business-Anwendung entwickeln, aber es ist sehr wichtig, wenn Sie eine Anwendung für eine größere Zielgruppe Exchange erstellen.
    
## <a name="features-by-schema-version"></a>Features von Schemaversion
<a name="bk_features"> </a>

Die Schemaversionen, die an einen Client verfügbar sind, werden **ExchangeVersionType** im einfachen Typ befindet sich im Schema types.xsd identifiziert. Die **ExchangeVersionType** wird vom [RequestServerVersion](http://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx) -Element implementiert. Das **RequestServerVersion** -Element wird alle EWS-Anforderungen, um auf den Server anzugeben, welche Version des Schemas der Ziele Client gesendet. Dies bezeichnet die wiederum die Featuregruppe, die an den Client verfügbar ist. 
  
**Tabelle 1: EWS-Features nach Produkt und die Schemaversion**

|**Version des Produkts**|**Zugehörige Schemaversion**|**Features**|
|:-----|:-----|:-----|
|Exchange Online  |Die neueste Schemaversion.  |Enthält alle Features in der aktuellen Version von Exchange neben alle neuen Features, die für online-Clients hinzugefügt werden. |
|Exchange 2013 SP1 |Exchange2013_SP1 | Enthält alle Features in Exchange 2013.<br/><br/>Die folgenden Funktionen wurden in Exchange 2013 SP1 eingeführt: <ul><li>[Postfach-Aufbewahrungsrichtlinie](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) </li><li> [Andere Zeit vorschlagen](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md) </li><li>  Lesen des Empfangs von Updates für [Aktualisieren](http://msdn.microsoft.com/EN-US/library/office/dn600559%28v=exchg.80%29.aspx) und [Löschen von](http://msdn.microsoft.com/EN-US/library/office/dn600557%28v=exchg.80%29.aspx) Elementen  </li><li> Update für Unterhaltungen [IRM-Informationen](http://msdn.microsoft.com/EN-US/library/office/microsoft.exchange.webservices.data.conversation.hasirm%28v=exchg.80%29.aspx)  </li></ul> |
|Exchange 2013   |Exchange2013   | Enthält alle Features in Exchange 2007 und Exchange 2010 eingeführt. <br/><br/>Die folgenden Funktionen wurden in Exchange 2013 eingeführt:<ul><li>Archivierung  </li><li>  eDiscovery  </li><li>  Personas  </li><li>  Aufbewahrungsrichtlinien  </li><li>  Einheitlicher Kontaktspeicher  </li><li>  Benutzerfotos  </li></ul> |
|Exchange 2010 SP2   |Exchange2010_SP2 | Enthält alle Features, die in Exchange 2010 SP1 eingeführt. <br/><br/>Die folgenden Funktionen wurden in Exchange 2010 SP2 eingeführt:<ul><li>Abrufen des Kennwortablaufs  </li><li>  DateTime mit doppelter Genauigkeit  </li><li>  Aktualisierte Eigenschaftenbezeichner für Kontakte  </li><li>  Neue Szenarien der Identitätswechsel  </li></ul> |
|Exchange 2010 SP1  |Exchange2010_SP1   | Enthält alle Features, die in Exchange 2010 eingeführt. <br/><br/>Die folgenden Funktionen wurden in Exchange 2010 SP1 eingeführt:<ul><li>Erstellen, abrufen und Ändern von Posteingangsregeln  </li><li>  Den programmgesteuerten Zugriff auf Archivpostfach  </li><li>  Unterhaltungen Aktionen  </li><li>  Durchlaufen von Benachrichtigungen der Firewall  </li><li>  Verbesserte Verwaltungsfeatures  </li><li>  Verbesserte Unterstützung für gemischte version  </li><li>  Drosselung Protection-Unterstützung  </li><li>  Steuerung der Anwendungszugriff auf Exchange-Webdienste  </li><li>  Clientunterstützung Zertifikat-Authentifizierung  </li></ul> |
|Exchange 2010  |Exchange2010   | Enthält alle Features in Exchange 2007 SP1 eingeführt. <br/><br/>Die folgenden Funktionen wurden in der ursprünglich freigegebenen Version von Exchange 2010 eingeführt:<ul><li>Vollständige Private Verteilerliste  </li><li>  Konfiguration der Benutzerobjekte  </li><li>  Ordner zugewiesene Elemente  </li><li>  Nachrichtenverfolgung  </li><li>  Unified Messaging  </li><li>  SOAP-AutoErmittlung  </li><li>  Verbesserte Unterstützung der Zeitzone  </li><li>  Informationen zur Verfügbarkeit Raum Ressource  </li><li>  Indizierte Suche  </li><li>  Dumpster Zugriff  </li><li>  E-Mail-Infos Informationen  </li></ul> |
|Exchange 2007 SP1   |Exchange2007_SP1  | Enthält alle Features, die in Exchange 2007 eingeführt. <br/><br/>Die folgenden Funktionen wurden in Exchange 2007 SP1 eingeführt:<ul><li>Delegieren der Verwaltung  </li><li>  Berechtigungen für Ordner  </li><li>  Öffentliche Ordner  </li><li>  Bereitstellungselemente  </li><li>  ID-Konvertierung  </li></ul>|
|Exchange 2007  |Exchange2007 | Die folgenden Funktionen wurden in der ursprünglich freigegebenen Version von Exchange 2007 eingeführt:<ul><li>Vollzugriff auf den Elemente, Ordner und Anlagen (erstellen, abrufen, Update, Delete)  </li><li>  Verfügbarkeit  </li><li>  Nicht genügend Einstellungen für Office  </li><li>  Benachrichtigungen  </li><li>  Synchronisierung  </li><li>  Namensauflösung  </li><li>  Erweiterung der Verteilerliste (DL)  </li><li>  Suchen  </li></ul> |
   
## <a name="relationship-between-the-ews-schema-and-the-service-version"></a>Beziehung zwischen der EWS-Schema und die Service-version
<a name="bk_features"> </a>

Die Schemaversion EWS bezieht sich auf die Version des EWS-Diensts, die der Server ausgeführt wird. Das Benennungsmuster für das Schema EWS bezieht sich auf den lokalen Exchange-Versionen. Die erste Version von Exchange 2013 verfügt beispielsweise über eine Service-Version von 15.00.0516.032 und der Name des Schemas **Exchange2013**. Da das Schema für Exchange 2013 aktualisiert wurde, haben Exchange 2013 und Exchange Online mit einer Service-Version von 15.00.0516.032 und höher gleichnamige Version für das aktuelle Schema. In früheren Versionen von Exchange wurde das Schema EWS nicht mit kumulativen Updates (früher als Rollups bezeichnet) aktualisiert. Aber, da Exchange häufiger aktualisiert werden, um Exchange Online zu unterstützen, enthalten kumulativen Updates jetzt Schemaupdates für EWS. Die Schema-Dateinamen und den Namen der verknüpften Schema-Version werden nur mit Servicepacks oder Hauptversionen der lokale Exchange-Organisation aktualisiert.
  
Während des EWS-Schemas in einigen Szenarien den Vertrag definiert wird, ist die Dienstversion die einzige Möglichkeit für einen Client, um zu bestimmen, wie sie sollte Interaktion mit dem Dienst ist. Verhalten geändert, die im Schema widergespiegelt werden nicht können nur zurückgegeben, die in allen EWS-Antworten Service-Version ermittelt werden. Beispielsweise wenn [Öffentliche Ordner](public-folder-access-with-ews-in-exchange.md) wurden in Exchange 2013 umgestaltet sodass, die Vorgänge, die dienen zum Verschieben und kopieren Sie Öffentliche Ordner geändert. Wenn Sie einen Client zum Kopieren von öffentlicher Ordnern in Exchange 2010 entwickelt wurde, müssen Sie zum Aktualisieren, um verschiedene Vorgänge verwenden, um in Exchange 2013 dasselbe Ergebnis zu erzielen. 
  
## <a name="how-the-ews-schema-is-updated"></a>So aktualisieren Sie das EWS-schema
<a name="bk_features"> </a>

Exchange-Server mit Exchange, beginnend mit Exchange 2007-Versionen enthalten das EWS-Schema in das virtuelle Verzeichnis, das den EWS-Dienst gehostet wird. Die aktuelle Schemaversion wird immer durch die Dateien types.xsd und messages.xsd dargestellt. Abbildung 1 zeigt, wie das Schema messages.xsd verzweigt wird, wenn eine neue Version des Schemas entwickelt wurde. Bevor neuer Funktionen hinzugefügt wird, wird eine Kopie des ursprünglichen messages.xsd Schemas enthalten und umbenannt, um die vorherige Version des Schemas darstellen. Die Datei messages.xsd wird mit der Beschreibung für die neue Version aktualisiert.
  
**Abbildung 1. So aktualisieren Sie das EWS-schema**

![Eine Abbildung, die zeigt, wie das EWS-Schema aktualisiert wird. Die aktuelle Schemaversion ist gegabelt, sodass sie bei der vorherigen Version umbenannt wird und der aktuelle Dateiname die aktuelle Version darstellt.](media/Ex15_EWS_Schema_Update1.png)
  
Bevor das EWS-Schema für eine neue Version aktualisiert werden, wird die aktuelle Version des Schemas verzweigt wird und mithilfe der folgenden Benennungskonvention umbenannt:
  
`<schemaname>-<majorserverversion><servicepack>.xsd`
  
Den Namen der Originaldatei stellt dann das aktuelle Schema. Das aktuelle Schema, mit Ausnahme von Updates und Patches für früheren Versionen des Schemas werden alle neuen Features hinzugefügt. 
  
## <a name="see-also"></a>Siehe auch

- [EWS-Schemaversionen in Exchange](ews-schema-versions-in-exchange.md) 
- [AutoErmittlung für Exchange](autodiscover-for-exchange.md) 
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    

