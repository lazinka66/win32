---
Description: Determines if a matrix is an identity matrix.
ms.assetid: 00f72d08-5d4b-4310-8167-e6b6371d24fd
title: D3DXMatrixIsIdentity function
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# D3DXMatrixIsIdentity function

Determines if a matrix is an identity matrix.

## Syntax


```C++
BOOL D3DXMatrixIsIdentity(
  _In_ const D3DXMATRIX *pM
);
```



## Parameters

<dl> <dt>

*pM* \[in\]
</dt> <dd>

Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***

Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that will be tested for identity.

</dd> </dl>

## Return value

Type: **[**BOOL**](https://msdn.microsoft.com/windows/desktop/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

If the matrix is an identity matrix, this function returns **TRUE**. Otherwise, this function returns **FALSE**.

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[Math Functions](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixIdentity**](d3dxmatrixidentity.md)
</dt> </dl>

 

 



