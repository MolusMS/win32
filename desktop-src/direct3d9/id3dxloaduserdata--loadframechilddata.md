---
Description: Load frame child data from a .x file.
ms.assetid: 79d251f3-c661-42e3-9385-84aabd58fd4f
title: ID3DXLoadUserData::LoadFrameChildData method
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# ID3DXLoadUserData::LoadFrameChildData method

Load frame child data from a .x file.

## Syntax


```C++
HRESULT LoadFrameChildData(
  [in] LPD3DXFRAME    pFrame,
  [in] LPD3DXFILEDATA pXofChildData
);
```



## Parameters

<dl> <dt>

*pFrame* \[in\]
</dt> <dd>

Type: **[**LPD3DXFRAME**](d3dxframe.md)**

Pointer to a mesh container. See [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*pXofChildData* \[in\]
</dt> <dd>

Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**

Pointer to a .x file data structure. This is defined in Dxfile.h.

</dd> </dl>

## Return value

Type: **[**HRESULT**](https://msdn.microsoft.com/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

The return values of this method are implemented by an application programmer. In general, if no error occurs, program the method to return D3D\_OK. Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[ID3DXLoadUserData](id3dxloaduserdata.md)
</dt> </dl>

 

 



