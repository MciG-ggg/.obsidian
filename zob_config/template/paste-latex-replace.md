---
words:
  2025-04-13: 110
  2025-04-30: 47
---
<%*
    const clipboardContent = await navigator.clipboard.readText ();
    if (clipboardContent) {
        // 修复关键：初始赋值 + 正确链式处理
        let replacedContent = clipboardContent; // 先完整赋值
        replacedContent = replacedContent.replace (/\$([\s\S]*?)\$/g, (_, p1) => '$' + p1.trim () + '$');
        
        tR = replacedContent;
    } else {
        tR = "";
    }
%>