---
title: ProtocolConnection (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 6eef2188-6194-48f1-ad7e-46104aecdf56
description: Das Element ProtocolConnection stellt die Protokoll Verbindung des Webclients Server dar.
ms.openlocfilehash: 8b5396821cd959e41d24fcf7a94c519f9c634a1f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830915"
---
# <a name="protocolconnection-soap"></a>ProtocolConnection (SOAP)

Das Element **ProtocolConnection** stellt die Protokoll Verbindung des Webclients Server dar. 
  
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
|[Hostname (SOAP)](hostname-soap.md) <br/> |Stellt die Hostnamenkomponente des den vollständigen Namen des Computers an.  <br/> |
|[Port (SOAP)](port-soap.md) <br/> |Stellt die Portnummer an, die für das Protokoll verwendet.  <br/> |
|[EncryptionMethod (SOAP)](encryptionmethod-soap.md) <br/> |Stellt die kryptografische-Methode, die für die POP-, IMAP- und SMTP-Protokolle verwendet wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ProtocolConnections (SOAP)](protocolconnections-soap.md) <br/> |Enthält null oder mehr Protocol-Verbindungen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ProtocolConnectionCollectionSetting (SOAP)](protocolconnectioncollectionsetting-soap.md)

