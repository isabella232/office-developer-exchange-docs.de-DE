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
description: Das DataType-Element beschreibt die Art der Daten, die von einem freigegebenen Ordner gemeinsam verwendet werden.
ms.openlocfilehash: b1adac8e3029abd64df96ab1560706babe4b12f2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757862"
---
# <a name="datatype"></a><span data-ttu-id="f3e60-103">DataType</span><span class="sxs-lookup"><span data-stu-id="f3e60-103">DataType</span></span>

<span data-ttu-id="f3e60-104">Das **DataType** -Element beschreibt die Art der Daten, die von einem freigegebenen Ordner gemeinsam verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3e60-104">The **DataType** element describes the type of data that is shared by a shared folder.</span></span> 
  
```xml
<DataType>Calendar or Contacts</DataType>
```

<span data-ttu-id="f3e60-105">**SharingDataType**</span><span class="sxs-lookup"><span data-stu-id="f3e60-105">**SharingDataType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f3e60-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f3e60-106">Attributes and elements</span></span>

<span data-ttu-id="f3e60-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f3e60-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3e60-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f3e60-108">Attributes</span></span>

<span data-ttu-id="f3e60-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f3e60-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f3e60-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f3e60-110">Child elements</span></span>

<span data-ttu-id="f3e60-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f3e60-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f3e60-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f3e60-112">Parent elements</span></span>

|<span data-ttu-id="f3e60-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f3e60-113">**Element**</span></span>|<span data-ttu-id="f3e60-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f3e60-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3e60-115">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="f3e60-115">GetSharingFolder</span></span>](getsharingfolder.md) <br/> |<span data-ttu-id="f3e60-116">Definiert eine Anforderung an den lokalen Ordner Bezeichner eines angegebenen freigegebenen Ordners abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f3e60-116">Defines a request to get the local folder identifier of a specified shared folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f3e60-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="f3e60-117">Text value</span></span>

<span data-ttu-id="f3e60-118">Die folgende Tabelle enthält die möglichen Werte für die **DataType** -Element.</span><span class="sxs-lookup"><span data-stu-id="f3e60-118">The following table lists the possible values for the **DataType** element.</span></span> 
  
<span data-ttu-id="f3e60-119">**DataType-Elementwerte**</span><span class="sxs-lookup"><span data-stu-id="f3e60-119">**DataType element values**</span></span>

|<span data-ttu-id="f3e60-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f3e60-120">**Value**</span></span>|<span data-ttu-id="f3e60-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f3e60-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3e60-122">Kalender</span><span class="sxs-lookup"><span data-stu-id="f3e60-122">Calendar</span></span>  <br/> |<span data-ttu-id="f3e60-123">Gibt an, dass der freigegebene Ordner Kalenderinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="f3e60-123">Indicates that the shared folder contains calendar information.</span></span>  <br/> |
|<span data-ttu-id="f3e60-124">Kontakte</span><span class="sxs-lookup"><span data-stu-id="f3e60-124">Contacts</span></span>  <br/> |<span data-ttu-id="f3e60-125">Gibt an, dass der freigegebene Ordner Kontaktinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="f3e60-125">Indicates that the shared folder contains contact information.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3e60-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f3e60-126">Remarks</span></span>

<span data-ttu-id="f3e60-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f3e60-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f3e60-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f3e60-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3e60-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="f3e60-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f3e60-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f3e60-130">Schema Name</span></span>  <br/> |<span data-ttu-id="f3e60-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f3e60-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f3e60-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f3e60-132">Validation File</span></span>  <br/> |<span data-ttu-id="f3e60-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f3e60-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f3e60-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f3e60-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="f3e60-135">False</span><span class="sxs-lookup"><span data-stu-id="f3e60-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f3e60-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3e60-136">See also</span></span>

- [<span data-ttu-id="f3e60-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f3e60-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

