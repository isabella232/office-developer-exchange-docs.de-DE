---
title: IsContactPhoto
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsContactPhoto
api_type:
- schema
ms.assetid: ae36b5f9-a787-4863-9dbc-258ad724801d
description: Das IsContactPhoto-Element gibt an, ob es sich bei der Dateianlage um ein Kontaktbild handelt.
ms.openlocfilehash: f60e558ab4f20b59c1d5ae51f9dfca430feeff00
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455548"
---
# <a name="iscontactphoto"></a><span data-ttu-id="81618-103">IsContactPhoto</span><span class="sxs-lookup"><span data-stu-id="81618-103">IsContactPhoto</span></span>

<span data-ttu-id="81618-104">Das **IsContactPhoto** -Element gibt an, ob es sich bei der Dateianlage um ein Kontaktbild handelt.</span><span class="sxs-lookup"><span data-stu-id="81618-104">The **IsContactPhoto** element indicates whether the file attachment is a contact picture.</span></span> 
  
```xml
<IsContactPhoto>true or false</IsContactPhoto>
```

 <span data-ttu-id="81618-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="81618-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="81618-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="81618-106">Attributes and elements</span></span>

<span data-ttu-id="81618-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="81618-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81618-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="81618-108">Attributes</span></span>

<span data-ttu-id="81618-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="81618-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="81618-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="81618-110">Child elements</span></span>

<span data-ttu-id="81618-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="81618-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="81618-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="81618-112">Parent elements</span></span>

|<span data-ttu-id="81618-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="81618-113">**Element**</span></span>|<span data-ttu-id="81618-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81618-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81618-115">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="81618-115">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="81618-116">Stellt eine Datei dar, die an ein Element im Exchange-Informationsspeicher angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="81618-116">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="81618-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="81618-117">Text value</span></span>

<span data-ttu-id="81618-118">Dieses Element kann entweder **true** oder **false**sein.</span><span class="sxs-lookup"><span data-stu-id="81618-118">This element can be either **true** or **false**.</span></span> <span data-ttu-id="81618-119">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="81618-119">The default value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="81618-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81618-120">Remarks</span></span>

<span data-ttu-id="81618-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="81618-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="81618-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="81618-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81618-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="81618-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="81618-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="81618-124">Schema Name</span></span>  <br/> |<span data-ttu-id="81618-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="81618-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="81618-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="81618-126">Validation File</span></span>  <br/> |<span data-ttu-id="81618-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="81618-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="81618-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="81618-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="81618-129">False</span><span class="sxs-lookup"><span data-stu-id="81618-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81618-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81618-130">See also</span></span>



- [<span data-ttu-id="81618-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="81618-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

