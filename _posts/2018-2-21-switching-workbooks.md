---
title: "Switching Workbooks"
excerpt: "Switching Workbooks"
header:
  overlay_image: /assets/images/unsplash-image-1.jpg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
layout: single
categories:
  - VBA
tags:
  - VBA
toc: true
toc_label: "My Table of Contents"
toc_icon: "gear"
---







Sub harvestdata()

    Dim xWBName As String

    Dim xWb As Workbook

    Dim xSelect As String

   

    

    WB = ThisWorkbook.Name

    For Each xWb In Application.Workbooks

        xWBName = xWBName & xWb.Name

    Next

    xWBName = Replace(xWBName, WB, "")

    xWBName = Replace(xWBName, "PERSONAL.XLSB", "")

    'MsgBox (xWBName)

   

    Application.Workbooks(xWBName).Activate

    Sheets("Sheet1").Select

    Range("a2:g17").Select

    Selection.Copy

   

    Windows(WB).Activate

    Range("a2:g18").Select

    ActiveSheet.Paste

 

 

End Sub
