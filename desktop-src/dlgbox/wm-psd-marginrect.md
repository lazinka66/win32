---
title: WM\_PSD\_MARGINRECT message
description: Notifies the hook procedure of a Page Setup dialog box, PagePaintHook, that the dialog box is about to draw the margin rectangle of the sample page.
ms.assetid: 81c057ab-6faf-4dd8-8b0c-34a2753e572c
keywords:
- WM_PSD_MARGINRECT message Dialog Boxes
topic_type:
- apiref
api_name:
- WM_PSD_MARGINRECT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# WM\_PSD\_MARGINRECT message

Notifies the hook procedure of a **Page Setup** dialog box, [**PagePaintHook**](https://www.bing.com/search?q=**PagePaintHook**), that the dialog box is about to draw the margin rectangle of the sample page.


```C++
#define WM_USER                  0x0400
#define WM_PSD_MARGINRECT       (WM_USER+3)
```



## Parameters

<dl> <dt>

*wParam* 
</dt> <dd>

A handle to the device context for the sample page.

</dd> <dt>

*lParam* 
</dt> <dd>

A pointer to a [**RECT**](https://msdn.microsoft.com/library/windows/desktop/dd162897) structure that contains the coordinates, in pixels, of the margin rectangle.

</dd> </dl>

## Return value

If the hook procedure returns **TRUE**, the dialog box does not draw the margin rectangle in the sample page.

If the hook procedure returns **FALSE**, the dialog box draws the margin rectangle in the sample page.

## Remarks

The **Page Setup** dialog box includes an image of a sample page that shows how the user's selections affect the appearance of the printed output. When you call the [**PageSetupDlg**](https://www.bing.com/search?q=**PageSetupDlg**) function, you can provide a [*PagePaintHook*](https://www.bing.com/search?q=*PagePaintHook*) hook procedure to customize the appearance of the sample page. Whenever the dialog box is about to draw the contents of the sample page, the dialog box sends a sequence of messages to the hook procedure.

## Requirements



|                                     |                                                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 2000 Professional \[desktop apps only\]<br/>                                               |
| Minimum supported server<br/> | Windows 2000 Server \[desktop apps only\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Commdlg.h (include Windows.h)</dt> </dl> |



## See also

<dl> <dt>

**Reference**
</dt> <dt>

[*PagePaintHook*](https://www.bing.com/search?q=*PagePaintHook*)
</dt> <dt>

[**PageSetupDlg**](https://www.bing.com/search?q=**PageSetupDlg**)
</dt> <dt>

[**WM\_PSD\_PAGESETUPDLG**](wm-psd-pagesetupdlg.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Common Dialog Box Library](common-dialog-box-library.md)
</dt> </dl>

 

 




