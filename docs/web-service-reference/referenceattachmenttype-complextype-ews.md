---
title: ReferenceAttachmentType ComplexType (EWS)
manager: sethgros
ms.date: 03/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 18bfa012-e903-d7f3-528a-31ccceb65463
ms.openlocfilehash: c53686ccd032cabcc3f64a3a6684f29afe63a9b1
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354176"
---
# <a name="referenceattachmenttype-complextype-ews"></a><span data-ttu-id="5c9e7-102">ReferenceAttachmentType ComplexType (EWS)</span><span class="sxs-lookup"><span data-stu-id="5c9e7-102">ReferenceAttachmentType complexType (EWS)</span></span>

## <a name="type-information"></a><span data-ttu-id="5c9e7-103">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="5c9e7-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c9e7-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5c9e7-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5c9e7-105">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="5c9e7-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5c9e7-106">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5c9e7-106">types.xsd</span></span>  <br/> |
|<span data-ttu-id="5c9e7-107">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="5c9e7-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5c9e7-108">t:AttachmentType</span><span class="sxs-lookup"><span data-stu-id="5c9e7-108">t:AttachmentType</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5c9e7-109">Definition</span><span class="sxs-lookup"><span data-stu-id="5c9e7-109">Definition</span></span>

```XML
<xs:complexType name="ReferenceAttachmentType">
    <xs:complexContent>
        <xs:extension base="t:AttachmentType">
            <xs:sequence>
                <xs:element name="AttachLongPathName" type="xs:string" maxOccurs="1" minOccurs="0"></xs:element>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="5c9e7-110">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="5c9e7-110">Elements and attributes</span></span>

<span data-ttu-id="5c9e7-111">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="5c9e7-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5c9e7-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5c9e7-112">Child elements</span></span>

|<span data-ttu-id="5c9e7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5c9e7-113">**Element**</span></span>|<span data-ttu-id="5c9e7-114">**Typ**</span><span class="sxs-lookup"><span data-stu-id="5c9e7-114">**Type**</span></span>|<span data-ttu-id="5c9e7-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5c9e7-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5c9e7-116">AttachLongPathName</span><span class="sxs-lookup"><span data-stu-id="5c9e7-116">AttachLongPathName</span></span>](attachlongpathname.md) <br/> |<span data-ttu-id="5c9e7-117">xs:string</span><span class="sxs-lookup"><span data-stu-id="5c9e7-117">xs:string</span></span>  <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5c9e7-118">Attribute</span><span class="sxs-lookup"><span data-stu-id="5c9e7-118">Attributes</span></span>

<span data-ttu-id="5c9e7-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="5c9e7-119">None.</span></span>
  

