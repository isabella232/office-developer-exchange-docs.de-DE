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
description: Das TimeZoneContext-Element wird in der Kopfzeile (SOAP = Simple Object Access Protocol) verwendet, um die Zeitzonendefinition an, das als Standard verwendet werden, wenn die Zeitzone für den DateTime-Eigenschaft der Objekte zuweisen, die erstellt, aktualisiert und durch abgerufen werden verwenden die Exchange-Webdienste (EWS).
ms.openlocfilehash: 38b7ab4c587adac45fc3bcf351f417ea72313a97
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839215"
---
# <a name="timezonecontext"></a><span data-ttu-id="8fd42-103">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="8fd42-103">TimeZoneContext</span></span>

<span data-ttu-id="8fd42-104">Das **TimeZoneContext** -Element wird in der Kopfzeile (SOAP = Simple Object Access Protocol) verwendet, um die Zeitzonendefinition an, das als Standard verwendet werden, wenn die Zeitzone für den DateTime-Eigenschaft der Objekte zuweisen, die erstellt werden, aktualisiert, und Mithilfe der Exchange-Webdienste (EWS) abgerufen.</span><span class="sxs-lookup"><span data-stu-id="8fd42-104">The **TimeZoneContext** element is used in the Simple Object Access Protocol (SOAP) header to specify the time zone definition that is to be used as the default when assigning the time zone for the DateTime properties of objects that are created, updated, and retrieved by using Exchange Web Services (EWS).</span></span> 
  
```xml
<TimeZoneContext>
   <TimeZoneDefinition/>
</TimeZoneContext>
```

 <span data-ttu-id="8fd42-105">**TimeZoneContextType**</span><span class="sxs-lookup"><span data-stu-id="8fd42-105">**TimeZoneContextType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8fd42-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8fd42-106">Attributes and elements</span></span>

<span data-ttu-id="8fd42-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8fd42-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8fd42-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8fd42-108">Attributes</span></span>

<span data-ttu-id="8fd42-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8fd42-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8fd42-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8fd42-110">Child elements</span></span>

|<span data-ttu-id="8fd42-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8fd42-111">**Element**</span></span>|<span data-ttu-id="8fd42-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8fd42-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8fd42-113">Zeitzonendefinition</span><span class="sxs-lookup"><span data-stu-id="8fd42-113">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="8fd42-114">Gibt den Zeiträume und Übergänge, die eine Zeitzone definiert.</span><span class="sxs-lookup"><span data-stu-id="8fd42-114">Specifies the periods and transitions that define a time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8fd42-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8fd42-115">Parent elements</span></span>

<span data-ttu-id="8fd42-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="8fd42-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8fd42-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8fd42-117">Remarks</span></span>

<span data-ttu-id="8fd42-118">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8fd42-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8fd42-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8fd42-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8fd42-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="8fd42-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8fd42-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8fd42-121">Schema Name</span></span>  <br/> |<span data-ttu-id="8fd42-122">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8fd42-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="8fd42-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8fd42-123">Validation File</span></span>  <br/> |<span data-ttu-id="8fd42-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8fd42-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8fd42-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8fd42-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="8fd42-126">False</span><span class="sxs-lookup"><span data-stu-id="8fd42-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8fd42-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fd42-127">See also</span></span>



- [<span data-ttu-id="8fd42-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8fd42-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

