---
title: 'Display Event Arguments'
description: 'Displays event arguments in a message box. Useful for debugging E10 customisations.'
pubDate: 2026-05-18
tags: [e10, customisation]
categories: [E10 Customisation]
pinned: false
toc: true
---

```csharp
// helper function for debugging
private void displayArgs(string title, System.EventArgs args)
{
    System.Text.StringBuilder sb = new System.Text.StringBuilder();
    
    foreach (var property in args.GetType().GetProperties())
    {
        object value = property.GetValue(args);
        sb.AppendLine(string.Format("{0}: {1}", property.Name, value != null ? value.ToString() : "NULL"));
    }
    
    MessageBox.Show(sb.ToString(), title);
}
```