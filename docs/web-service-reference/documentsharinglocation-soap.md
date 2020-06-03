---
title: DocumentSharingLocation (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21bc388c-33be-422b-a89d-30ade0fae8f1
description: Das DocumentSharingLocation-Element enthält Speicherort-und Metadateninformationen für einen Dokumentfreigabe Speicherort.
ms.openlocfilehash: 6fed933da979ab3e3fca51ba606127b7f0a4e3f8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457060"
---
# <a name="documentsharinglocation-soap"></a>DocumentSharingLocation (SOAP)

Das **DocumentSharingLocation** -Element enthält Speicherort-und Metadateninformationen für einen Dokumentfreigabe Speicherort. 
  
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
|[ServiceUrl (SOAP)](serviceurl-soap.md) <br/> |Stellt die URL des Dokumentfreigabe-Webdiensts dar.  <br/> |
|[LocationUrl (SOAP)](locationurl-soap.md) <br/> |Stellt die URL des Speicherorts für die Dokumentfreigabe dar.  <br/> |
|[DisplayName (SOAP)](displayname-soap.md) <br/> |Stellt den Namen des Dokumentfreigabe Speicherorts dar, der in der Benutzeroberfläche verwendet werden soll.  <br/> |
|[SupportedFileExtensions (SOAP)](supportedfileextensions-soap.md) <br/> |Stellt die Dateierweiterungen dar, die am Dokumentfreigabe Speicherort gespeichert werden können.  <br/> |
|[ExternalAccessAllowed (SOAP)](externalaccessallowed-soap.md) <br/> |Gibt an, ob der Speicherort der Dokumentfreigabe für externe Verbindungen verfügbar ist.  <br/> |
|[AnonymousAccessAllowed (SOAP)](anonymousaccessallowed-soap.md) <br/> |Gibt an, ob für den Zugriff auf den Freigabespeicherort ein authentifizierter Benutzer erforderlich ist.  <br/> |
|[CanModifyPermissions (SOAP)](canmodifypermissions-soap.md) <br/> |Gibt an, ob der Benutzerzugriffsberechtigungen für den Speicherort der Dokumentfreigabe ändern kann.  <br/> |
|[IsDefault (SOAP)](isdefault-soap.md) <br/> |Gibt an, ob der Speicherort für die Dokumentfreigabe der Standardfreigabe Speicherort des Benutzers ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DocumentSharingLocations (SOAP)](documentsharinglocations-soap.md) <br/> |Enthält eine Liste der Speicherorte und Metadaten für die Freigabe von Dokumenten.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |Auto Ermittlungs Schema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)
- [AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
- [XML-Elemente der SOAP-AutoErmittlung für Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

