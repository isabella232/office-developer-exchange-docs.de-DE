---
title: ProtocolConnection (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 6eef2188-6194-48f1-ad7e-46104aecdf56
description: Das ProtocolConnection-Element stellt die Protokollverbindung des Serverwebclients dar.
ms.openlocfilehash: a4f48a12981a83206aff266700708745e9d3c1bb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512583"
---
# <a name="protocolconnection-soap"></a>ProtocolConnection (SOAP)

Das **ProtocolConnection-Element** stellt die Protokollverbindung des Serverwebclients dar. 
  
```XML
<ProtocolConnection>
   <Hostname/>
   <Port/>
   <EncryptionMethod/>
</ProtocolConnection>
```

 **ProtocolConnection**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Hostname (SOAP)](hostname-soap.md) <br/> |Stellt den Hostnamenteil des vollständigen Computernamens des Computers dar.  <br/> |
|[Port (SOAP)](port-soap.md) <br/> |Stellt die Portnummer dar, die für das Protokoll verwendet werden soll.  <br/> |
|[EncryptionMethod (SOAP)](encryptionmethod-soap.md) <br/> |Stellt die kryptografische Methode dar, die für die POP-, IMAP- und SMTP-Protokolle verwendet wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ProtocolConnections (SOAP)](protocolconnections-soap.md) <br/> |Enthält null oder mehr Protokollverbindungen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ProtocolConnectionCollectionSetting (SOAP)](protocolconnectioncollectionsetting-soap.md)

