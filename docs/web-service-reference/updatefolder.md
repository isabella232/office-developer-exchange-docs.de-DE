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
description: Das Element UpdateFolder stellt die Operation, die verwendet wird, um Eigenschaften für einen angegebenen Ordner zu aktualisieren.
ms.openlocfilehash: 9a86bf6b3b5917600b3b09f23b3ee4e9cdc0364f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839349"
---
# <a name="updatefolder"></a><span data-ttu-id="13824-103">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="13824-103">UpdateFolder</span></span>

<span data-ttu-id="13824-104">Das Element **UpdateFolder** stellt die Operation, die verwendet wird, um Eigenschaften für einen angegebenen Ordner zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="13824-104">The **UpdateFolder** element represents the operation that is used to update properties for a specified folder.</span></span> 
  
```xml
<UpdateFolder>
   <FolderChanges/>
</UpdateFolder>
```

 <span data-ttu-id="13824-105">**UpdateFolderType**</span><span class="sxs-lookup"><span data-stu-id="13824-105">**UpdateFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="13824-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="13824-106">Attributes and elements</span></span>

<span data-ttu-id="13824-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="13824-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13824-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="13824-108">Attributes</span></span>

<span data-ttu-id="13824-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="13824-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="13824-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="13824-110">Child elements</span></span>

|<span data-ttu-id="13824-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="13824-111">**Element**</span></span>|<span data-ttu-id="13824-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13824-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13824-113">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="13824-113">FolderChanges</span></span>](folderchanges.md) <br/> |<span data-ttu-id="13824-114">Enthält eine Auflistung von Änderungen für einen angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="13824-114">Contains a collection of changes for a specified folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="13824-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="13824-115">Parent elements</span></span>

<span data-ttu-id="13824-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="13824-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="13824-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13824-117">Remarks</span></span>

<span data-ttu-id="13824-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="13824-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="13824-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="13824-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13824-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="13824-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="13824-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="13824-121">Schema Name</span></span>  <br/> |<span data-ttu-id="13824-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="13824-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="13824-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="13824-123">Validation File</span></span>  <br/> |<span data-ttu-id="13824-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="13824-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="13824-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="13824-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="13824-126">False</span><span class="sxs-lookup"><span data-stu-id="13824-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13824-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13824-127">See also</span></span>



[<span data-ttu-id="13824-128">UpdateFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="13824-128">UpdateFolder operation</span></span>](updatefolder-operation.md)

