---
title: TimeZoneContext
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZoneContext
api_type:
- schema
ms.assetid: 573c462b-aa1d-4ba0-8852-e3f48b26873b
description: Das timezonecontext-Element wird im Simple Object Access Protocol (SOAP)-Header verwendet, um die Zeitzonendefinition anzugeben, die als Standard verwendet werden soll, wenn die Zeitzone für die DateTime-Eigenschaften von Objekten zugewiesen wird, die mithilfe von Exchange-Webdienste erstellt, aktualisiert und abgerufen werden.
ms.openlocfilehash: 26727317ccf34338e8d62ec92bd7a44d43a6cfdb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460253"
---
# <a name="timezonecontext"></a><span data-ttu-id="ef888-103">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="ef888-103">TimeZoneContext</span></span>

<span data-ttu-id="ef888-104">Das **timezonecontext** -Element wird im Simple Object Access Protocol (SOAP)-Header verwendet, um die Zeitzonendefinition anzugeben, die als Standard verwendet werden soll, wenn die Zeitzone für die DateTime-Eigenschaften von Objekten zugewiesen wird, die mithilfe von Exchange-Webdienste erstellt, aktualisiert und abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ef888-104">The **TimeZoneContext** element is used in the Simple Object Access Protocol (SOAP) header to specify the time zone definition that is to be used as the default when assigning the time zone for the DateTime properties of objects that are created, updated, and retrieved by using Exchange Web Services (EWS).</span></span> 
  
```xml
<TimeZoneContext>
   <TimeZoneDefinition/>
</TimeZoneContext>
```

 <span data-ttu-id="ef888-105">**TimeZoneContextType**</span><span class="sxs-lookup"><span data-stu-id="ef888-105">**TimeZoneContextType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef888-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ef888-106">Attributes and elements</span></span>

<span data-ttu-id="ef888-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ef888-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef888-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ef888-108">Attributes</span></span>

<span data-ttu-id="ef888-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ef888-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef888-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef888-110">Child elements</span></span>

|<span data-ttu-id="ef888-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ef888-111">**Element**</span></span>|<span data-ttu-id="ef888-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef888-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef888-113">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="ef888-113">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="ef888-114">Gibt die Punkte und Übergänge an, die eine Zeitzone definieren.</span><span class="sxs-lookup"><span data-stu-id="ef888-114">Specifies the periods and transitions that define a time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ef888-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ef888-115">Parent elements</span></span>

<span data-ttu-id="ef888-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="ef888-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ef888-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef888-117">Remarks</span></span>

<span data-ttu-id="ef888-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ef888-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef888-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ef888-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef888-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef888-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ef888-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ef888-121">Schema Name</span></span>  <br/> |<span data-ttu-id="ef888-122">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ef888-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="ef888-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ef888-123">Validation File</span></span>  <br/> |<span data-ttu-id="ef888-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ef888-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ef888-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ef888-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="ef888-126">False</span><span class="sxs-lookup"><span data-stu-id="ef888-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef888-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef888-127">See also</span></span>



- [<span data-ttu-id="ef888-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ef888-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

