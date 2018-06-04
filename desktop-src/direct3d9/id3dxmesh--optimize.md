---
Description: Generates a new mesh with reordered faces and vertices to optimize drawing performance.
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: ID3DXMesh::Optimize method
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# ID3DXMesh::Optimize method

Generates a new mesh with reordered faces and vertices to optimize drawing performance.

## Syntax


```C++
HRESULT Optimize(
  [in]            DWORD        Flags,
  [in]      const DWORD        *pAdjacencyIn,
  [in, out]       DWORD        *pAdjacencyOut,
  [in, out]       DWORD        *pFaceRemap,
  [out]           LPD3DXBUFFER *ppVertexRemap,
  [out]           LPD3DXMESH   *ppOptMesh
);
```



## Parameters

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Type: **[**DWORD**](https://msdn.microsoft.com/windows/desktop/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

Specifies the type of optimization to perform. This parameter can be set to a combination of one or more flags from [**D3DXMESHOPT**](https://msdn.microsoft.com/windows/desktop/32ef227a-b299-47c4-96b8-c0ea7bf549e1) and [**D3DXMESH**](https://msdn.microsoft.com/windows/desktop/c94e19ab-8024-4a28-9d1a-6d57707c3a52) (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).

</dd> <dt>

*pAdjacencyIn* \[in\]
</dt> <dd>

Type: **const [**DWORD**](https://msdn.microsoft.com/windows/desktop/4553cafc-450e-4493-a4d4-cb6e2f274d46)\***

Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the source mesh. If the edge has no adjacent faces, the value is 0xffffffff. See Remarks.

</dd> <dt>

*pAdjacencyOut* \[in, out\]
</dt> <dd>

Type: **[**DWORD**](https://msdn.microsoft.com/windows/desktop/4553cafc-450e-4493-a4d4-cb6e2f274d46)\***

Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the optimized mesh. If the edge has no adjacent faces, the value is 0xffffffff.

</dd> <dt>

*pFaceRemap* \[in, out\]
</dt> <dd>

Type: **[**DWORD**](https://msdn.microsoft.com/windows/desktop/4553cafc-450e-4493-a4d4-cb6e2f274d46)\***

An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh. If the value supplied for this argument is **NULL**, face remap data is not returned.

</dd> <dt>

*ppVertexRemap* \[out\]
</dt> <dd>

Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***

Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices. This remap is useful if you need to alter external data based on the new vertex mapping.

</dd> <dt>

*ppOptMesh* \[out\]
</dt> <dd>

Type: **[**LPD3DXMESH**](id3dxmesh.md)\***

Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the optimized mesh.

</dd> </dl>

## Return value

Type: **[**HRESULT**](https://msdn.microsoft.com/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the method succeeds, the return value is D3D\_OK. If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.

## Remarks

This method generates a new mesh. Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md). The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.

This method is very similar to the [**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh. The output mesh inherits all of the creation parameters of the input mesh.

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::OptimizeInplace**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 



