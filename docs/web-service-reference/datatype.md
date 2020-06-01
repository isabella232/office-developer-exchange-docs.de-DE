---
title: DataType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DataType
api_type:
- schema
ms.assetid: 267fe5aa-f9b1-4d4c-ac11-0f2e50ec2627
description: Das DataType-Element beschreibt den Typ der Daten, die von einem freigegebenen Ordner gemeinsam verwendet werden.
ms.openlocfilehash: a7df8d38e10f0ab31038d790d8f35208d1be66d5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458831"
---
# <a name="datatype"></a><span data-ttu-id="cba57-103">DataType</span><span class="sxs-lookup"><span data-stu-id="cba57-103">DataType</span></span>

<span data-ttu-id="cba57-104">Das **DataType** -Element beschreibt den Typ der Daten, die von einem freigegebenen Ordner gemeinsam verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cba57-104">The **DataType** element describes the type of data that is shared by a shared folder.</span></span> 
  
```xml
<DataType>Calendar or Contacts</DataType>
```

<span data-ttu-id="cba57-105">**SharingDataType**</span><span class="sxs-lookup"><span data-stu-id="cba57-105">**SharingDataType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="cba57-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cba57-106">Attributes and elements</span></span>

<span data-ttu-id="cba57-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cba57-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cba57-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cba57-108">Attributes</span></span>

<span data-ttu-id="cba57-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="cba57-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cba57-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cba57-110">Child elements</span></span>

<span data-ttu-id="cba57-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="cba57-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cba57-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cba57-112">Parent elements</span></span>

|<span data-ttu-id="cba57-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="cba57-113">**Element**</span></span>|<span data-ttu-id="cba57-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cba57-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cba57-115">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="cba57-115">GetSharingFolder</span></span>](getsharingfolder.md) <br/> |<span data-ttu-id="cba57-116">Definiert eine Anforderung zum Abrufen der lokalen Ordner-ID eines angegebenen freigegebenen Ordners.</span><span class="sxs-lookup"><span data-stu-id="cba57-116">Defines a request to get the local folder identifier of a specified shared folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cba57-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="cba57-117">Text value</span></span>

<span data-ttu-id="cba57-118">In der folgenden Tabelle sind die möglichen Werte für das **DataType** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cba57-118">The following table lists the possible values for the **DataType** element.</span></span> 
  
<span data-ttu-id="cba57-119">**DataType-Elementwerte**</span><span class="sxs-lookup"><span data-stu-id="cba57-119">**DataType element values**</span></span>

|<span data-ttu-id="cba57-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="cba57-120">**Value**</span></span>|<span data-ttu-id="cba57-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cba57-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cba57-122">Kalender</span><span class="sxs-lookup"><span data-stu-id="cba57-122">Calendar</span></span>  <br/> |<span data-ttu-id="cba57-123">Gibt an, dass der freigegebene Ordner Kalenderinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="cba57-123">Indicates that the shared folder contains calendar information.</span></span>  <br/> |
|<span data-ttu-id="cba57-124">Kontakte</span><span class="sxs-lookup"><span data-stu-id="cba57-124">Contacts</span></span>  <br/> |<span data-ttu-id="cba57-125">Gibt an, dass der freigegebene Ordner Kontaktinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="cba57-125">Indicates that the shared folder contains contact information.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cba57-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cba57-126">Remarks</span></span>

<span data-ttu-id="cba57-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="cba57-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cba57-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cba57-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cba57-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="cba57-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cba57-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cba57-130">Schema Name</span></span>  <br/> |<span data-ttu-id="cba57-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="cba57-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cba57-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cba57-132">Validation File</span></span>  <br/> |<span data-ttu-id="cba57-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cba57-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cba57-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cba57-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="cba57-135">False</span><span class="sxs-lookup"><span data-stu-id="cba57-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cba57-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cba57-136">See also</span></span>

- [<span data-ttu-id="cba57-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cba57-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

