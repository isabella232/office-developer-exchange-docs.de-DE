---
title: DocumentSharingLocation (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 21bc388c-33be-422b-a89d-30ade0fae8f1
description: Das DocumentSharingLocation-Element enthält Standort- und Metadateninformationen für einen Dokumentfreigabespeicherort.
ms.openlocfilehash: f4011dfb846d314d926ba644f4ddc2176283008a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541483"
---
# <a name="documentsharinglocation-soap"></a>DocumentSharingLocation (SOAP)

Das **DocumentSharingLocation-Element** enthält Standort- und Metadateninformationen für einen Dokumentfreigabespeicherort. 
  
```XML
<DocumentSharingLocation>
   <ServiceUrl />
   <LocationUrl />
   <DisplayName />
   <SupportedFileExtensions />
   <ExternalAccessAllowed />
   <AnonymousAccessAllowed />
   <CanModifyPermissions />
   <IsDefault />
</DocumentSharingLocation>
```

 **DocumentSharingLocation**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ServiceUrl (SOAP)](serviceurl-soap.md) <br/> |Stellt die URL des Dokumentfreigabewebdiensts dar.  <br/> |
|[LocationUrl (SOAP)](locationurl-soap.md) <br/> |Stellt die URL des Speicherorts für die Dokumentfreigabe dar.  <br/> |
|[DisplayName (SOAP)](displayname-soap.md) <br/> |Stellt den Namen des Speicherorts für die Dokumentfreigabe dar, der auf der Benutzeroberfläche verwendet werden soll.  <br/> |
|[SupportedFileExtensions (SOAP)](supportedfileextensions-soap.md) <br/> |Stellt die Dateierweiterungen dar, die am Speicherort für die Dokumentfreigabe gespeichert werden können.  <br/> |
|[ExternalAccessAllowed (SOAP)](externalaccessallowed-soap.md) <br/> |Gibt an, ob der Speicherort für die Dokumentfreigabe für externe Verbindungen verfügbar ist.  <br/> |
|[AnonymousAccessAllowed (SOAP)](anonymousaccessallowed-soap.md) <br/> |Gibt an, ob für den Zugriff auf den Freigabespeicherort ein authentifizierter Benutzer erforderlich ist.  <br/> |
|[CanModifyPermissions (SOAP)](canmodifypermissions-soap.md) <br/> |Gibt an, ob der Benutzer Zugriffsberechtigungen für den Speicherort für die Dokumentfreigabe ändern kann.  <br/> |
|[IsDefault (SOAP)](isdefault-soap.md) <br/> |Gibt an, ob der Speicherort für die Dokumentfreigabe der Standardmäßige Freigabespeicherort des Benutzers ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DocumentSharingLocations (SOAP)](documentsharinglocations-soap.md) <br/> |Enthält eine Liste der Speicherorte und Metadaten für die Dokumentfreigabe.  <br/> |
   
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

- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
- [AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
- [SOAP AutoDiscover XML-Elemente für Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

