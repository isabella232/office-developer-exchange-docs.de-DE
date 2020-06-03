---
title: UpdateFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateFolder
api_type:
- schema
ms.assetid: 412d0683-2819-40c5-a0ae-f613499a7b66
description: Das UpdateFolder-Element stellt den Vorgang dar, der zum Aktualisieren der Eigenschaften für einen angegebenen Ordner verwendet wird.
ms.openlocfilehash: 124ffd02a5ea2e7bf6f21cc7009dde08837906f9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457046"
---
# <a name="updatefolder"></a><span data-ttu-id="c1186-103">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="c1186-103">UpdateFolder</span></span>

<span data-ttu-id="c1186-104">Das **UpdateFolder** -Element stellt den Vorgang dar, der zum Aktualisieren der Eigenschaften für einen angegebenen Ordner verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1186-104">The **UpdateFolder** element represents the operation that is used to update properties for a specified folder.</span></span> 
  
```xml
<UpdateFolder>
   <FolderChanges/>
</UpdateFolder>
```

 <span data-ttu-id="c1186-105">**UpdateFolderType**</span><span class="sxs-lookup"><span data-stu-id="c1186-105">**UpdateFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1186-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c1186-106">Attributes and elements</span></span>

<span data-ttu-id="c1186-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c1186-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1186-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c1186-108">Attributes</span></span>

<span data-ttu-id="c1186-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1186-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1186-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1186-110">Child elements</span></span>

|<span data-ttu-id="c1186-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1186-111">**Element**</span></span>|<span data-ttu-id="c1186-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1186-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1186-113">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="c1186-113">FolderChanges</span></span>](folderchanges.md) <br/> |<span data-ttu-id="c1186-114">Enthält eine Auflistung von Änderungen für einen angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="c1186-114">Contains a collection of changes for a specified folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c1186-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1186-115">Parent elements</span></span>

<span data-ttu-id="c1186-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1186-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c1186-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1186-117">Remarks</span></span>

<span data-ttu-id="c1186-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c1186-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1186-119">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c1186-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1186-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1186-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c1186-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c1186-121">Schema Name</span></span>  <br/> |<span data-ttu-id="c1186-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c1186-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c1186-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c1186-123">Validation File</span></span>  <br/> |<span data-ttu-id="c1186-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c1186-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c1186-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c1186-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1186-126">False</span><span class="sxs-lookup"><span data-stu-id="c1186-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1186-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1186-127">See also</span></span>



[<span data-ttu-id="c1186-128">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c1186-128">UpdateFolder operation</span></span>](updatefolder-operation.md)

